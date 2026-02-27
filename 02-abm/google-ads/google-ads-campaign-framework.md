# Google Ads Campaign Structure Framework

Campaign naming conventions, ad group structure, RSA strategy, budget allocation, targeting, audience layering, and conversion tracking for B2B accounts.

---

## Campaign Naming Convention

Consistent naming lets you filter, report, and optimize without guessing what each campaign does.

### Standard Format

```
{Region}_{Theme}_{CampaignType}_{Language}_{MatchType}_{Device}
```

### Components

| Element | Options | Examples |
|---|---|---|
| **Region** | US, EU, UK, APAC, Global | US |
| **Theme** | Brand, NonBrand, Competitor, RLSA, Content, DSA | NonBrand |
| **Campaign Type** | Search, PMax, Display, Video, DemandGen | Search |
| **Language** | EN, FR, DE, ES, Multi | EN |
| **Match Type** | Exact, Phrase, Broad, Mixed | Exact |
| **Device** | AllDevices, Desktop, Mobile | AllDevices |

### Examples

```
US_NonBrand_Search_EN_Exact_AllDevices
US_Brand_Search_EN_Phrase_AllDevices
EU_NonBrand_Search_Multi_Exact_AllDevices
US_Competitor_Search_EN_Exact_AllDevices
US_RLSA_Search_EN_Broad_AllDevices
US_Remarketing_Display_EN_AllDevices
US_Awareness_Video_EN_AllDevices
US_LeadGen_PMax_EN_AllDevices
```

### Ad Group Naming

```
{keyword theme}
```

Keep it simple. The ad group name should describe the keyword cluster it contains.

**Examples:**
- `data enrichment software`
- `lead generation platform`
- `zoominfo alternatives`
- `crm data quality`

### Ad Label Naming

```
{angle}-{start date}
```

Label every ad with the messaging angle and launch date. This makes performance analysis and creative rotation much easier.

**Examples:**
- `pain-callout-15Jan2025`
- `social-proof-01Feb2025`
- `benefit-focused-15Mar2025`
- `competitor-contrast-01Apr2025`

---

## Ad Group Structure

### SKAG vs Themed Ad Groups

**SKAGs (Single Keyword Ad Groups) are outdated.** Google's close variant matching and RSA combinations make SKAGs unnecessary and create management overhead.

**Use themed ad groups instead:**

| Approach | Keywords Per Ad Group | When to Use |
|---|---|---|
| **Themed Ad Groups** | 3-5 keywords sharing the same intent | Default approach for all campaigns |
| **Single Theme, Multiple Variations** | 3-5 variations of the same core concept | When keyword volume is high enough |
| **SKAG** | 1 keyword | Only for extremely high-value keywords where you need full control |

### How to Theme Ad Groups

Group keywords by **shared intent** - all keywords in one ad group should trigger the same ad and send users to the same landing page.

**Good Ad Group Theme:** `data enrichment software`
```
[data enrichment software]
[data enrichment platform]
[data enrichment tool]
"data enrichment software"
"data enrichment platform"
```
All these keywords have the same intent. One set of ads and one landing page works for all.

**Bad Ad Group Theme:** `data tools` (too broad)
```
[data enrichment software]
[data visualization tool]
[data warehouse platform]
```
These have completely different intents. You can't write one ad that matches all three.

### Ad Group Composition

| Element | Quantity | Notes |
|---|---|---|
| **Keywords** | 3-5 per ad group | Same intent, different variations |
| **RSAs** | 2-3 per ad group | Different messaging angles (pain, benefit, proof) |
| **Extensions** | All types at campaign level | Sitelinks, callouts, snippets, images |
| **Landing Page** | 1 per ad group | Must match keyword intent |

---

## RSA Best Practices

### Headline Strategy (15 Slots Available)

Use all 15 headline slots. Give Google enough options to test while maintaining control over key positions.

**Headline Allocation:**

| Position | Purpose | Pinning | Example |
|---|---|---|---|
| **Headline 1** | Keyword relevance | Pin to Position 1 | "Enterprise Data Enrichment Platform" |
| **Headline 2** | Value proposition | Pin to Position 2 | "Enrich CRM Data in Real-Time" |
| **Headline 3** | CTA | Pin to Position 3 | "Book a Demo Today" |
| **Headlines 4-15** | Testing pool | Unpinned | Various benefits, features, social proof |

