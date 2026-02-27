# Google Ads Audience Strategy for B2B — Targeting, Layering, and Segmentation

How to build, layer, and manage audiences in Google Ads for B2B companies. Covers RLSA, Customer Match, in-market segments, custom audiences, observation vs targeting mode, bid adjustments, exclusions, and audience strategy by campaign type.

---

## Why Audiences Matter More in B2B

In B2C, keywords do most of the targeting work. In B2B, keywords alone are not enough - the same search term can come from a Fortune 500 VP or a college student writing a paper. Audiences let you differentiate between them.

**The core problem:** B2B search volume is small. CPCs are high. You cannot afford to pay $30-50 per click for the wrong people. Audience layering lets you bid more for high-value searchers and less (or nothing) for everyone else.

**The principle:** Use audiences to answer "who is searching" - not just "what are they searching for."

---

## Audience Types Available in Google Ads

| Audience Type | Data Source | Best For | Minimum Size |
|---|---|---|---|
| **RLSA (Remarketing Lists)** | Website visitors via Google tag | Re-engaging known visitors in Search | 1,000 users |
| **Customer Match** | CRM uploads (email, phone, address) | Targeting existing contacts and building Similar Audiences | 1,000 matched users |
| **In-Market Segments** | Google's behavioral signals | Reaching people actively researching B2B categories | N/A (Google-managed) |
| **Affinity Segments** | Google's interest-based signals | Broad awareness, less useful for B2B | N/A (Google-managed) |
| **Custom Segments** | Your keyword/URL/app definitions | Intent-based targeting beyond standard segments | N/A (Google-managed) |
| **Similar Audiences** | Modeled from your first-party lists | Expanding reach from proven audiences | Source list needs 1,000+ users |
| **Combined Segments** | Boolean logic across multiple audiences | Precise intersection targeting | Varies |

---

## RLSA - Remarketing Lists for Search Ads

RLSA is the highest-ROI audience strategy in B2B Google Ads. It lets you show Search ads only to (or bid higher for) people who have already visited your website.

### Why RLSA Is Critical for B2B

- B2B buyers research for weeks or months before converting
- First-visit conversion rates are typically 1-3% - most buyers leave without converting
- RLSA recaptures that research traffic when they search again
- You can bid on broader, more expensive keywords - but only for known visitors (controlling cost)

### RLSA Setup

1. **Install the Google tag** on all website pages (or use Google Tag Manager)
2. **Create remarketing lists** in Google Ads (Audience Manager - Your Data Segments)
3. **Define segments by behavior:**

| Segment | Definition | Membership Duration | Use Case |
|---|---|---|---|
| All visitors | All website traffic | 540 days (max) | Broad RLSA, baseline |
| High-intent pages | Visited pricing, demo, or contact page | 90 days | Aggressive bid adjustments |
| Content consumers | Visited 3+ pages or spent 2+ minutes | 180 days | Medium-intent RLSA |
| Converters | Completed a form submission or demo request | 540 days | Exclude from prospecting, upsell |
| Blog/resource visitors | Visited blog or resource pages only | 30 days | Low-intent, use for awareness only |

4. **Apply lists to Search campaigns** (see Observation vs Targeting below)

### RLSA Strategy by Intent Level

| Scenario | Approach | Bid Adjustment |
|---|---|---|
| High-intent keywords + known visitors | RLSA in observation mode, bid +30-50% | Aggressive - these convert well |
| Broad keywords + known visitors only | RLSA in targeting mode, standard bids | Controls cost on expensive broad terms |
| Competitor keywords + known visitors | RLSA in targeting mode, bid +20% | Only show competitor ads to people who already know you |
| Brand keywords | No RLSA needed | Already high-intent by definition |

---

## Customer Match - CRM Audience Uploads

Customer Match lets you upload first-party CRM data (emails, phone numbers, mailing addresses) to Google Ads, which then matches it against Google accounts.

### What You Can Upload

| Data Type | Match Quality | Notes |
|---|---|---|
| Email addresses | Highest match rate | Use all available emails - work and personal |
| Phone numbers | Good | Include country code, E.164 format preferred |
| Mailing addresses | Lower | Requires first name, last name, country, zip minimum |
| Combined | Best | Upload all available data points for each contact |

### Match Rate Expectations

- **Business emails only:** 30-50% match rate (better than Meta because Google has work accounts)
- **Personal emails included:** 60-80% match rate
- **Combined data (email + phone + address):** 70-90% match rate

