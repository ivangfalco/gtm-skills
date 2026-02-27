# LinkedIn Ads Campaign Framework - Structure, Execution, and Scaling

The operational bible for LinkedIn Ads campaigns - from account architecture through launch, scaling, and performance benchmarks. Covers campaign structure, bidding mechanics, ad format specs, copy frameworks, landing pages, launch procedures, scaling strategy, and benchmark data.

For audience strategy and targeting, see [linkedin-ads-audience-guide.md](./linkedin-ads-audience-guide.md)
For creative angles and messaging, see [linkedin-ads-creative-strategy.md](./linkedin-ads-creative-strategy.md)
For weekly optimization workflows, see [linkedin-ads-optimization-guide.md](./linkedin-ads-optimization-guide.md)
For ABM-specific campaign structure, see [linkedin-ads-abm-guide.md](./linkedin-ads-abm-guide.md)

---

## 1. Campaign Structure

### Account Architecture

Organize campaigns into groups from the start. Even with only 2-3 campaigns, the group structure creates clean reporting and prevents scaling headaches later.

| Level | What It Contains | When to Create |
|-------|-----------------|----------------|
| Ad Account | All campaign groups, billing, Insight Tag | One per business entity (or region at scale) |
| Campaign Group | Related campaigns sharing a funnel stage or theme | When you have 2+ campaigns with a shared purpose |
| Campaign | One audience + one objective + one bid strategy | Each unique audience/objective combination |
| Ads | 4+ creatives per campaign minimum | Always - fewer than 4 limits algorithm optimization |

### Campaign Group Model

Start with Product Value + Remarketing. Add additional groups as budget grows.

| Group | Purpose | Budget Priority | Content Type |
|-------|---------|----------------|-------------|
| Product Value | Showcase what your product does | 1st (start here) | Demos, features, use cases |
| Remarketing | Re-engage people who already interacted | 2nd | Demo offers, testimonials |
| Content | Drive traffic with valuable knowledge | 3rd | Reports, guides, educational |
| Social Proof | Build trust through validation | 4th | Customer stories, reviews, awards |
| Thought Leadership | Build brand affinity through expertise | 5th (add last) | Executive insights, industry analysis |

### Campaign Group Naming Convention

| Level | Format | Example |
|-------|--------|---------|
| Basic | Persona + Intent | Marketing - Awareness |
| Intermediate | Persona + Intent + Content Type | Marketing - Awareness - Product Value |
| Advanced | Persona + Intent + Region | Marketing - Awareness - EMEA - Content |
| Enterprise | Persona + Intent + Region + Size | Marketing - Awareness - Product Value - Enterprise |

### Critical Structural Rules

| Rule | Detail |
|------|--------|
| Never mix prospecting and retargeting in the same group | Different funnel stages need separate budget control |
| One campaign objective per group | Do not mix reach and traffic objectives in the same group |
| Separate enterprise and SMB campaigns | Algorithm favors cheaper audiences - enterprise campaigns get starved if mixed |
| Do not mix ad formats in campaign group budgets | Static + video in one group sends 80%+ budget to video |
| LinkedIn does not allow moving campaigns between groups | You must duplicate campaigns to reorganize (losing historical data) |
| New audience segments get their own campaign | Never add new targeting to an existing campaign - contaminates performance data |

### Ad Naming Convention

Use consistent format for clean reporting and easy filtering:

```
[Persona]_[Format][#]_[CopyVariant]_{Date}
```

| Component | Example Values |
|-----------|---------------|
| Persona | SalesDirector, VPEngineering, CTO, CMO |
| Format | Image, Video, Carousel, Document, TLA |
| Number | 1, 2, 3 (creative variant number) |
| CopyVariant | TextA, TextB, TextC (copy version) |
| Date | 2026-02 (launch month) |

**Examples:**
- `VPEngineering_Image1_TextA_2026-02`
- `CMO_TLA2_TextB_2026-03`
- `SalesDirector_Video1_TextA_2026-02`

### Budget Allocation by Monthly Spend

| Monthly Total Budget | Recommended Campaign Split |
|---------------------|---------------------------|
| $500 - $1,000 | 1-2 campaigns. Skip TOF, focus on highest-intent audience. |
| $1,000 - $2,500 | 2-3 campaigns. Light TOF + focused BOF. |
| $2,500 - $5,000 | Full 3-layer funnel. 3-5 campaigns. |
| $5,000 - $10,000 | Full funnel + creative testing. 5-7 campaigns. |
| $10,000 - $20,000 | Full funnel + niche campaigns + ABM. 7-10+ campaigns. |
| $20,000+ | Full funnel + multi-region + format testing. 10+ campaigns. |

---

## 2. Bidding Strategy

### Bidding Options Overview

LinkedIn offers four bidding strategies. Each has a specific use case - choosing the wrong one wastes money.

| Bid Type | How It Works | Best For | Risk |
|----------|-------------|----------|------|
| Maximum Delivery (Automated) | LinkedIn optimizes to spend full budget at lowest cost | New campaigns, learning phase, small audiences | Low control, can overspend on poor clicks |
| Cost Cap | Sets a target cost per result - algorithm stays near that target | Lead gen forms, conversion campaigns with known CPL targets | May underspend if cap is too low |
| Manual CPC | You set the max CPC - LinkedIn bids up to that amount | Mature campaigns with CPC history, cost control | Requires monitoring, can underdeliver if bid is too low |
| Manual CPM | You set the max cost per 1,000 impressions | Brand awareness, video views, reach campaigns | No click optimization - pay for impressions regardless |

### Phase 1: Automated Bidding (Week 1)

Every new campaign starts with Maximum Delivery. This is non-negotiable.

| Rule | Detail |
|------|--------|
| Duration | Run automated for the full first week (7 days minimum) |
| Budget | Set daily budget at the level you plan to maintain long-term |
| Do not adjust | No bid changes, no audience tweaks, no creative swaps during this phase |
| Monitor only | Track CPCs, CTR, and spend pacing - do not intervene |
| Record baseline | Note the average CPC at end of week 1 - this is your transition number |

**Health signals during Phase 1:**
- **Healthy:** Spending 80-100% of daily budget with consistent CPCs
- **Warning:** Spending less than 50% of budget - audience may be too small or targeting too narrow
- **Red flag:** CPCs wildly inconsistent day to day - audience quality may be mixed

### Phase 2: Manual CPC Transition (Week 2+)

After week 1, switch to Manual CPC. This is where significant cost savings happen.

**The formula:**
```
Manual CPC Bid = Average CPC from Phase 1 x 0.80
```

Set your manual bid at 20% below your average CPC from the automated phase. This works in the vast majority of cases.

### Bid Adjustment Rules

| Scenario | Action | Adjustment |
|----------|--------|------------|
| Spending full budget, CPCs stable | Hold | No change needed |
| Spending full budget, CPCs rising | Lower bid by 5-10% | Prevents cost creep |
| Underspending (below 70% of budget) | Raise bid by 10-15% | Increase competitiveness |
| Severely underspending (below 40%) | Raise bid by 20-25% or return to automated | Audience may need higher bids |
| CTR declining while spend is stable | Refresh creative, not bid | Bidding is not the problem |
| CPCs consistently below bid | Lower bid to match actual CPCs + 10% buffer | You are overbidding |

### When NOT to Switch to Manual

