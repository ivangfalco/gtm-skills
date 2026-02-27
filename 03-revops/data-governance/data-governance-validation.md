# Data Governance — Validation Rules

Field validation rules, standardization logic, and HubSpot configuration for maintaining data quality.

---

## Validation Rule Types

### Text Field Validation

| Rule Type | Example | HubSpot Implementation |
|---|---|---|
| **Character limit** | Max 100 characters for job title | Settings > Properties > Validation Rules |
| **Numeric only** | Phone field accepts only numbers | Restrict to numeric characters |
| **No special characters** | Company name without symbols | Disallow special characters |
| **Regex pattern** | LinkedIn URL format | Custom regex validation |
| **Unique values** | External ID must be unique | Enable unique value constraint |

### Number Field Validation

| Rule Type | Example | Implementation |
|---|---|---|
| **Range limits** | Employee count 1-500,000 | Set min/max values |
| **Decimal places** | Revenue with 2 decimals | Require specific decimals |
| **Positive only** | Deal amount cannot be negative | Minimum value = 0 |

### Email Validation

| Rule Type | Implementation |
|---|---|
| **Format check** | Built-in email validation |
| **Domain validation** | No free email domains (gmail, yahoo) |
| **Deliverability** | Email verification tool integration |
| **Duplicate check** | Prevent duplicate emails |

### Phone Validation

| Rule Type | Implementation |
|---|---|
| **Auto-format** | Enable phone number formatting |
| **Country code** | Require or auto-detect country code |
| **Length check** | 7-15 digits |
| **Format standardization** | Output: +1 415 555 1234 |

---

## Field-by-Field Validation Rules

### Contact Fields

| Field | Validation Rule | On Failure |
|---|---|---|
| **First Name** | Required, 1-50 chars, no numbers | Reject submission |
| **Last Name** | Required, 1-50 chars, no numbers | Reject submission |
| **Email** | Required, valid format, verified | Flag for review |
| **Phone** | 7-15 digits, valid format | Flag for review |
| **Job Title** | From approved list OR custom | Flag if custom |
| **LinkedIn URL** | Contains linkedin.com/in/ | Auto-correct or flag |
| **Lead Source** | From dropdown, immutable | Cannot change after create |
| **Lifecycle Stage** | Sequential progression only | Prevent skip-ahead |

### Company Fields

| Field | Validation Rule | On Failure |
|---|---|---|
| **Company Name** | Required, 2-200 chars | Reject |
| **Domain** | Required, valid URL format | Reject |
| **Industry** | From standardized list | Reject if not in list |
| **Employee Count** | Positive integer, 1-10,000,000 | Flag for review |
| **Revenue** | Positive number or range | Flag for review |
| **Country** | From ISO country list | Auto-map or reject |
| **Website** | Valid URL, https preferred | Auto-prefix https |

### Deal Fields

| Field | Validation Rule | On Failure |
|---|---|---|
| **Deal Name** | Required, 5-200 chars | Reject |
| **Amount** | Required after Discovery stage, > 0 | Block stage progression |
| **Close Date** | Future date or today if closed | Auto-correct or reject |
| **Pipeline** | From valid pipelines | Reject |
| **Stage** | Sequential progression | Prevent skip-stages |
| **Owner** | Valid user | Reject |

---

## Standardization Rules

### Country Name Mapping

| Input Variations | Standardized To |
|---|---|
| United States, US, U.S., USA, America, United States of America | United States |
| United Kingdom, UK, U.K., Great Britain, England, Britain | United Kingdom |
| Deutschland, Germany, GER | Germany |
| The Netherlands, Netherlands, Holland, NL | Netherlands |
| Schweiz, Switzerland, Suisse, CH | Switzerland |

**HubSpot Implementation:**
```
Workflow Trigger: Contact/Company created or "Country" property updated
Action: Custom code - Map country variations to standard name
```

### Job Title Normalization

