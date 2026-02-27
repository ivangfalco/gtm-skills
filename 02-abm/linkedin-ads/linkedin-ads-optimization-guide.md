# LinkedIn Ads Optimization — Guide

Weekly workflows, bidding strategy, audience penetration rules, demographic audits, creative testing, and budget optimization for B2B campaigns on LinkedIn.

For campaign structure, ad formats, and budget math, see [linkedin-ads-abm-guide.md](./linkedin-ads-abm-guide.md)
For creative strategy and messaging frameworks, see [linkedin-ads-creative-strategy.md](./linkedin-ads-creative-strategy.md)

---

## Weekly Optimization Workflow

Run this every week. Most advertisers skip the demographic audit - that is where the biggest savings hide.

### Step 1: Demographic Audit (15 minutes)

Open Campaign Manager - Demographics tab for each active campaign.

| Dimension | What to Check | Action |
|---|---|---|
| **Job Title** | Are irrelevant titles consuming budget? | Exclude them immediately |
| **Job Function** | Aligned with your ICP functions? | Flag any off-target functions |
| **Seniority** | Any unpaid, training, or entry-level showing? | Exclude - these are not decision-makers |
| **Industry** | Off-target industries getting impressions? | Exclude those with impressions but zero engagement |
| **Company Size** | Aligned with your target segments? | Exclude company sizes outside ICP |
| **Company Name** | Any competitors or existing customers? | Exclude from cold campaigns |

**The job function approach:** If using job function + seniority targeting (instead of specific titles), treat the demographics report like a negative keyword list. Exclude every irrelevant title that shows up. After 6-8 weeks, the noise stops.

### Step 2: Performance Metrics Review (10 minutes)

| Metric | Healthy Range (TOF) | Healthy Range (MOF) | Healthy Range (BOF) | Action If Below |
|---|---|---|---|---|
| **CTR to Landing Page** | 0.30-0.55% | 0.55-0.80% | 0.80-1.30% | Refresh creative or tighten audience |
| **CPC** | $8-19 | $8-15 | $10-22 | Switch to manual bidding or refresh creative |
| **CPE (Cost per Engagement)** | Below $5 | Below $3 | N/A | Review targeting if above |
| **Frequency** | <3/week per person | <3/week per person | <5/week per person | Rotate creative or expand audience |
| **Spend Pacing** | Spending full daily budget | Spending full daily budget | Spending full daily budget | Audience too small or bid too low |

### Step 3: Creative Health Check (10 minutes)

- Any ad running 3+ months without refresh? - Replace it
- Fewer than 4 active ads per campaign? - Add more to prevent fatigue
- CTR declining 2+ consecutive weeks? - Creative fatigue, rotate in new ads
- Check ad rotation: new ads should run with even rotation for 7-10 days, then switch to auto rotation so the algorithm favors winners

### Step 4: Audience Penetration Check (5 minutes)

| Timeframe | Penetration Target | Action If Below |
|---|---|---|
| 30 days | 25%+ of audience reached | Increase budget - you are underspending |
| 60 days | 40%+ of audience reached | Increase budget - leaving reach on the table |
| Sustained | 35%+ penetration | Healthy - maintain current budget |

**Key rule:** One well-budgeted campaign at 35%+ penetration outperforms three underfunded campaigns at 12% each. Consolidate budget before adding more campaigns.

### Step 5: Budget Reallocation (5 minutes)

- Shift budget from underperformers to outperformers
- Never change more than 20% of a campaign's budget at once - the algorithm needs stability
- If a campaign has fewer than 10 results per week, it lacks enough data to optimize

---

## Bidding Strategy

### Phase 1: Automated Bidding (Week 1)

Start every new campaign with automated/maximum delivery bidding. This lets LinkedIn's algorithm learn who engages and at what cost. Do not touch bids during this phase.

### Phase 2: Manual CPC (Week 2+)

After week 1, switch to manual CPC bidding at **20% below your average CPC** from the automated phase. This works for significant CPC reductions in most campaigns.

### When to Stay on Automated

| Scenario | Why |
|---|---|
| Small retargeting audiences (<10K) | Manual bidding causes underdelivery on tiny audiences |
| ABM company list campaigns | Same reason - audience too small for manual optimization |
| New campaign objective | Reset to automated for the first week when changing objectives |

### Bid Strategy by Campaign Objective