Google Ads matches significantly better than Meta for B2B because many professionals use work Gmail or Google Workspace accounts.

### CRM Segments to Upload

| Segment | Source | Purpose |
|---|---|---|
| Closed-won customers | CRM - won deals | Build Similar Audiences, exclude from prospecting |
| High-value customers | CRM - top 20% by revenue | Build Similar Audiences from best customers |
| Pipeline contacts | CRM - active opportunities | Reinforce during sales cycle (acceleration) |
| Marketing qualified leads | CRM - MQL stage | Re-engage leads that have not progressed |
| Lost deals | CRM - closed-lost | Win-back campaigns with new messaging |
| Target account contacts | ABM list | Direct targeting of named accounts |

### Customer Match Best Practices

- **Refresh lists weekly** - stale lists miss new CRM entries and include converted contacts
- **Segment aggressively** - a list of "all CRM contacts" is less useful than targeted segments
- **Hash before upload** - Google accepts SHA-256 hashed data for privacy compliance
- **Minimum 1,000 matched users** required for the list to be usable
- **Use Customer Match for Similar Audiences** - your best customer list is the strongest seed

---

## In-Market and Affinity Audiences

### In-Market Segments for B2B

In-market audiences include people Google has identified as actively researching products or services in a specific category. Google determines this from search history, YouTube watch history, and browsing behavior.

**B2B-relevant in-market segments:**

| Category | Segment Examples |
|---|---|
| Business Services | Accounting services, CRM software, HR software, payroll services |
| Business Technology | Cloud computing, cybersecurity, data management, ERP systems |
| Software | Project management, marketing automation, sales software |
| Financial Services | Business lending, commercial insurance, payment processing |

**How to use in-market for B2B:**
- **Observation mode first** - add segments and monitor performance before adjusting bids
- **Layer with keywords** - in-market alone is too broad; combine with Search keywords for precision
- **Test multiple segments** - try 3-5 related segments, compare conversion rates after 2-4 weeks
- **Use for Display and YouTube** - in-market is more effective on Display/YouTube than Search (Search already has keyword intent)

### Affinity Segments for B2B

Affinity audiences represent long-term interests rather than active purchase intent. They are less useful for B2B lead generation but have niche applications.

**When affinity works for B2B:**
- YouTube brand awareness campaigns targeting "business professionals" or "technology enthusiasts"
- Display campaigns where you need reach above all else
- Layered with other signals (demographics, location) to narrow the audience

**When affinity does NOT work for B2B:**
- Search campaigns (keywords already capture intent - affinity adds noise)
- Any campaign optimizing for conversions (too broad, low signal)

---

## Custom Segments - Intent-Based Audiences

Custom segments let you define audiences based on search behavior, website visits, and app usage. This is one of the most powerful B2B targeting tools in Google Ads.

### Building Custom Segments

**Option 1: Search term-based**
Define an audience of people who have searched for specific terms on Google:

| Use Case | Search Terms to Include |
|---|---|
| Competitor researchers | Competitor brand names, "[competitor] alternative", "[competitor] vs" |
| Category buyers | "best [category] software", "[category] platform comparison" |
| Problem-aware | "[specific problem] solution", "how to fix [problem]" |
| Industry-specific | "[industry] [category] tools", "[industry] compliance software" |

**Option 2: URL-based**
Define an audience of people who browse websites similar to URLs you specify:

| Use Case | URLs to Include |
|---|---|
| Competitor audience | Competitor websites, competitor blog URLs |
| Industry readers | Industry publication URLs, analyst report sites |
| Review site visitors | G2, Capterra, TrustRadius pages for your category |

**Option 3: App-based**
Less common for B2B but useful if targeting users of specific business apps.

### Custom Segment Best Practices