| Scenario | Why | Keep |
|----------|-----|------|
| Small retargeting audiences (under 10K) | Manual bidding causes severe underdelivery | Automated permanently |
| ABM audiences (under 5K) | Too small for manual bid constraints | Automated permanently |
| Video views objective | Video views are typically cheap - manual adds little benefit | Automated or Manual CPM |
| New campaign objective change | Algorithm needs a fresh learning phase | Automated for week 1 again |

### Bid Strategy by Campaign Objective

| Objective | Phase 1 | Phase 2 | Notes |
|-----------|---------|---------|-------|
| Engagement (TOF) | Maximum Delivery | Manual CPC at 80% of avg | Optimize for lowest cost per engagement |
| Video Views (TOF) | Maximum Delivery | Stay automated or Manual CPM | Manual adds little benefit for video |
| Website Visits (MOF/BOF) | Maximum Delivery | Manual CPC at 80% of avg | Monitor CPC closely - can get expensive |
| Lead Gen Forms (BOF) | Cost Cap at target CPL | Manual CPC once you have data | Set cap at realistic CPL based on historical data |
| Conversions (BOF) | Maximum Delivery | Manual CPC for large audiences, keep automated for small | Conversion optimization needs volume to learn |

### Budget Pacing

LinkedIn's ad day starts at UTC midnight (8:00 PM Eastern). This affects budget distribution.

| Time Zone | LinkedIn Ad Day Starts |
|-----------|----------------------|
| UTC | 12:00 AM (midnight) |
| Eastern (ET) | 8:00 PM previous day |
| Pacific (PT) | 5:00 PM previous day |
| Central European (CET) | 1:00 AM |

**Recommended ad schedule:** Run ads 5:00 AM to 2:00 PM Eastern (peak professional engagement hours). Concentrating spend during peak hours delivers more efficient results than spreading budget across 24 hours.

### Budget Change Rules

| Change Type | Maximum Adjustment | Why |
|-------------|-------------------|-----|
| Daily budget increase | +20% at a time | Larger jumps destabilize the algorithm |
| Daily budget decrease | -20% at a time | Sharp cuts can crash delivery |
| Frequency of changes | Once per week maximum | Algorithm needs stability to optimize |
| Emergency pause | Acceptable anytime | Pausing does not hurt future performance |

### Campaign Group Budget Optimization

Setting one budget at the campaign group level instead of individual campaigns lets the algorithm allocate across campaigns automatically.

| Metric | Group Budget | Individual Campaign Budget |
|--------|-------------|---------------------------|
| Cost per reach | Approximately 10% cheaper | Baseline |
| Audience penetration | Nearly 2x higher (1 month group = 2 months individual) | Baseline |
| In-platform metrics | Marginally better (around 1%) | Baseline |

**Group budget rules:**
- One objective per group
- Do not mix audience tiers (enterprise starved if mixed with SMB)
- Do not mix formats (80%+ budget goes to video if mixed with static)
- Be granular - separate by audience tier, format type, and objective

### Ad Rotation Strategy

| Phase | Duration | Rotation Type | Purpose |
|-------|----------|--------------|---------|
| Launch | Days 1-7 | Even rotation (equal budget per ad) | Prevents premature winner selection |
| Optimization | Day 8+ | Auto rotation (algorithm favors winners) | Let LinkedIn push budget to top performers |
| Refresh | Every 3 months | Swap underperformers | Prevent creative fatigue |

### Budget-Constrained Rotation Trick

If budget is tight and you need to run 6 campaigns but can only afford $30/day each:

- **Set A (3 campaigns):** Run Monday, Wednesday, Friday
- **Set B (3 campaigns):** Run Tuesday, Thursday, Saturday

This gives each campaign a $30/day budget on active days while halving daily spend. Campaigns still build reach over time at a 3-day-per-week pace.

### Bidding Quick Reference - Decision Tree

```
New campaign?
  YES --> Maximum Delivery (automated) for week 1
  NO --> Has the campaign run for 7+ days?
    NO --> Keep automated, wait for data
    YES --> Is the audience under 10K?
      YES --> Keep automated permanently
      NO --> Switch to Manual CPC at 80% of average CPC
        Is it a lead gen campaign with a CPL target?
          YES --> Consider Cost Cap at target CPL
          NO --> Manual CPC is correct
```

### Key Bidding Numbers

| Number | What It Means |
|--------|--------------|
| 0.80 | Multiplier for Phase 1 to Phase 2 CPC transition (20% below average) |
| 20% | Maximum budget change in a single adjustment |
| 10K | Minimum audience size for manual bidding |
| 4 | Minimum active ads per campaign |
| 3 | Maximum frequency per week per person before rotation |
| 35% | Target audience penetration for healthy campaigns |
| 7 days | Minimum automated phase before switching to manual |
| 10 results/week | Minimum data threshold for meaningful optimization |

---

## 3. Ad Formats

### Format Performance Comparison

| Format | Auction Competition | CTR Range | CPC Range | Best Funnel Stage | When to Use |
|--------|-------------------|-----------|-----------|-------------------|-------------|
| Single Image | Highest | 0.35-0.50% | $8-$22 | All stages | Default workhorse, versatile |
| Thought Leader Ads | Lower | 1.7x higher than standard | $4-$8 | TOF + BOF | Priority format - add first |
| Video (10-30s) | Moderate | 0.20-0.35% | $6-$15 | TOF | Awareness, retargeting pool building |
| Document Ads | Lower | 0.40-0.60% | $5-$12 | MOF | Education, nurture, less auction competition |
| Carousel | Moderate | ~0.30-0.45% | $7-$18 | MOF/BOF | Multi-point storytelling, feature showcases |
| Conversation Ads | Different auction (per-send) | 1-5% click rate | $8-$25 | MOF/BOF | Interactive engagement, events, ABM |
| Text Ads | Lowest | 0.02-0.05% | $3-$8 | Always-on | Ultra-cheap brand reinforcement |
| Spotlight Ads | Low | Low CTR | $4-$8 CPM | MOF | ~74% cheaper CPM than single image |

**Key insight:** Different formats compete in different auctions. Adding document ads targeting the same audience as your single image ads will have less auction competition, meaning cheaper cost per reach on the same audience.

### Document Ads

**Format specs:**

| Spec | Detail |
|------|--------|
| Slide dimensions | 1080 x 1080px (square) or 1080 x 1350px (portrait 4:5) |
| Recommended slide count | 5-7 slides for mid-funnel content |
| Maximum slide count | 10 slides (LinkedIn limit) |
| File format | PDF upload (each page becomes one slide) |
| File size limit | 100 MB maximum |
| Gating options | Gated (Lead Gen Form) or Ungated (free to swipe) |

**The 7-Slide Formula:**

| Slide | Role | Content |
|-------|------|---------|
| 1 | Hook | Strong headline + subtitle - this is your ad |
| 2-3 | Pain / Cost | What the audience is dealing with (different framing per segment) |
| 4 | Principle / Shift | The "aha" moment - a reframe that changes how they see the problem |
| 5 | Solution (Generic) | What any capable system needs (generic requirements) |
| 6 | Solution (Specific) | What your product uniquely delivers (unique differentiators) |
| 7 | CTA | Demo booking or next step - clean, minimal, brand-consistent |

**Critical rule:** Slides 5 and 6 must not be redundant. Slide 5 describes what any solution needs. Slide 6 describes what THIS product uniquely does. If both say the same thing with different words, merge or differentiate.

**Content types that work:**

