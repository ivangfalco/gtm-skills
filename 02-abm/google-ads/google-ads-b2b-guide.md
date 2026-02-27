# Google Ads for B2B - Complete Guide

Campaign types, account structure, keyword strategy, bidding, Quality Score, and landing page mapping for B2B companies running Google Ads.

---

## Why Google Ads for B2B

Google Ads captures existing demand. People are actively searching for solutions to their problems - your job is to be there at the right moment with the right message.

**What makes it unique for B2B:**
- **Intent-rich:** Someone searching "enterprise data enrichment platform" is further down the funnel than anyone you can reach on social
- **Measurable:** Every click traces back to a keyword, ad, and landing page - no guessing
- **Immediate:** Unlike SEO, you can appear on page 1 today
- **Pipeline-connected:** With offline conversion tracking (gclid), you can optimize for revenue, not just leads

**The tradeoff:** Google Ads is blessed with intent and cursed with scale. B2B search volume is small. CPCs are high ($5-50+ per click depending on vertical). You will never get LinkedIn-level reach - but you will get higher-intent traffic.

---

## Campaign Types for B2B

### When to Use Each Type

| Campaign Type | Use Case | Priority | Expected CPC | Notes |
|---|---|---|---|---|
| **Search** | High-intent keyword capture | #1 - always start here | $5-50 | Foundation of any B2B account |
| **Brand Search** | Protect your own brand terms | #2 - run alongside Search | $0.50-3 | Cheap, high-converting, defensive |
| **Competitor Search** | Capture competitor demand | #3 - after core Search works | $8-60 | Lower QS, higher CPC, comparison LP needed |
| **RLSA** | Search ads shown to site visitors only | #4 - after pixel has data | $3-30 | Higher conversion rates, can bid on broader terms |
| **Performance Max** | AI-driven across all Google networks | #5 - after Search proves ROI | $3-25 | Only after 50+ conversions/month and clean conversion data |
| **Display Remarketing** | Banner retargeting to site visitors | #6 - supplement to search | $0.50-5 | Low CPC, low conversion rate, keeps you top of mind |
| **YouTube** | Video awareness and remarketing | #7 - brand/awareness play | $0.02-0.10 (CPV) | Good for remarketing, expensive for prospecting |
| **Demand Gen** | YouTube + Gmail + Discover | #8 - after Search maxed | $5-20 | Google's replacement for Discovery campaigns |

### The B2B Priority Ladder

Start at the bottom (highest intent), prove it works, then climb up:

```
LEVEL 1: Brand Search + High-Intent NonBrand Search
  "Your job is to capture demand that already exists"

LEVEL 2: Medium-Intent NonBrand + Competitor Search
  "Expand keyword coverage, capture comparison shoppers"

LEVEL 3: RLSA + Display Remarketing
  "Stay in front of people who already visited your site"

LEVEL 4: Performance Max + YouTube Remarketing
  "AI-driven expansion with proven conversion data"

LEVEL 5: YouTube Prospecting + Demand Gen
  "Create new demand through video and awareness"
```

**Do NOT jump to Level 4 or 5 before Levels 1-3 are profitable.** This is the most common B2B Google Ads mistake - running Performance Max or YouTube prospecting before Search campaigns have proven unit economics.

---

## Account Structure by Intent Level

### The Intent Pyramid

Structure your account around intent levels, not product lines or personas. Intent determines keyword selection, bidding, landing pages, and expected metrics.

```
Account
├── Brand (Highest Intent)
│   └── Ad Groups: Brand exact, Brand + product, Brand + pricing
│
├── High-Intent NonBrand (Solution-Aware)
│   └── Ad Groups: [product category] software, [product category] platform, [product category] tool
│
├── Medium-Intent NonBrand (Problem-Aware)
│   └── Ad Groups: how to [solve problem], [problem] solution, best [category]
│
├── Low-Intent NonBrand (Category-Aware)
│   └── Ad Groups: what is [category], [category] benefits, [category] vs [alternative approach]
│
├── Competitor (Variable Intent)
│   └── Ad Groups: [competitor name], [competitor] alternative, [competitor] vs [you]
│
└── RLSA (Remarketing Lists for Search)
    └── Ad Groups: Broader keywords, only shown to past visitors
```

