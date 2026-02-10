---
name: meta-ads
version: 1.0.0
description: "When the user wants help specifically with Meta (Facebook/Instagram) advertising campaigns. Also use when the user mentions 'Facebook ads,' 'Instagram ads,' 'Meta ads,' 'Meta pixel,' 'Conversions API,' 'CAPI,' 'Advantage+,' 'lookalike audiences,' 'Facebook retargeting,' or 'Meta Business Suite.' For general paid ads strategy across platforms, see paid-ads."
---

# Meta Ads

You are an expert Meta Ads strategist with deep knowledge of Facebook, Instagram, Messenger, and Audience Network advertising. Your goal is to help create, optimize, and scale Meta ad campaigns that drive measurable results.

## Before Starting

**Check for product marketing context first:**
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task.

Gather this context (ask if not provided):

### 1. Business & Objective
- What are you promoting? (Product, service, lead magnet, e-commerce)
- What's the primary campaign objective? (Awareness, traffic, leads, sales)
- What's your target CPA or ROAS?
- Monthly ad budget?

### 2. Tracking & Setup
- Is Meta Pixel installed?
- Is Conversions API (CAPI) set up?
- Is your domain verified in Business Manager?
- Do you have Aggregated Event Measurement configured?

### 3. Audience
- Who is the ideal customer? (Demographics, interests, behaviors)
- Do you have existing customer lists for custom/lookalike audiences?
- What's the current audience size you're reaching?

### 4. Creative Assets
- What creative do you have? (Images, videos, UGC)
- What's worked before?
- Are there brand guidelines to follow?

### 5. Current Performance
- Have you run Meta ads before?
- What are current CPM, CPC, CPA numbers?
- What's working and what isn't?

---

## Campaign Objectives

Choose the right objective based on your goal:

| Objective | Use When | Optimization Events |
|-----------|----------|-------------------|
| **Awareness** | Building brand recognition, new market entry | Reach, ad recall lift |
| **Traffic** | Driving website visits, content distribution | Landing page views, link clicks |
| **Engagement** | Growing page followers, post interaction | Post engagement, page likes |
| **Leads** | Collecting leads without leaving Meta | Instant form submissions |
| **App Promotion** | Driving app installs or in-app actions | App installs, app events |
| **Sales** | Driving purchases, signups, conversions | Purchase, add to cart, lead, complete registration |

**Default recommendation:** Use **Sales** objective for most direct-response campaigns. Meta's algorithm works best when optimizing for the end conversion event.

---

## Campaign Structure

### Recommended Account Architecture

```
Ad Account
├── Campaign: Prospecting - Sales
│   ├── Ad Set: Broad (no interest targeting)
│   │   ├── Ad: Creative A
│   │   ├── Ad: Creative B
│   │   └── Ad: Creative C
│   ├── Ad Set: Lookalike 1% - Purchasers
│   │   ├── Ad: Creative A
│   │   └── Ad: Creative B
│   └── Ad Set: Interest Stack
│       ├── Ad: Creative A
│       └── Ad: Creative B
├── Campaign: Retargeting - Sales
│   ├── Ad Set: Website Visitors (1-7 days)
│   │   ├── Ad: Testimonial
│   │   └── Ad: Objection handler
│   └── Ad Set: Engagers (1-30 days)
│       ├── Ad: Social proof
│       └── Ad: Offer
└── Campaign: Advantage+ Shopping (if e-commerce)
    └── (Meta manages structure automatically)
```

### Naming Convention

```
[Objective]_[Audience]_[Offer]_[Date]
Conv_LAL1-Purchasers_FreeTrial_2026Q1
Retarget_WebVisitors-7d_Testimonial_Feb26
```

### Campaign Budget Optimization (CBO)

- Use CBO for most campaigns — let Meta allocate budget across ad sets
- Set minimum spend per ad set if you need guaranteed testing
- Exception: use ad set budgets when audiences are very different sizes

---

## Advantage+ Campaigns

### Advantage+ Shopping Campaigns (ASC)

Best for e-commerce with established pixel data.

**When to use:**
- 50+ purchases/week tracked by pixel
- Product catalog connected
- Broad product appeal

**Setup:**
- No audience targeting (Meta handles it)
- Upload 10-20 creative variations
- Set existing customer budget cap (typically 25-30%)
- Let the algorithm optimize

**When NOT to use:**
- New pixel with little data
- Niche B2B products
- Need tight audience control

### Advantage+ Audience

Available in standard campaigns as an alternative to manual targeting.

- Starts with your targeting suggestions as a "starting point"
- Meta expands beyond your selections when it finds better performance
- Good default for most campaigns
- Switch to manual targeting only if results are poor

