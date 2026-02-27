# LinkedIn Ads Audience Strategy — Guide

Audience sizing, targeting approaches, exclusion strategy, retargeting setup, and ABM list targeting for B2B campaigns on LinkedIn.

For campaign structure and budget math, see [linkedin-ads-abm-guide.md](./linkedin-ads-abm-guide.md)
For optimization and bidding, see [linkedin-ads-optimization-guide.md](./linkedin-ads-optimization-guide.md)

---

## Audience Sizing Rules

### Cold Audience Sweet Spots by Stage

| Stage | Recommended Size | Why |
|---|---|---|
| **TOF (Cold Awareness)** | 50K-300K | Large enough for the algorithm to optimize, small enough to stay relevant |
| **MOF (Retargeting/Nurture)** | 1K-30K | Warm audiences are naturally smaller - this is expected |
| **BOF (Conversion)** | 1K-5K | Smallest, highest intent - retargeting from MOF engagers |
| **ABM Company Lists** | 300+ matched members minimum | LinkedIn's hard floor - below this, ads will not serve |

### What Happens at Wrong Sizes

| Problem | Symptoms | Fix |
|---|---|---|
| **Too narrow (<15K cold)** | CPMs spike (can go 5-10x above benchmark), algorithm cannot optimize, penetration stays below 10%, budget does not spend fully | Broaden audience - add related job functions, expand industries, or remove a targeting layer |
| **Too broad (>400K cold)** | Low CTR, budget spread thin, poor relevance, off-target impressions | Add filters - narrow by seniority, company size, or industry |
| **Retargeting too small (<500)** | Ads barely serve, frequency spikes, cost per result very high | Increase TOF budget to fill the retargeting pool faster, or extend the lookback window (30-day to 90-day) |

### Audience Size Estimation

LinkedIn Campaign Manager shows estimated audience size when you build targeting. Use these guidelines:

| Your Target | LinkedIn Shows | Interpretation |
|---|---|---|
| Decision-makers at enterprise SaaS | 25K | Too narrow for cold campaign - broaden company size or functions |
| Marketing leaders in US tech | 180K | Sweet spot for TOF |
| All professionals in finance in US | 2M+ | Too broad - add seniority and function filters |

### What Happens When You Broaden an Audience

This is expected behavior when expanding targeting scope:
- **CPMs go down** - more inventory available, less competition
- **CPCs go down** - same reason
- **CTR drops** - broader audience is less precisely relevant
- **Engagement rate drops** - same reason as CTR

This is normal. Do not flag CTR declines as unexpected when the audience was broadened. The trade-off is lower cost per impression but lower engagement quality.

---

## Job Function vs Job Title Targeting

### The Core Difference

| Approach | Reach | Precision | Cost | Maintenance |
|---|---|---|---|---|
| **Job Title targeting** | Narrow | High - exact titles only | Higher CPC | Low - set and forget |
| **Job Function + Seniority** | Broad | Medium - captures related roles | Lower CPC | High - requires weekly negative title exclusions |

### When to Use Job Title Targeting

- You are 100% certain who your ICP is and their exact titles
- You want maximum focus and precision
- You are willing to pay higher costs for that precision
- Your audience is large enough (50K+) with just title targeting
- You have a small number of target titles (5-10)

### When to Use Job Function Targeting

- Your ICP has many different titles (SDRs, MDRs, AEs, Heads of Sales, etc.)
- You want broader reach and cheaper cost per impression
- Your audience size is too small with title targeting alone
- You want to discover which titles exist in your ICP
- You are scaling and need cost-efficient reach

### The Job Function Approach in Practice

**Results from a $500K+ test over 6 months:**
- Target audience size tripled
- Engagement rate stayed similar
- Reach was 2x better
- Cost per reach was 1.6x cheaper
- Required ongoing exclusion of irrelevant titles

**The process:**
1. Target by job function (e.g., "Sales") + seniority (e.g., "Director+")
2. Check demographics report weekly
3. Exclude every irrelevant title that appears - treat it like negative keywords in Google Ads
4. After 6-8 weeks, the irrelevant titles stop showing up

**Common irrelevant titles when targeting broad functions:**

| Function Targeted | Irrelevant Titles to Exclude |
|---|---|
| Sales | Regional Managers, Call Center Supervisors, Retail Associates, Telemarketers |
| Marketing | Fashion Designers, Interior Designers, Graphic Artists (non-digital) |
| Engineering | Civil Engineers, Mechanical Engineers (if targeting software) |
| Operations | Warehouse Managers, Logistics Coordinators (if targeting SaaS ops) |

### Important: Job Title and Seniority Are Mutually Exclusive