| Content Type | Slide Count | Best For | Gated or Ungated |
|-------------|-------------|----------|-------------------|
| Industry reports | 7-10 | TOF awareness, thought leadership | Gated |
| How-to guides | 5-7 | MOF education, building trust | Ungated |
| Checklists | 5-6 | MOF/BOF practical value | Either |
| Case studies | 5-7 | BOF social proof, conversion | Ungated |
| Framework breakdowns | 5-7 | MOF positioning as expert | Ungated |
| Comparison guides | 5-7 | MOF/BOF differentiation | Gated or ungated |

**Design rules:**
- One lead-in sentence + one bullet list per slide (ideal density)
- Give key statistics a standalone visual break slide (big number, accent color, large type)
- Every slide needs a design note specifying hierarchy, colors, elements
- Provide two options for product slides: real UI screenshot or designed mockup
- Use flow diagrams over text descriptions for processes
- Post body: tease content, do not summarize (2-4 lines, create reason to swipe)

### Conversation Ads

**Format specs:**

| Spec | Detail |
|------|--------|
| Subject line | Max 60 characters - the ONLY thing prospects see before opening |
| Message body | Up to 8,000 characters per message |
| CTA buttons | Up to 5 total (1 mandatory "Not Interested" = 4 custom CTAs max) |
| Branching | Follow-up messages based on which CTA is clicked |
| Companion banner | 300 x 250px (desktop only), JPG/PNG, max 2 MB |
| Lead Gen Form | One per conversation (can be attached to any CTA) |
| Sender | Must be a real LinkedIn member (employee or partner) |

**Basic decision tree structure:**

```
Opening Message
  +-- CTA 1: "Yes, show me" --> Lead Gen Form or Scheduling Link
  +-- CTA 2: "Tell me more first" --> Second Message (USPs + social proof)
  |     +-- CTA 2a: "Ok, I'm in" --> Lead Gen Form
  |     +-- CTA 2b: "Send me a resource" --> Content download
  +-- CTA 3: "Not right now" --> Soft close + resource offer
  +-- "Not Interested" (mandatory) --> Conversation ends
```

**Decision tree rules:**
- Maximum 3 levels deep (more feels like a maze)
- Every branch must end somewhere useful (no dead ends)
- Put the primary action first (position 1)
- Include a soft exit ("Not right now" with a resource converts better than binary yes/no)
- Use action language: "Yes, let's do it" outperforms "Book a Demo"

**The Walkthrough Format (high-performing structure):**
1. Open with the pain (1-2 lines stating the specific problem)
2. Name the product as the solution (1 line)
3. Frame the demo as learning: "In a 20-minute walkthrough, I can show you:"
4. 3 specific bullets (what they will see - be concrete)
5. Personalized close: "Want to see if it's relevant for %COMPANYNAME%?"
6. Casual CTAs: "Yes, let's do it" / "Tell me more first" / "Not interested"

**Sender selection:**

| Sender Type | Effectiveness | When to Use |
|-------------|--------------|-------------|
| Founder / CEO | Highest trust and open rates | ABM campaigns, high-value accounts |
| VP / Director | High credibility | Industry-specific campaigns |
| Subject matter expert | High relevance | Technical audiences |
| SDR / junior rep | Low trust | Avoid unless prior interaction exists |

**Frequency rules:**
- Each member receives max one conversation ad per 30 days (platform-enforced)
- Use 2-3 senders to increase total send volume
- Minimum 1,000 members in target audience (LinkedIn requirement)

**When to use conversation ads:**
- ABM campaigns targeting named accounts
- Complex B2B buying journeys with multiple stakeholder paths
- Qualification before demo (branch logic separates ready-to-buy from researching)
- Event promotion with multiple sessions
- Retargeting warm audiences who engaged with content

**When NOT to use:**
- Single clear goal with one action (use Message Ads)
- Cold audiences with zero brand awareness (warm them up first)
- Budget under $2,000/month for this format (not enough data)

### Video Ads

| Spec | Recommendation |
|------|---------------|
| Length | 10-30 seconds for TOF, 1-2 minutes for MOF |
| Orientation | Horizontal (16:9) for highest view and completion rates |
| Hook | Must capture attention in first 3 seconds |
| Subtitles | Required - most users scroll with sound off |
| CTA | Clear end card with specific action (last 3-5 seconds) |

**Orientation performance:**
- Horizontal (16:9): Highest view rates and completion rates
- Vertical (9:16): Sub-3% completion rates - significantly worse on LinkedIn
- Square (1:1): Middle ground, works for mobile

### Single Image Ads

| Element | Spec |
|---------|------|
| Primary text | 60-120 characters ideal, 150 max before truncation |
| Headline (below image) | 70 characters max, CTA-focused |
| Description | 100 characters max |
| Image text | Less than 20% of image area (LinkedIn penalizes text-heavy images) |
| CTA button | Must match ad message and landing page |

### Text and Spotlight Ads

| Element | Text Ads | Spotlight Ads |
|---------|----------|---------------|
| Headline | 25 characters | 50 characters |
| Description | 75 characters | 70 characters |
| Image | 100 x 100px thumbnail | Company logo + member profile |
| CPM | $2-$6 (cheapest) | $4-$8 (~74% cheaper than single image) |
| Best use | Always-on brand presence | Always-on brand reinforcement |
| CTR expectation | 0.02-0.05% (low is normal) | Low CTR is normal |

### Format Scaling Priority

Add formats in this order when scaling:

| Priority | Format | Expected Impact |
|----------|--------|-----------------|
| 1 | Thought Leader Ads | 1.7x CTR improvement, lowest CPC |
| 2 | Video (10-30s) | Builds retargeting pools, strong awareness |
| 3 | Document Ads | Less auction competition, strong for nurture |
| 4 | Carousel | Multi-point storytelling for MOF/BOF |
| 5 | Conversation Ads | Interactive format for specific CTAs and events |
| 6 | Text + Spotlight Ads | Ultra-low-cost brand reinforcement layer |

---

## 4. Copy Framework

### The 5-Layer Copy Audit System

Run all 5 layers in order before any ad goes live. Each catches a different category of problems.

| Layer | Primary Question | How to Check |
|-------|-----------------|--------------|
| 1. Factual Accuracy | Can every claim be verified? | Trace each claim to verified source material |
| 2. Tone of Voice | Does it sound like the brand? | Check "never do" list first, then vocabulary and structure |
| 3. Structure and Relevance | Does every element earn its place? | Check each section for distinct purpose |
| 4. Design and Text Density | Would the audience actually read this? | Visual scan for walls of text, check brand palette |
| 5. Audience Fit | Does it speak their language? | Check pain points, terminology, framing against audience profile |

### Layer 1: Factual Accuracy - Red Flags

| Red Flag | Example | Risk |
|----------|---------|------|
| Absolute claims | "Required," "mandatory," "the only way" | May be legally or factually incorrect |
| Unattributed statistics | "73% of teams..." with no source | Audience questions credibility |
| Technical framing contradicting source | Calling something "mandatory" when source says "recommended" | Expert audiences catch this instantly |
| Product capabilities not confirmed | Claiming a feature that does not exist or is in beta | Destroys trust when discovered |
| Claims about competitors | "Most tools can't do this" | Often inaccurate and unprovable |

### Layer 2: Tone of Voice - Common Violations

