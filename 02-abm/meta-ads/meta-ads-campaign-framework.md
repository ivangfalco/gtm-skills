# Meta Ads Campaign Structure Framework

Campaign architecture, audience strategy, offer strategy by funnel stage, budget allocation, scaling roadmap, and naming conventions for B2B Meta Ads.

---

## Three-Phase Campaign Architecture

Meta campaigns for B2B follow a strict progression. Each phase has a specific purpose. Do not skip phases.

### Phase 1: Audience Validation (ABO - Ad Set Budget)

**Purpose:** Determine which audience sources produce quality leads before spending on creative testing.

**When to use:** Starting Meta for the first time, launching a new offer, entering a new market segment.

**Structure:**
```
Campaign: [Product] - Prospecting - ABO - Audience Validation
  Ad Set 1: 1% CRM Lookalike          [$X/day]
  Ad Set 2: Third-Party Data (Primer)  [$X/day]
  Ad Set 3: Interest + Job Titles      [$X/day]
  Ad Set 4: Broad Targeting            [$X/day]
    Same 3-4 ads in every ad set (isolate the audience variable)
```

**Critical settings:**
- Use Ad Set Budget (ABO), NOT Campaign Budget Optimization - guarantees each audience gets dedicated budget
- Same ads across all ad sets - you are testing audiences, not creative
- Equal budgets per ad set for fair comparison
- Run for 2-4 weeks minimum
- Turn off Advantage+ audience expansion - select your specific audience per ad set

**Validation criteria (check in CRM, not Ads Manager):**

| Criteria | What to Check | Why It Matters |
|---|---|---|
| **Job title match** | Do leads match your ICP titles? | Bad titles = wrong audience |
| **Company match** | Do companies match target firmographics? | Right person at wrong company is still wrong |
| **Lead-to-MQL rate** | What percentage of leads qualify? | Raw CPL means nothing without quality |
| **Cost per qualified lead** | Spend divided by MQLs, not raw leads | This is your real CPA |
| **Pipeline rate** | Are these leads becoming opportunities? | Ultimate validation of audience quality |

**After validation:**
- Kill ad sets producing low-quality leads (even if CPL is cheap)
- Take winning audience(s) to Phase 2
- Document what worked and what did not

**Simpler alternative (for smaller budgets):** Two ad sets only - open/broad targeting vs interest-based. After 2-4 weeks, compare which brings better results. Use the winner going forward.

### Phase 2: Creative Scaling (CBO - Campaign Budget Optimization)

**Purpose:** Scale winning audiences through creative concept testing.

**When to use:** After validating audience quality in Phase 1.

**Structure (Option A - by concept):**
```
Campaign: [Product] - Prospecting - CBO - [Winning Audience]
  Ad Set 1: UGC Concept                 [CBO distributes budget]
    3-4 UGC variations
  Ad Set 2: Before/After Concept
    3-4 Before/After variations
  Ad Set 3: Problem/Solution Concept
    3-4 Problem/Solution variations
```

**Structure (Option B - by batch):**
```
Campaign: [Product] - Prospecting - CBO - [Winning Audience]
  Ad Set 1: Creative Batch 1 (mix of concepts)
  Ad Set 2: Creative Batch 2 (iterations from Batch 1 winners)
  Ad Set 3: Creative Batch 3 (double down on winners)
```

**Critical settings:**
- Use Campaign Budget Optimization (CBO) - let Meta shift budget to winning creative concepts
- Target only the validated winning audience from Phase 1
- Give each batch/concept 7-10 days minimum before judging
- When a concept wins, create more variations of that concept
- When a concept dies, replace with a dramatically different concept

**Transition trigger to Phase 3:** 50+ conversions per week consistently with a proven offer and audience.

### Phase 3: Automated Scaling (Advantage+)

**Purpose:** Maximum scale with full automation.

**When to use:** Proven offer, proven audience, strong tracking (Pixel + CAPI), 50+ conversions per week.

**Structure:**
```
Campaign: [Product] - Advantage+ Leads
  Ad Set: Broad with audience suggestions
    5-10 proven creative assets + new test variations
    Advantage+ Creative enabled
```

**Settings:**
- Campaign objective: Leads
- Advantage+ Audience ON (provide custom audiences and lookalikes as suggestions - not hard limits)
- Campaign Budget Optimization (automatic)
- Work email validation + SMS verification on lead form
- 3-5+ creative variations minimum