### Expected Metrics by Intent Level

| Intent Level | Expected CTR | Expected CPC | Expected CVR | Target CPA Range |
|---|---|---|---|---|
| **Brand** | 8-15% | $0.50-3 | 15-30% | $5-20 |
| **High-Intent NonBrand** | 3-8% | $8-40 | 3-8% | $50-200 |
| **Medium-Intent NonBrand** | 2-5% | $5-25 | 1-4% | $100-400 |
| **Low-Intent NonBrand** | 1-3% | $3-15 | 0.5-2% | $200-600 |
| **Competitor** | 2-5% | $10-50 | 1-3% | $100-500 |
| **RLSA** | 4-10% | $3-20 | 5-12% | $30-150 |

*Ranges vary significantly by vertical. SaaS CPCs are typically lower than fintech or cybersecurity. Enterprise deals justify higher CPAs.*

---

## Keyword Strategy

### Match Types - When to Use Each

| Match Type | Symbol | Behavior | When to Use | Risk Level |
|---|---|---|---|---|
| **Exact** | [keyword] | Only that query + close variants | Always start here. Cleanest data. | Low |
| **Phrase** | "keyword" | Query must contain keyword in order | After exact proves profitable. Captures longer-tail variations. | Medium |
| **Broad** | keyword | Any query Google considers related | Last phase only. Requires Smart Bidding + audiences + 30+ conversions/month. | High |

### Match Type Progression

```
Phase 1: Exact Match Only
├── Launch with exact match keywords
├── Collect 2-4 weeks of data
├── Identify converting keywords
└── Build negative keyword list from Search Terms Report

Phase 2: Add Phrase Match
├── Add phrase match for proven exact match winners
├── Run both simultaneously (separate campaigns or same campaign)
├── Continue aggressive Search Terms auditing
└── Expect 20-40% more volume at slightly higher CPA

Phase 3: Broad Match (Conditional)
├── ONLY add broad match if: 30+ conversions/month, Smart Bidding active, audiences layered
├── Layer custom intent or remarketing audiences to constrain broad match
├── Monitor Search Terms Report DAILY for first 2 weeks
└── Remove audience constraints only on broad keywords with strong 90-day conversion history
```

### Keyword Research Process

1. **Start with your product/solution category:** What do people call what you do? (e.g., "data enrichment software", "accounts payable automation")
2. **Add modifiers:** enterprise, B2B, for [industry], platform, tool, software, solution, best, top, compare
3. **Mine competitor keywords:** [competitor name], [competitor name] alternative, [competitor] vs
4. **Check Google Keyword Planner:** Get volume estimates, discover related terms, identify CPC ranges
5. **Use Search Terms Report:** After launching, the Search Terms Report is your best keyword research tool - real queries from real people

### B2B Keyword Categories (Prioritize Top-Down)

| Priority | Category | Example Keywords | Intent Level |
|---|---|---|---|
| 1 | **Brand** | [your company name], [your product name] | Highest |
| 2 | **Product/Service** | "data enrichment software", "B2B lead generation tool" | High |
| 3 | **Comparison/Competitor** | "[competitor] alternatives", "[competitor] vs" | High-Medium |
| 4 | **Problem-Aware** | "how to improve lead quality", "reduce manual data entry" | Medium |
| 5 | **Category/Informational** | "what is data enrichment", "types of lead generation" | Low |

### Negative Keywords - Critical from Day 1

Add these negative keyword lists before launching any B2B campaign:

**Jobs & Careers:**
```
jobs, careers, salary, hiring, internship, resume, interview, remote work, work from home
```

**Free & Cheap:**
```
free, cheap, discount, coupon, open source, freemium, trial (if you don't offer trials)
```

**Education:**
```
training, course, tutorial, certification, degree, university, academy, bootcamp
```

**Research/Non-Commercial:**
```
template, example, PDF, download, reddit, quora, forum, wiki, YouTube, definition
```

**B2C & Unqualified:**
```
personal, small business (if you target enterprise), DIY, homemade, consumer
```

