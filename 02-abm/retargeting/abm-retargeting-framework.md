# ABM Retargeting — Framework

Audience segmentation, frequency management, and multi-channel orchestration for Account-Based Marketing retargeting campaigns.

---

## Why Retargeting Matters in ABM

ABM retargeting is **not** the same as generic display retargeting. ABM retargeting:

1. **Targets known accounts** — People at specific companies already in your ICP
2. **Respects the buying committee** — Different messages for different roles
3. **Coordinates across channels** — Ads + email + BDR outreach + direct mail in sync
4. **Accelerates pipeline** — Re-engages warm accounts that stalled
5. **Wins back lost deals** — Systematically reactivates churned or lost opportunities

---

## Audience Segmentation

### Core Retargeting Segments

| Segment | Definition | Time Window | Use Case |
|---|---|---|---|
| **Recent Engagers** | Visited site, clicked ad, engaged with content in last 2 weeks | 0-14 days | Hot follow-up, strike while iron is hot |
| **Warm Traffic** | Engaged 30-90 days ago but haven't converted | 30-90 days | Re-engagement, new angle/offer |
| **Page-Specific Visitors** | Visited high-intent pages (pricing, demo, case studies) | 30-60 days | Direct conversion campaigns |
| **Content Engagers** | Downloaded content, watched videos, attended webinars | 60-90 days | Nurture deeper into funnel |
| **Company List Retargeting** | Known accounts from CRM, not yet engaged | Ongoing | Account awareness campaigns |
| **Buying Committee** | Multiple contacts at same account | Ongoing | Surround the account |

### Segment Priority Matrix

| Priority | Segment | Why | Monthly Budget % |
|---|---|---|---|
| **1st** | Recent engagers (0-14 days) | Highest intent, freshest interest | 30-40% |
| **2nd** | Page-specific (pricing/demo) | Clear buying signals | 25-30% |
| **3rd** | Warm traffic (30-90 days) | Need reactivation push | 20-25% |
| **4th** | Content engagers | Educated but not ready | 10-15% |
| **5th** | Company list (no engagement yet) | Awareness stage | 5-10% |

### Advanced Segmentation Strategies

#### Engagement Depth Scoring

```
Score accounts by cumulative engagement:

1-2 touchpoints  → Light engagement    → Awareness content
3-5 touchpoints  → Moderate engagement → Solution content
6-10 touchpoints → Heavy engagement    → Conversion content
10+ touchpoints  → Hot account         → BDR outreach + direct offers
```

#### Recency-Frequency Matrix

| Recency | High Frequency (5+ visits) | Medium (2-4 visits) | Low (1 visit) |
|---|---|---|---|
| **Recent (0-14 days)** | Hot lead — BDR priority | Warm — conversion push | Curious — nurture |
| **Mid (15-45 days)** | Cooling — re-engage urgently | Lukewarm — new angle | Fading — awareness content |
| **Old (46-90 days)** | Was hot, now cold — win-back | Stalled — problem/solution | One-time — exclude or light touch |

---

## LinkedIn Retargeting Audiences

### Available Audience Types

| Audience Type | How to Build | Minimum Size | Best For |
|---|---|---|---|
| **Website Retargeting** | LinkedIn Insight Tag on site | 300 members | High-intent page visitors |
| **Company List Upload** | CSV upload from CRM | 300 matched companies | Account-level targeting |
| **Contact List Upload** | Email list via HubSpot sync | 300 matched members | Person-level precision |
| **Video Viewers** | People who watched 25/50/75/97% of video ads | 300 members | Nurture video engagers |
| **Lead Gen Form Openers** | Opened but didn't submit form | 300 members | Form abandonment recovery |
| **Event Attendees** | LinkedIn Event RSVPs | 300 members | Event follow-up campaigns |
| **Engaged with Company Page** | Followers, page visitors, ad engagers | 300 members | Brand awareness retargeting |

### LinkedIn Audience Building Best Practices

```
Website Retargeting Setup:
1. Install LinkedIn Insight Tag on all pages
2. Create URL-based audiences for key pages:
   - /pricing → "Pricing Page Visitors"
   - /demo → "Demo Page Visitors"
   - /case-studies/* → "Case Study Readers"
   - /blog/* → "Blog Readers"
3. Set lookback windows (7, 30, 90, 180 days)
4. Exclude converted leads to avoid waste
```

### Audience Exclusion Strategy

| Audience | Exclude From | Why |
|---|---|---|
| Current customers | All prospecting campaigns | Don't waste budget |
| Closed-won last 90 days | All retargeting | They already bought |
| Disqualified leads | All campaigns | Known bad fit |
| Competitors | All campaigns | Competitive intelligence risk |
| Bounced/unsubscribed contacts | Email-synced audiences | Compliance + waste |

---

## Frequency Management

### The Frequency Problem

**Too low:** Account never remembers you, no brand recall, wasted impressions.
**Too high:** Ad fatigue, negative brand perception, wasted budget, annoying buyers.

### Frequency Caps by Sales Cycle Length