| Raw Title Variations | Normalized To | Seniority |
|---|---|---|
| VP of Marketing, Vice President Marketing, VP Marketing, Marketing VP | VP of Marketing | Executive |
| Head of Growth, Growth Lead, Director of Growth, Growth Director | Head of Growth | Director |
| Marketing Manager, Marketing Mgr, Mktg Manager | Marketing Manager | Manager |
| SDR, Sales Development Rep, BDR, Business Dev Rep, Sales Dev | SDR/BDR | IC |
| CEO, Chief Executive, Chief Executive Officer | CEO | C-Suite |
| CTO, Chief Technology Officer, Chief Tech Officer | CTO | C-Suite |
| CFO, Chief Financial Officer, Chief Finance Officer | CFO | C-Suite |

### Phone Number Formatting

| Input Format | Normalized Output |
|---|---|
| (415) 555-1234 | +1 415 555 1234 |
| 415.555.1234 | +1 415 555 1234 |
| 415-555-1234 | +1 415 555 1234 |
| 4155551234 | +1 415 555 1234 |
| +14155551234 | +1 415 555 1234 |
| 0044 20 7946 0958 | +44 20 7946 0958 |

**Rule:** Always store with country code, spaces between segments, no special characters.

### Company Name Cleaning

| Input | Output | Rule Applied |
|---|---|---|
| Acme, Inc. | Acme | Remove legal suffixes |
| Acme Corporation | Acme | Remove "Corporation" |
| The Acme Company | Acme | Remove "The" and "Company" |
| Acme Corp (fka OldCo) | Acme | Remove historical references |
| ACME | Acme | Normalize capitalization |
| acme llc | Acme | Title case, remove LLC |

### URL Standardization

| Input | Output | Rule |
|---|---|---|
| acme.com | https://acme.com | Add https:// |
| http://acme.com | https://acme.com | Upgrade to https |
| HTTPS://ACME.COM | https://acme.com | Lowercase |
| https://acme.com/ | https://acme.com | Remove trailing slash |
| https://www.acme.com | https://acme.com | Remove www (optional) |

---

## HubSpot Configuration

### Property Validation Setup

**Path:** Settings > Data Management > Properties > Select Property > Validation Rules

**Available Options:**
- Character limits (min/max)
- Numeric-only restriction
- Special character restriction
- Number ranges
- Decimal place requirements
- Regex patterns (custom)
- Unique value requirement
- Phone number auto-formatting

### Workflow-Based Validation

```
Workflow: Contact Data Validation

Triggers:
- Contact is created
- Property "Email" is updated
- Property "Phone" is updated

Actions:
1. If Email is blank → Set "Data Quality Issue" = "Missing Email"
2. If Email not valid format → Set "Data Quality Issue" = "Invalid Email"
3. If Phone format invalid → Reformat using custom code
4. If Job Title not in approved list → Add to "Manual Review" list
5. If Company blank → Set "Data Quality Issue" = "Missing Company"
```

### Required Fields by Object

**Contact Required Fields:**
- Email (always)
- First Name (on form submission)
- Last Name (on form submission)
- Company (before MQL)
- Lead Source (on creation)

**Company Required Fields:**
- Company Name (always)
- Domain (always)
- Industry (before qualification)
- Employee Count (before qualification)

**Deal Required Fields:**
- Deal Name (always)
- Amount (after Discovery stage)
- Close Date (always)
- Associated Company (always)
- Associated Contact (always)

### Form-Level Validation

| Form Type | Required Fields | Validation |
|---|---|---|
| Demo Request | Email, First Name, Last Name, Company | Email verified |
| Content Download | Email, First Name | GDPR consent |
| Contact Us | Email, Message | Anti-spam (reCAPTCHA) |
| Newsletter | Email | Double opt-in |

---

## Data Quality Scoring

### Scoring Model

```
Data Quality Score (0-100) = Weighted sum of quality dimensions

Weights:
- Completeness: 25%
- Accuracy: 30%
- Timeliness: 20%
- Validity: 15%
- Uniqueness: 10%

Example calculation:
Completeness: 85%
Accuracy: 90%
Timeliness: 80%
Validity: 95%
Uniqueness: 100%

Score = (0.85 × 25) + (0.90 × 30) + (0.80 × 20) + (0.95 × 15) + (1.0 × 10)
     = 21.25 + 27 + 16 + 14.25 + 10 = 88.5
```