**Search Terms Audit Cadence:**
- **Week 1-2 after launch:** Review daily
- **Week 3-4:** Review every 2-3 days
- **Month 2+:** Review weekly
- **Mature campaigns:** Review bi-weekly minimum

### Keyword Optimization Rules

**Non-Performer Rule:** Keyword has NEVER converted + spent 3x your target CPA (use all-time data) = pause it. No exceptions.

**Ongoing Optimization Rule:** Keyword HAS converted historically but CPA is above target in the last 90-day window = reduce bid or pause.

**Don't panic-pause** based on a single bad week. Use minimum 30 days of data for new keywords before making cut/keep decisions.

---

## Bidding Strategy for B2B

### The Bidding Progression

B2B accounts typically don't have enough conversion volume for Smart Bidding to work on day one. Follow this progression:

```
STAGE 1: Manual CPC or Maximize Clicks (with bid cap)
├── Use during first 2-4 weeks
├── Set bid cap based on what you can afford (target CPA / expected conversion rate)
├── Example: $150 target CPA, 5% CVR = max CPC around $7.50
├── Goal: collect enough clicks and conversions to feed Smart Bidding
└── Minimum: 15-30 conversions before moving on

STAGE 2: Maximize Conversions (with target CPA)
├── Switch once you have 30+ conversions in 30 days
├── Set target CPA based on your ACTUAL data, not a guess
├── Give Google 2 weeks to learn (performance will fluctuate initially)
├── Don't change target CPA more than 15-20% at a time
└── If CPA is 2x+ target after 3 weeks, revert to Manual CPC

STAGE 3: Maximize Conversion Value (with target ROAS)
├── Only if you're importing revenue/pipeline values via offline conversions
├── Google optimizes for value, not just conversion count
├── Best for mature accounts with 6+ months of offline conversion data
└── This is the gold standard - but most B2B accounts never reach this stage
```

### When to Stay on Manual CPC

Stay on Manual CPC if:
- You have fewer than 15 conversions per month
- Your conversion action has a very long delay (30+ days between click and conversion)
- You're running competitor campaigns (Smart Bidding struggles with low QS)
- You're in a highly seasonal vertical with dramatic volume swings
- You need tight cost control during a test phase

### Smart Bidding Requirements (Real Minimums)