| Violation | Example | Fix |
|-----------|---------|-----|
| Accusatory "your" when brand uses third-person | "Your process is broken" | "Most teams manage this across 5+ tools" |
| Informal slang for a measured brand | "Fire drill," "chaos" | Use professional, measured language |
| Marketing pivots for educational brand | "It doesn't have to be this way" | Maintain educational framing |
| Superlatives for a brand that uses qualifiers | "The biggest," "the best" | "Significant," "leading," "among the first" |

### Layer 3: Structure - All Format Checks

| Check | Question | Action if Failing |
|-------|----------|-------------------|
| Hook specificity | Is the hook specific enough to name the real problem? | Replace generic hooks with specific ones |
| CTA funnel match | Does the CTA match the funnel stage? | MOF = "See how it works." BOF = "Book a demo." |
| Creative alignment | Is the post body aligned with the creative? | They must feel like the same piece of content |
| Single clear message | Does the ad try to say too many things? | One message per ad. 3 things = 3 ads. |
| Value before ask | Does the ad provide value before requesting action? | Lead with insight, proof, or empathy before CTA |

### Layer 5: Audience Fit Checks

| Check | Question | Action if Failing |
|-------|----------|-------------------|
| Language match | Does copy use terms the audience actually uses? | Replace marketing jargon with audience vocabulary |
| Pain prominence | Is the primary pain point given appropriate prominence? | Make primary pain central, not one bullet among many |
| Role-level framing | Does framing match seniority? | C-suite: outcomes and risk. Managers: efficiency. ICs: daily workflows. |
| Variant differentiation | Is this version different from other audience variants? | Each version must speak to specific concerns |

### Audit Scoring

| Level | Definition | Action Required |
|-------|-----------|-----------------|
| Critical | Factually wrong, legally risky, or fundamentally misaligned | Must fix before launch - no exceptions |
| Significant | Tone mismatch, structural weakness, or audience misfit | Should fix before launch - will hurt performance |
| Minor | Small optimization opportunities, slight wording improvements | Can fix in next iteration - not blocking |

### Copy Formulas That Work

**Formula 1: Pain - Agitate - Solve (PAS)** - Best for single image ads, TOF awareness
```
[Specific pain the audience faces]
[Why this pain gets worse over time / what it costs]
[How the product solves it + specific result]
[CTA]
```

**Formula 2: Result - Method - Invitation** - Best for BOF retargeting, case study ads
```
[Specific result achieved by a customer or segment]
[Brief explanation of how / what changed]
[Invitation to see if it applies to them]
[CTA]
```

**Formula 3: Question - Data - Bridge** - Best for MOF education, thought leadership
```
[Provocative question the audience is asking themselves]
[Data point or stat that reframes the answer]
[Bridge to how the product connects]
[CTA]
```

**Formula 4: Before - After - Bridge (BAB)** - Best for document ads, video scripts
```
[What life looks like before the product (specific pain)]
[What life looks like after (specific outcome)]
[How to get from before to after (the product)]
[CTA]
```

**Formula 5: Social Proof Lead** - Best for BOF conversion, retargeting warm audiences
```
[Specific customer result with numbers]
[What they were dealing with before]
[What changed when they adopted the solution]
[CTA: "See how they did it" or "Get similar results"]
```

### Copy Rules by Format

| Format | Primary Text | Headline | Key Constraint |
|--------|-------------|----------|----------------|
| Single Image | 60-120 chars ideal, 150 max | 70 chars max, CTA-focused | Less than 20% text in image |
| Document Ads | Post body 2-4 lines, tease not summarize | Slide 1 hook + subtitle | One purpose per slide, minimal text |
| Video | 2-3 lines post body | First 3 seconds = hook | Subtitles required |
| Conversation | Subject 2-4 words, 3-5 short lines per message | N/A | Write like a text, not a landing page |
| Text Ads | N/A | 25 chars max | Description 75 chars max |

### The 10 Most Common Copy Problems

| Problem | Fix |
|---------|-----|
| Generic hook | Research the specific frustration, name it directly |
| Feature dump in body | One feature per ad - save the rest for landing page |
| No clear CTA | Every ad needs one explicit, unmissable CTA |
| CTA mismatch with funnel stage | TOF = Learn, MOF = See How, BOF = Book |
| Buzzword overload | Replace every buzzword with a concrete outcome or number |
| Weak value proposition | Formula: "[Feature] so you can [outcome] without [pain]" |
| Missing social proof | Add a specific metric, customer quote, or recognizable logo |
| Too many messages in one ad | One audience, one message, one CTA per ad |
| Passive voice | "Teams reduce churn by 43%" not "Churn is reduced by 43%" |
| No urgency or reason to act now | Add time-based element, competitive pressure, or cost of delay |

### A/B Testing Copy

**Priority order:**

| Priority | Element | Test Approach |
|----------|---------|---------------|
| 1 | Hook / headline | 2-3 variations with the same body |
| 2 | CTA | Same ad, different CTA copy |
| 3 | Value proposition angle | Same structure, different benefit emphasized |
| 4 | Social proof type | Stat vs customer quote vs logo bar |
| 5 | Copy length | Short (2-3 lines) vs medium (4-6 lines) |

**Testing rules:**
- One variable at a time
- Minimum 7-10 days per test
- Minimum 1,000 impressions per variant
- Wait for 95% confidence before declaring a winner
- Document hypothesis, changes, results, and learning

**Testing cadence:**

| Phase | Duration | Focus |
|-------|----------|-------|
| Week 1-2 | Launch | Even rotation, gather baseline |
| Week 3-4 | Hook test | 2-3 headline variations |
| Week 5-6 | CTA test | Winning hook, 2-3 CTA variations |
| Week 7-8 | Value prop test | Winning hook + CTA, different benefit angles |
| Ongoing | Iteration | Continuous improvement |

---

## 5. Landing Pages

### Landing Page Type by Funnel Stage

| Stage | Visitor State | Where to Send | CTA Style |
|-------|-------------|---------------|-----------|
| TOF | Problem-aware, exploring | Homepage, content hub, educational resources | "Learn more," "Read the guide" |
| MOF | Solution-aware, comparing | Solution landing pages, comparison pages, case studies | "See how it works," "Get a walkthrough" |
| BOF | Product-aware, deciding | Demo request page, free trial, pricing page | "Book a demo," "Start free trial" |

### Page Elements by Stage

**TOF pages:**

| Element | Include | Avoid |
|---------|---------|-------|
| Headline | Pain-point focused, empathetic | Product name or feature list |
| Body copy | Problem validation, industry context | Technical specifications |
| Social proof | Industry credibility, thought leadership | Product reviews, G2 badges |
| CTA | "Learn more," "Read the guide" | "Book a demo," "Start free trial" |
| Form | None - ungated content preferred | Multi-field lead capture |

**MOF pages:**

| Element | Include | Avoid |
|---------|---------|-------|
| Headline | Benefit-driven, specific to problem | Generic value props |
| Body copy | How you solve their specific problem | Exhaustive feature lists |
| Social proof | Case studies with metrics, recognizable logos | Generic testimonials |
| CTA | "See how it works," "Get a walkthrough" | Aggressive "Buy now" |
| Form | Light - email + company for gated assets | 8+ field forms |

**BOF pages:**

| Element | Include | Avoid |
|---------|---------|-------|
| Headline | Direct, action-oriented, specific offer | Vague or aspirational language |
| Body copy | Results, ROI data, competitive advantages | Educational content |
| Social proof | Named testimonials, specific metrics, logos | Anonymous quotes |
| CTA | "Book a demo," "Start free trial" | "Learn more" (too soft) |
| Form | Short - 3-5 fields maximum | Long qualification forms |

