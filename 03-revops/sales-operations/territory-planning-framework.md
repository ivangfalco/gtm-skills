# Territory Planning — Framework

How to design, assign, and manage sales territories. Territory models, capacity planning, and rebalancing strategies.

---

## Why Territory Planning Matters

Territory design alone can increase revenue by **2-7%** without any changes to overall company strategy or resources (Harvard Business Review). Organizations using data-driven territory planning see up to **30% higher quota attainment**.

Bad territory design causes:
- **Unequal opportunity** — Some reps have goldmines, others have barren land
- **Rep turnover** — 9% of reps quit over commission/territory disputes
- **Customer experience gaps** — Accounts fall through cracks or get multiple reps
- **Wasted capacity** — Reps travel inefficiently or work mismatched accounts

---

## Territory Models

### Geographic Territories

**Description:** Dividing sales coverage by regions, states, cities, or zip codes.

| Criteria | Assessment |
|---|---|
| **Best for** | Field sales, local support required, broad customer base |
| **Sales motion** | "Hunter" roles focused on new logo acquisition |
| **Advantages** | Clear boundaries, efficient travel, local expertise |
| **Limitations** | Unequal revenue potential across regions |

**When to use:**
- Products requiring in-person visits or local support
- Companies with widespread customer distribution
- Regional regulatory differences to navigate

### Vertical/Industry Territories

**Description:** Assigning accounts by business vertical (healthcare, financial services, manufacturing, etc.).

| Criteria | Assessment |
|---|---|
| **Best for** | Complex products, regulated industries, deep expertise needed |
| **Sales motion** | "Farmer" roles focused on expansion |
| **Advantages** | Specialization drives higher win rates |
| **Limitations** | Travel inefficiency, harder to scale |

**When to use:**
- Products with industry-specific use cases
- Regulated industries (healthcare, finance, government)
- Selling to fewer, larger accounts

### Account Size/Tier Territories

**Description:** Segmenting by revenue, employee count, or strategic value.

| Tier | Definition | Sales Motion |
|---|---|---|
| **Enterprise** | >$10M revenue or 1,000+ employees | High-touch, dedicated AE |
| **Mid-Market** | $1M-$10M revenue or 100-999 employees | Balanced touch, pooled/dedicated |
| **SMB** | <$1M revenue or <100 employees | Velocity, self-serve + support |

**When to use:**
- SaaS companies with tiered pricing
- Different sales motions by segment
- Organizations with specialized teams

### Named Account Programs

**Description:** Specifically identified, high-value accounts assigned to dedicated reps or teams.

| Criteria | Assessment |
|---|---|
| **Best for** | Enterprise, strategic account management, ABM |
| **Selection criteria** | ICP fit, revenue potential, strategic value |
| **Team structure** | Dedicated AE + CSM + SE + executive sponsor |
| **Coverage** | Single point of contact, deep relationship |

**ABM impact:**
- 80% of marketers say ABM initiatives outperform other investments
- Companies using ABM generate 208% more revenue

### Hybrid Territories

**Description:** Combining multiple criteria (e.g., geography + vertical, size + region).

**Examples:**
- "Healthcare accounts in Northeast"
- SMB reps by geography, Enterprise reps by vertical
- Named accounts for top-tier, geographic for mid-market/SMB

**Recommendation:** Hybrid models (geography + vertical) deliver better results than pure geography for most B2B organizations.

---

## Territory Model Selection Framework

| Factor | Geographic | Vertical | Size-Based | Named | Hybrid |
|---|---|---|---|---|---|
| **Product complexity** | Low-Med | High | Med-High | High | Med-High |
| **Sales cycle length** | Short | Long | Varies | Long | Varies |
| **Customer distribution** | Widespread | Concentrated | Varies | Concentrated | Varies |
| **Rep expertise needed** | General | Deep vertical | Segment-specific | Account-specific | Balanced |
| **Travel requirements** | High | Low | Medium | Medium | Medium |
| **Scalability** | High | Medium | High | Low | High |

---

## Capacity Planning

### Core Capacity Formula