| Objective | Recommended Bid Type | Notes |
|---|---|---|
| Engagement (TOF) | Start automated - switch manual week 2 | Optimize for lowest cost per engagement |
| Video Views (TOF) | Automated usually fine | Video views are cheap on LinkedIn |
| Website Visits (MOF/BOF) | Start automated - switch manual week 2 | Monitor CPC closely after switch |
| Lead Gen Forms (BOF) | Cost cap or manual | Set cap at your target CPL |
| Conversions (BOF) | Automated for small audiences, manual for large | Depends on audience size |

### Cost Cap Bidding

Use cost cap when you have a strict CPL target. Set the cap at your target CPL, not below it. LinkedIn will try to deliver at or below your cap, but setting it too low causes underdelivery.

---

## Audience Penetration Rules

### When to Scale Budget

| Signal | What It Means | Action |
|---|---|---|
| Penetration below 25% at 30 days | Budget is too low for audience size | Increase budget 20-30% |
| Penetration below 40% at 60 days | Still leaving reach on the table | Increase budget or narrow audience |
| Penetration at 35%+ and steady | Healthy reach | Maintain - consider expanding audience |
| Penetration at 50%+ | Audience is close to saturated | Expand audience or reduce budget |
| Budget increasing but reach flat | Competitors outbidding you or low ad quality | Improve creative quality first |

### When to Narrow Audience

| Signal | Action |
|---|---|
| High impressions, very low CTR (<0.20%) | Audience too broad - not relevant enough |
| Demographics show 40%+ off-target titles/industries | Add exclusions to cut waste |
| CPMs spiking without engagement improvement | Audience may be too narrow already - check size |

### The Penetration Math

Doubling budget typically boosts penetration by 50-70%, not 100%. There are diminishing returns.

**Example:**
- Current: $5K/month, 18% penetration
- After doubling to $10K/month: expect ~28-30% penetration (not 36%)
- To hit 35%+: may need $12-15K/month for this audience size

### Diagnosing Stalled Reach

If spending increases but reach does not grow (while frequency rises):

1. **Check competitors** - Are others outbidding you for the same audience?
2. **Check ad quality** - Low engagement signals = LinkedIn deprioritizes your ads
3. **Check audience size** - May be smaller than reported if many members are inactive

Fix creative quality first. If ads are strong and audience is well-structured, then increase budget.

---

## Demographic Audit Process

### The Full Audit (Run Monthly)

Beyond the weekly demographic check, run a deep audit monthly:

**1. Company Demographics**

| Dimension | Look For | Action |
|---|---|---|
| Company name | Top spenders that are competitors or existing customers | Exclude immediately |
| Company size | Budget going to wrong company sizes | Exclude off-target sizes |
| Industry | Non-ICP industries eating budget | Exclude low-engagement industries |

**2. Professional Demographics**

| Dimension | Look For | Action |
|---|---|---|
| Job title | Titles with high spend but zero conversions | Exclude them |
| Job function | Functions that don't match ICP | Exclude or create separate campaigns |
| Seniority | Entry-level, training, unpaid consuming budget | Exclude from all campaigns |

**3. Geography (if multi-region)**

| Dimension | Look For | Action |
|---|---|---|
| Country/Region | Expensive regions with low conversion rates | Split into separate campaigns or exclude |
| Cost disparities | US CPCs 2-3x higher than EMEA | Set separate budgets per region |

### The Negative Title List

When using job function targeting, build a running exclusion list:

**Common irrelevant titles that consume B2B SaaS budget:**
- Regional Managers, Branch Managers
- Call Center Supervisors, Customer Service Reps
- Fashion Designers, Interior Designers (if targeting "design" function)
- Telemarketers, Retail Associates
- Teachers, Professors (if targeting "training" function)

Add to exclusions weekly. After 6-8 weeks of consistent exclusions, the noise drops significantly.

---

## Creative Testing Methodology

### What to Test (Priority Order)

| Priority | Element | Impact | Minimum Data Needed |
|---|---|---|---|
| 1 | **Messaging angle** | Highest | 1,000+ impressions per variant |
| 2 | **Visual style** | High | 1,000+ impressions per variant |
| 3 | **Social proof type** | High | 1,000+ impressions per variant |
| 4 | **Headline** | Medium | 2,000+ impressions per variant |
| 5 | **CTA** | Medium | 2,000+ impressions per variant |
| 6 | **Ad format** | Medium | 5,000+ impressions per variant |
| 7 | **Copy length** | Low | 5,000+ impressions per variant |