On LinkedIn, job title targeting and seniority targeting **cannot be used together** in the same campaign. You must choose one approach:

- Target specific job titles (e.g., "VP of Sales", "Head of Revenue") - OR
- Target by seniority level (e.g., "Director+") combined with job function

This means excluding entry-level seniority is only possible when using seniority-based targeting, not when targeting specific job titles.

### Critical: Business Development Function Includes C-Suite

LinkedIn's Business Development job function includes CEOs, CMOs, and Managing Directors. Do NOT exclude the Business Development function if your ICP includes C-suite.

**Correct approach:** Use seniority exclusions (Entry, Senior, Manager) to filter out non-executive BD roles while keeping CXO/VP/Director-level professionals.

---

## Seniority and Company Size Targeting

### Seniority Targeting

| Seniority Level | Typical Roles | B2B SaaS Relevance |
|---|---|---|
| **CXO** | CEO, CTO, CFO, CMO, CRO | Decision-makers - highest value |
| **VP** | VP Sales, VP Marketing, VP Engineering | Decision-makers - primary targets |
| **Director** | Director of Sales, Director of Marketing | Key influencers and budget holders |
| **Manager** | Marketing Manager, Sales Manager | Users and influencers - secondary targets |
| **Senior** | Senior Developer, Senior Analyst | Individual contributors |
| **Entry** | Analyst, Coordinator, Associate | Rarely ICP for B2B SaaS |
| **Training** | Intern, Trainee | Never ICP |
| **Unpaid** | Volunteer | Never ICP |

**Always exclude:** Unpaid, Training, and Entry seniority from B2B campaigns. These roles do not have purchasing authority and waste budget.

**Decision-makers vs Individual Contributors:** If your product is used by one group but purchased by another, split campaigns:
- Campaign 1: Directors, VPs, C-levels - ROI and strategic messaging
- Campaign 2: Managers, Seniors - productivity and daily-use messaging

### Company Size Targeting

| Segment | Employee Count | Sales Cycle | ACV Expectation |
|---|---|---|---|
| **SMB** | 1-200 | Fast (1-3 months) | Lower |
| **Mid-Market** | 200-500 | Moderate (3-6 months) | Moderate |
| **Enterprise** | 500+ | Long (6-12+ months) | Highest |

**Rules:**
- Use **employee count**, not revenue. LinkedIn does not have access to private company revenue data - only estimates. Employee count is accurate.
- Start with 2 splits, not 3 (e.g., SMB+Mid vs Enterprise)
- The 500-employee threshold is the standard enterprise cutoff - buying processes get significantly slower above this

**LinkedIn distribution bias:** If you target all company sizes together, LinkedIn shows ads mostly to companies with 50-200 and 10,000+ employees. Mid-market companies (200-5,000) get underserved. Splitting by size forces fair distribution.

---

## ABM List Targeting

### Company Lists

Upload your target account list from CRM (CSV with company names, domains, or LinkedIn URLs).

| Requirement | Detail |
|---|---|
| Minimum matched members | 300 to run ads |
| Typical match rate | 60-80% of companies |
| Sync time | ~48 hours for audience to populate |
| Update method | Replace the list to update (HubSpot active lists sync automatically) |

**Layering persona filters on company lists:** After uploading the company list, use LinkedIn's native filters to narrow within those accounts:
- Add job function filter (e.g., "Marketing")
- Add seniority filter (e.g., "Director+")
- Result: only Marketing Directors+ at your target accounts

**Warning:** Each filter layer reduces the matched audience. A list of 500 companies may match 15K members, but adding job function + seniority may drop it to 2K. Check that the final audience still exceeds 300.

### Contact Lists

Upload a list of specific contacts (email addresses). LinkedIn matches on email.

| Requirement | Detail |
|---|---|
| Minimum matched contacts | 300 to run ads |
| Typical match rate | 30-50% (people use personal emails on LinkedIn) |
| Best practice | Combine with company list targeting for better coverage |

**Why match rates are low:** Most professionals created their LinkedIn account with a personal email, not their work email. Your CRM has their work email. The mismatch means low match rates.

### Company Lists vs Contact Lists

| Feature | Company Lists | Contact Lists |
|---|---|---|
| Match rate | Higher (60-80%) | Lower (30-50%) |
| Targeting precision | Company-level (still need persona filters) | Individual-level |
| Audience size | Usually larger | Usually smaller |
| Best for | ABM campaigns targeting specific accounts | Retargeting known contacts, sales acceleration |
| Maintenance | Update as target account list changes | Update as CRM contacts change |

---

## Exclusion Strategy

### Exclusion Priority Order

Apply these from top to bottom. Top priority exclusions are non-negotiable.

