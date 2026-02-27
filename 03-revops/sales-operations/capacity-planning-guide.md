# Capacity Planning — Guide

Sales capacity formulas, headcount modeling, and quota setting for revenue operations.

---

## The Capacity Planning Formula

### Basic Capacity Calculation

```
Sales Capacity = Number of Reps × Quota × Attainment Rate

Example:
10 reps × $500K quota × 80% attainment = $4M capacity
```

### Effective Capacity (With Ramp and Attrition)

```
Effective Capacity = Total Reps × Ramped % × Quota Attainment × (1 - Turnover Rate)

Example:
12 reps × 83% ramped × $500K × 80% attainment × (1 - 15% turnover)
= 12 × 0.83 × $500K × 0.80 × 0.85
= $3.39M effective capacity
```

---

## Ramp Time Modeling

### Standard Ramp Periods

| Role | Full Ramp Period | Productivity by Month |
|---|---|---|
| **SDR** | 3-4 months | M1: 25%, M2: 50%, M3: 75%, M4: 100% |
| **AE (SMB)** | 4-6 months | M1: 20%, M2: 40%, M3: 60%, M4: 80%, M5-6: 100% |
| **AE (Mid-Market)** | 6-8 months | M1: 15%, M3: 40%, M5: 70%, M7+: 100% |
| **AE (Enterprise)** | 9-12 months | M1: 10%, M3: 30%, M6: 60%, M9: 85%, M12: 100% |

### Ramped Rep Equivalent Calculation

```
Ramped Rep Equivalent = Σ (Rep × Productivity Factor)

Example:
8 fully ramped AEs × 100% = 8.0
2 AEs at month 3 × 60% = 1.2
1 AE at month 1 × 20% = 0.2
────────────────────────
Total: 9.4 Ramped Rep Equivalents
```

### Ramp Quota Treatment

| Approach | Description | When to Use |
|---|---|---|
| **Prorated Quota** | Full quota × months remaining / 12 | Standard approach |
| **Ramped Quota** | Quota matches productivity curve | More accurate, complex |
| **Grace Period** | No quota first 1-3 months | Encourages learning |
| **Milestone-Based** | Quota tied to certification/training | Ensures readiness |

---

## Headcount Planning Model

### Bottom-Up Planning

```
Step 1: Define revenue target
  Target Revenue: $10M

Step 2: Determine productivity assumption
  Quota per Rep: $750K
  Expected Attainment: 80%
  Effective Productivity: $600K/rep

Step 3: Calculate base headcount
  Reps Needed: $10M / $600K = 16.7 → 17 reps

Step 4: Add ramp buffer
  Average Ramp: 6 months (50% productive first year)
  New Hires: 4 reps
  Effective from New: 4 × 0.5 = 2 productive

Step 5: Add attrition buffer
  Expected Attrition: 20%
  Buffer: 17 × 0.20 = 3.4 → 4 reps

Step 6: Final headcount
  Base: 17 + Ramp Buffer: 4 + Attrition Buffer: 4 = 25 reps needed
```

### Roll-Forward Model

```
Quarter-over-Quarter Headcount:

Q1 Start: 20 reps
+ Planned Hires: 5
- Expected Attrition: 2
= Q1 End: 23 reps

Productive Capacity Q1:
Tenured (20 reps × 0.8 attrition adjustment): 16 productive
New (5 reps × 0.25 first quarter): 1.25 productive
= 17.25 ramped rep equivalents
```

### Hiring Timing Model

```
To have X productive reps by date Y, hire by date (Y - Ramp Period):

Example:
Need 5 new productive AEs by Jan 1
Enterprise ramp: 9 months
Must hire by: April 1 (previous year)

Hiring schedule with buffer:
- Start recruiting: Jan 1
- Extend offers: Feb-March
- Start dates: April 1
- Fully productive: Jan 1
```

---

## Quota Setting Framework

### Top-Down vs. Bottom-Up

| Approach | Method | Risk |
|---|---|---|
| **Top-Down** | Revenue target / Number of reps = Quota | May be unrealistic if not achievable |
| **Bottom-Up** | Historical performance × growth factor | May not hit company targets |
| **Blended** | Reconcile both, adjust capacity | Best practice |

### Quota Components

```
Annual Quota = New Business + Expansion + Renewal

Example (Expansion Rep):
New Logos: 40% of quota ($200K)
Expansion: 50% of quota ($250K)
Renewal: 10% of quota ($50K)
Total: $500K annual quota
```

### Quota Attainment Targets

| Percentile | Attainment | Rep Outcome |
|---|---|---|
| Top 10% | 125%+ | President's Club |
| Top 25% | 100-124% | At or above target |
| Median | 80-99% | Acceptable |
| Bottom 25% | 60-79% | Coaching needed |
| Bottom 10% | <60% | PIP or transition |

**Target Distribution:**
- 60-70% of reps at or above quota = healthy
- <50% at quota = quotas too high or team issues
- >80% at quota = quotas too low, leaving money on table

---

## Coverage Ratios