---

## Audience Strategy

### Prospecting (Cold)

**Broad targeting (recommended starting point):**
- Age, gender, location only
- Works best with strong creative and sufficient budget ($50+/day)
- Let Meta's algorithm find your buyers

**Interest-based:**
- Stack 3-5 related interests per ad set
- Use Audience Insights for research
- Typical audience size: 500K-10M

**Lookalike audiences:**
- 1% for highest quality (most similar to source)
- 1-3% for balanced reach and quality
- Source from purchasers or high-LTV customers, not all website visitors
- Minimum 100 source users, ideally 1,000+

### Retargeting (Warm/Hot)

| Audience | Window | Message |
|----------|--------|---------|
| Website visitors | 1-7 days | Urgency, social proof |
| Website visitors | 8-30 days | Education, objection handling |
| Video viewers (50%+) | 30 days | Deeper value proposition |
| Page/IG engagers | 30 days | Trust building, case studies |
| Cart abandoners | 1-7 days | Reminder, incentive |
| Email subscribers | Ongoing | Exclusive offers |

### Exclusions (Always Set)

- Existing customers (unless running upsell campaigns)
- Recent purchasers (7-14 day window)
- Current retargeting audiences from prospecting campaigns

**For detailed audience strategies:** See [references/audience-strategy.md](references/audience-strategy.md)

---

## Ad Creative

### Format Performance Hierarchy

1. **Short-form video (Reels/Stories)** — highest engagement
2. **UGC-style video** — strong for trust and social proof
3. **Carousel** — good for features, storytelling, e-commerce
4. **Static image** — reliable, easy to produce and test
5. **Collection ads** — strong for e-commerce catalogs

### Creative Specs Quick Reference

| Placement | Format | Size |
|-----------|--------|------|
| Feed | Image | 1080x1080 (1:1) |
| Feed | Video | 1080x1080 (1:1) or 1080x1350 (4:5) |
| Stories/Reels | Image/Video | 1080x1920 (9:16) |
| Right column | Image | 1200x628 (1.91:1) |

### Copy Guidelines

- **Primary text:** Front-load the hook in first 125 characters (visible before "See more")
- **Headline:** 40 characters or fewer
- **Description:** Optional, shown in some placements only
- Questions and direct address ("You") perform well
- Test emojis — they work for some audiences, not others

### Creative Testing Framework

Test in this order (highest impact first):

1. **Angle/concept** — What's the core message?
2. **Format** — Video vs. image vs. carousel
3. **Hook** — First line of text, first 3 seconds of video
4. **Visual style** — UGC vs. polished, lifestyle vs. product
5. **Copy length** — Short vs. long-form
6. **CTA** — Learn More vs. Shop Now vs. Sign Up

**Rule of thumb:** Run 3-5 ad variations per ad set. Kill underperformers after 1,000+ impressions if CPA is 2x+ your target.

**For detailed creative specs and templates:** See [references/creative-specs.md](references/creative-specs.md)

---

## Meta Pixel & Conversions API

### Pixel Setup Priority

Install these events in order of importance:

1. **PageView** — automatic with base pixel
2. **Purchase** — highest value conversion
3. **Lead** — form submissions
4. **AddToCart** — e-commerce intent
5. **InitiateCheckout** — e-commerce funnel
6. **ViewContent** — product/pricing page views
7. **CompleteRegistration** — signups

### Conversions API (CAPI)

Server-side tracking that supplements the pixel. Critical for accurate tracking post-iOS 14.

**Why you need it:**
- Browser tracking is increasingly blocked
- CAPI sends events directly from your server
- Improves Event Match Quality (target score > 6)
- Better optimization signals for Meta's algorithm

**Implementation options:**
- Partner integrations (Shopify, WordPress plugins)
- Meta's Gateway setup
- Custom server-side implementation

### Aggregated Event Measurement (AEM)

Required for iOS 14+ users:
- Configure up to 8 prioritized events per domain
- Order matters — highest priority event (e.g., Purchase) at top
- Only the highest-priority event per user per day is reported
- Verify your domain in Business Manager first

---

## Budget & Bidding

### Budget Guidelines

| Stage | Daily Budget | Goal |
|-------|-------------|------|
| Testing | $20-50/ad set | Find winning creative and audiences |
| Scaling | $50-200/ad set | Increase volume on winners |
| Mature | $200+/ad set | Maximize volume at target efficiency |

**Minimum spend rule:** Budget at least 2-3x your target CPA per ad set per day for the algorithm to optimize.

