# Google Ads Optimization Playbook

Weekly optimization checklists, search terms audit workflow, bid management, Quality Score tactics, ad testing, budget reallocation, Performance Max optimization, and scale-vs-cut decision framework.

---

## Weekly Optimization Checklist

Run this every Monday morning. Takes 30-45 minutes for a standard B2B account.

### 1. Budget and Pacing (5 min)
- [ ] Check month-to-date spend vs monthly budget target
- [ ] Verify no campaigns are limited by budget unexpectedly (IS Lost Budget > 20%)
- [ ] Confirm all campaigns are delivering (no disapprovals, no zero-impression campaigns)
- [ ] Check for any campaigns that exhausted daily budget before 2pm consistently

### 2. Conversion Performance (10 min)
- [ ] Pull last 7 days vs previous 7 days: leads, CPA, CVR, spend
- [ ] Flag any campaign with CPA 50%+ above target in the last 14 days
- [ ] Check conversion tracking is still firing (sudden drops = broken tags)
- [ ] Review offline conversion uploads - are they current? (MQL, SQL, Opp data)

### 3. Search Terms Audit (10 min)
- [ ] Pull Search Terms Report for last 7 days
- [ ] Add negative keywords for irrelevant queries
- [ ] Flag high-spend/no-conversion search terms for deeper review
- [ ] Identify new keyword opportunities from converting search terms

### 4. Keyword Health (5 min)
- [ ] Pause any keyword that has spent 3x target CPA with zero conversions (all-time data)
- [ ] Review Quality Score changes - flag any keyword that dropped below 5
- [ ] Check for "Low Search Volume" keywords - consolidate or replace
- [ ] Review auction insights for top campaigns - any new competitors?

### 5. Ad Performance (5 min)
- [ ] Check for disapproved ads and fix immediately
- [ ] Review ad-level CTR and CVR - any ad with 50%+ lower CTR than its ad group average after 1,000+ impressions = candidate for pause
- [ ] Verify all ad groups have at least 2 active RSAs

### 6. Action Items (5 min)
- [ ] Document what you changed this week and why
- [ ] List 1-3 experiments to run next week
- [ ] Flag anything that needs escalation (budget increase, landing page changes, conversion tracking issues)

---

## Search Terms Audit Workflow

The Search Terms Report is the single highest-ROI optimization activity in Google Ads. It tells you exactly what people typed before clicking your ad.

### Step-by-Step Process

**Step 1: Pull the Report**
- Go to Keywords > Search Terms in Google Ads
- Date range: Last 7 days (weekly review) or Last 14 days (bi-weekly)
- Sort by Cost (highest first)

**Step 2: Classify Each Search Term**

| Classification | Definition | Action |
|---|---|---|
| **Relevant + Converting** | Matches intent, has conversions | Keep. Consider adding as a keyword if not already. |
| **Relevant + Not Converting** | Matches intent, but no conversions yet | Monitor. Only take action after 2-3x CPA spend. |
| **Irrelevant + Any Spend** | Does not match intent | Add as negative keyword immediately. |
| **Ambiguous** | Could be relevant, unclear intent | Monitor for 1-2 more weeks. |

**Step 3: Add Negatives**

For irrelevant terms:
- Add as **exact match negative** if only that specific query is irrelevant
- Add as **phrase match negative** if the theme is irrelevant (e.g., "free data enrichment")
- Add to a **shared negative keyword list** if it applies across multiple campaigns

**Step 4: Mine New Keywords**

For converting search terms that aren't in your keyword list:
- Add them as exact match keywords in the appropriate ad group
- If the term represents a new theme, consider creating a new ad group for it
- Track these additions - they often become your best performers

### Search Terms Red Flags

