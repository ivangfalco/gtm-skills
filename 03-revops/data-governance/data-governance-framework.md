# Data Governance — Framework

How to maintain clean, accurate, and actionable CRM data. The foundation for every revenue operation — without it, automation fails, reporting lies, and sales loses trust.

---

## Why Data Governance Matters

Bad data compounds. Every workflow, report, and automation relies on the underlying data quality. When data is dirty:

- **Lead routing breaks** — Leads go to wrong reps or don't route at all
- **Reporting becomes fiction** — Pipeline numbers are unreliable, forecasts miss
- **Automation backfires** — Workflows trigger on wrong conditions, spam customers
- **Sales loses trust** — Reps stop updating CRM because "the data is wrong anyway"
- **Revenue leaks** — Duplicate records, missed follow-ups, wrong attribution

**The cost:** Companies lose 12-25% of revenue due to bad data (Gartner). The average CRM has 25-30% duplicate records.

---

## Data Quality Dimensions

### The Six Pillars of Data Quality

| Dimension | Definition | Example of Failure | How to Measure |
|---|---|---|---|
| **Accuracy** | Data correctly represents reality | Job title says "Manager" but person is now VP | % of records verified as correct (sampling) |
| **Completeness** | Required fields are populated | Email exists but no phone, company size, or industry | % of required fields filled |
| **Consistency** | Same data formatted the same way | "United States" vs "US" vs "USA" vs "U.S." | % of records matching format standards |
| **Timeliness** | Data is current and up-to-date | Contact left company 6 months ago, still in CRM | % of records updated within decay window |
| **Uniqueness** | No duplicate records | Same person appears 3 times with slight name variations | Duplicate rate (# duplicates / total records) |
| **Validity** | Data conforms to defined rules | Email field contains "TBD" instead of valid email | % of records passing validation rules |

### Quality Scoring Model

Assign a Data Quality Score (DQS) to each record:

```
DQS = (Completeness Score x 0.25) + (Accuracy Score x 0.30) +
      (Timeliness Score x 0.20) + (Validity Score x 0.15) +
      (Uniqueness Score x 0.10)

Score ranges:
- 90-100: Excellent — ready for automation
- 70-89: Good — minor gaps, usable
- 50-69: Fair — needs enrichment before use
- <50: Poor — high risk, requires review
```

---

## Data Decay Rates by Field Type

**Data decays faster than you think.** Annual decay rates by field type:

| Field Type | Annual Decay Rate | Half-Life | Implication |
|---|---|---|---|
| **Work email** | 25-30% | ~2.5 years | Re-verify every 6 months for active sequences |
| **Phone number** | 15-20% | ~3.5 years | Verify before calling campaigns |
| **Job title** | 30-35% | ~2 years | Highest decay — people get promoted/leave |
| **Company name** | 10-15% | ~5 years | M&A, rebrands, bankruptcies |
| **Company size** | 15-20% | ~3.5 years | Hiring/layoffs change tier classification |
| **Industry** | 5-10% | ~8 years | Pivots happen but rare |
| **Physical address** | 20-25% | ~3 years | Office moves, remote transitions |
| **Tech stack** | 25-30% | ~2.5 years | Tool switches happen frequently |
| **LinkedIn URL** | 5-10% | ~8 years | Rarely changes unless person leaves |
| **Revenue** | 20-25% | ~3 years | Growth, contraction, funding rounds |

### Decay Mitigation Schedule

| Field Category | Verification Frequency | Method |
|---|---|---|
| Contact-level fields (email, title, phone) | Every 6 months | Enrichment tools (Clay, ZoomInfo, Apollo) |
| Company-level fields (size, revenue, tech) | Every 12 months | Bulk enrichment + manual review |
| Engagement data | Real-time | Automated via integrations |
| Deal data | Continuous | Sales-entered, validated at stage gates |

---

## Field Governance Matrix

### Who Owns What

| Field Category | Owner | Update Frequency | Validation Rules |
|---|---|---|---|
| **Contact: Email** | Marketing Ops | On creation + every 6 months | Must be valid format, verified status |
| **Contact: Phone** | Sales Ops | On creation + before call campaigns | Must be valid format with country code |
| **Contact: Job Title** | Marketing Ops | On creation + every 6 months | Must be from approved list or flagged |
| **Contact: Lifecycle Stage** | RevOps | Automated via workflows | Must follow stage progression rules |
| **Contact: Lead Source** | Marketing Ops | On creation only | Immutable after creation |
| **Contact: Lead Status** | Sales | Manual, updated as worked | Must change within SLA timeframes |
| **Company: Industry** | Marketing Ops | On creation + annually | Must be from standardized list |
| **Company: Employee Count** | Marketing Ops | On creation + annually | Must be number, validated against range |
| **Company: Revenue** | Marketing Ops | Annually | Must be number or range, normalized |
| **Company: ICP Score** | RevOps | Automated | Calculated field, recalc on data change |
| **Deal: Amount** | Sales | At creation + stage changes | Must be non-zero after Discovery stage |
| **Deal: Close Date** | Sales | Continuous | Must be future date (or today if closed) |
| **Deal: Stage** | Sales | Continuous | Must follow stage progression |

### Field Edit Permissions

| Role | Can Edit | Cannot Edit |
|---|---|---|
| **Sales Rep** | Lead status, deal fields, activity notes, next steps | Lead source, ICP score, lifecycle stage (auto), company firmographics |
| **Sales Manager** | All rep fields + deal amount overrides | Lead source, system fields |
| **Marketing Ops** | Contact/company enrichment fields, segmentation | Deal fields, sales activity data |
| **RevOps** | All fields (admin) | Historical data (audit trail preserved) |

---

## Standardization Rules

### Country Names

| Accept | Normalize To |
|---|---|
| United States, US, U.S., USA, America | United States |
| United Kingdom, UK, U.K., Great Britain, England | United Kingdom |
| Deutschland, Germany | Germany |

**Implementation:** Use HubSpot workflow or validation rule to auto-correct on save.

### Job Title Normalization

| Raw Title | Normalized To | Seniority Level |
|---|---|---|
| VP of Marketing, Vice President Marketing, VP Marketing | VP of Marketing | Executive |
| Head of Growth, Growth Lead, Director of Growth | Head of Growth | Director |
| Marketing Manager, Marketing Mgr, Mktg Manager | Marketing Manager | Manager |
| SDR, Sales Development Rep, BDR, Business Development Rep | SDR/BDR | Individual Contributor |

### Phone Number Format

| Raw Format | Normalized To |
|---|---|
| (415) 555-1234 | +1 415 555 1234 |
| 415.555.1234 | +1 415 555 1234 |
| 0044 20 7946 0958 | +44 20 7946 0958 |

**Rule:** Always store with country code, spaces between segments, no special characters.

### Company Name Normalization

| Raw Name | Normalized To | Notes |
|---|---|---|
| Acme, Inc. | Acme | Remove legal suffixes |
| Acme Corporation | Acme | Remove legal suffixes |
| The Acme Company | Acme | Remove articles and "Company" |
| Acme Corp (fka OldCo) | Acme | Remove historical references |

---

## Duplicate Detection and Merge Strategies

### Duplicate Sources

| Source | How Duplicates Appear | Prevention |
|---|---|---|
| **Form submissions** | Same person fills multiple forms | Dedupe on email before creation |
| **List imports** | Imported list has records already in CRM | Match on email + company before import |
| **Integration syncs** | Same record created by multiple integrations | Canonical source designation |
| **Manual entry** | Sales creates record without checking | Required search before create |
| **Company variations** | "Acme" vs "Acme Inc" vs "Acme Corporation" | Company name normalization |

### Duplicate Matching Logic

**Contact Matching (in priority order):**

| Match Type | Confidence | Auto-Merge? |
|---|---|---|
| Exact email match | 100% | Yes |
| Same company + same name (fuzzy) | 95% | Flag for review |
| Same phone + same company | 90% | Flag for review |
| Same LinkedIn URL | 100% | Yes |
| Same name + same company domain | 85% | Flag for review |
| Same name only | 50% | Do not auto-merge |

**Company Matching:**

| Match Type | Confidence | Auto-Merge? |
|---|---|---|
| Exact domain match | 100% | Yes |
| Domain match after normalization (www removal, etc.) | 100% | Yes |
| Same name (normalized) + same country | 90% | Flag for review |
| Same name (normalized) only | 70% | Do not auto-merge |

### Merge Rules: Surviving Record Selection

When merging duplicates, which record "wins"?

| Scenario | Winning Record | Rationale |
|---|---|---|
| One has deals, one doesn't | Record with deals | Preserve revenue history |
| One has activities, one doesn't | Record with activities | Preserve engagement history |
| Both have activities | Most recent activity | Most current relationship |
| One is enriched, one isn't | Enriched record | Better data quality |
| One from integration, one manual | Manual record | Human-verified |

### Field-Level Merge Rules

| Field | Merge Rule |
|---|---|
| **Email** | Keep primary from winning record; others become secondary |
| **Phone** | Keep primary from winning record; others become secondary |
| **Job Title** | Use most recently updated |
| **Lead Source** | Keep original (oldest) source |
| **Lifecycle Stage** | Keep most advanced stage |
| **Lead Status** | Keep from winning record |
| **Custom properties** | Keep non-blank value; if both have values, keep winning record |
| **Activities** | Merge all activities to surviving record |
| **Deals** | Reassociate all deals to surviving record |

---

## Data Enrichment Best Practices

### Enrichment Hierarchy

Not all enrichment sources are equal. Prioritize by accuracy:

| Source | Accuracy | Coverage | Cost | Best For |
|---|---|---|---|---|
| **Manual research** | 95%+ | Low | High (time) | High-value accounts, executive contacts |
| **LinkedIn Sales Navigator** | 90%+ | High | $$$ | Job titles, company info, connections |
| **Clay** | 85-90% | High | $$ | Bulk enrichment, waterfall approach |
| **ZoomInfo** | 80-85% | Very High | $$$$ | Enterprise, comprehensive data |
| **Apollo** | 75-80% | High | $ | Cost-effective bulk enrichment |
| **Clearbit** | 80-85% | Medium | $$$ | Tech stack, firmographics |
| **Hunter** | 70-75% | Medium | $ | Email finding only |

### Waterfall Enrichment Strategy

Don't rely on one source. Use a waterfall approach:

```
Step 1: Check existing CRM data (free)
  ↓ If missing fields
Step 2: Clay enrichment (uses multiple sources)
  ↓ If still missing
Step 3: ZoomInfo/Apollo lookup
  ↓ If still missing
Step 4: Manual research (LinkedIn, company website)
  ↓ If still missing
Step 5: Flag for human verification
```

### What to Enrich and When

| Trigger | Fields to Enrich | Priority |
|---|---|---|
| **New lead created** | Email verified, phone, job title, company size, industry | High — do immediately |
| **Lead becomes MQL** | Full firmographics, tech stack, LinkedIn URL | High — before sales touches |
| **Deal created** | Decision-makers, org chart, recent news | Medium |
| **Quarterly refresh** | Job title verification, company size update | Medium |
| **Before campaign** | Email verification, phone validation | High |

### Enrichment Quality Control

After enrichment, validate:

| Check | How | Action if Failed |
|---|---|---|
| Email valid format | Regex validation | Reject enrichment for that field |
| Email verified | Email verification tool (NeverBounce, etc.) | Flag as unverified, don't use in sequences |
| Phone valid format | Regex + length check | Reject enrichment for that field |
| Title in valid list | Match against approved titles | Flag for review |
| Company size reasonable | Check against known range for industry | Flag for review |

---

## Data Quality KPIs and Targets

### Contact Data Quality Metrics

| Metric | Formula | Target | Red Flag |
|---|---|---|---|
| **Email fill rate** | Contacts with email / Total contacts | >95% | <90% |
| **Email verification rate** | Verified emails / Total emails | >85% | <75% |
| **Phone fill rate** | Contacts with phone / Total contacts | >70% | <50% |
| **Job title fill rate** | Contacts with title / Total contacts | >90% | <80% |
| **Duplicate rate** | Duplicate contacts / Total contacts | <5% | >10% |
| **Bounce rate (last 90d)** | Bounced emails / Emails sent | <2% | >5% |
| **Average completeness score** | Avg of all contact completeness scores | >80% | <70% |

### Company Data Quality Metrics

| Metric | Formula | Target | Red Flag |
|---|---|---|---|
| **Industry fill rate** | Companies with industry / Total companies | >95% | <90% |
| **Company size fill rate** | Companies with size / Total companies | >90% | <80% |
| **Domain fill rate** | Companies with domain / Total companies | >99% | <95% |
| **Duplicate rate** | Duplicate companies / Total companies | <3% | >7% |
| **ICP score coverage** | Companies with ICP score / Total companies | >95% | <90% |

### Deal Data Quality Metrics

| Metric | Formula | Target | Red Flag |
|---|---|---|---|
| **Amount fill rate** | Deals with amount / Total open deals | 100% | <95% |
| **Close date accuracy** | Deals closed within 30 days of predicted / Total closed | >70% | <50% |
| **Stage progression compliance** | Deals following stage order / Total deals | >95% | <90% |
| **Required field compliance** | Deals with all stage-required fields / Total deals | >90% | <80% |

### Reporting Dashboard

Build a Data Quality Dashboard with these widgets:

```
Row 1: Overall Health
- Data Quality Score (gauge: 0-100)
- Trend: DQS over last 6 months (line chart)
- Records needing attention (count)

Row 2: Contacts
- Completeness by field (bar chart)
- Duplicate trend (line chart)
- Enrichment coverage (pie chart)

Row 3: Companies
- ICP score distribution (histogram)
- Missing fields breakdown (bar chart)
- Duplicate rate trend (line chart)

Row 4: Deals
- Required field compliance by stage (heatmap)
- Amount fill rate trend (line chart)
- Close date accuracy trend (line chart)
```

---

## CRM Hygiene Audit Framework

### Weekly Tasks (15 minutes)

| Task | What to Check | Action |
|---|---|---|
| New duplicates | Duplicates created in last 7 days | Merge or flag for review |
| Bounced emails | Contacts that bounced this week | Update email or remove |
| Missing required fields | New leads missing critical fields | Enrich or flag |
| SLA breaches | Leads not worked within SLA | Alert sales managers |

### Monthly Tasks (1 hour)

| Task | What to Check | Action |
|---|---|---|
| Full duplicate scan | All potential duplicates | Merge confirmed duplicates |
| Email verification | Re-verify 10% sample | Update invalid emails |
| Stale leads | Leads untouched for 90+ days | Recycle or archive |
| Data completeness report | Overall fill rates by field | Prioritize enrichment |
| Source quality analysis | Lead quality by source | Adjust source scoring |

### Quarterly Tasks (Half day)

| Task | What to Check | Action |
|---|---|---|
| Full enrichment refresh | All active contacts/companies | Re-enrich job titles, company data |
| Lifecycle stage audit | Contacts stuck in wrong stages | Correct stage assignments |
| Field usage analysis | Fields never/rarely used | Deprecate or make required |
| Integration health check | All data sync integrations | Fix broken syncs |
| User permission audit | Who can edit what | Adjust permissions as needed |

### Annual Tasks (Full day)

| Task | What to Check | Action |
|---|---|---|
| Full data audit | Complete CRM review | Document findings, create remediation plan |
| Field governance review | Field ownership, validation rules | Update governance matrix |
| Archival policy review | What to keep, what to archive | Archive old data per policy |
| Data decay analysis | Actual decay rates vs expected | Adjust enrichment frequency |
| Tool evaluation | Enrichment and data tools | Renew, replace, or consolidate |

---

## Data Quality Automation

### Automated Validation Rules

| Field | Validation Rule | On Failure |
|---|---|---|
| Email | Must match email regex pattern | Reject submission / flag for review |
| Phone | Must be 7-15 digits with optional + prefix | Reject submission / flag for review |
| Website | Must start with http:// or https:// | Auto-prefix https:// |
| LinkedIn URL | Must contain linkedin.com/in/ or linkedin.com/company/ | Reject / flag for review |
| Employee count | Must be positive integer | Reject / flag for review |
| Revenue | Must be positive number or valid range | Reject / flag for review |

### Automated Standardization

| Field | Auto-Standardization |
|---|---|
| Country | Map variations to standard names |
| State/Province | Map abbreviations to full names (or vice versa) |
| Job title | Normalize to standard titles where possible |
| Phone | Format to international standard |
| Website | Lowercase, remove trailing slash |
| Company name | Remove legal suffixes, standardize capitalization |

### Automated Enrichment Triggers

| Trigger | Enrichment Action |
|---|---|
| Contact created with email only | Enrich name, company, title, phone |
| Contact moved to MQL | Full enrichment (all available fields) |
| Company created with domain only | Enrich name, industry, size, tech stack |
| Deal created | Enrich company news, additional contacts |
| Contact email bounced | Find alternate email |
| Contact job title changed | Verify new title, update seniority level |

---

## Data Governance Roles

### RACI Matrix

| Activity | RevOps | Marketing Ops | Sales Ops | Sales | Marketing |
|---|---|---|---|---|---|
| Define data standards | A/R | C | C | I | I |
| Implement validation rules | A | R | C | I | I |
| Monitor data quality | R | R | R | I | I |
| Remediate data issues | A | R | R | C | I |
| Import data | A | R | C | I | I |
| Enrich data | A | R | C | I | I |
| Merge duplicates | A | R | R | I | I |
| Update deal data | I | I | C | R | I |
| Update contact data | I | R | R | C | C |

**Legend:** R = Responsible, A = Accountable, C = Consulted, I = Informed

### Data Steward Responsibilities

Each team should have a designated Data Steward:

| Role | Responsibilities |
|---|---|
| **RevOps Data Steward** | Overall governance, cross-functional issues, escalations |
| **Marketing Data Steward** | Contact/company data quality, enrichment, list hygiene |
| **Sales Data Steward** | Deal data quality, activity logging compliance |

---

## Implementation Roadmap

### Phase 1: Foundation (Month 1)

- [ ] Document current state (fields, owners, issues)
- [ ] Define field governance matrix
- [ ] Implement basic validation rules
- [ ] Set up data quality dashboard
- [ ] Run initial duplicate analysis

### Phase 2: Standardization (Month 2)

- [ ] Implement standardization rules
- [ ] Clean historical data (duplicates, formatting)
- [ ] Set up automated enrichment
- [ ] Train team on data entry standards
- [ ] Establish weekly/monthly audit cadence

### Phase 3: Automation (Month 3)

- [ ] Automate validation on all entry points
- [ ] Automate enrichment workflows
- [ ] Set up duplicate prevention
- [ ] Implement data quality scoring
- [ ] Create alerting for quality degradation

### Phase 4: Optimization (Ongoing)

- [ ] Monitor KPIs monthly
- [ ] Quarterly governance reviews
- [ ] Annual full audits
- [ ] Continuous improvement based on findings

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