| Priority | Exclusion | Why | Apply To |
|---|---|---|---|
| 1 | **Converted users** | Never spend money targeting people who already converted | All campaigns |
| 2 | **Competitors** | Competitors clicking your ads waste budget | Cold campaigns |
| 3 | **Existing customers** | Should be in Expand campaigns, not cold | Cold + MOF campaigns |
| 4 | **Website visitors** | They belong in retargeting, not cold prospecting | Cold campaigns only |
| 5 | **Unpaid/Training/Entry seniority** | No purchasing authority | All campaigns |
| 6 | **Your own employees** | Inflates engagement metrics | All campaigns |
| 7 | **Agency employees** | If working with agencies, exclude their team | All campaigns |

### How to Build Exclusion Audiences

| Audience Type | How to Create | Lookback Window |
|---|---|---|
| Website visitors | LinkedIn Insight Tag - create matched audience | 30, 90, 180 days |
| Competitors | Upload company list of competitor names | Ongoing |
| Existing customers | Upload customer company list from CRM | Sync regularly |
| Converted users | Create audience from conversion event | 90-180 days |
| Employees | Company name exclusion in targeting | Ongoing |

### Exclusion Mistakes to Avoid

| Mistake | Why It Hurts |
|---|---|
| Not excluding converted users from all campaigns | Paying to reach people who already bought |
| Excluding website visitors from retargeting campaigns | That is exactly who retargeting should target |
| Excluding too broadly (entire industry instead of specific companies) | Losing potential ICP accounts |
| Forgetting to update exclusion lists | Stale lists let waste back in |

---

## Audience Expansion and LinkedIn Audience Network

### Audience Expansion - ALWAYS OFF

LinkedIn Audience Expansion is auto-enabled in campaign setup. **Turn it OFF immediately.**

Why: LinkedIn's similarity matching is unreliable. Example: targeting Marketing Managers, LinkedIn finds a "Harvard attendance" pattern, starts targeting Harvard alumni regardless of role.

**There are zero scenarios where Audience Expansion improves B2B campaign performance.** It dilutes targeting precision for negligible reach gains.

### LinkedIn Audience Network (LAN) - ALWAYS OFF

LinkedIn Audience Network places your ads on third-party websites and apps outside LinkedIn.

Why to keep it off:
- Ad quality on partner sites is significantly lower
- No control over which sites show your ads
- Engagement quality drops dramatically
- Dilutes your performance data with low-quality impressions

**If you must test LAN:** Download the publisher list first (Campaign Manager - Plan - Audiences - Brand Safety) and create a block list of misaligned sites. But the recommendation remains: keep it OFF.

---

## Lookalike Audiences

### How Lookalikes Work on LinkedIn

Upload a source audience (matched list, website visitors, or lead gen form submitters). LinkedIn creates a new audience of similar professionals.

| Parameter | Detail |
|---|---|
| Source audience minimum | 300 members |
| Resulting audience | 5x-10x the source audience |
| Creation time | 48-72 hours |
| Quality | Varies - test extensively before committing budget |

### When Lookalikes Are Useful

| Use Case | Source Audience | Expected Quality |
|---|---|---|
| Expanding a proven customer list | Current customer company list | Medium-High |
| Scaling beyond ABM lists | High-performing ABM account list | Medium |
| Finding new personas | Lead gen form submitters | Medium-Low |

### Lookalike Rules

- **Test before committing budget.** Run a small test ($500-1K) before allocating meaningful spend. Match rates and audience quality are often low.
- **Do not combine** lookalike audiences with job title/skill targeting in the same campaign. Layer only broad filters (seniority, company size) on top.
- **Refresh source audiences quarterly.** As your customer base evolves, so should your lookalike seed.
- **Use as a last resort** for audience expansion. Try job functions, different industries, and different regions before relying on lookalikes.

---

## Retargeting Audiences

### Critical Setup Rule

Set up ALL retargeting audiences **before launching any campaigns.** LinkedIn retargeting audiences are NOT retroactive. They only start collecting members from the moment you create them. If you wait 3 months to set up a 90-day website visitor audience, you lose 3 months of data permanently.

### Retargeting Audience Checklist

Create ALL of these before your first campaign launches:

| Audience | Lookback Window | Minimum Size | Funnel Stage |
|---|---|---|---|
| Website visitors (all pages) | 30, 90, 180 days | Varies | MOF |
| Website visitors (high-intent pages: pricing, demo, features) | 30, 90 days | 1K-5K | BOF |
| Video viewers (50%+) | 30, 90 days | 5K-20K | MOF |
| Video viewers (97%+) | 30 days | 1K-5K | BOF (highest intent) |
| Single image ad engagers | 90 days | 5K-20K | MOF |
| Company page visitors/followers | 180 days or lifetime | Varies | MOF |
| Lead gen form openers (non-submitters) | 90 days | Varies | BOF |
| Demo/pricing page visitors | 30, 90 days | 1K-5K | BOF |