### Headline Categories to Cover

Fill your 15 headlines across these categories:

| Category | # of Headlines | Examples |
|---|---|---|
| **Keyword Match** | 2-3 | Include the primary keyword and close variants |
| **Value Proposition** | 2-3 | Main benefit, unique differentiator |
| **Social Proof** | 2-3 | "Trusted by 500+ Companies", "4.8/5 on G2" |
| **CTA** | 2-3 | "Get a Demo", "Start Free Trial", "See Pricing" |
| **Pain/Problem** | 1-2 | "Stop Wasting Time on Manual Data Entry" |
| **Feature** | 1-2 | "Real-Time API, 99.9% Uptime" |
| **Urgency/Specificity** | 1-2 | "Results in 30 Days", "Set Up in Under 1 Hour" |

### Description Strategy (4 Slots Available)

| Slot | Purpose | Example |
|---|---|---|
| **Description 1** | Expand on the primary value prop | "Automatically enrich every lead in your CRM with 50+ data points. No manual work required." |
| **Description 2** | Social proof or feature support | "Trusted by 500+ B2B companies. Integrates with Salesforce, HubSpot, and 30+ tools." |
| **Description 3** | Handle objections or add urgency | "Start with a free pilot. No credit card required. See results in your first week." |
| **Description 4** | Alternative angle or CTA | "Replace manual research with automated enrichment. Book a 15-minute demo today." |

### The "Fake ETA" Strategy

Pin headlines 1, 2, 3 AND descriptions 1, 2 to create a fully controlled ad that behaves like the old Expanded Text Ad format.

Use this as your **control ad** in each ad group. Run it alongside a true RSA (minimal pinning) as your **test ad**.

| Ad | Pinning | Purpose |
|---|---|---|
| **RSA 1 (Control - "Fake ETA")** | Pin H1, H2, H3 + D1, D2 | Predictable, controlled messaging |
| **RSA 2 (Test - Open)** | Pin H1 only, rest unpinned | Let Google optimize combinations |
| **RSA 3 (Angle B)** | Pin H1, H2 only | Different messaging theme |

### RSA Copy Rules

- **Never repeat the same message** across pinned positions (H1 and H2 should say different things)
- **Each RSA should have a unique messaging THEME** - don't create 3 identical RSAs with slightly different wording
- **Include numbers and stats** when possible - they increase CTR ("2x pipeline", "50+ integrations", "$0 setup fee")
- **Use Dynamic Keyword Insertion** {KeyWord:Data Enrichment} in one headline as a test variant
- **Write headlines that work independently** - any combination of H1 + H2 + H3 should make sense together
- **Refresh RSAs every 8-12 weeks** or when CTR declines 20%+ from baseline

---

## Budget Allocation by Intent Level

### Allocation Framework

Allocate budget proportionally to intent and proven performance. High-intent campaigns should get the lion's share.

### Starting Budget Allocation (New Account)

| Campaign | % of Budget | Rationale |
|---|---|---|
| **Brand Search** | 5-10% | Low CPC, high CVR, must-run defensively |
| **High-Intent NonBrand Search** | 50-60% | Highest quality leads, prove unit economics here first |
| **Competitor Search** | 10-15% | Capture competitor demand, higher CPC but valuable |
| **RLSA** | 5-10% | Low volume but high conversion rate |
| **Display Remarketing** | 5-10% | Low CPC awareness for past visitors |
| **Reserve** | 10-15% | For testing, scaling winners, seasonal spikes |

### Mature Account Budget Allocation (6+ Months of Data)

| Campaign | % of Budget | Rationale |
|---|---|---|
| **Brand Search** | 3-5% | Stable, low-maintenance |
| **High-Intent NonBrand Search** | 35-45% | Still the core, but share decreases as you expand |
| **Medium-Intent NonBrand Search** | 15-20% | Expanded keyword coverage |
| **Competitor Search** | 10-15% | Stable allocation |
| **RLSA** | 5-10% | Scale with remarketing list size |
| **Performance Max** | 10-15% | After 50+ conversions/month |
| **Display Remarketing** | 5-10% | Maintains top-of-mind awareness |
| **YouTube/Demand Gen** | 5-10% | Brand and awareness |