### Testing Rules

| Rule | Why |
|---|---|
| Test one variable at a time | Know what caused the difference |
| Run minimum 2 weeks | Account for weekly variations |
| Need 1,000+ impressions per variant | Below this, results are random noise |
| Don't test more than 2-3 variants | Budget dilution kills test quality |
| Winner takes all | Pause losers completely, scale winner |

### Statistical Significance Quick Reference

| Impressions per Variant | Minimum CTR Difference to Be Meaningful |
|---|---|
| 1,000 | 0.15% |
| 5,000 | 0.07% |
| 10,000 | 0.05% |
| 20,000 | 0.03% |

With 5,000 impressions each, you need roughly 0.07% CTR difference to be confident the result is not noise.

### Test Execution Framework

**Week 1-2:** Launch test variants with even rotation (equal budget per ad)
**Week 2-3:** Review results - pause clear losers early if data is sufficient
**Week 3-4:** Declare winner based on statistical significance
**Week 4+:** Scale winner to other campaigns, launch next test

### What to Do with Results

| Result | Action |
|---|---|
| Clear winner (>0.07% CTR difference at 5K impressions) | Scale winner, pause loser, test next variable |
| No clear winner (difference within noise range) | Both are fine - keep both running, test a different variable |
| Both performing poorly (<0.20% CTR) | Problem is not the variable you tested - check audience or offer |

---

## When to Pause vs Scale a Campaign

### Pause When

| Signal | Timeframe | Why |
|---|---|---|
| CTR below 0.20% after 2 weeks | 14+ days | Audience is not responding |
| CPC 3x above benchmark with no trend improvement | 14+ days | Too expensive to sustain |
| Zero conversions after spending 3x your target CPL | Anytime | Not converting - fix before spending more |
| Frequency above 6/month per person | Monthly | Audience fatigue - you are annoying people |
| Demographics show 60%+ waste (off-target impressions) | Weekly check | Budget is being burned on wrong people |

### Scale When

| Signal | Timeframe | Action |
|---|---|---|
| CTR above benchmark and stable for 2+ weeks | 14+ days | Increase budget 20-30% |
| CPC below benchmark and improving | 14+ days | Increase budget or expand audience |
| Penetration below 25% at 30 days | 30 days | Increase budget - audience is underserved |
| Strong pipeline attribution from campaign | 60+ days | Double down - this is working |
| High engagement + retargeting pool growing | 30+ days | Maintain or increase - funnel is filling |

### The Pause Decision Tree

```
Campaign underperforming?
  ├── Is audience size adequate (50K+ cold, 1K+ retargeting)?
  │     ├── No → Expand audience, don't pause
  │     └── Yes → Continue
  ├── Is creative fresh (<3 months)?
  │     ├── No → Refresh creative first, don't pause
  │     └── Yes → Continue
  ├── Are demographics showing waste?
  │     ├── Yes → Add exclusions, reassess in 1 week
  │     └── No → Continue
  ├── Has it been running 2+ weeks with data?
  │     ├── No → Wait - not enough data
  │     └── Yes → Continue
  └── Still underperforming after all checks?
        └── Pause. Reallocate budget to performing campaigns.
```

---

## Budget Optimization Across Campaign Groups

### Group Budget Feature

LinkedIn's campaign group budget lets the algorithm allocate budget across campaigns within a group instead of setting individual budgets.

**Benefits (from real data at scale):**
- Cost per reach decreases ~10% on average
- Audience penetration nearly doubles vs individual campaign budgets
- One month of group budget = two months of campaign-level budget in audience penetration

### When to Use Group Budget

| Scenario | Use Group Budget? |
|---|---|
| All campaigns in group target same audience type | Yes |
| Mix of enterprise and SMB campaigns | No - algorithm starves the expensive enterprise audience |
| Mix of static and video campaigns | No - 80%+ budget goes to video (cheaper) |
| All campaigns share one objective | Yes |
| Campaigns have different objectives | No - one objective per group required |

### Budget Allocation by Funnel Stage

| Stage | Budget Share | Objective |
|---|---|---|
| **TOF (Cold Awareness)** | 30-50% | Build brand, fill retargeting pool |
| **MOF (Retargeting/Nurture)** | 18-25% | Build trust, deepen engagement |
| **BOF (Conversion)** | 20-30% | Drive demos, trials, conversions |

**Key insight:** Product Aware retargeting often gets the single biggest budget allocation - larger than either TOF stage. Once someone knows you, the highest-ROI move is converting that awareness into pipeline.