**Important:** Most B2B SaaS with $30K+ ACV will not reach Phase 3 quickly. That is fine. Phase 2 (CBO) with validated audiences and strong creative is where most B2B companies will operate long-term.

---

## Full Account Architecture

For a B2B SaaS running full-funnel Meta:

```
Campaign 1: Remarketing (Start Here - Month 1)
  Ad Set: Website visitors (30/90/180 day)
  Ad Set: Video viewers (50%+)
  Ad Set: Cross-channel UTM retargeting
  Budget: $20-50/day (small audience)
  Objective: Leads or Conversions

Campaign 2: Prospecting - ABO (Testing - Month 2-3)
  Ad Set: 1% CRM Lookalike
  Ad Set: Third-party data audience
  Ad Set: Interest + Job Titles
  Budget: Equal per ad set
  Objective: Leads

Campaign 3: Prospecting - CBO or Advantage+ (Scaling - Month 3+)
  Ad Set: Winning audience from testing
  Multiple creative concepts
  Budget: Main prospecting budget here
  Objective: Leads or Conversions

Campaign 4: ABM (If Applicable - Month 4+)
  Ad Set: Tier A accounts
  Ad Set: Tier B accounts
  Budget: ABO (control per tier)
  Objective: Awareness or Video Views

Campaign 5: Acceleration (If Applicable - Month 4+)
  Ad Set: Open pipeline (high-value)
  Ad Set: Stalled deals
  Budget: ABO
  Objective: Awareness
```

---

## Audience Strategy

### The Data Hierarchy

Three tiers of audience sources in priority order. Always validate quality before scaling.

#### Tier 1: First-Party CRM Data (Start Here)

Your CRM is the highest-quality data source. Upload it into Meta and build lookalike audiences.

**How to build CRM lookalikes:**
1. Export your best customers - highest ACV, shortest sales cycle, best retention
2. Upload as a Custom Audience in Meta Ads Manager
3. Build a 1% lookalike audience from that seed list
4. Validate audience quality (see Phase 1 above)
5. Once quality is confirmed, scale to 2% lookalike

**Rules for CRM seed lists:**

| Rule | Why |
|---|---|
| Start with existing customers | They are your best signal - they already bought |
| Segment by quality | Win rate, industry, deal size, product line - feed the best data in |
| Use closed-won + late-stage pipeline | Larger seed, but do not dilute with early-stage leads |
| Include personal emails if available | Meta matches personal emails at much higher rates than business emails |

**Email matching caveat:** Meta does not match business email addresses well. Match rates on work emails are often under 5%. Upload whatever you have (business emails, personal emails, phone numbers), check the match rate, and proceed if viable. For better match rates, use enrichment tools (see Tier 2).

#### Tier 2: Third-Party Data Sources

When CRM data is insufficient (too small, too new, low match rates), use third-party data providers to build LinkedIn-like targeting on Meta.

| Provider | What It Does | Match Rate | Best For |
|---|---|---|---|
| **Primer** | Firmographic + technographic audience building, identity graph matching, multi-channel activation | 85%+ persona accuracy | Multi-channel ABM (Meta + LinkedIn + YouTube + Reddit) |
| **Metadata.io (MetaMatch)** | Firmographic/technographic audiences, 1.5B email identity graph, upload to Meta | ~40% | LinkedIn-like targeting on Meta |
| **ZoomInfo** | CRM data enrichment - appends personal emails, phones to CRM records | N/A (enrichment) | Enriching CRM data before uploading to Meta |
| **Clearbit (HubSpot Breeze)** | Real-time CRM enrichment, firmographic updates | N/A (enrichment) | HubSpot users, CRM-first enrichment |

**How these tools work:**
1. Define your audience using firmographic criteria (industry, company size, revenue, tech stack)
2. The tool matches those criteria against their identity graph (personal emails, phone numbers, social profiles)
3. The matched contacts are uploaded into Meta as a first-party Custom Audience
4. You can target the list directly (if large enough) or build a 1% lookalike from it

**Why this matters:** These tools give you LinkedIn-like targeting precision on a platform with lower costs. You can target "VP of Marketing at SaaS companies with 200-500 employees using Salesforce" - something Meta's native targeting cannot do.

#### Tier 3: Broad Targeting

Full broad targeting lets Meta's algorithm find your audience based on creative signals and user behavior rather than explicit targeting.