### Retargeting Windows by Purpose

| Window | Best For | Why |
|---|---|---|
| **30-day** | High-intent BOF retargeting | Freshest engagement, strongest intent |
| **90-day** | Standard nurture | Balances recency with audience size |
| **180-day** | Low-cost sustainer (text ads, spotlight ads) | Keeps brand visible at minimal cost |

### Retargeting Strategy by Stage

**MOF Retargeting (90-day nurture):**
- Target: video viewers (50%+), ad engagers, company page visitors
- Content: case studies, product demos, educational content, templates
- Objective: Website Visits or Video Views
- Budget: 18-25% of total

**BOF Retargeting (30-day high-intent):**
- Target: video viewers (97%+), demo page visitors, lead gen form openers
- Content: strong CTAs, customer testimonials, ROI data, free trial offers
- Objective: Website Conversions or Lead Gen Forms
- Budget: 20-30% of total

**180-day Sustainer (low-cost brand reinforcement):**
- Target: all prior engagers, broad retargeting
- Content: text ads, spotlight ads, follower ads
- Objective: Brand Awareness
- Budget: Minimal ($5-10/day)

### Cross-Channel Retargeting: Paid Search + LinkedIn

For companies spending $30K+/month on paid search (Google Ads, Bing Ads):

1. Tag all paid search traffic with UTM parameters
2. Create a LinkedIn retargeting audience filtering for website visitors with those UTMs
3. Retarget paid search visitors on LinkedIn with brand-building and social proof content

**Why it works:** Paid search visitors have demonstrated active buying intent (they searched for your solution). Retargeting on LinkedIn reinforces your brand during their evaluation.

**Only worth it** if paid search drives meaningful traffic volume. Below $30K/month search spend, the retargeting audience will be too small to serve ads.

---

## Targeting Do's and Don'ts

### Do

| Action | Why |
|---|---|
| Keep cold audiences 50K-300K | Algorithm needs room to optimize |
| Use 2-3 broad industry groups per campaign | Balance between relevance and reach |
| Target Director+ for decision-makers | These are the people who sign contracts |
| Turn OFF Audience Expansion | It dilutes targeting precision |
| Turn OFF LinkedIn Audience Network | Low-quality impressions |
| Build retargeting audiences before launching | Not retroactive - data is lost permanently |
| Use AND narrowing for audience parameters | Creates precise intersections |
| Exclude competitors and existing customers | Prevents budget waste |
| Exclude converted users from all campaigns | They already converted |
| Group campaigns by similar country costs | Prevents expensive markets from eating all budget |

### Don't

| Action | Why |
|---|---|
| Split into micro-segments under 10K | CPMs spike, algorithm cannot optimize |
| Create separate campaigns per industry | Budget dilution, small audiences |
| Target specific job titles only (unless audience is large enough) | Misses ICP members with unexpected titles |
| Use age, gender, or language targeting | LinkedIn has limited data on these - unreliable |
| Mix expensive markets (US, UK) with cheap markets | US/UK eats all the budget |
| Leave Audience Expansion on by default | LinkedIn auto-enables it - always check |
| Mix lookalike audiences with job title targeting | Conflicting targeting logic |

---

## Audience Splitting for Scale

When initial campaigns are running well, scale by splitting audiences. Priority order:

### Splitting Priority

| Priority | Split Dimension | When to Split |
|---|---|---|
| 1 | **Intent/Content Stage** | First split - separate awareness from retargeting |
| 2 | **Persona** | When you have enough budget for 2+ persona campaigns |
| 3 | **Region** | When targeting multiple geographies |
| 4 | **Company Size** | When product use cases differ by segment |
| 5 | **Seniority** | Last - only after all above splits are covered |

### Region Splitting Rules

| Region | Recommendation |
|---|---|
| **US** | Always separate - most expensive market |
| **UK** | Separate if budget allows |
| **DACH** | Separate from English-speaking markets - different language/content needed |
| **UK + Canada + Australia** | Can group together if budget is tight (similar costs, same language) |
| **France, Germany** | English ads underperform - create localized content |
| **Nordics, Netherlands, Middle East** | English ads perform fine |

**Minimum audience per cold campaign:** 15,000 members. If splitting a region drops below this, combine with a similar region.

### Each Split Requires

Every time you split an audience into a new campaign, you need:
- Unique messaging matched to that segment
- Dedicated creatives
- Appropriate landing pages
- Separate budget allocation

Do not split just because you can. Split when you have the budget and creative capacity to serve each segment properly.

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).**