### Accounts per Rep by Segment

| Segment | Accounts per Rep | Rationale |
|---|---|---|
| **Enterprise** | 10-25 | High-touch, long cycles |
| **Mid-Market** | 50-100 | Balanced attention |
| **SMB** | 200-500 | Velocity, lower touch |
| **Self-Serve** | 1,000+ | Tech-enabled scale |

### Leads per SDR

| Motion | Leads per SDR/Month | Rationale |
|---|---|---|
| **Inbound** | 100-200 | Higher volume, lower touch |
| **Outbound** | 200-400 accounts | Prospecting focused |
| **Hybrid** | 50-100 inbound + 150 outbound | Balanced motion |

### SDR to AE Ratio

| Sales Cycle | Ratio | Notes |
|---|---|---|
| **Short (<30 days)** | 1 SDR : 2-3 AEs | AEs can handle more |
| **Medium (30-90 days)** | 1 SDR : 1-2 AEs | Balanced |
| **Long (90+ days)** | 2 SDRs : 1 AE | More pipeline needed |

---

## Pipeline Coverage Model

### Pipeline to Quota Ratio

```
Required Pipeline = Quota × (1 / Win Rate)

Example:
Quota: $500K
Win Rate: 25%
Required Pipeline: $500K × 4 = $2M in pipeline
```

### Pipeline Coverage Benchmarks

| Coverage Ratio | Assessment |
|---|---|
| < 2x | Critical - unlikely to hit quota |
| 2-3x | At risk - need more pipeline |
| 3-4x | Healthy - on track |
| 4-5x | Strong - high probability |
| > 5x | Over-covered - qualify harder |

### Stage-Weighted Pipeline

```
Weighted Pipeline = Σ (Deal Value × Stage Probability)

Example:
Stage 1 (Discovery): $500K × 10% = $50K
Stage 2 (Demo): $300K × 30% = $90K
Stage 3 (Proposal): $200K × 50% = $100K
Stage 4 (Negotiation): $100K × 80% = $80K
────────────────────────────────────────
Weighted Pipeline: $320K
```

---

## Scenario Planning

### Scenario Analysis Template

| Scenario | Assumption | Headcount | Revenue Impact |
|---|---|---|---|
| **Aggressive** | 100% attainment, low attrition | 20 reps | $10M |
| **Base Case** | 80% attainment, 15% attrition | 24 reps | $9M |
| **Conservative** | 70% attainment, 25% attrition | 28 reps | $8M |

### Sensitivity Analysis

```
Key Variables to Test:
- Quota attainment: ±10%
- Attrition rate: ±5%
- Ramp time: ±2 months
- New hire success rate: ±20%

Impact on Revenue:
Each 5% change in attainment = ±$X impact
Each 5% change in attrition = ±$Y impact
```

---

## Capacity Dashboard Metrics

### Leading Indicators

| Metric | Target | Red Flag |
|---|---|---|
| Pipeline coverage ratio | 3-4x | <2x |
| Opportunity creation rate | Steady/growing | Declining 2+ weeks |
| Win rate trend | Stable/improving | Declining >5% |
| Average deal size | Stable/growing | Shrinking |
| Sales cycle length | Stable/shortening | Lengthening |

### Lagging Indicators

| Metric | Target | Red Flag |
|---|---|---|
| Quota attainment | >80% median | <70% median |
| Revenue per rep | Per quota | <70% of quota |
| Rep attrition | <15% annual | >25% annual |
| Time to productivity | Per role benchmark | 50%+ longer |

---

## Common Mistakes

| Mistake | Impact | Fix |
|---|---|---|
| Ignoring ramp time | Overestimated capacity | Factor in ramp curve |
| Not budgeting for attrition | Surprise gaps | 15-20% buffer |
| Setting quotas too high | Demoralized team, turnover | Use data, not wishes |
| Setting quotas too low | Missed company targets | Benchmark against market |
| Equal quotas for unequal territories | Unfair outcomes | Potential-based quotas |
| Annual planning only | Can't adjust mid-year | Quarterly reviews |

---

## Implementation Checklist

### Annual Planning (Q4)

- [ ] Review current year performance
- [ ] Gather revenue targets for next year
- [ ] Model headcount needs
- [ ] Set quotas by role and segment
- [ ] Plan hiring timeline
- [ ] Build scenario models

### Quarterly Reviews

- [ ] Compare actual vs. planned capacity
- [ ] Assess quota attainment distribution
- [ ] Evaluate pipeline coverage
- [ ] Adjust hiring plan if needed
- [ ] Review ramp progress for new hires

### Monthly Monitoring

- [ ] Track ramped rep equivalents
- [ ] Monitor pipeline coverage
- [ ] Check attrition vs. forecast
- [ ] Review productivity metrics

---

## Cross-References

- **Territory Planning:** See `territory-planning-framework.md`
- **SLA Management:** See `sla-management-framework.md`
- **Pipeline Reporting:** See `pipeline-reporting/pipeline-reporting-framework.md`

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