**Only use broad targeting if ALL of these are true:**
- You are NOT doing ABM (ABM needs explicit targeting)
- You have a large total addressable market (SMB or lower mid-market)
- Your creative is highly specific about who the ad is for
- You have already tested Tier 1 and Tier 2 sources

**How to make broad work:**
- Ad copy must explicitly call out who this is for and who it is not for
- Example: "For B2B marketing teams spending $50K+/month on ads" immediately filters non-ICP
- The creative does the targeting work - Meta's algorithm learns from who engages
- Monitor lead quality closely - broad drifts toward low-quality leads if creative is not specific enough

**When broad does NOT work:**
- Enterprise-only companies with small TAM (500 possible companies)
- Niche verticals where the ICP is too specific for algorithm learning
- When you have no creative volume to feed the algorithm

### Audience Validation Process

| Step | Action | Duration |
|---|---|---|
| 1 | Create ABO campaign with one ad set per audience source | Day 1 |
| 2 | Use the same ads across all ad sets | Day 1 |
| 3 | Set equal budgets per ad set | Day 1 |
| 4 | Run and collect data | 2-4 weeks |
| 5 | Audit leads in CRM by job title, company, and fit | Week 2-4 |
| 6 | Compare quality across ad sets | After 2-4 weeks |
| 7 | Kill low-quality ad sets, promote winners to CBO | After validation |

### Customer Intelligence (Before Touching Ads Manager)

Before building audiences, do this research:

**Interview existing customers:**
- Why they bought - what problem they were solving, what triggered the search
- What made them hesitate - address this in ad messaging
- Where they hang out online - validates whether Meta is the right channel

**Segment your best customers:**
- Highest ACV (paid the most)
- Shortest sales cycle (bought quickest)
- Best retention/LTV (stayed longest)

These three signals identify your top 5% of ideal buyers. Your targeting strategy starts with finding more of these people.

### The Top 5% Framework

Instead of targeting your entire TAM, start with the top 5% of in-market buyers - those with the shortest sales cycle, fewest objections, and most urgency. Land them first. Once you have converted or reached most of that 5% (typically after ~12 months of focused prospecting), expand to the next tier.

---

## Offer Strategy by Funnel Stage

Your ads will never outperform a bad offer. This is the number one lever for campaign success on Meta.

**Core rule:** You cannot sell a $30K+ contract from a cold Meta ad. You sell the click. The landing page sells the next step. The next step sells the meeting. The meeting sells the deal. Each step only needs to earn the NEXT step.

### Why Demo Requests Fail on Cold Meta Traffic

| Problem | Why It Happens |
|---|---|
| **Intent mismatch** | Meta = discovery mode. Google = "I'm ready to buy" mode. Cold prospects are not solution-shopping yet. |
| **Commitment too high** | A demo asks for 30-60 minutes with a stranger. For a $30K decision with procurement and 3 stakeholders - nobody impulse-books that. |
| **Sales cycle mismatch** | $30K+ ACV = 3-9 month sales cycle. You are asking for a step-10 action at step 1. |
| **Low volume for optimization** | Few cold prospects convert to demo, so Meta cannot optimize and CPA spirals. |

**Exception:** Demo requests CAN work for retargeting warm audiences, SMB/low-ACV ($5K-$15K), and very hot intent signals (pricing page visitors).

### Offer Types by Funnel Stage

#### Cold - Awareness/Education (Prospecting)

**Goal:** Capture contact info, build retargeting audience, demonstrate expertise.

| Offer Type | Example | Why It Works | Effort |
|---|---|---|---|
| **Industry benchmark report** | "2026 B2B SaaS Pipeline Benchmarks" | Proprietary data they cannot Google. Positions you as authority. | High (needs real data) |
| **ROI calculator** | "Calculate Your Pipeline Leakage Cost" | Interactive, immediately useful, directly tied to your value prop. | Medium |
| **Educational guide** | "The Enterprise CRM Migration Playbook" | Solves a problem they have right now. | Medium |
| **Webinar (live)** | "How [Company] Reduced Churn 43% in 90 Days" | Specific, time-bound, story-driven. Live creates urgency. | Medium |
| **Assessment tool** | "B2B Data Quality Maturity Assessment" | Self-serve diagnostic reveals their problem. Your product is the fix. | High |