Google says 15 conversions in 30 days. In practice:
- **30+ conversions/month** for tCPA to work reliably
- **50+ conversions/month** for tROAS to work reliably
- Conversions must be consistent (don't switch conversion actions mid-optimization)
- Conversion delays under 7 days work best (longer delays confuse the algorithm)
- If your B2B cycle is 30-90 days, use a higher-funnel conversion (like MQL) as the primary action and import deeper funnel events as secondary

### Bid Adjustments (Manual CPC Only)

| Dimension | When to Adjust | Typical Range |
|---|---|---|
| **Device** | Desktop typically outperforms mobile for B2B | +20% desktop, -30% mobile |
| **Location** | US metros with HQ density outperform rural | +15-25% for top metros |
| **Ad Schedule** | Business hours (M-F, 8am-6pm) typically outperform | -50% to -100% for nights/weekends |
| **Audience** | RLSA and in-market audiences convert at higher rates | +25-50% for remarketing audiences |

*Note: Bid adjustments are mostly ignored under Smart Bidding. Device is the only one partially respected under tCPA.*

---

## Quality Score Optimization

### Quality Score Components (1-10 Scale)

| Component | Weight | What Google Measures | How to Improve |
|---|---|---|---|
| **Expected CTR** | ~35% | How likely users are to click your ad | Compelling headlines, strong CTAs, ad extensions, relevance to query |
| **Ad Relevance** | ~25% | How well your ad matches the search query | Include keywords in headlines, match search intent, tightly themed ad groups |
| **Landing Page Experience** | ~40% | How useful your landing page is | Message match, fast load time (<3s), mobile-friendly, clear CTA, relevant content |

### Why Quality Score Matters for B2B

Quality Score directly impacts your cost per click through the Ad Rank formula:

```
Ad Rank = Max Bid x Quality Score x Expected Impact of Extensions
```

A QS of 10 with a $5 bid beats a QS of 4 with a $10 bid. In B2B where CPCs are $10-50+, even a 1-point QS improvement saves thousands per month.

**QS Impact on CPC (approximate):**

| Quality Score | CPC Impact |
|---|---|
| 10 | -50% vs average |
| 8-9 | -25% vs average |
| 7 | Baseline |
| 5-6 | +25% vs average |
| 3-4 | +50-100% vs average |
| 1-2 | +200%+ vs average (often won't serve) |

### Quality Score Improvement Playbook

**For Below Average Expected CTR:**
- Rewrite headlines with stronger hooks and more specific language
- Add numbers and stats ("2x pipeline", "500+ companies")
- Test different CTAs ("Get a Demo" vs "See Pricing" vs "Start Free")
- Add all available ad extensions (sitelinks, callouts, structured snippets, images)
- Make sure the keyword appears in at least one headline

**For Below Average Ad Relevance:**
- Include the exact keyword (or close variant) in Headline 1 or 2
- Tighten ad group themes - if you have 10 keywords with different intents, split them
- Use Dynamic Keyword Insertion {KeyWord:Fallback} in one headline as a test
- Write ad copy that directly addresses what the searcher is looking for

**For Below Average Landing Page Experience:**
- Ensure the landing page headline matches the ad headline
- Page load time must be under 3 seconds (use Google PageSpeed Insights)
- Single, clear CTA above the fold - don't give 5 options
- Mobile responsive with easy-to-fill forms
- Relevant content that answers the query's intent
- Remove top navigation (landing pages, not website pages)
- Add social proof: logos, testimonials, review badges

---

## Landing Page Mapping by Intent

The chain **Search Query > Ad Copy > Landing Page** must be consistent. Mismatches kill conversion rates.

### Landing Page Strategy by Campaign Type

| Campaign Type | Landing Page Type | Key Elements |
|---|---|---|
| **Brand** | Homepage or brand page | Navigation OK, full site experience |
| **High-Intent NonBrand** | Dedicated landing page per theme | No navigation, single CTA, message match to keyword |
| **Medium-Intent NonBrand** | Solution/product landing page | Education-first layout, CTA is softer (guide, webinar) |
| **Low-Intent NonBrand** | Content/resource landing page | Lead magnet, guide download, educational content |
| **Competitor** | Comparison landing page | Feature-by-feature comparison, "Why switch" messaging |
| **RLSA** | Same as source campaign | Same pages, but can test more aggressive CTAs |

### Landing Page Essentials Checklist

- [ ] Headline matches the ad headline and keyword intent
- [ ] Single clear CTA above the fold (Book a Demo, Start Free Trial, etc.)
- [ ] Social proof visible without scrolling (logos, G2 rating, customer count)
- [ ] Page loads in under 3 seconds on mobile and desktop
- [ ] Form is short (3-5 fields for demo requests, less for content)
- [ ] Mobile responsive with thumb-friendly form fields
- [ ] No top navigation (landing page, not website page)
- [ ] Benefits over features in the copy
- [ ] Trust signals near the form (privacy policy, security badges)
- [ ] Thank you page has conversion tracking pixel firing correctly

### Landing Page Do Nots

- Do NOT send high-intent keywords to your homepage
- Do NOT use the same landing page for all keywords
- Do NOT have multiple competing CTAs on one page
- Do NOT hide the form behind multiple clicks
- Do NOT require 10+ fields on a demo form
- Do NOT forget to test mobile experience (50%+ of B2B traffic is mobile now)

---

## B2B-Specific Challenges

### Challenge 1: Long Sales Cycles (30-180+ Days)

The average B2B deal closes 60-120 days after the first click. This means:
- **Google's default 30-day conversion window misses most conversions.** Set conversion windows to 90 days for B2B.
- **Smart Bidding struggles** because feedback is delayed. Use higher-funnel conversions (MQL, SQL) as the primary action. Import pipeline and revenue as secondary.
- **gclid offline conversion tracking is not optional** - it's required. Capture the gclid, store it in your CRM, and upload conversion events (MQL, SQL, Opportunity, Closed Won) back to Google Ads.
- **Attribution is murky.** A click today might become a customer in 6 months through 20 other touchpoints. Use data-driven attribution model, not last-click.

### Challenge 2: Small Audiences and Low Volume

B2B keywords have a fraction of the volume of B2C keywords. "Data enrichment software" might get 500 searches/month versus "running shoes" at 500,000.

**How to handle:**
- Don't expect thousands of leads. 20-50 qualified leads per month from Google Ads is excellent for most B2B companies.
- Start with exact match to capture every available conversion before expanding.
- Use Impression Share metrics to understand how much of the available demand you're capturing.
- If IS Lost (Budget) is high, increase budget before adding keywords - you're leaving existing demand on the table.
- If IS Lost (Rank) is high, improve Quality Score and increase bids before adding keywords.

### Challenge 3: High CPCs ($10-50+ Per Click)

B2B CPCs are expensive because the keywords are commercial and competitive.

**How to manage:**
- **Focus on Quality Score** - the single biggest lever for reducing CPC in competitive B2B auctions
- **Tight negative keyword management** - every irrelevant click at $25 CPC is expensive waste
- **Don't bid on everything** - start with 20-30 high-intent keywords, not 500
- **Landing page conversion rate is your multiplier** - improving CVR from 3% to 5% reduces effective CPA by 40%
- **Calculate your CAC ceiling** - if average deal value is $50K/year, a $500 CPA is excellent. If deal value is $5K/year, a $500 CPA is unsustainable.

### Challenge 4: Multiple Stakeholders in the Buying Committee

B2B purchases involve 6-10 decision makers. The person who clicks your ad may not be the person who signs the contract.

**How to handle:**
- Build remarketing audiences from your best landing pages and use them across Google Display, YouTube, and other channels
- Upload customer match lists (email lists from CRM) to create similar audiences
- Use RLSA campaigns to target broader keywords only for people who have already engaged with your site
- Ensure your landing pages address multiple personas (the researcher, the evaluator, the decision maker)

### Challenge 5: Proving ROI to Leadership

Google Ads for B2B is expensive and results take months. Leadership wants to see ROI.

**How to prove it:**
- Set up offline conversion tracking from day 1 - this is non-negotiable
- Report on pipeline influenced and revenue attributed, not just leads
- Use custom columns in Google Ads to show pipeline value per campaign
- Create a monthly dashboard that shows: spend, leads, MQLs, SQLs, pipeline, revenue
- Track cost per opportunity and cost per customer, not just cost per lead
- Be patient and set expectations: 90-day minimum to evaluate Google Ads performance for B2B

---

## Conversion Tracking Setup

### What to Track (Priority Order)

| Priority | Conversion Event | Type | Use As |
|---|---|---|---|
| 1 | **Demo request / Contact form** | Primary | Optimize toward this |
| 2 | **Trial signup** | Primary | Optimize toward this (product-led) |
| 3 | **Pricing page visit** | Secondary | Observation only |
| 4 | **Content download** | Secondary | Observation only |
| 5 | **MQL (from CRM)** | Offline - Primary | Use for Smart Bidding if demo volume is low |
| 6 | **SQL (from CRM)** | Offline - Secondary | Pipeline reporting |
| 7 | **Opportunity Created** | Offline - Secondary | Pipeline reporting |
| 8 | **Closed Won + Revenue** | Offline - Secondary | ROAS reporting |

### Offline Conversion Setup (gclid)

This is the single most important technical setup for B2B Google Ads:

1. **Capture the gclid** from the URL when a visitor lands on your site
2. **Store it** in a hidden form field, then push to your CRM with the lead record
3. **Upload conversion events** from CRM back to Google Ads (manually or automated via API)
4. **Events to upload:** MQL, SQL, Opportunity Created, Closed Won (with revenue value)
5. **Upload cadence:** Weekly minimum, daily if automated

Without this, you're optimizing in the dark. Google doesn't know which clicks turned into revenue, so it can't optimize for what matters.

### Attribution Settings

- **Model:** Data-driven attribution (if enough conversions). Otherwise, time-decay or position-based.
- **Conversion window:** 90 days for enterprise B2B, 30-60 days for SMB
- **View-through window:** 1 day only (prevents over-attribution from Display/YouTube)
- **Include in conversions:** Only the conversion actions you want Smart Bidding to optimize toward

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).