### Budget Reallocation Signals

| Signal | Action |
|---|---|
| Campaign at target CPA + IS Lost (Budget) > 20% | Increase budget - you're leaving money on the table |
| Campaign at 2x+ target CPA after 30 days | Decrease budget, investigate root cause |
| Campaign CPA improving month-over-month | Gradually increase budget 15-20% per week |
| Campaign exhausting daily budget before 2pm | Increase budget or tighten targeting to spread spend |
| New campaign consistently outperforming old campaign | Shift 20% budget from old to new, monitor for 2 weeks |

### Minimum Budget Requirements

| Campaign Type | Minimum Monthly Budget | Why |
|---|---|---|
| **Search (per campaign)** | $2,000-5,000 | Need enough clicks at $10-30 CPC to generate conversions |
| **Display Remarketing** | $500-1,500 | Low CPC, smaller audiences |
| **Performance Max** | $3,000-5,000 | Needs volume to optimize across networks |
| **YouTube** | $1,500-3,000 | CPV-based, needs reach to be effective |

*If your total monthly budget is under $5,000, run Search only. Don't dilute across channels until Search is maxed out.*

---

## Device and Location Targeting for B2B

### Device Strategy

| Device | Typical B2B Performance | Default Bid Adjustment |
|---|---|---|
| **Desktop** | Highest conversion rate, longest sessions | +0% to +20% |
| **Mobile** | Lower CVR, but growing (especially for research) | -20% to -30% |
| **Tablet** | Low volume, similar to desktop | +0% |

**Rules:**
- Start with all devices, then adjust bids based on actual data after 30 days
- Never exclude mobile entirely - people research on mobile and convert on desktop
- If mobile CVR is less than half of desktop CVR, apply a -30% to -50% bid adjustment
- For Smart Bidding (tCPA/tROAS), device bid adjustments are mostly ignored - Google optimizes automatically

### Location Targeting

**Critical setting:** Target by **"Presence: People in or regularly in your targeted locations"** - NOT "Presence or Interest." The default "Presence or Interest" setting will show your ads to people in other countries who are merely interested in your target location.

| Approach | When to Use | Example |
|---|---|---|
| **Country-level** | Broad targeting, SMB product | United States |
| **State/Region-level** | When specific markets outperform | California, New York, Texas |
| **Metro/City-level** | Enterprise, localized services | San Francisco, New York City, Chicago |
| **Radius targeting** | Events, local services | 25-mile radius around conference venue |

**B2B Location Best Practices:**
- Start country-level, then analyze geo performance after 60 days
- Major tech hubs and business centers typically outperform (SF, NYC, Boston, Austin, Chicago, Seattle, LA)
- Apply positive bid adjustments (+15-25%) for top-performing metros
- Apply negative bid adjustments (-20-50%) for consistently underperforming regions
- If targeting internationally, create separate campaigns per country/region for budget control and language settings

### Ad Schedule for B2B

**Default B2B Schedule:** Monday-Friday, 7am-7pm in your target timezone

| Time Block | Typical B2B Performance | Recommendation |
|---|---|---|
| **Weekday Business Hours (8am-6pm)** | Best conversion rate | Full bids |
| **Weekday Extended (6am-8am, 6pm-9pm)** | Moderate performance | -10% to -20% bid adjustment |
| **Weekday Late Night (9pm-6am)** | Low quality, low intent | -50% to -100% |
| **Weekend** | Mixed - some research, less intent | -30% to -50% |

**Rules:**
- Don't turn off weekends/nights entirely on day 1 - collect 30 days of data first
- Some B2B verticals convert well on weekends (founders, solo operators, startup teams)
- Use ad scheduling data to make bid adjustments, not to exclude time blocks (unless data clearly shows zero value)

---

## Audience Layering

### Audience Types Available in Google Ads