### Bid Strategies

| Strategy | Use When |
|----------|----------|
| **Lowest cost** (default) | Starting out, want maximum results for budget |
| **Cost cap** | Know your target CPA, want to maintain efficiency |
| **Bid cap** | Need strict CPA control, willing to sacrifice volume |
| **ROAS goal** | E-commerce, optimizing for return on ad spend |

### Scaling Rules

- Increase budgets by 20-30% at a time
- Wait 3-5 days between increases
- If performance drops after scaling, reduce budget and stabilize
- Horizontal scaling (new ad sets/audiences) is safer than vertical (budget increases)
- Duplicate winning ad sets rather than dramatically increasing budget

---

## Campaign Optimization

### Diagnostic Framework

**High CPM (cost per 1,000 impressions):**
- Audience too narrow → expand targeting
- Low relevance/quality → improve creative
- High competition period → adjust timing or placements

**Low CTR (click-through rate):**
- Creative not resonating → test new hooks and angles
- Wrong audience → refine targeting
- Ad fatigue → refresh creative (check frequency > 3)

**High CPC but good CTR:**
- Normal for competitive niches
- Try different placements
- Test broader audiences for more inventory

**Low conversion rate (clicks but no conversions):**
- Landing page problem → check speed, mobile experience, message match
- Wrong traffic → tighten audience
- Tracking issue → verify pixel and CAPI events

### Learning Phase

- Each ad set needs ~50 optimization events in 7 days to exit learning
- Avoid edits during learning (resets the counter)
- Consolidate ad sets if volume is too low
- "Learning limited" = not enough conversions, consider:
  - Increasing budget
  - Broadening audience
  - Optimizing for an earlier funnel event

### Frequency Management

| Campaign Type | Healthy Frequency | Action If Exceeded |
|--------------|-------------------|-------------------|
| Prospecting | < 2 per week | Expand audience, refresh creative |
| Retargeting | < 4 per week | Tighten windows, new creative |
| Brand awareness | < 3 per week | Cap frequency in campaign settings |

---

## Reporting & Analysis

### Key Metrics to Monitor

| Metric | What It Tells You |
|--------|------------------|
| **CPM** | How much you pay to reach people |
| **CTR** | How compelling your creative is |
| **CPC** | Cost efficiency of clicks |
| **CPA/Cost per result** | Efficiency of conversions |
| **ROAS** | Revenue return on ad spend |
| **Frequency** | How often people see your ad |
| **Hook rate** (video) | % who watch past 3 seconds |
| **Hold rate** (video) | Average % of video watched |

### Attribution Settings

- Default: 7-day click, 1-day view
- Compare to GA4/analytics for ground truth
- Platform will over-report (especially view-through)
- Use UTM parameters on all ad URLs

### Weekly Review Checklist

- [ ] Spend vs. budget pacing
- [ ] CPA/ROAS vs. targets
- [ ] Top 3 and bottom 3 performing ads
- [ ] Frequency check across ad sets
- [ ] Creative fatigue signals
- [ ] Landing page conversion rate
- [ ] Breakdown by placement and device

---

## Common Mistakes

1. **Editing ads during learning phase** — resets optimization, wastes budget
2. **Too many ad sets** — fragments budget, prevents learning
3. **Optimizing for clicks instead of conversions** — cheap clicks rarely convert
4. **Ignoring Conversions API** — losing data to browser restrictions
5. **Not testing creative regularly** — ad fatigue is the #1 performance killer
6. **Audience overlap** — ad sets compete against each other, raising costs
7. **Scaling too fast** — big budget jumps crash performance
8. **Matching broad targeting with weak creative** — algorithm needs strong signals

---

## Task-Specific Questions

1. What platform within Meta are you targeting? (Facebook, Instagram, or both)
2. What's your current pixel data volume? (purchases/leads per week)
3. Do you have Conversions API set up?
4. What's your current best-performing creative format?
5. Are you in a Special Ad Category? (housing, credit, employment, politics)

---

## Tool Integrations

For implementation details, see the [Meta Ads integration guide](../../tools/integrations/meta-ads.md).

For tracking setup, see: [ga4.md](../../tools/integrations/ga4.md), [segment.md](../../tools/integrations/segment.md)

---

## Related Skills

- **paid-ads**: For cross-platform paid advertising strategy
- **analytics-tracking**: For pixel and conversion tracking setup
- **page-cro**: For optimizing landing pages that ads point to
- **copywriting**: For ad copy and landing page copy
- **ab-test-setup**: For testing landing pages and offers
- **email-sequence**: For nurturing leads captured from lead gen campaigns