**What does not work on cold:** Demo requests, free trials (only for PLG/low-ACV), generic "Download our whitepaper," "Contact us."

**Rules for cold offers:**
- Perceived value must dramatically exceed the cost (their email + 5 minutes)
- Must be unavailable elsewhere (cannot be Googled)
- Must relate to the problem your product solves
- Keep form to 4 fields max: first name, last name, email, one qualifier
- Lead forms outperform landing pages for cold traffic volume

#### Warm - Consideration (Remarketing)

**Goal:** Deepen engagement, build trust, move toward buying intent.

**Audience:** People who consumed Stage 1 content, visited your website, watched videos, or engaged with ads.

| Offer Type | Example | Why It Works |
|---|---|---|
| **Case study** | "How [Similar Company] Closed $2M Pipeline in 90 Days" | Specific proof with metrics. Prospects see themselves in the story. |
| **Product comparison guide** | "[Your Product] vs [Competitor] for Enterprise Teams" | Addresses the evaluation they are already doing privately. |
| **Interactive product tour** | "See How [Product] Works in 3 Minutes" | Low-commitment way to experience the product without sales pressure. |
| **Workshop/masterclass** | "Live Workshop: Building Your B2B Pipeline Engine" | Higher engagement than webinar. Positions as thought partner, not vendor. |
| **Customer video testimonial** | "[Name], VP Sales: 'We 3x'd pipeline in 6 months'" | Video social proof from someone who looks like your ICP. |

**Budget:** Remarketing is cheap (small audience) with high ROI. Even $20-50/day creates the "they're everywhere" perception.

#### Hot - Decision (High-Intent Retargeting + Pipeline)

**Goal:** Convert to qualified opportunity.

**Audience:** Pricing page visitors, multiple content consumers, webinar attendees, open pipeline.

| Offer Type | Example | Why It Works |
|---|---|---|
| **Custom assessment** | "Free Pipeline Audit - We'll Analyze Your Last 90 Days" | High-value, personalized. Natural bridge to sales conversation. |
| **Strategy session** | "30-Min Pipeline Strategy Session with Our Team" | Not "demo" - it is a value-exchange meeting. |
| **Demo (warm only)** | "See [Product] Solve [Their Specific Problem]" | Only push demos to prospects who have consumed content and shown intent. |
| **ROI proposal** | "Get a Custom ROI Analysis for [Their Company]" | Quantifies value, addresses CFO/procurement objections. |
| **Limited pilot** | "14-Day Pilot Program for Enterprise Teams" | Lower risk than full contract. Only for high-value accounts. |

### Offer Strategy by ACV Tier

| Segment | ACV | Cold Offer | Warm Offer | Hot Offer | Meta's Role |
|---|---|---|---|---|---|
| **SMB** | $5-15K | Free trial, quick guide | Product tour, case study | Demo, sign up | Can drive full funnel |
| **Mid-Market** | $15-50K | Benchmark report, calculator, webinar | Comparison guide, workshop | Strategy session, custom assessment | Education + retargeting |
| **Enterprise** | $50-250K+ | Industry report, executive briefing | Detailed case studies, product tours | Custom ROI analysis, pilot | Awareness + remarketing only |

**Key difference:** As ACV increases, Meta's role shifts from conversion channel to influence channel. For enterprise, Meta creates awareness and stays top-of-mind; the conversion happens through sales-led motions.

### The "No-Brainer" Offer Checklist

For an offer to convert cold B2B traffic on Meta, it must pass these tests:

| Test | Question | Strong Offer | Weak Offer |
|---|---|---|---|
| **Value asymmetry** | Would they pay for this? | Yes - proprietary data, custom analysis | No - generic information |
| **Unavailability** | Can they Google this for free? | No - proprietary or personalized | Yes - available everywhere |
| **Problem alignment** | Does it relate to what your product solves? | Directly tied to product value prop | Generic industry content |
| **Specificity** | Is it about a specific outcome? | "Fix pipeline leakage in 60 days" | "Improve your marketing" |
| **Immediate gratification** | Do they get value within 24 hours? | Instant access to calculator or report | Long PDF nobody reads |
| **Low friction** | How much do they need to give? | 4 fields max, mobile-optimized | 10-field form, desktop-only |

### Full Offer Progression for $30K+ ACV