| Audience Type | What It Is | How to Use for B2B |
|---|---|---|
| **Remarketing** | People who visited your website | Bid higher on these users in Search, retarget on Display/YouTube |
| **Customer Match** | Upload email lists from CRM | Target existing leads, exclude customers, create similar audiences |
| **In-Market** | People Google identifies as actively researching a category | Layer on Search campaigns for bid adjustments |
| **Custom Intent** | Custom audience based on keywords/URLs people search/visit | Build from your top converting keywords + competitor URLs |
| **Similar Audiences** | Deprecated - use Optimized Targeting in PMax | Was useful, now replaced |
| **Combined Segments** | AND/OR logic combining multiple audiences | Target remarketing visitors who are also in-market |

### Audience Layering Strategy

**For Search Campaigns - Observation Mode First:**

1. Add all relevant audiences in **Observation mode** (not Targeting mode)
2. Run for 30 days to collect performance data by audience
3. Apply bid adjustments based on what you see:
   - Remarketing visitors converting at 2x rate? Add +50% bid adjustment
   - In-market "Business Software" audience converting well? Add +25%
   - Customer Match list of existing leads? Add +75% (they're already in your pipeline)

**For Display/YouTube - Targeting Mode:**

1. Use **Targeting mode** to restrict ads to specific audiences
2. Remarketing lists are your #1 Display audience for B2B
3. Customer Match lists for nurturing existing pipeline
4. Custom Intent audiences for prospecting (built from competitor URLs + keywords)

### Recommended Audiences for B2B

| Audience | Mode | Bid Adjustment | Purpose |
|---|---|---|---|
| **All website visitors (30 days)** | Observation | +30-50% | Recent visitors with high intent |
| **High-intent page visitors** | Observation | +50-75% | Pricing/demo page visitors |
| **Customer Match - Open Leads** | Observation | +50-75% | Nurture existing pipeline |
| **Customer Match - Customers** | Observation | Exclude or -100% | Don't waste spend on existing customers |
| **In-Market: Business Software** | Observation | +10-25% | Broader intent signal |
| **Custom Intent: Competitor URLs** | Observation | +15-30% | People researching competitors |

### Performance Max Audience Signals

For Performance Max campaigns, audience signals guide Google's AI but don't restrict targeting:

1. **Your remarketing lists** (highest quality signal)
2. **Customer Match lists** (lookalike seed)
3. **Custom intent audiences** from top converting keywords
4. **In-market audiences** relevant to your category
5. **Competitor URL audiences** as custom segments

---

## Conversion Tracking Setup

### Primary vs Secondary Conversions

| Type | Definition | Use in Smart Bidding | Examples |
|---|---|---|---|
| **Primary** | The action you optimize toward | Yes - Smart Bidding uses these | Demo request, trial signup, contact form |
| **Secondary** | Actions you track but don't optimize toward | No - observation only | Pricing page visit, content download, chat started |

**Rule:** Only mark 1-2 conversion actions as Primary. If you mark everything as Primary, Smart Bidding doesn't know what to optimize for and performance suffers.

### Offline Conversion Import (gclid Pipeline)

The most important technical setup for B2B Google Ads:

```
Click (gclid captured) → Form Fill → CRM Record Created →
  → MQL (upload to Google Ads)
  → SQL (upload to Google Ads)
  → Opportunity (upload to Google Ads with value)
  → Closed Won (upload to Google Ads with revenue)
```

**Setup Steps:**
1. Add gclid capture to all landing page forms (hidden field populated from URL parameter)
2. Pass gclid to your CRM with the lead record
3. Create offline conversion actions in Google Ads for each stage (MQL, SQL, Opp, Won)
4. Upload conversions weekly (minimum) or daily via API
5. Set appropriate conversion values: MQL = $X, SQL = $Y, Opp = $Z, Won = actual deal value

**Conversion Value Suggestions (adjust to your business):**

| Stage | Suggested Value | Rationale |
|---|---|---|
| **MQL** | $50-100 | Base qualification signal |
| **SQL** | $200-500 | Sales-accepted, higher quality |
| **Opportunity** | $1,000-5,000 | Real pipeline value |
| **Closed Won** | Actual revenue | True ROI measurement |

### Attribution Settings

| Setting | Recommendation | Why |
|---|---|---|
| **Attribution Model** | Data-driven (if eligible) or Time-decay | Distributes credit across touchpoints |
| **Conversion Window** | 90 days for enterprise, 30-60 for SMB | B2B sales cycles are long |
| **View-through Window** | 1 day | Prevents over-attribution from Display |
| **Count** | One (for lead gen) | Counts one conversion per click, not multiple form fills |

### Conversion Tracking Verification

Before launching any campaign, verify:

- [ ] Google Tag / gtag.js is installed on all landing pages
- [ ] gclid auto-tagging is enabled in Google Ads settings
- [ ] Primary conversion actions are firing correctly (test with Google Tag Assistant)
- [ ] Offline conversion import is set up and tested with sample data
- [ ] Conversion value is assigned correctly for each conversion action
- [ ] Attribution model is set to data-driven or time-decay
- [ ] Conversion window matches your typical sales cycle length
- [ ] Google Analytics is linked to Google Ads account
- [ ] Only the right conversion actions are marked as Primary

---

## Ad Extensions (Assets)

### Required Extensions for B2B

| Extension Type | Minimum | Best Practice | Notes |
|---|---|---|---|
| **Sitelinks** | 4 | 6-8 | Link to key pages: Pricing, Product, Case Studies, About, Blog |
| **Callout Extensions** | 4 | 6-8 | Short benefit phrases: "Free Demo", "24/7 Support", "No Contract" |
| **Structured Snippets** | 1 | 2-3 | List features, services, or integrations |
| **Image Extensions** | 1 | 3-5 | Product screenshots, logos, team photos |
| **Call Extensions** | Optional | Add if phones matter | B2B phone calls can be high value |
| **Lead Form Extensions** | Optional | Test as additional capture | In-SERP form, lower quality than landing page leads |

### Sitelink Strategy

| Sitelink | Link To | When to Use |
|---|---|---|
| **Product/Features** | Product page | Always |
| **Pricing** | Pricing page | If transparent pricing exists |
| **Case Studies** | Customer stories | Always (strong social proof) |
| **Integrations** | Integration directory | If integrations are a selling point |
| **About Us** | About page | Brand campaigns |
| **Blog/Resources** | Content hub | Content/low-intent campaigns |
| **Free Trial/Demo** | Trial signup or demo form | High-intent campaigns |
| **Contact** | Contact page | Always as a backup |

### Extension Application Levels

- **Account level:** Apply sitelinks, callouts, and structured snippets that work across all campaigns
- **Campaign level:** Apply specific sitelinks and callouts that match the campaign theme
- **Ad group level:** Apply highly specific extensions only when necessary (rare in most B2B accounts)

---

## Campaign Settings Checklist

Before launching any new Google Ads campaign, verify every setting:

### Network Settings
- [ ] Search Network: ON
- [ ] Display Network: OFF (create separate Display campaigns)
- [ ] Search Partners: OFF (turn on only after 60+ days if you want to test)

### Location Settings
- [ ] Correct geographic targeting set
- [ ] Location option: "Presence: People in or regularly in your targeted locations"
- [ ] NOT "Presence or Interest" (this is the default and it's wrong for B2B)

### Language Settings
- [ ] Correct language selected (usually English for US campaigns)
- [ ] Separate campaigns for each language if targeting multiple

### Bidding Settings
- [ ] Appropriate bid strategy for account maturity
- [ ] Bid cap set if using Maximize Clicks
- [ ] Target CPA set if using Maximize Conversions (based on real data)

### Budget Settings
- [ ] Daily budget set and realistic for keyword CPCs
- [ ] Monthly budget calculated (daily x 30.4)
- [ ] Delivery method: Standard (not accelerated)

### Ad Rotation
- [ ] "Do not optimize" during testing phase (first 4-6 weeks)
- [ ] "Optimize: Prefer best performing ads" after testing phase

### Ad Schedule
- [ ] Business hours set (M-F, 7am-7pm as default)
- [ ] Weekend/night bid adjustments applied after data collection

### Conversion Tracking
- [ ] Primary conversion action selected
- [ ] Conversion tracking verified and firing
- [ ] Attribution model set correctly
- [ ] Conversion window appropriate for sales cycle

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).