| Sales Cycle | Frequency Cap (Daily) | Frequency Cap (Weekly) | Rationale |
|---|---|---|---|
| **Short (< 30 days)** | 3-4 impressions/day | 15-20/week | Aggressive — they decide fast |
| **Medium (30-90 days)** | 1-2 impressions/day | 7-12/week | Balanced — stay top of mind |
| **Long (90+ days)** | 0.5-1 impression/day | 3-7/week | Light touch — avoid fatigue |

### Channel-Specific Frequency Guidelines

| Channel | Recommended Frequency | Notes |
|---|---|---|
| **LinkedIn Ads** | 2-3x/week per user | LinkedIn's algorithm manages some capping |
| **LinkedIn InMail/Messages** | 1-2x/month | Very limited — high annoyance risk |
| **Meta Ads (Retargeting)** | 3-5x/week | Meta allows tighter frequency control |
| **Google Display** | 3-4x/day | Cheap impressions, higher tolerance |
| **CTV/Streaming** | 2-3x/week | Premium, don't oversaturate |
| **Email** | 1-2x/week | Coordinated with ad sequences |
| **BDR Outreach** | 1-2 touches/week | Multi-channel (email + LinkedIn) |

### Detecting Ad Fatigue

| Signal | Threshold | Action |
|---|---|---|
| **CTR decline** | -20-30% from baseline | Refresh creative immediately |
| **CPM increase** | +30-40% from baseline | Reduce frequency or pause audience |
| **Frequency > 5** (retargeting) | For any segment | Rotate creative or expand audience |
| **Frequency > 8** | For any campaign | Hard pause — audience exhausted |
| **Negative engagement** | Hide ad, negative comments | Kill the creative |
| **Conversion rate drop** | -25%+ from baseline | Review entire funnel, not just ads |

### Creative Rotation Strategy

```
Rotation Schedule by Audience Temperature:

HOT audiences (0-14 days):
  → Rotate creative every 2 weeks
  → 3-4 active variants minimum
  → Test different CTAs aggressively

WARM audiences (15-45 days):
  → Rotate creative every 3-4 weeks
  → 2-3 active variants
  → Test different angles/proof points

COOL audiences (46-90 days):
  → Rotate creative monthly
  → 2 active variants sufficient
  → Focus on reactivation messaging
```

---

## Multi-Channel Orchestration

### Channel Mix by Funnel Stage

| Stage | Primary Channels | Secondary Channels | Budget % |
|---|---|---|---|
| **Awareness** | LinkedIn Ads, CTV, Podcast/Audio | Meta (brand), Google Display | 25-30% |
| **Interest** | LinkedIn Ads, Meta Retargeting | Email nurture, Content syndication | 30-35% |
| **Consideration** | LinkedIn Ads, Meta Retargeting, Email | BDR outreach, Direct mail | 25-30% |
| **Decision** | BDR outreach, Email, Direct mail | LinkedIn InMail, Personalized landing pages | 10-15% |

### Multi-Channel Sequence Example

```
Day 0:  Account visits pricing page (trigger)
        → Add to "Hot" retargeting segment

Day 1:  LinkedIn ad (case study)
        Email: "Saw you checking us out..."

Day 3:  Meta retargeting ad (social proof)

Day 5:  LinkedIn ad (product demo)
        BDR LinkedIn connection request

Day 7:  Email: Value proposition reminder
        LinkedIn ad (comparison content)

Day 10: BDR outreach email
        Meta ad (urgency/offer)

Day 14: Direct mail (if high-value account)
        LinkedIn InMail (if executive)

Day 21: If no response → move to "Warm" segment
        Reduce frequency, change messaging angle
```

### Channel Coordination Rules

| Rule | Implementation | Why |
|---|---|---|
| **No channel in isolation** | Every ad should have email backup | Redundancy increases touch probability |
| **BDR follows ads** | Outreach within 48 hours of high engagement | Strike while they're thinking about you |
| **Suppress ads during active sales** | Pause retargeting when in active sales convo | Avoid undermining BDR relationship |
| **Escalate high-value accounts** | Trigger direct mail at engagement threshold | Premium touch for premium accounts |
| **Coordinate messaging** | Same theme across all channels per week | Unified story, stronger recall |

### Channel Attribution Model

```
Multi-Touch Attribution for ABM:

First Touch (20%):    What channel introduced the account?
Last Touch (20%):     What channel got the meeting/conversion?
Linear (60%):         Distributed across all touchpoints

Weight adjustments:
  - BDR meeting booked: 2x weight
  - Content download: 1.5x weight
  - Ad click: 1x weight
  - Ad impression: 0.5x weight
  - Email open: 0.25x weight
```

---

## Platform-Specific Retargeting Setup

### LinkedIn Retargeting

```
Campaign Manager Setup:
1. Audience > Create Audience > Website
2. Select pages to retarget (use OR logic for multiple URLs)
3. Set lookback window (7/30/90/180 days)
4. Create matched audience from company list (separate)
5. Combine: Website visitors AND Company list
   → This retargets only known accounts who visited
```

### Meta Retargeting for ABM

```
Meta Business Manager Setup:
1. Install Meta Pixel on ABM landing pages
2. Create Custom Audience from website traffic
3. Upload company email domains (limited match rate)
4. Use Lookalike audiences sparingly (dilutes ABM precision)
5. Focus on retargeting, not prospecting on Meta
```