| Red Flag | What It Means | Action |
|---|---|---|
| High spend, zero conversions | Budget waste on irrelevant or low-intent queries | Negative keyword + investigate why it's matching |
| Competitor name appearing | You're showing for competitor searches (possibly from broad match) | Add as negative or create a dedicated Competitor campaign |
| Job-related queries | "data enrichment jobs", "data analyst salary" | Add full jobs negative list |
| Educational queries | "what is data enrichment", "data enrichment tutorial" | Negative or move to a content campaign with content LP |
| Geographic mismatch | Queries from locations outside your target market | Check location settings (Presence only) |
| Duplicate keywords | Same search term triggering multiple campaigns | Add cross-campaign negatives to prevent cannibalization |

### Search Terms Audit Schedule

| Account Maturity | Frequency | Focus |
|---|---|---|
| **Week 1-2 (new campaign)** | Daily | Aggressive negative keyword addition, validate match type behavior |
| **Week 3-4** | Every 2-3 days | Continue negatives, start mining new keywords |
| **Month 2-3** | Weekly | Standard weekly audit |
| **Month 4+** | Bi-weekly | Mature account, fewer new terms appearing |

---

## Bid Management Rules

### Manual CPC Bid Rules

| Scenario | Rule | Example |
|---|---|---|
| **Keyword converting at target CPA** | Maintain current bid | CPA target: $150, actual CPA: $140 - keep bid |
| **Keyword converting below target CPA** | Increase bid by 15-20% | CPA: $100 vs $150 target - increase bid to capture more volume |
| **Keyword converting above target CPA** | Decrease bid by 15-20% | CPA: $200 vs $150 target - decrease bid |
| **Keyword never converted, spent > 3x CPA** | Pause keyword | Spent $450+ with zero conversions - pause |
| **Keyword never converted, spent < 3x CPA** | Continue monitoring | Spent $200 of $450 threshold - let it run |

### Smart Bidding Management Rules

Smart Bidding (tCPA, tROAS) manages bids automatically, but you still need to manage the targets:

| Scenario | Rule | Example |
|---|---|---|
| **CPA consistently 10%+ below target** | Lower target CPA by 10% | Achieving $120 CPA on $150 target - change to $135 |
| **CPA consistently 10%+ above target** | Raise target CPA by 10% or investigate | Achieving $180 CPA on $150 target - investigate before raising |
| **CPA wildly fluctuating** | Do nothing for 2 weeks | Smart Bidding needs time to calibrate |
| **CPA doubling overnight** | Check conversion tracking first | Broken tags cause Smart Bidding to go haywire |
| **Volume dropped after tCPA decrease** | Raise target back, decrease more gradually | You went too aggressive, Google restricted auctions |

### Bid Adjustment Cadence

| Bidding Type | Adjustment Frequency | Data Threshold |
|---|---|---|
| **Manual CPC** | Weekly | 200+ clicks or 10+ conversions per keyword |
| **Smart Bidding (tCPA)** | Every 2-4 weeks | 30+ conversions in the evaluation window |
| **Smart Bidding (tROAS)** | Monthly | 50+ conversions with value data |

**Critical rule:** Never change Smart Bidding targets more than 15-20% at a time. Drastic changes force the algorithm to re-learn, causing a performance dip.

---

## Quality Score Improvement Tactics

### Diagnosing Quality Score Issues

Pull Quality Score data at the keyword level and sort by spend. Focus on your highest-spend keywords first.

| QS Component | Status | Diagnosis | Fix |
|---|---|---|---|
| **Expected CTR** | Below Average | Ad copy isn't compelling enough | Rewrite headlines, add numbers/stats, stronger CTAs |
| **Expected CTR** | Average | Room to improve | Test new ad angles, add extensions |
| **Ad Relevance** | Below Average | Ad doesn't match the keyword | Include keyword in headlines, tighten ad group themes |
| **Ad Relevance** | Average | Adequate | Can improve with DKI or closer keyword-ad alignment |
| **Landing Page** | Below Average | Page doesn't serve the searcher well | Fix message match, improve load speed, add content |
| **Landing Page** | Average | Functional but not great | Improve mobile experience, add social proof, speed |

### Quick Win QS Improvements