```
Sales Capacity = Number of Reps × (Quarterly Quota × Average Quota Attainment)
```

### Enhanced Formula (Accounting for Ramp and Attrition)

```
Effective Capacity = Total Reps × Ramped % × Avg Quota Attainment × (1 - Turnover Rate)
```

### Ramp Time Calculations

| Rep Status | Productivity Factor | Notes |
|---|---|---|
| Fully ramped (7+ months) | 100% | At full quota capacity |
| Ramping (0-7 months) | 50% | Average across ramp period |
| New hire (first 30 days) | 0-25% | Training, onboarding |

**Formula:**
```
Ramped Rep Equivalent = (Fully Ramped Reps × 1.0) + (Ramping Reps × 0.5)
```

### Roll-Forward Headcount Model

```
Ending AE Reps = Beginning AE Reps + New Hires - Churn

Example:
Q1 Start: 10 AEs
+ New Hires: 3
- Churn: 1
= Q1 End: 12 AEs

Effective Capacity: 10 × 1.0 + 2 × 0.5 = 11 Ramped Rep Equivalents
```

### Account Capacity Calculation

```
Accounts per Rep = Available Selling Hours / Hours per Account

Available Selling Hours: ~1,800/year (factoring in admin, travel, meetings)
Hours per Account: Varies by segment
  - Enterprise: 40-80 hours/year
  - Mid-Market: 20-40 hours/year
  - SMB: 5-15 hours/year
```

---

## Capacity Planning Models

| Model | Description | Best For |
|---|---|---|
| **Workload Model** | Total workload required per account segment | Differentiated account needs |
| **Revenue Model** | Total revenue per segment × target productivity | Revenue-focused planning |
| **Account Ratios** | Market benchmark for accounts per rep by segment | Standardized coverage |

### Workload Model Example

```
Target Accounts: 500
Hours per Account: 30
Total Hours Needed: 15,000
Available Hours per Rep: 1,800
Reps Needed: 15,000 / 1,800 = 8.3 → 9 reps
```

### Revenue Model Example

```
Target Revenue: $5M
Quota per Rep: $750K
Attainment Rate: 80%
Effective Quota: $600K
Reps Needed: $5M / $600K = 8.3 → 9 reps
```

---

## Territory Assignment Rules

### Assignment Criteria (Priority Order)

| Priority | Criteria | Weight |
|---|---|---|
| 1 | Geographic proximity (if field sales) | 25% |
| 2 | Industry expertise match | 25% |
| 3 | Account size/tier match | 20% |
| 4 | Workload balance | 15% |
| 5 | Historical relationship | 15% |

### Round-Robin Rules

```
Conditions for Round-Robin:
1. Lead meets qualification criteria
2. No territory assignment overrides apply
3. Rep is available (not on PTO, quota not exceeded)

Weighting Options:
- Equal distribution
- Weighted by capacity (inverse of current load)
- Weighted by performance (top performers get more)
```

### Holdout Rules

| Scenario | Rule |
|---|---|
| **Rep on PTO** | Skip in rotation, reassign leads |
| **Rep at capacity** | Skip until workload decreases |
| **Open territory** | Pool distribution or manager coverage |
| **Transitioning rep** | Shadow period with both old/new rep |

---

## Automation Approaches

### HubSpot Territory Assignment

```
Workflow Logic:
1. Trigger: Contact/Company created OR ownership blank
2. Branch by: Region/Country property
3. Rotate among: Reps assigned to that region
4. Fallback: Manager if no match

Advanced: Use HubDB for territory mapping
- Table: territory_assignments
- Columns: postal_code, country, owner_id
- Lookup in workflow via custom code action
```

### Salesforce Enterprise Territory Management (ETM)

```
Territory Hierarchy:
1. Define territory model
2. Create territory types (geo, vertical, named)
3. Assign accounts to territories via rules
4. Assign users to territories
5. Enable territory sharing rules

Benefits:
- Native forecasting by territory
- Complex hierarchies supported
- Account/opportunity assignment rules
```

### Third-Party Tools