```
COLD (Meta Prospecting)
  Offer: Industry benchmark report / ROI calculator
  Form: 4 fields (name, email, company size)
  Goal: Email capture + retargeting pixel

  WARM (Meta Remarketing + Email Nurture)
    Offer: Case studies, comparison guides, product tours
    Touchpoints: 4-7 emails over 2-4 weeks
    Goal: Build trust, demonstrate expertise

    HOT (Meta Retargeting + Sales Outreach)
      Offer: Custom assessment / strategy session
      Signal: Pricing page visit, 3+ content pieces, webinar attended
      Goal: Qualified meeting

      PIPELINE (Meta Acceleration + Sales)
        Offer: Custom ROI analysis, pilot program
        Ads: Case studies, social proof, competitive comparison
        Goal: Close deal, shorten cycle
```

**Timeline reality for $30K+ ACV:**
- Cold to first meeting: 30-60 days
- First meeting to proposal: 30-60 days
- Proposal to close: 30-90 days
- Total: 3-9 months (Meta influences the entire journey but rarely causes the purchase directly)

---

## Budget Allocation and Scaling Roadmap

### The 12-Month Roadmap

| Phase | Timeline | Focus | Budget Split |
|---|---|---|---|
| **1. Remarketing** | Month 1 | Prove Meta works for your brand. Cross-channel retargeting. | $500-2,000/month |
| **2. Audience Validation** | Month 2-3 | ABO testing of audience sources. Find which produce quality leads. | $2,000-5,000/month |
| **3. Creative Scaling** | Month 3-6 | CBO with winning audiences. Test creative concepts at volume. | $5,000-15,000/month |
| **4. Scaling + ABM** | Month 4-12 | Advantage+ for broad. Manual for ABM. Acceleration campaigns. | $10,000-30,000/month |
| **5. Expansion** | Month 12+ | Expand beyond top 5% of in-market buyers. Story-based ads for colder audiences. | $20,000+/month |

### Why Start with Remarketing

- Lowest risk, highest ROI
- People already know you - just stay top of mind
- Cross-channel remarketing amplifies existing LinkedIn/Google investment
- Small budget required (audience is small)
- Proves Meta works for your brand before committing prospecting budget
- Creates the "they're everywhere" perception with minimal spend

### Budget Formula

```
Minimum Daily Budget = (Target CPA x 50 conversions) / 7 days
```

| Target CPA | Minimum Daily Budget | Monthly Budget |
|---|---|---|
| $20 | $143/day | $4,300/month |
| $50 | $357/day | $10,700/month |
| $100 | $714/day | $21,400/month |

### Minimum Budget Requirements

| Campaign Type | Minimum Monthly | Why |
|---|---|---|
| **Remarketing** | $500-1,500 | Small audience, low CPMs |
| **Prospecting (ABO testing)** | $2,000-5,000 | Need equal budgets per ad set for fair comparison |
| **Prospecting (CBO scaling)** | $5,000-15,000 | Algorithm needs budget to optimize creative |
| **Advantage+** | $5,000+ | Requires volume to exit learning phase |
| **ABM** | $3,000+ | Minimum to reach target accounts with meaningful frequency |

### Budget Reallocation Signals

| Signal | Action |
|---|---|
| Ad set hitting target CPA with strong quality | Increase budget 15-20% per week |
| Ad set at 2x+ target CPA after 30 days | Decrease budget, investigate root cause |
| Audience exhausted (frequency above 4.0) | Refresh creative or expand audience |
| One audience producing 3x better quality | Shift budget from weak audiences to strong |
| Learning phase not exiting after 2 weeks | Consolidate ad sets, increase budget, or optimize for upper-funnel event |

### Cross-Channel Budget Split (When Running Multiple Platforms)

| Total Budget | Recommended Split | Notes |
|---|---|---|
| **$5K-10K/month** | 100% one channel | Pick highest-impact channel, do not spread thin |
| **$10K-25K/month** | 60-70% primary + 30-40% secondary | Example: 70% LinkedIn + 30% Meta remarketing |
| **$25K-50K/month** | 3 channels | Example: 40% LinkedIn + 35% Google + 25% Meta |
| **$50K+/month** | Full mix + testing | All channels active + experimentation budget |

---

## Optimization Events