**Week 1: Ad Relevance (Fastest to Fix)**
1. Audit your top 20 keywords by spend
2. Check if each keyword appears (or a close variant) in at least one headline
3. If not, either add it to the RSA headlines or create a tighter ad group
4. Test Dynamic Keyword Insertion in one headline: {KeyWord:Your Fallback}

**Week 2: Expected CTR**
1. Add all available ad extensions (sitelinks, callouts, snippets, images)
2. Review headlines for all RSAs - replace generic ones with specific, benefit-driven language
3. Add numbers: "500+ Companies", "2x Pipeline", "Setup in 1 Hour"
4. Test different CTAs: "Get a Demo" vs "See Pricing" vs "Start Free"

**Week 3-4: Landing Page Experience (Slowest but Biggest Impact)**
1. Run Google PageSpeed Insights on all landing pages - target score 90+
2. Ensure headline on landing page matches the ad headline
3. Remove site navigation from landing pages
4. Simplify forms to 3-5 fields max
5. Add social proof above the fold (logos, G2 rating, customer count)
6. Make CTA visible without scrolling on both mobile and desktop

### Quality Score Monitoring

| Frequency | What to Check | Action Threshold |
|---|---|---|
| **Weekly** | Top 20 keywords by spend - QS changes | Any keyword dropping below 5 |
| **Monthly** | Full keyword QS distribution | More than 30% of keywords below 6 |
| **Quarterly** | Landing page speed and content audit | Load time above 3 seconds |

---

## Ad Testing Methodology

### Testing Framework

Always have a **control** and a **test** running in each ad group:

| Ad | Role | Pinning Strategy | When to Change |
|---|---|---|---|
| **RSA 1 (Control)** | Current best performer | Pinned H1, H2, H3, D1, D2 ("Fake ETA") | Only replace with a proven winner |
| **RSA 2 (Test)** | New angle being tested | Pinned H1 only, rest unpinned | Replace after 2-4 weeks or 1,000+ impressions |
| **RSA 3 (Optional)** | Additional test | Minimal pinning | Replace after testing period |

### What to Test (Priority Order)

| Priority | Element | Typical Impact | Minimum Test Duration |
|---|---|---|---|
| 1 | **Messaging angle** (pain vs benefit vs proof) | 20-50% CTR difference | 2-3 weeks |
| 2 | **Headline 1** (primary keyword hook) | 10-30% CTR difference | 2 weeks |
| 3 | **CTA** (Get Demo vs See Pricing vs Start Free) | 10-25% CVR difference | 2-3 weeks |
| 4 | **Value proposition** (speed vs quality vs price vs support) | 10-20% CTR difference | 2 weeks |
| 5 | **Social proof** (logos vs stats vs awards) | 5-15% CTR difference | 2 weeks |
| 6 | **Description copy** | 5-10% CTR difference | 2-3 weeks |

### Ad Testing Rules

1. **Test one variable at a time.** If you change the headline AND the description AND the CTA, you don't know what caused the difference.
2. **Minimum 1,000 impressions per ad** before drawing conclusions. For B2B with low volume, this might take 2-4 weeks.
3. **Use Google's ad rotation setting "Do not optimize"** during testing periods so both ads get equal distribution.
4. **Winner criteria:** Higher CTR AND at least equal or better CVR. A high-CTR ad that doesn't convert is worse than a lower-CTR ad that does.
5. **After declaring a winner:** Pause the loser, make the winner your new control, create a new test.
6. **Label every ad:** `{angle}-{start date}` format (e.g., `pain-callout-15Jan2025`). This makes historical analysis possible.

### Ad Refresh Schedule

| Situation | Action | Timing |
|---|---|---|
| **CTR declining 20%+ from baseline** | Refresh creative | Immediately |
| **No decline, running for 8 weeks** | Proactive refresh | Before fatigue sets in |
| **New product feature or messaging** | Create new test ads | As soon as messaging is approved |
| **Seasonal shift** | Update copy for the season | Q1 planning, back-to-school, EOY |
| **Competitor changes** | Update comparison messaging | When you notice competitor shifts |

---

## Budget Reallocation Signals