### Message Match Checklist

| Element | Must Match |
|---------|-----------|
| Headline | Ad headline and page headline reinforce the same message |
| Offer | Whatever the ad promises must be immediately visible on the page |
| Visual style | Ad imagery and page design should feel connected |
| CTA language | Ad CTA and page CTA should use same or closely related wording |
| Audience voice | If ad speaks to CTOs, page must speak to CTOs |
| Value prop | Primary benefit in the ad must be primary benefit on the page |

**Rule of thumb:** If a visitor clicks your ad and cannot confirm they are in the right place within 3 seconds, your message match is broken.

### Conversion Rate Benchmarks

| Page Type | Conversion Rate Range | Strong Performance |
|-----------|-----------------------|-------------------|
| Homepage (TOF traffic) | 1-3% | Above 2% |
| Content hub / blog | 2-5% | Above 3% |
| Solution landing page (MOF) | 3-8% | Above 5% |
| Gated content download page | 10-25% | Above 15% |
| Demo request page (BOF retargeting) | 5-15% | Above 10% |
| Free trial signup page | 8-20% | Above 12% |
| LinkedIn Lead Gen Form (on-platform) | 8-25% | Above 15% |

### Lead Gen Form vs Landing Page Decision

| Factor | Lead Gen Form Wins | Landing Page Wins |
|--------|-------------------|-------------------|
| Audience warmth | Warm/retargeting audiences | Cold audiences needing education |
| Offer type | Simple offers (download, demo) | Complex offers requiring explanation |
| Lead volume priority | Higher volume needed | Quality matters more than volume |
| Current LP conversion rate | Below 5% (form reduces friction) | Above 10% (LP is working) |
| Mobile traffic | High mobile share (form is frictionless) | Desktop-heavy audience |
| Brand experience | Less important | Landing page IS part of the pitch |
| Tracking needs | Basic attribution sufficient | Need detailed behavior tracking |

**When Lead Gen Forms backfire:**
- Lead quality drops (zero friction = submissions without real intent)
- No website behavior data (no scroll depth, time on page)
- No retargeting pixel fires (visitor never reached your site)

**Hybrid approach:** Lead Gen Forms for BOF retargeting (warm audiences). Landing pages for TOF/MOF (education and experience matter).

### Essential Page Elements

**Above the fold (visible without scrolling):**
- Clear headline (primary value prop)
- Supporting subheadline
- Hero visual or product screenshot
- Primary CTA button
- Social proof snippet (logo bar, "Trusted by 500+ companies")

**Remove from landing pages:**
- Top navigation menu (reduces exit paths)
- Footer links except legal
- Multiple competing CTAs
- Walls of text
- Auto-playing video with sound
- Generic stock photos

### Mobile Optimization

Over 60% of LinkedIn usage happens on mobile. Non-optimized pages lose more than half your traffic.

| Element | Requirement |
|---------|-------------|
| Page load speed | Under 3 seconds on 4G |
| CTA button | Minimum 44x44 pixels |
| Text readability | 16px minimum font, high contrast |
| Form fields | Appropriate input types (email keyboard for email fields) |
| Sticky CTA | Consider fixed CTA button on scroll for longer pages |

---

## 6. Launch Checklist

### Pre-Launch Verification

Complete every section before activating any campaign. A missed setting wastes weeks of budget.

**Account setup:**

| Check | Status |
|-------|--------|
| Campaign Manager access confirmed (admin or campaign manager role) | [ ] |
| Correct ad account selected (verify account ID) | [ ] |
| Billing information active and valid | [ ] |
| Company Page connected to ad account | [ ] |
| LinkedIn Insight Tag installed and firing (check Tag Helper extension) | [ ] |
| Team members have appropriate access levels | [ ] |

**Tracking and conversions:**

| Check | Status |
|-------|--------|
| Conversion events created (one per meaningful action) | [ ] |
| Events fire on actual completions, not button clicks | [ ] |
| UTM parameters configured for every destination URL | [ ] |
| UTMs verified with marketing ops for CRM routing | [ ] |
| Google Analytics receiving LinkedIn traffic correctly | [ ] |
| CRM integration tested (Lead Gen Form submissions route correctly) | [ ] |
| Retargeting audiences created and populating | [ ] |
| Conversion window set (30-day click, 7-day view typical) | [ ] |

**Audience configuration:**

| Check | Status |
|-------|--------|
| Target audience defined and documented | [ ] |
| Audience size within recommended range for funnel stage | [ ] |
| Audience Expansion OFF (non-negotiable) | [ ] |
| LinkedIn Audience Network OFF | [ ] |
| Competitors excluded | [ ] |
| Existing customers excluded from prospecting | [ ] |
| Converted leads excluded from ALL campaigns | [ ] |
| Website visitors excluded from cold campaigns | [ ] |
| Unpaid, training, and entry-level seniority excluded | [ ] |
| Matched audiences uploaded and processed (allow 24-48 hours) | [ ] |

**Creative review:**

| Check | Status |
|-------|--------|
| Minimum 4 active ads per campaign | [ ] |
| Ad formats mixed within each campaign | [ ] |
| Copy reviewed (5-layer audit passed) | [ ] |
| CTA matches funnel stage and landing page | [ ] |
| Ad naming convention applied | [ ] |
| Landing page URL correct and loading | [ ] |
| Landing page message matches ad creative | [ ] |
| UTMs appended to all destination URLs | [ ] |
| Mobile preview checked for all ads | [ ] |

**Budget and bidding:**

| Check | Status |
|-------|--------|
| Daily budget sufficient for 10+ results per week | [ ] |
| Bid strategy set (Week 1: Maximum Delivery) | [ ] |
| Optimization goal matches campaign objective | [ ] |
| No campaign underfunded relative to audience size | [ ] |

**Campaign settings:**

| Setting | Required Value |
|---------|---------------|
| Campaign objective | Matches actual goal |
| Conversion event | Correct event selected |
| Schedule | Start date set, end date as needed |
| Ad rotation | Even rotation at launch |
| Audience Expansion | OFF |
| LinkedIn Audience Network | OFF |
| Location targeting | Correct regions verified |

### Launch Sequence

Launch in this order. Each step depends on the previous.

| Step | Action | Timing |
|------|--------|--------|
| 1 | Verify Insight Tag active and conversion events firing | Day before launch |
| 2 | Confirm all audiences populated and configured | Day before launch |
| 3 | Submit all ads for review | Day before launch (review takes 12-24 hours) |
| 4 | Activate retargeting campaigns FIRST | Launch day |
| 5 | Activate MOF campaigns | Launch day (after retargeting) |
| 6 | Activate TOF campaigns LAST | Launch day (after MOF) |
| 7 | Verify all campaigns Active and delivering | 2-4 hours after launch |
| 8 | Check first impression and spend data | End of launch day |

**Why this order:** If TOF launches without retargeting in place, warm visitors from awareness campaigns have nowhere to go. They visit your site, leave, and are lost because no retargeting campaign exists to bring them back. Always have the bottom ready before opening the top.

### First 48 Hours

**Hours 1-4 (Delivery check):**

| Check | Expected | Red Flag | Action |
|-------|----------|----------|--------|
| Campaign status | Active, delivering | "Pending review" or "Not delivering" | Contact support if stuck |
| Impressions | Growing | Zero impressions | Audience too small, bid too low, or ad rejected |
| Budget pacing | Spending steadily | Exhausting in first hours | Lower bid or increase daily budget |
| Ad status | All ads approved | Ads rejected | Review reason, fix, resubmit |