### Score Thresholds

| Score Range | Assessment | Action |
|---|---|---|
| 90-100 | Excellent | Ready for automation |
| 70-89 | Good | Minor gaps, usable |
| 50-69 | Fair | Needs enrichment before use |
| <50 | Poor | High risk, requires review |

### HubSpot Implementation

Create calculated property "Data Quality Score":
```
Formula:
(IF([Email] != "", 10, 0)) +
(IF([First Name] != "", 10, 0)) +
(IF([Last Name] != "", 10, 0)) +
(IF([Company Name] != "", 15, 0)) +
(IF([Job Title] != "", 10, 0)) +
(IF([Phone] != "", 10, 0)) +
(IF([Industry] != "", 10, 0)) +
(IF([Employee Count] != "", 15, 0)) +
(IF([Lead Source] != "", 10, 0))
```

---

## Duplicate Prevention

### Matching Rules (Contacts)

| Priority | Match Criteria | Confidence |
|---|---|---|
| 1 | Exact email match | 100% - Auto-merge |
| 2 | LinkedIn URL match | 100% - Auto-merge |
| 3 | Same company + same name (fuzzy) | 95% - Flag for review |
| 4 | Same phone + same company | 90% - Flag for review |
| 5 | Same name + same company domain | 85% - Flag for review |
| 6 | Same name only | 50% - Do not auto-merge |

### Matching Rules (Companies)

| Priority | Match Criteria | Confidence |
|---|---|---|
| 1 | Exact domain match | 100% - Auto-merge |
| 2 | Domain after www removal | 100% - Auto-merge |
| 3 | Same name (normalized) + same country | 90% - Flag for review |
| 4 | Same name (normalized) only | 70% - Do not auto-merge |

### Import Validation

Before import, check:
- [ ] Deduplicate within import file
- [ ] Match against existing CRM records
- [ ] Validate email formats
- [ ] Verify required fields present
- [ ] Check for obvious data quality issues

---

## Validation Workflow Examples

### New Lead Validation

```
Trigger: Contact created with Lead Source = "Inbound"

Step 1: Email Validation
  IF Email blank OR invalid format
    → Set "Validation Status" = "Failed"
    → Add to "Invalid Leads" list
    → End workflow

Step 2: Duplicate Check
  IF Email matches existing contact
    → Set "Validation Status" = "Duplicate"
    → Merge with existing
    → End workflow

Step 3: Enrichment Trigger
  IF Company blank OR Employee Count blank
    → Trigger enrichment workflow
    → Set "Needs Enrichment" = Yes

Step 4: Assignment
  IF Validation Status != "Failed"
    → Assign based on territory rules
    → Set "Validation Status" = "Passed"
```

### Deal Stage Validation

```
Trigger: Deal stage updated

Step 1: Required Field Check
  IF Stage = "Demo Scheduled" AND Demo Date blank
    → Prevent stage change
    → Show error: "Demo Date required"

Step 2: Amount Validation
  IF Stage = "Proposal Sent" AND Amount = 0
    → Prevent stage change
    → Show error: "Deal Amount required"

Step 3: Close Date Validation
  IF Stage = "Closed Won" AND Close Date > Today
    → Auto-set Close Date = Today

Step 4: Association Check
  IF Stage = "Negotiation" AND No contacts associated
    → Show warning: "Add decision maker contacts"
```

---

## Common Validation Mistakes

| Mistake | Impact | Fix |
|---|---|---|
| Validating too strictly | Good leads rejected | Balance validation with conversion |
| Validating too loosely | Bad data enters CRM | Enforce critical field rules |
| No validation on imports | Bulk bad data | Require import validation |
| Manual validation only | Human error, inconsistency | Automate via workflows |
| Validation without feedback | Users don't know why rejected | Clear error messages |
| Not testing validation | False positives/negatives | Test with sample data |

---

## Cross-References

- **Data Governance Framework:** See `data-governance-framework.md`
- **Enrichment Strategies:** See `data-governance-enrichment.md`
- **Audit Framework:** See `data-governance-framework.md#crm-hygiene-audit-framework`

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