### Google Display for ABM

```
Google Ads Setup:
1. Create remarketing lists from Google Tag
2. Target specific pages (pricing, demo request)
3. Use RLSA for search intent + retargeting combo
4. Combine with company IP targeting (DemandBase, RollWorks)
5. Note: Match rates are low for B2B — use as supplement only
```

---

## Audience Sync Architecture

### HubSpot to LinkedIn Flow

```
CRM Data Flow:

HubSpot Company Lists (by ABM stage)
  ↓
Active list filters (e.g., "ABM Stage = Interested")
  ↓
HubSpot Ad Audiences (auto-sync to LinkedIn)
  ↓
LinkedIn Matched Audiences (~48 hour sync)
  ↓
Campaign Manager targets audience
  ↓
Engagement data flows back via ZenABM/Fibbler
  ↓
HubSpot updates account stage
  ↓
List membership changes automatically
  ↓
LinkedIn audience updates (removes old, adds new)
```

### Recommended List Structure

| HubSpot List | LinkedIn Audience | Campaign Type |
|---|---|---|
| ABM - Identified | ABM - Cold Accounts | Awareness campaigns |
| ABM - Aware | ABM - Aware Accounts | Awareness + light solution |
| ABM - Interested | ABM - Interested Accounts | Solution-focused |
| ABM - Considering | ABM - Hot Accounts | Conversion + BDR coordination |
| ABM - Lost Deals (90 days) | ABM - Win Back | Win-back campaigns |
| ABM - Churned Customers | ABM - Churned | Re-acquisition campaigns |

---

## Budget Allocation for Retargeting

### Retargeting vs. Prospecting Split

| Program Maturity | Prospecting % | Retargeting % | Why |
|---|---|---|---|
| **New ABM program** | 70-80% | 20-30% | Build audience first |
| **6-12 months** | 60-70% | 30-40% | Retargeting pools growing |
| **Mature (12+ months)** | 50-60% | 40-50% | Large engaged audience |
| **Saturated accounts** | 40-50% | 50-60% | Maximize existing engagement |

### Cost Efficiency by Segment

| Segment | Expected CPC | Expected Conversion Rate | Priority |
|---|---|---|---|
| Recent engagers (0-14 days) | $6-10 | 3-5% | Highest ROI |
| Pricing page visitors | $8-12 | 4-6% | Very high ROI |
| Content engagers | $5-8 | 1-2% | Medium ROI |
| Warm traffic (30-90 days) | $7-10 | 1-3% | Medium ROI |
| Cold account list | $10-15 | 0.5-1% | Lower ROI, but necessary |

---

## Measurement Framework

### Retargeting-Specific KPIs

| Metric | Benchmark | When to Worry |
|---|---|---|
| **Retargeting CTR** | 0.5-0.8% (2x prospecting) | Below 0.4% |
| **Retargeting CPC** | 20-30% lower than prospecting | Higher than prospecting |
| **Frequency (retargeting)** | 4-6/week | Above 8/week |
| **Conversion rate (retargeting)** | 2-4% (3x prospecting) | Below 1.5% |
| **Return visitor rate** | 30-40% of retargeted users | Below 20% |
| **Pipeline velocity increase** | 15-25% faster | No measurable improvement |

### Reporting Cadence

| Frequency | What to Review |
|---|---|
| **Daily** | Frequency caps, budget pacing, any anomalies |
| **Weekly** | CTR by segment, conversion by segment, creative performance |
| **Bi-weekly** | Channel mix effectiveness, sequence optimization |
| **Monthly** | Pipeline attribution, cost per opportunity, audience health |
| **Quarterly** | Full funnel analysis, segment profitability, strategy adjustments |

---

## Common Retargeting Mistakes

| Mistake | Impact | Fix |
|---|---|---|
| No frequency caps | Audience burnout, wasted budget | Set caps per channel and segment |
| Same creative for all segments | Poor relevance, low engagement | Tailor messaging to segment intent |
| Retargeting everyone equally | Budget waste on low-intent | Prioritize by recency and behavior |
| Ignoring cross-channel coordination | Disjointed experience, annoyed buyers | Orchestrate sequences across channels |
| No exclusions | Targeting customers, competitors | Build robust exclusion lists |
| Set and forget | Diminishing returns over time | Weekly optimization, creative refresh |
| Treating ABM retargeting like B2C | Wrong tactics, poor results | Account-level thinking, buying committee awareness |

---

## Cross-References

- **LinkedIn Campaign Setup:** See `/gtm-skills/skills-abm/linkedin-ads/linkedin-ads-abm-guide.md`
- **Persona Targeting:** See `/gtm-skills/skills-abm/persona-mapping/persona-mapping-framework.md`
- **Retargeting Playbooks:** See `/gtm-skills/skills-abm/abm-retargeting/abm-retargeting-playbooks.md`
- **Landing Page Personalization:** See `/gtm-skills/skills-abm/abm-retargeting/abm-retargeting-landing-pages.md`

*Source: ColdIQ*

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