**Hours 4-24 (Performance check):**

| Check | Expected | Red Flag | Action |
|-------|----------|----------|--------|
| CTR (landing page) | Above 0.30% for TOF | Below 0.20% | Creative or targeting issue |
| CPC | Within benchmark | 2x above benchmark | Bid too high or audience too narrow |
| Conversion events | Firing (if BOF) | Zero conversions with significant clicks | Tracking broken - verify immediately |

**Hours 24-48 (Calibration check):**

| Check | Expected | Red Flag | Action |
|-------|----------|----------|--------|
| Demographics | Relevant titles and industries | Budget to irrelevant titles | Add exclusions immediately |
| Frequency | Under 2.0 | Above 3.0 already | Audience too small for budget |
| Quality of clicks | Reasonable time on site | 90%+ bounce rate | Message match or landing page issue |

### First Week Triggers

| Metric | Trigger | Action |
|--------|---------|--------|
| CTR below 0.25% after 3 days | Creative not resonating | Pause underperformers, test new creative |
| CPC 50%+ above benchmark | Audience or bid issue | Switch to manual bidding at 20% below observed CPC |
| Zero conversions after 5 days (BOF) | Tracking or funnel issue | Verify pixel, check landing page, review form |
| One ad consuming 80%+ of budget | Premature winner selection | Switch to even rotation |
| Frequency above 4.0 by end of week | Audience saturation risk | Expand audience or reduce daily budget |

### Week 1 to Week 2 Transition

| Action | Timing |
|--------|--------|
| Switch from even to auto ad rotation | After 7-10 days of even rotation |
| Switch from automated to manual bidding | Week 2, using Week 1 data as baseline |
| Exclude irrelevant demographics identified in Week 1 | Immediately when identified |
| Add first creative test variants | Beginning of Week 2 |
| Review and refine audience based on delivery data | End of Week 1 |
| Document all learnings from Week 1 | Before making Week 2 changes |

---

## 7. Scaling Strategy

### Scaling Prerequisites

Do not scale until ALL conditions are met. Scaling a broken campaign amplifies waste.

| Prerequisite | Threshold |
|-------------|-----------|
| Conversion tracking verified and accurate | Events firing on actual completions |
| CTR at or above benchmark | TOF: above 0.35%, MOF: above 0.55%, BOF: above 0.80% |
| CPC within acceptable range | Below $20 standard, below $10 TLAs |
| Lead quality confirmed by sales | SQLs, not just MQLs |
| Current budget fully spending | Daily budget consistently consumed |
| Audience penetration measured | Know your current reach percentage |
| At least 30 days of performance data | Minimum one full optimization cycle |
| Landing page conversion rate acceptable | Above 5% for BOF pages |

**Failing even one prerequisite?** Fix it before scaling.

### Audience Penetration - The Foundation

Penetration is the percentage of your target audience that has seen your ads. This is the single most important metric for scaling decisions.

| Timeframe | Penetration | Interpretation | Action |
|-----------|-------------|---------------|--------|
| 30 days | Below 15% | Severely underspending | Increase budget significantly |
| 30 days | 15-25% | Underspending | Increase budget |
| 30 days | 25-35% | Healthy range | Monitor and optimize |
| 30 days | 35-50% | Well-penetrated | Consider audience expansion before more budget |
| 30 days | Above 50% | Approaching saturation | Expand audience or diversify |

**Key insight:** Doubling budget typically boosts penetration by only 50-70%, not 100%. One well-budgeted campaign reaching 35%+ always outperforms multiple underfunded campaigns each reaching 10-15%.

### Five Scaling Dimensions

**1. Budget Scaling**

| Rule | Detail |
|------|--------|
| Increment size | 20-30% at a time, not 2x or 3x |
| Frequency | One increase per week maximum |
| Stabilization | Wait 5-7 days after each increase |
| Watch metric | If CPA rises more than 20%, pause and evaluate |
| Algorithm reset | Large jumps (2x+) can reset learning - avoid |

**Budget increase decision tree:**

| Current CPA vs Target | Penetration | Decision |
|----------------------|-------------|----------|
| CPA below target | Below 30% | Increase budget 25-30% |
| CPA at target | Below 30% | Increase budget 15-20% |
| CPA above target | Below 30% | Fix creative/targeting first |
| CPA below target | 30-50% | Increase budget 10-15% cautiously |
| CPA at target | 30-50% | Hold - good equilibrium |
| CPA above target | 30-50% | Optimize, do not increase |
| Any CPA | Above 50% | Expand audience before more budget |

**2. Audience Scaling**

| Method | When to Use |
|--------|------------|
| Add new job titles | Core titles are well-penetrated |
| Expand company size range | Current segment saturated |
| Add new industries | Core industry well-covered |
| Split by seniority | Mixed seniority has unclear performance |
| Lookalike audiences | Strong seed list (1K+ converters) |
| Skills-based targeting | Job title targeting exhausted |

**Critical:** Always launch new audience segments as separate campaigns. Never add new targeting to existing campaigns.

**3. Geographic Scaling**

| Phase | Markets | Approach |
|-------|---------|----------|
| Phase 1 | Primary market (usually US) | Prove the model, establish benchmarks |
| Phase 2 | English-speaking (UK, Canada, Australia) | Same language, similar buying behavior |
| Phase 3 | Western Europe (DACH, Nordics, Benelux) | May need localized creative |
| Phase 4 | Southern/Eastern Europe, APAC | Requires local market understanding |
| Phase 5 | Emerging markets (LATAM, SEA, India) | Lower costs but different buying cycles |

**Why separate campaigns per region:** CPAs vary significantly. Mixing US and India means the algorithm spends most budget on cheap Indian impressions, starving the US audience. Always segment by cost-similar regions.

**4. Creative Scaling**

| Level | Volume | Description |
|-------|--------|-------------|
| Starting | 4 ads per campaign | Minimum for algorithm optimization |
| Growing | 6-8 ads per campaign | Enough variety to test and rotate |
| Scaled | 8-12 ads per campaign | Full creative testing engine |
| Mature | 12+ with monthly refresh | Continuous creative pipeline |

**Creative fatigue signals:**
- CTR declining over 2+ weeks with no other changes
- Frequency climbing above 5x monthly
- Engagement rate dropping below 0.5%

When fatigue hits, refresh creative before increasing budget.

**5. Ad Format Scaling**

Different formats compete in different auctions - diversifying is an auction strategy, not just a creative strategy. See the Format Scaling Priority table in Section 3.

### The Scaling Progression

**Level 1: One campaign to two campaigns**
1. Launch one awareness campaign targeting core ICP
2. Build retargeting audiences (website visitors, video viewers, ad engagers)
3. Wait until retargeting pool reaches 1K+ members
4. Launch retargeting campaign with different creative and stronger CTAs

**Level 2: Campaigns to campaign groups**
Once you have 4+ campaigns, organize into groups (see Campaign Group Model in Section 1).

**Level 3: Campaign groups to multiple accounts**

| Signal | Threshold |
|--------|-----------|
| Campaign count | Above 200 campaigns |
| Campaign groups | Above 50 groups |
| Management complexity | Different teams for different regions |
| Budget separation | Different invoicing needed per region |

Split strategy: More regions than personas = one account per region. More personas than regions = one account per persona. Use LinkedIn Business Manager to unify.

### Performance Guardrails During Scaling