| Tool | Best For | Key Features |
|---|---|---|
| **Fullcast** | End-to-end RevOps | Auto-balancing, routing, holdouts |
| **LeanData** | Lead routing | Complex matching, SLA tracking |
| **Clari** | Territory intelligence | Forecasting, coverage analysis |

---

## Rebalancing Triggers

### Quantitative Triggers

| Metric | Threshold | Action |
|---|---|---|
| **Territory performance variance** | >±20% of average | Review and rebalance |
| **Quota attainment gap** | Significant variance between similar territories | Investigate root cause |
| **Pipeline coverage** | Below 3x target | Add accounts or reduce quota |
| **Conversion rates declining** | -15% from baseline | Review account quality |

### Qualitative Triggers

| Event | Timing | Action |
|---|---|---|
| **Rep departure** | Immediately | Absorption or babysitting |
| **Rep promotion** | At transition | Territory reassignment |
| **Major account churn** | Within 30 days | Account replacement |
| **New market expansion** | Quarterly | Territory creation |
| **M&A activity** | Post-close | Full rebalancing |

### Rebalancing Cadence

| Review Type | Frequency | Scope |
|---|---|---|
| **Spot adjustments** | As needed | Individual territory fixes |
| **Quarterly review** | Every quarter | Performance variance check |
| **Annual planning** | Yearly | Full redesign consideration |
| **Major event response** | Event-driven | Partial or full rebalance |

---

## Compensation Implications

### Territory Change Scenarios

| Scenario | Compensation Approach |
|---|---|
| **Account reassignment** | Pro-rate quota, credit splits, transition period |
| **Territory expansion** | Quota adjustment or stretch targets |
| **Territory reduction** | Quota relief, protection period |
| **Turnover coverage** | Absorption vs. babysitting methodology |

### Handling Open Territories

**Absorption Method:**
- Accounts permanently reassigned
- Territory disappears
- Full quota inherited
- Risk: Overpayment if accounts easier than expected

**Babysitting Method:**
- Temporary coverage during vacancy
- Reduced commission rate (e.g., 50%)
- Original quota maintained for rehire
- Better for planned short-term gaps

### Best Practices

- Redesign territories and quotas together (not separately)
- Adjust pay curves closer to market benchmarks
- Ensure fairness through data-backed territory potential analysis
- Build in transition protection when changes occur
- Communicate clearly how comp will be handled during changes

---

## Common Mistakes

| Mistake | Impact | Fix |
|---|---|---|
| Gut-based territory design | Unequal opportunity, resentment | Use data for potential analysis |
| Static territories | Changing market ignored | Quarterly review cadence |
| Ignoring ramp time | Capacity overestimated | Factor in ramp productivity |
| One-size-fits-all | Mismatched motions | Segment-specific models |
| No automation | Inconsistent assignment | Encode rules in CRM |
| Territory without comp alignment | Unfair earnings | Design together |

---

## Implementation Checklist

### Phase 1: Discovery (Week 1-2)

- [ ] Audit current territory model and assignments
- [ ] Document rep coverage and capacity
- [ ] Analyze historical performance by territory
- [ ] Identify pain points and gaps

### Phase 2: Design (Week 3-4)

- [ ] Define territory model (geo, vertical, hybrid)
- [ ] Calculate capacity requirements
- [ ] Map accounts to territories
- [ ] Balance workload and opportunity

### Phase 3: Automation (Week 5-6)

- [ ] Configure CRM routing rules
- [ ] Set up round-robin logic
- [ ] Build holdout management
- [ ] Test assignment accuracy

### Phase 4: Rollout (Week 7-8)

- [ ] Communicate changes to team
- [ ] Train on new structure
- [ ] Monitor for issues
- [ ] Document for future reference

---

## Cross-References

- **Capacity Planning Formulas:** See `territory-planning-capacity.md`
- **Assignment Automation:** See `territory-planning-automation.md`
- **SLA Management:** See `sla-management-framework.md`
- **Lead Routing:** See `lead-management/lead-routing-framework.md`

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