| Event | When to Use | Min Volume Needed |
|---|---|---|
| **Lead** | Lead form submissions, demo requests | 50/week per ad set |
| **Landing Page Views** | Low conversion volume, need more events for learning | 50/week per ad set |
| **CompleteRegistration** | Webinar signups, trial signups | 50/week per ad set |
| **Custom: MQL** | Sending qualified lead events via CAPI | 50/week per ad set |
| **Custom: Opportunity** | Sending pipeline events via CAPI (advanced) | Lower volume OK if pipeline-focused |

**The 50-event threshold:** Meta needs 50 optimization events per ad set per week to exit learning phase. If you cannot hit 50 demos per week, optimize for a higher-volume event (lead form submissions, landing page views) and retarget converters toward demos.

---

## Cross-Channel Remarketing

Retarget traffic from validated channels (LinkedIn, Google) on Meta at lower cost:

1. Run ads on LinkedIn - traffic lands on website with LinkedIn UTMs
2. In Meta: Audiences - Create - Custom Audience - Website - URL contains `utm_source=linkedin`
3. Retarget your LinkedIn-validated audience on Meta at 50-70% lower CPM
4. Same works for Google traffic: `utm_source=google&utm_medium=cpc`

**Why it works:** LinkedIn's precision targeting validates who the right people are. Meta's cheap retargeting keeps you in front of them. Result: LinkedIn-quality audience at Meta-level costs.

**Requires:** Sufficient traffic volume from those channels to build a usable audience size.

---

## Campaign Naming Conventions

### Standard Format

```
[Product] - [Campaign Type] - [Budget Type] - [Audience/Detail]
```

### Components

| Element | Options | Examples |
|---|---|---|
| **Product** | Product or brand name | LeadRouter, DataSync, AcmeCRM |
| **Campaign Type** | Prospecting, Remarketing, ABM, Acceleration | Prospecting |
| **Budget Type** | ABO, CBO, ASC (Advantage+ Shopping/Leads) | CBO |
| **Audience/Detail** | Audience source or specific detail | 1% CRM Lookalike, Website 90d, Tier A Accounts |

### Campaign Name Examples

```
LeadRouter - Prospecting - ABO - Audience Validation
LeadRouter - Prospecting - CBO - 1% CRM Lookalike
LeadRouter - Remarketing - CBO - Website 90d
LeadRouter - Remarketing - CBO - Cross-Channel UTM
LeadRouter - ABM - ABO - Tier A Accounts
LeadRouter - ABM - ABO - Tier B Accounts
LeadRouter - Acceleration - ABO - Open Pipeline
LeadRouter - Advantage+ Leads - Broad
```

### Ad Set Naming

```
[Audience Source] - [Targeting Detail]
```

**Examples:**
- `CRM Lookalike 1% - Closed Won Customers`
- `Primer - VP Marketing SaaS 200-500`
- `Interest - B2B Marketing + SaaS`
- `Broad - US 25-65`
- `Website Visitors - 90 Day`
- `Video Viewers - 50%+ Completion`

### Ad Naming

```
[Format] - [Concept] - [Offer] - [Date]
```

**Examples:**
- `Static - Problem/Solution - Benchmark Report - Jan2026`
- `Video - UGC Testimonial - ROI Calculator - Feb2026`
- `Carousel - Before/After - Webinar Invite - Mar2026`

---

## What to Avoid

| Mistake | Why It Hurts |
|---|---|
| **Mixing ABM and broad prospecting in one campaign** | Completely different targeting logic - separate them |
| **Running CBO during audience validation** | CBO shifts budget to cheapest audience, not best quality |
| **Changing campaign settings during learning phase** | Any significant edit resets the 50-conversion counter |
| **More than 5-6 ad sets per campaign** | Dilutes signal, slows learning |
| **Optimizing for Link Clicks** | Vanity metric - optimize for leads or conversions |
| **Launching campaigns on Friday** | Weekend has lower B2B engagement, wastes initial learning budget |
| **No conversion tracking before launch** | Flying blind - install Meta Pixel + CAPI first |
| **Judging campaigns before 2 weeks of data** | Algorithm needs time to learn - do not panic-pause |

---

## Exclusion Strategy

Always exclude from prospecting campaigns:

- **Closed-won customers** (waste of prospecting budget)
- **Recent converters** (7-30 day suppression after form fill)
- **Employees and internal traffic** (skews data)
- **Disqualified accounts from CRM** (already vetted and rejected)

This keeps attribution clean, prevents budget waste, and focuses spend on accounts that matter.

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