| Guardrail | Threshold | Action if Breached |
|-----------|-----------|-------------------|
| CPA increase | More than 20% above pre-scale baseline | Pause increase, investigate |
| CTR decline | More than 25% below pre-scale baseline | Creative fatigue - refresh |
| Lead quality drop | SQL rate below 50% of pre-scale | Tighten targeting |
| Frequency spike | Above 8x monthly | Audience saturation - expand |
| ROAS decline | More than 30% below pre-scale | Review full funnel |

### Scaling Decision Framework

| Question | If No | If Yes |
|----------|-------|--------|
| Is current performance above benchmark? | Optimize first, do not scale | Continue |
| Is audience penetration below 35%? | Expand audience or geography | Increase budget 20-30% |
| Is lead quality confirmed by sales? | Tighten targeting | Continue |
| Is there room in a new geography or persona? | Diversify formats and creative | Launch new campaign in new segment |

### Scaling Timeline

| Phase | Timeline | Focus |
|-------|----------|-------|
| Foundation | Month 1-2 | Single market, core ICP, prove the model |
| Expansion | Month 3-4 | Add retargeting, test new audiences and formats |
| Optimization | Month 5-6 | Refine based on 90+ days of data |
| Scaling | Month 7-9 | Geographic expansion, new persona segments |
| Maturation | Month 10-12 | Multi-account, ABM layers, full format mix |

### Forecasting for Scale

Match budget allocation to pipeline potential, not evenly.

| Step | Action | Data Source |
|------|--------|-------------|
| 1 | Pull pipeline data by persona | CRM |
| 2 | Map current spend by persona | Campaign Manager |
| 3 | Check reach/penetration by persona | Campaign Manager demographics |
| 4 | Find the mismatch | Compare pipeline share vs budget share vs penetration |

**Decision example:**

| Persona | Pipeline Share | Budget Share | Penetration | Decision |
|---------|--------------|-------------|-------------|----------|
| VP Sales | 45% | 25% | 18% | Increase budget - high pipeline, low penetration |
| Dir Marketing | 30% | 40% | 42% | Maintain - well-matched |
| CTO | 25% | 35% | 55% | Reduce slightly - diminishing returns |

---

## 8. Benchmarks

### CTR Benchmarks by Funnel Stage

LinkedIn reports two CTR metrics:
- **CTR (all)** - includes reactions, comments, profile clicks, post expansions
- **CTR to Landing Page (CTRTLP)** - only clicks that leave LinkedIn to your URL

Always use CTRTLP for apples-to-apples comparison.

| Funnel Stage | Audience Type | CTRTLP Range | Strong Performance |
|-------------|--------------|-------------|-------------------|
| TOF | Cold prospecting | 0.30-0.55% | Above 0.44% |
| MOF | Warm retargeting | 0.55-0.80% | Above 0.70% |
| BOF | High-intent retargeting | 0.80-1.30% | Above 1.00% |

Platform average CTRTLP: 0.45%. Above 1.0% is genuinely strong.

### CPC Benchmarks by Format

| Ad Type | CPC Range |
|---------|-----------|
| Thought Leader Ads | $4-$8 |
| Text ads | $3-$8 |
| Document ads | $5-$12 |
| Video ads | $6-$15 |
| Carousel ads | $7-$18 |
| Single image | $8-$22+ |
| Conversation ads | $8-$25 |

### CPM Benchmarks by Format

| Ad Type | CPM Range |
|---------|-----------|
| Text ads | $2-$6 |
| Spotlight ads | $4-$8 |
| Thought Leader Ads | $20-$45 |
| Document ads | $20-$40 |
| Video ads | $25-$55 |
| Single image | $33-$65 |

### Cost Per Lead Benchmarks

| Metric | Range | Context |
|--------|-------|---------|
| Cost per engagement | $2-$5 | Below $3 is strong |
| Cost per Lead Gen Form completion | $15-$50 | Depends on offer and audience warmth |
| Cost per lead (Lead Gen Form) | $50-$200 | Standard B2B SaaS range |
| Cost per website form submission | $200-$500 | Higher friction than native forms |
| Cost per SQL | $200-$500+ | Depends on ACV and qualification |
| Cost per demo booked | $150-$400 | Varies by industry |

### Lead Gen Form Fill Rate

| Performance Level | Fill Rate |
|------------------|-----------|
| Below average | Under 8% |
| Average | 8-12% |
| Strong | 12-20% |
| Excellent | Above 20% |

### Benchmarks by Industry

| Industry | Avg CPC | Avg CPL | CPM Range | Competition |
|----------|---------|---------|-----------|-------------|
| SaaS / Software | $10-$20 | $80-$200 | $35-$60 | High |
| Financial Services | $12-$25 | $100-$300 | $40-$70 | Very High |
| Healthcare / Life Sciences | $15-$30 | $120-$350 | $45-$80 | High |
| Cybersecurity | $12-$22 | $100-$250 | $40-$65 | High |
| HR / Recruiting Tech | $8-$18 | $60-$180 | $30-$55 | Moderate |
| Marketing / AdTech | $8-$16 | $50-$150 | $28-$50 | Moderate |
| Manufacturing / Industrial | $10-$20 | $80-$220 | $35-$60 | Moderate |
| Education / EdTech | $6-$14 | $40-$120 | $25-$45 | Lower |
| Professional Services | $10-$22 | $90-$250 | $35-$65 | Moderate-High |

### Benchmarks by Company Size

| Company Size | CPC Multiplier | CPM Multiplier |
|-------------|---------------|---------------|
| 1-50 employees | 0.7x | 0.6x |
| 51-200 employees | 0.8x | 0.75x |
| 201-500 employees | 1.0x (baseline) | 1.0x |
| 501-1,000 employees | 1.2x | 1.15x |
| 1,001-5,000 employees | 1.4x | 1.3x |
| 5,001-10,000 employees | 1.6x | 1.5x |
| 10,001+ employees | 1.8-2.5x | 1.7-2.2x |

### Benchmarks by Geography

| Region | CPC Range | CPM Range | CPL Range |
|--------|-----------|-----------|-----------|
| United States | $10-$25 | $40-$75 | $80-$250 |
| United Kingdom | $8-$22 | $35-$65 | $75-$220 |
| Canada | $8-$20 | $30-$60 | $70-$200 |
| Australia / New Zealand | $8-$20 | $30-$60 | $70-$210 |
| Western Europe (DACH, Nordics) | $7-$18 | $30-$55 | $65-$200 |
| France / Southern Europe | $6-$15 | $25-$50 | $55-$180 |
| Middle East (UAE, Saudi) | $6-$18 | $25-$55 | $60-$180 |
| Eastern Europe | $4-$12 | $15-$35 | $35-$120 |
| Southeast Asia | $3-$10 | $12-$30 | $30-$100 |
| Latin America | $3-$12 | $10-$35 | $30-$120 |
| India | $2-$8 | $8-$25 | $20-$80 |

### Seasonal Patterns

| Quarter | Cost Trend | Notes |
|---------|-----------|-------|
| Q1 (Jan-Mar) | Lower costs | New budgets ramping. January cheapest. Good for testing. |
| Q2 (Apr-Jun) | Rising costs | Peak B2B buying season. Budget approvals, fiscal year spend. |
| Q3 (Jul-Sep) | Moderate dip | Summer slowdown. August cheapest summer month. Good for testing. |
| Q4 (Oct-Dec) | Highest costs | Year-end budget flush. Plan 20-40% higher CPMs vs Q1. |