### When to Increase Budget

| Signal | Data Threshold | Action |
|---|---|---|
| **IS Lost (Budget) > 20%** on a profitable campaign | Sustained for 7+ days | Increase daily budget 20-30% |
| **CPA consistently below target** for 14+ days | CPA 20%+ below target | Increase budget 15-20% per week |
| **Campaign exhausting budget before 3pm** | 3+ days in a row | Increase daily budget 30% |
| **New keyword theme proving profitable** | 10+ conversions at target CPA | Create dedicated campaign, allocate budget |

### When to Decrease Budget

| Signal | Data Threshold | Action |
|---|---|---|
| **CPA 2x+ above target** for 14+ days | After troubleshooting root causes | Decrease budget 20-30%, focus on best ad groups only |
| **No conversions for 7+ days** on a $50+/day campaign | After verifying conversion tracking | Pause and investigate |
| **Quality Score dropping** across the campaign | 3+ keywords dropping below 5 | Pause low-QS keywords, fix landing pages, reduce budget until fixed |
| **Seasonal downturn** (holidays, summer, etc.) | Industry-specific, compare YoY | Reduce budget 20-40% during low periods |

### Budget Reallocation Framework

Run this monthly:

1. **Rank all campaigns** by cost per opportunity (or cost per MQL if pipeline data isn't available)
2. **Top 20% campaigns** (lowest cost per opportunity): Increase budget if IS Lost (Budget) > 10%
3. **Middle 60% campaigns**: Maintain budget, focus on optimization
4. **Bottom 20% campaigns** (highest cost per opportunity): Decrease budget 20%, investigate root cause, give 30 days to improve, pause if no improvement

---

## Performance Max Optimization

### When to Launch Performance Max

**Prerequisites (all must be true):**
- [ ] Search campaigns are profitable and maxed out (IS Lost Budget < 10%)
- [ ] 50+ conversions per month across the account
- [ ] Offline conversion tracking is set up and uploading regularly
- [ ] High-quality creative assets available (images, videos, headlines, descriptions)
- [ ] Minimum $3,000/month budget for PMax specifically

**Do NOT launch Performance Max if:**
- You have fewer than 30 conversions per month
- You don't have offline conversion tracking
- Your Search campaigns still have IS Lost (Budget) > 20%
- You only have one or two landing pages with no visual assets

### Performance Max Asset Group Strategy

| Element | Minimum | Recommended | Notes |
|---|---|---|---|
| **Final URLs** | 1 | 2-3 per asset group | Group by landing page theme |
| **Headlines** | 5 | 10-15 | Same RSA principles apply |
| **Long Headlines** | 1 | 3-5 | 90 characters, more descriptive |
| **Descriptions** | 2 | 4-5 | 90 characters each |
| **Images** | 3 | 10-15 | Landscape (1.91:1), Square (1:1), Portrait (4:5) |
| **Logos** | 1 | 2 (square + landscape) | High-res, clear brand mark |
| **Videos** | 0 | 2-3 | If you don't provide video, Google auto-generates terrible ones - upload your own |

### Performance Max Audience Signals

Audience signals tell Google who to target. They're suggestions, not restrictions - Google may expand beyond them.

**Priority order for audience signals:**
1. **Your website remarketing lists** - highest quality signal
2. **Customer Match lists** (leads and customers from CRM) - gives Google your ideal customer profile
3. **Custom segments** built from top-converting search keywords - tells Google what topics matter
4. **Custom segments** built from competitor URLs - captures competitor audience
5. **In-market audiences** for your category - broadest signal

### Performance Max Optimization Levers

| Lever | What to Do | When |
|---|---|---|
| **Asset group performance** | Pause low-performing asset groups, scale high-performers | After 30 days of data |
| **Asset performance ratings** | Replace "Low" rated assets with new ones | Check monthly |
| **Search term insights** | Review what queries PMax is showing for, add negatives via account-level negative lists | Weekly |
| **Placement reports** | Check where ads are showing (YouTube, Display, Gmail, etc.) | Monthly - exclude junk placements |
| **Audience signal refinement** | Update customer match lists, add new remarketing segments | Monthly |
| **URL expansion** | Turn OFF "Final URL expansion" if PMax is sending traffic to blog posts or irrelevant pages | Check in first 2 weeks |
| **Brand exclusions** | Exclude your own brand terms from PMax so they don't cannibalize Brand Search campaigns | Set up on launch |

### Performance Max Warning Signs

| Warning Sign | What It Means | Action |
|---|---|---|
| **Brand Search conversions dropping after PMax launch** | PMax is cannibalizating Brand Search | Add brand exclusions to PMax |
| **High spend on Display/YouTube with low conversions** | PMax is allocating to low-intent channels | Improve audience signals, consider pausing PMax |
| **"New customer" conversions are actually existing leads** | Conversion tracking or customer list is stale | Update customer match lists, review conversion actions |
| **CPA climbing steadily over 30 days** | PMax is expanding to lower-quality audiences | Tighten audience signals, reduce budget |
| **Great overall numbers but pipeline isn't growing** | PMax is optimizing for low-quality conversions | Switch to offline conversion optimization, not just form fills |

---

## When to Scale vs When to Cut

### The Decision Framework

Every campaign, keyword, and ad eventually reaches one of four states:

```
                    PERFORMING
                        |
         +--------------+--------------+
         |                             |
    AT CAPACITY                   ROOM TO GROW
    (IS Lost Budget < 10%)        (IS Lost Budget > 20%)
         |                             |
    Hold or expand to              Scale: increase
    new themes/channels             budget 15-20%/week
         |                             |
         +--------------+--------------+
                        |
                  UNDERPERFORMING
                        |
         +--------------+--------------+
         |                             |
    FIXABLE                        BROKEN
    (Root cause identified)        (No clear fix)
         |                             |
    Fix: QS, LP, ads, targeting    Cut: pause, reallocate
    then re-evaluate in 30 days     budget to winners
```

### Scale Signals (Green Light)

| Signal | Threshold | Scaling Action |
|---|---|---|
| CPA at or below target for 30+ days | Consistent performance | Increase budget 15-20% per week |
| IS Lost (Budget) > 20% on profitable campaign | Consistently budget-limited | Increase daily budget 25-30% |
| Conversion rate improving month-over-month | 3+ months trend | Add more keywords in the same theme |
| New keyword converting from Search Terms | 5+ conversions from a new query | Create dedicated ad group for it |
| Exact match maxed out, profitable | IS Lost < 10% | Add phrase match for proven keywords |
| Phrase match maxed out, profitable | 30+ conversions/month | Add broad match with audience layering |

### Cut Signals (Red Light)

| Signal | Threshold | Cutting Action |
|---|---|---|
| Keyword spent 3x CPA, zero conversions (all-time) | No exceptions | Pause keyword |
| Campaign CPA 2x+ target for 30+ days | After all troubleshooting | Reduce budget 50%, give 14 more days, then pause |
| Quality Score dropped to 3 or below | After landing page fix attempt | Pause keyword, it's costing too much |
| CTR below 1% for Search campaign | After ad copy refresh | Investigate keyword-ad relevance, likely pause |
| Broad match generating 80%+ irrelevant queries | After adding negatives | Pause broad match, revert to phrase/exact |
| PMax spending heavily on Display with no conversions | After 30 days + audience signal improvements | Pause PMax, go back to Search only |

### Scale Decision Checklist

Before scaling any campaign, confirm:
- [ ] CPA has been at or below target for 30+ days (not just 7 days)
- [ ] Conversion tracking is verified and accurate
- [ ] Landing page conversion rate is stable (not declining)
- [ ] You have budget headroom (client approved increase)
- [ ] You've checked that scaling won't cannibalize other campaigns
- [ ] You have a plan to monitor the increased spend daily for the first 2 weeks

### Cut Decision Checklist

Before cutting any campaign, confirm:
- [ ] You've looked at all-time data, not just last 7 days
- [ ] You've verified conversion tracking is working (a campaign might look like it has zero conversions because the tag is broken)
- [ ] You've checked offline conversions (maybe the click converted into an SQL 45 days later)
- [ ] You've tried optimization fixes first (QS improvement, landing page changes, ad copy refresh)
- [ ] The underperformance has persisted for 30+ days
- [ ] You're not cutting during a known seasonal dip

---

## Monthly Optimization Review

### Monthly Deep Dive Checklist

Run this on the first Monday of each month. Covers everything the weekly review doesn't.

**1. Full Pipeline Review (15 min)**
- [ ] Pull month-over-month: spend, leads, MQLs, SQLs, pipeline, revenue
- [ ] Calculate true cost per opportunity and cost per customer
- [ ] Identify which campaigns are generating pipeline vs which generate leads that go nowhere
- [ ] Update offline conversion data in Google Ads

**2. Quality Score Audit (10 min)**
- [ ] Pull QS distribution across all keywords
- [ ] Flag any keyword above $50/month spend with QS below 5
- [ ] Create action items: ad relevance fixes, landing page improvements
- [ ] Track QS trends month-over-month

**3. Geographic Performance (10 min)**
- [ ] Pull conversion data by location (state or metro level)
- [ ] Apply positive bid adjustments to top-performing geos (+15-25%)
- [ ] Apply negative bid adjustments to underperforming geos (-20-50%)
- [ ] Check for geographic anomalies (sudden spikes from unexpected locations)

**4. Device Performance (5 min)**
- [ ] Pull conversion data by device
- [ ] Update device bid adjustments based on actual CVR data
- [ ] Note mobile vs desktop form completion rates

**5. Match Type Performance (10 min)**
- [ ] Compare exact vs phrase vs broad match: CPA, CVR, volume
- [ ] Assess readiness for match type expansion
- [ ] Review Search Terms quality by match type

**6. Competitor Analysis (10 min)**
- [ ] Check Auction Insights for new competitors or market share changes
- [ ] Review competitor ads via Google Ads Transparency Center
- [ ] Note any messaging changes from competitors
- [ ] Adjust competitor campaign bids if necessary

**7. Ad Rotation and Refresh (10 min)**
- [ ] Identify ads running for 8+ weeks without refresh
- [ ] Review ad-level CTR and CVR trends
- [ ] Plan next round of ad tests
- [ ] Update ad labels for tracking

**8. Budget Reallocation (10 min)**
- [ ] Rank campaigns by cost per opportunity
- [ ] Increase budget for top performers with IS Lost (Budget) > 10%
- [ ] Decrease budget for bottom performers
- [ ] Document all changes and rationale

---

## Quarterly Strategic Review

Every 90 days, zoom out from tactical optimization and review strategic direction.

### Quarterly Questions

1. **Are we capturing all available high-intent demand?**
   - Check IS across all Search campaigns. If IS > 90% on NonBrand, consider expanding to new themes.
   - If IS < 60% on NonBrand, don't expand yet - capture what exists first.

2. **Is our CPA improving or degrading over time?**
   - Plot 90-day CPA trend. If trending up despite optimization, there may be market-level changes (more competitors, rising CPCs).
   - If trending down, consider scaling.

3. **Which campaigns should we expand, and which should we sunset?**
   - Use the scale-vs-cut framework above.
   - Any campaign running at a loss for 90+ days with no clear fix path should be paused.

4. **Should we expand to new channels within Google Ads?**
   - If Search is maxed (IS > 85%), consider PMax, YouTube, or Demand Gen.
   - Never expand channels before Search is profitable.

5. **Are our landing pages still competitive?**
   - Audit competitor landing pages.
   - Check if conversion rates have declined (may indicate landing page staleness).
   - Plan A/B tests for next quarter.

6. **Is our conversion tracking still accurate?**
   - Full conversion tracking audit: tags firing, offline imports current, attribution settings correct.
   - A broken tag can silently destroy performance for weeks before anyone notices.

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).