- Create separate segments for each intent signal (don't mix competitor + category + problem terms)
- Use 10-15 terms or URLs per segment for optimal specificity
- Test segments in observation mode first, then move to targeting mode if they outperform
- Custom segments work best on Display, YouTube, and Discovery - they have limited impact on Search

---

## Observation vs Targeting Mode

This is the most important audience setting in Google Ads and one of the most misunderstood.

| Mode | What It Does | When to Use |
|---|---|---|
| **Observation** | Ads show to everyone; audience data is collected for bid adjustments and reporting | Default for Search campaigns - learn before restricting |
| **Targeting** | Ads ONLY show to people in the selected audience | RLSA-only campaigns, Customer Match campaigns, Display/YouTube prospecting |

### Decision Framework

| Campaign Type | Recommended Mode | Rationale |
|---|---|---|
| Search - core keywords | Observation | Don't restrict reach; use bid adjustments instead |
| Search - broad keywords | Targeting (RLSA only) | Control cost by limiting to known visitors |
| Search - competitor keywords | Targeting (RLSA) or Observation | Targeting saves budget; observation gives data |
| Display - prospecting | Targeting | Must restrict or Display shows to everyone |
| YouTube - awareness | Targeting | Must define audience or spend is wasted |
| Performance Max | Neither (PMax manages this) | Audience signals guide PMax but don't restrict |

### Common Mistake

Adding audiences in **targeting mode** to Search campaigns when you mean **observation mode**. This silently restricts your reach to only people in those audiences - you lose all other Search traffic. Always double-check the mode after adding audiences.

---

## Audience Bid Adjustments

Bid adjustments let you increase or decrease bids for specific audiences without restricting reach (when using observation mode).

### Recommended Bid Adjustments for B2B

| Audience | Bid Adjustment | Rationale |
|---|---|---|
| Pricing/demo page visitors (RLSA) | +40% to +60% | Highest intent - they were ready to buy |
| Multi-page visitors (RLSA) | +20% to +30% | Research behavior indicates interest |
| Customer Match - pipeline contacts | +30% to +50% | Reinforcing during active sales cycle |
| Customer Match - MQLs | +20% to +30% | Re-engaging known qualified leads |
| In-market - relevant segments | +10% to +20% | Mild uplift for behavioral signal |
| Converters (RLSA) | -100% (exclude) | Already converted - don't pay again |
| Customer Match - closed-won | -100% (exclude) | Already a customer |

### How to Set Bid Adjustments

1. Go to the campaign or ad group
2. Click **Audiences** in the left menu
3. Add audiences in **Observation** mode
4. After 2-4 weeks of data, review performance by audience
5. Set bid adjustments based on conversion rate and CPA differences
6. Re-evaluate monthly - audience performance shifts over time

---

## Negative Audiences and Exclusions

Exclusions prevent wasted spend on people who should never see your ads.

### Must-Have Exclusions for B2B

| Exclusion | How to Build | Apply To |
|---|---|---|
| **Existing customers** | Customer Match list of closed-won contacts | All prospecting campaigns |
| **Recent converters** | RLSA list of thank-you page visitors (7-30 days) | All prospecting campaigns |
| **Job applicants** | RLSA list of careers page visitors | All campaigns |
| **Competitor employees** | Customer Match list (if you have competitor employee emails) | All campaigns |
| **Internal employees** | Customer Match list of employee emails | All campaigns |
| **Disqualified leads** | Customer Match list of DQ contacts from CRM | All prospecting campaigns |

### Exclusion Setup

1. Build the exclusion list in **Audience Manager** (Your Data Segments or Customer Segments)
2. Go to the campaign - **Audiences** - **Exclusions**
3. Add the relevant exclusion list
4. Verify the exclusion is active (check audience insights to confirm list size)

**Important:** Exclusion lists need the same minimum 1,000 users as targeting lists. If your exclusion list is too small, Google may not apply it consistently.

---

## Audience Strategy by Campaign Type

### Search Campaigns

| Audience Action | Priority |
|---|---|
| Add RLSA lists in observation mode | Must-have |
| Add Customer Match lists in observation mode | Must-have |
| Set bid adjustments based on 2-4 weeks of data | Must-have |
| Exclude converters and existing customers | Must-have |
| Add in-market segments in observation mode | Nice-to-have |
| Create RLSA-only ad groups for broad keywords | Advanced |

### Performance Max Campaigns

PMax uses "audience signals" rather than traditional targeting or observation:

| Signal Type | What to Provide | Impact |
|---|---|---|
| Customer Match lists | Best customer list, pipeline list | Strongest signal - tells PMax who your ideal customer looks like |
| Website visitor lists | High-intent page visitors | Good signal for finding similar in-market users |
| Custom segments | Competitor URLs, category search terms | Guides PMax toward relevant inventory |
| Demographics | Age, gender, income (if relevant) | Light signal - use sparingly in B2B |

**PMax audience guidance:**
- Provide multiple audience signals - PMax uses them as starting points, not restrictions
- Your best customer list is the single most valuable signal you can give PMax
- Monitor PMax audience insights to see where it is actually spending
- PMax will go beyond your signals - use exclusions to prevent waste

### Display Campaigns

| Audience Approach | When to Use | Expected Performance |
|---|---|---|
| RLSA retargeting | Always - cheapest conversions | CPA 40-60% lower than prospecting |
| Customer Match targeting | ABM, pipeline acceleration | High engagement, low volume |
| In-market + custom segment | Prospecting when Search is maxed | Higher volume, lower quality |
| Managed placements + audience | Niche targeting on specific sites | Low volume, high relevance |

### YouTube Campaigns

| Audience Approach | When to Use | Expected Performance |
|---|---|---|
| Custom segment (competitor URLs) | Reach competitor's audience | Good awareness, hard to measure conversion |
| Customer Match (pipeline) | Reinforce during sales cycle | High engagement with known contacts |
| In-market segments | Broad awareness | Low CPV, brand lift studies recommended |
| RLSA (website visitors) | Retargeting with video | Strong recall, supports Search conversion |

---

## Audience Sizing and Management

### Minimum Audience Sizes

| Audience Type | Minimum Required | Recommended for Optimization |
|---|---|---|
| RLSA (Search) | 1,000 users | 5,000+ for meaningful bid adjustments |
| Customer Match | 1,000 matched users | 3,000+ for Similar Audiences |
| Display remarketing | 100 users | 1,000+ for stable delivery |
| YouTube remarketing | 1,000 users | 5,000+ for consistent delivery |
| Similar Audiences | Source list 1,000+ | Source list 5,000+ for quality |

### Audience Health Checks

Run these checks monthly:

| Check | What to Look For | Action |
|---|---|---|
| List size trend | Is the list growing, stable, or shrinking? | Shrinking lists need longer membership duration or more traffic |
| Match rate (Customer Match) | Is match rate above 30%? | Below 30% - add more data fields (phone, address) |
| Audience overlap | Are multiple lists targeting the same people? | Consolidate or use exclusions to prevent overlap |
| Performance by audience | Which audiences convert? Which waste spend? | Increase bids on winners, exclude losers |
| Membership duration | Are durations appropriate for your sales cycle? | B2B sales cycles of 90+ days need longer durations |

### Audience Refresh Schedule

| Audience Type | Refresh Frequency | Why |
|---|---|---|
| Customer Match - pipeline | Weekly | Pipeline changes fast - new opps, closed deals |
| Customer Match - customers | Monthly | Customer list changes slowly |
| Customer Match - ABM list | Bi-weekly | New target accounts added, disqualified removed |
| RLSA lists | Automatic | Google tag updates in real-time |
| Custom segments | Quarterly | Review terms/URLs for relevance |

---

## Combined Segments - Advanced Targeting

Combined segments let you use AND/OR/NOT logic across multiple audiences.

### B2B Use Cases

| Combined Segment | Logic | Result |
|---|---|---|
| In-market for CRM software AND visited your site | AND | High-intent researchers who already know you |
| Customer Match pipeline AND NOT converters | AND + NOT | Active pipeline contacts who have not converted yet |
| Custom segment (competitor) OR in-market (category) | OR | Broader prospecting pool with intent signals |
| RLSA pricing page AND Customer Match ABM list | AND | Named account contacts who checked your pricing |

### How to Create Combined Segments

1. Go to **Audience Manager** - **Combined Segments**
2. Select your first audience
3. Choose AND/OR/NOT operators
4. Add additional audiences
5. Name the combined segment descriptively
6. Apply to campaigns as needed

**Limitation:** Combined segments require each individual audience to meet minimum size requirements. If any component is too small, the combined segment will not serve.

---

## Audience Strategy Checklist

Use this checklist when setting up a new B2B Google Ads account or auditing an existing one:

- [ ] Google tag installed and firing on all pages
- [ ] RLSA segments created (all visitors, high-intent pages, content consumers, converters)
- [ ] Customer Match lists uploaded (customers, pipeline, MQLs, ABM targets)
- [ ] Exclusion lists active (existing customers, converters, employees, DQ leads)
- [ ] All Search campaigns have RLSA and Customer Match in observation mode
- [ ] Bid adjustments set after initial 2-4 week learning period
- [ ] Custom segments created for competitor and category intent
- [ ] PMax campaigns have audience signals configured
- [ ] Display/YouTube campaigns use targeting mode with defined audiences
- [ ] Audience refresh schedule documented and followed
- [ ] Monthly audience health check scheduled

---

## Related Files

- **google-ads-b2b-guide.md** - Campaign types, account structure, keyword strategy, bidding
- **google-ads-tracking-guide.md** - Conversion tracking, GTM, enhanced conversions, offline import

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or if you want something like this built for your team, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