### Budget Reallocation Cadence

| Frequency | What to Adjust |
|---|---|
| **Weekly** | Shift 10-20% between campaigns based on performance |
| **Bi-weekly** | Assess campaign group budget splits |
| **Monthly** | Full budget review - reallocate between funnel stages |
| **Quarterly** | Strategic budget review - persona and region allocation |

### The Budget-to-Persona Alignment

Map budget to pipeline contribution, not to equal distribution:

| Persona | Pipeline Share | Current Budget Share | Penetration | Action |
|---|---|---|---|---|
| VP Sales | 45% | 25% | 18% | Increase budget significantly |
| Dir Marketing | 30% | 40% | 42% | Maintain - well penetrated |
| CTO | 25% | 35% | 55% | Reduce slightly - highly penetrated |

The goal is matching budget allocation to pipeline potential. Check this monthly.

---

## Key Benchmarks by Funnel Stage

### Performance Benchmarks

| Metric | TOF (Cold) | MOF (Retargeting) | BOF (Conversion) |
|---|---|---|---|
| **CTR to Landing Page** | 0.30-0.55% | 0.55-0.80% | 0.80-1.30% |
| **CPC** | $8-19 | $8-15 | $10-22 |
| **CPM** | $33-65 | $33-55 | $40-65 |
| **CPE** | $2-5 | $2-3 | N/A |
| **Cost per Lead** | N/A | $50-200 | $50-200 |
| **Cost per Form Submit (Website)** | N/A | N/A | $200-500 |
| **Form Fill Rate** | N/A | N/A | 8%+ target |

### Ad Format Benchmarks

| Format | Avg CTR | Avg CPC | Best Funnel Stage |
|---|---|---|---|
| **TLA** | 1.7x standard ads | As low as $4 | TOF + BOF |
| **Single Image** | 0.35-0.45% | $8-19 | All stages |
| **Video** | 0.28% | $24 | TOF |
| **Carousel** | Moderate | $8-12 | MOF |
| **Document** | Moderate | Moderate | MOF |
| **Spotlight** | Very low CTR | ~$5 CPM | MOF (cheap reinforcement) |
| **Text Ads** | Very low CTR | Negligible | Always-on brand |

### Efficiency Targets

| Metric | Target | When to Worry |
|---|---|---|
| **Pipeline per $1 spent** | $10+ | Below $5 after 90 days |
| **Engagement rate** | Above 1% | Below 0.5% |
| **Video view rate (starts/impressions)** | Above 40% | Below 25% |
| **Video completion rate** | 8-15% | Below 5% |
| **BOF conversion rate** | Above 5% | Below 2% |
| **SQL cost** | Below $500 | Above $500 (unless enterprise ACV justifies it) |

### Industry Context

Adjust expectations based on your market:

| Market | CPC Adjustment | CPL Adjustment |
|---|---|---|
| Enterprise / high ACV ($50K+) | Higher CPCs acceptable | CPLs of $300-500+ justified by deal size |
| SMB / low ACV (<$20K) | Need cheaper CPCs ($5-10) | CPLs must stay $50-150 for unit economics |
| Healthcare | Higher CPMs - smaller specialized audiences | Expect 20-30% premium |
| Tech/SaaS | Most competitive, benchmark CPCs at higher end | Standard benchmarks apply |

---

## Optimization Calendar

### Weekly (Every Monday)

- [ ] Demographic audit - exclude irrelevant titles, industries, companies
- [ ] Performance metrics review - CTR, CPC, CPE per campaign
- [ ] Creative health check - any fatigued ads?
- [ ] Audience penetration check
- [ ] Budget reallocation (small adjustments only)

### Bi-Weekly (Every Other Friday)

- [ ] Campaign group performance review
- [ ] Ad format mix assessment - shift budget to best-performing formats
- [ ] Review retargeting pool sizes - is TOF feeding the funnel?

### Monthly

- [ ] Full demographic audit (deep dive)
- [ ] Budget-to-persona alignment check
- [ ] Pipeline per $ spent calculation
- [ ] Creative refresh planning for next month
- [ ] Pipeline attribution review with sales team

### Quarterly

- [ ] Full account audit
- [ ] Strategy evaluation - is funnel structure still right?
- [ ] Benchmark comparison - are you above or below industry?
- [ ] Budget planning for next quarter
- [ ] ICP refinement based on conversion data

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).**