**Weekly patterns:**
- Tuesday through Thursday: Peak engagement days
- Monday: Strong (professionals catch up on feeds)
- Friday: Moderate decline
- Saturday-Sunday: Lowest engagement but cheapest CPMs (can be cost-efficient for awareness)

**Launch timing:** Start new campaigns Tuesday or Wednesday to maximize initial learning during peak days.

### Video Ad Benchmarks

| Metric | Floor | Average | Strong |
|--------|-------|---------|--------|
| View rate (starts / impressions) | 25% | 35-45% | Above 40% |
| Completion rate (completions / starts) | 5% | 8-15% | Above 15% |
| Cost per 50% view | $5+ | $2-$4 | Below $2 |

### Conversation Ad Benchmarks

| Metric | Below Average | Average | Good | Excellent |
|--------|--------------|---------|------|-----------|
| Open rate | Below 30% | 30-40% | 40-50% | Above 50% |
| CTA click rate | Below 1.5% | 1.5-3% | 3-5% | Above 5% |
| Cost per send | Above $1.50 | $0.50-$1.50 | $0.30-$0.50 | Below $0.30 |
| Lead gen form completion | Below 5% | 5-10% | 10-20% | Above 20% |

### Document Ad Benchmarks

| Metric | Below Average | Average | Good | Excellent |
|--------|--------------|---------|------|-----------|
| Slide-through rate | Below 15% | 15-25% | 25-40% | Above 40% |
| CTR to landing page | Below 0.30% | 0.30-0.45% | 0.45-0.60% | Above 0.60% |
| Engagement rate | Below 1.0% | 1.0-2.0% | 2.0-3.5% | Above 3.5% |

### Key Ratios to Monitor

| Ratio | Healthy Range | What It Tells You |
|-------|--------------|-------------------|
| Engagement rate | Above 1.0% | Creative resonates with audience |
| CTRTLP / Engagement rate | Above 0.15 | People clicking through, not just engaging |
| Video view rate | Above 40% | Hook captures attention |
| Video completion rate | 8-15% | Content holds interest |
| Form fill rate | Above 8% | Offer-audience alignment |
| Frequency (monthly) | 2-5x | Balanced exposure |
| Audience penetration (30 days) | 25-35% | Budget adequacy |

### ROAS and Pipeline Context

Direct-response ROAS is not the right primary metric for LinkedIn. The platform drives pipeline through brand awareness over extended timeframes.

| Metric | Benchmark |
|--------|-----------|
| Direct ROAS (last-click) | ~113% for B2B SaaS (misleadingly low - misses influence) |
| Pipeline attribution window | 3-6 months |
| BOF conversion rate | Above 5% |
| Retargeting pool growth rate | 10-20% monthly (TOF doing its job) |

**Better metrics:** Pipeline influenced by LinkedIn touchpoints, cost per SQL, assisted conversions, brand search lift.

### Budget Planning Formulas

**Lead generation campaigns:**
```
Daily budget = Target CPL x Target leads per week / 7
Example: $150 CPL x 10 leads/week / 7 = $214/day
```

**Awareness campaigns:**
```
Daily budget = Target audience size x Target penetration / 1000 x CPM / 30
Example: 100,000 x 30% / 1000 x $45 / 30 = $45/day
```

**Minimum viable budget per campaign:**
```
Min daily budget = Target CPA x 10 results/week / 7
Example: $50 CPA x 10 / 7 = ~$72/day minimum
```

---

## 9. Common Mistakes

### Campaign Structure Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Mixing prospecting and retargeting in one group | Cannot control budget per funnel stage | Separate groups by funnel stage |
| Mixing enterprise and SMB in one campaign | Algorithm spends on cheaper SMB impressions | Separate campaigns by company size |
| Adding new audience targeting to existing campaigns | Contaminates performance data | Launch new segments as separate campaigns |
| Fewer than 4 ads per campaign | Limits algorithm, accelerates fatigue | Maintain 4+ active ads always |
| No naming convention | Reporting becomes impossible at scale | Apply format before first campaign |

### Bidding Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Starting with manual bids on new campaigns | No baseline - bids are guesses | Always start automated for week 1 |
| Never switching from automated | Overpay indefinitely | Switch to manual at 80% of avg after week 1 |
| Manual bidding on audiences under 10K | Severe underdelivery | Keep automated permanently |
| Changing bids daily | Constant learning resets | Adjust weekly at most |
| Budget changes larger than 20% | Destabilizes algorithm | Make 10-20% incremental adjustments |

### Creative and Copy Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Generic hooks ("Struggling with X?") | Low CTR - audience scrolls past | Name the specific frustration directly |
| Feature dumps in body copy | Nobody reads feature lists in ads | One feature per ad, details on landing page |
| CTA mismatch with funnel stage | TOF asking for demos, BOF saying "learn more" | Match CTA to awareness stage |
| Buzzword overload | Buyers mentally skip these | Replace with concrete outcomes and numbers |
| No social proof anywhere | B2B buyers are risk-averse | Add metric, quote, or logo to every ad |

### Document Ad Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Adjacent slides say the same thing | Feels repetitive, wastes slide position | Merge or differentiate (generic vs specific) |
| Product introduced without a bridge | Feels like a sales pitch | Use natural transition phrase |
| Text-heavy slides with no visual treatment | Users swipe past without reading | Add content blocks, visual breaks |
| Burying key statistics in paragraphs | Wastes most powerful proof point | Give stats standalone visual break slide |
| Gating thin content | Users feel tricked after form submit | Only gate content that justifies the exchange |

### Conversation Ad Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Treating inbox like feed ads | Wrong context, wrong expectations | Write like a text message |
| Messages too long (500+ words) | Nobody reads long inbox messages | 3-5 short lines per message |
| Sending from SDRs or generic profiles | Low trust, low open rates | Send from founder, VP, or SME |
| Big blocks of text with no breaks | Reader scans and opts out | Max 3 lines before a paragraph break |
| No warm-up before sending | Cold inbox messages underperform | Run TLAs or content ads first, retarget |

### Landing Page Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| One page for all campaigns | Different audiences need different messages | Create stage-specific pages |
| Sending TOF traffic to demo page | Cold audiences are not ready | Send to educational content |
| Broken message match | High bounce, wasted spend | Same headline, offer, visual style |
| Slow page load (5+ seconds) | 53%+ of mobile visitors abandon | Compress images, minimize scripts |
| No mobile optimization | Losing 60%+ of traffic | Mobile-first design |

### Scaling Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Scaling before prerequisites are met | Amplifies waste | Fix every prerequisite first |
| Doubling budget overnight | Algorithm reset, performance collapse | Increase 20-30% at a time |
| Good CPAs but no pipeline | Wrong people converting | Review demographics, tighten targeting |
| Scaling without penetration data | No idea if room to grow | Check penetration before every budget increase |
| Skipping scaling phases | Missing data and infrastructure | Each phase builds foundation for the next |

### Tracking Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Tracking button clicks, not completions | Inflated conversion numbers | Track actual submission confirmation |
| No UTM parameters | Cannot attribute leads to campaigns | Add UTMs to every destination URL |
| UTMs not verified with ops | Data routing breaks | Confirm mapping before launch |
| No Insight Tag on landing page | Lose retargeting and conversion data | Install and verify on all pages |
| Multiple conversion events firing | Duplicate counting | Audit triggers, one fire per action |

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or if you want something like this built for your team, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
