# Meta Ads Audience Strategy

Detailed audience targeting strategies for Meta advertising campaigns.

## Prospecting Audience Tiers

Build your prospecting strategy in tiers, from broadest to most targeted:

### Tier 1: Broad Targeting

**Setup:** Age, gender, and geography only. No interests or behaviors.

**Why it works:**
- Meta's algorithm is highly effective at finding converters within large pools
- Avoids the "targeting tax" of overly narrow audiences
- Best when you have strong creative and 50+ weekly conversions

**Requirements:**
- Minimum $50/day budget per ad set
- Well-optimized pixel with conversion history
- Strong, scroll-stopping creative

**When to avoid:**
- New ad accounts with no pixel data
- Very niche B2B products
- Budget under $30/day

### Tier 2: Lookalike Audiences

**Best source audiences (in order):**
1. Purchasers/subscribers (highest LTV first)
2. Add-to-cart or initiate-checkout users
3. Lead form completions
4. Email subscribers (engaged segment)
5. Website visitors (specific high-intent pages)

**Size recommendations:**
| Size | Reach | Best For |
|------|-------|----------|
| 1% | ~2.3M (US) | Highest quality, limited budget |
| 1-3% | ~4.6M (US) | Best balance for most advertisers |
| 3-5% | ~4.6M (US) | Scaling when 1-3% is saturated |
| 5-10% | ~11.6M (US) | Broad prospecting, awareness |

**Lookalike stacking:**
- Test multiple source audiences separately first
- Combine winning lookalikes into a single ad set for consolidation
- Exclude the source audience from each lookalike

**Refreshing lookalikes:**
- Re-upload customer lists monthly
- Pixel-based lookalikes update automatically
- Performance often improves as the source audience grows

### Tier 3: Interest-Based Targeting

**Building effective interest stacks:**

1. **Identify core interests** — direct competitors, industry tools, thought leaders
2. **Find adjacent interests** — related topics your audience also cares about
3. **Stack with AND logic** — interest A AND interest B for precision
4. **Test interest groups separately** — don't mix too many in one ad set

**Interest research methods:**
- Meta Audience Insights tool
- Competitor analysis (who do they follow/engage with?)
- Customer surveys ("What tools/publications do you use?")
- Industry publications and conferences

**Common interest stacks by business type:**

| Business | Stack Example |
|----------|--------------|
| B2B SaaS | Industry software + Business publications + Job titles |
| E-commerce | Product category + Related hobbies + Shopping behaviors |
| Online education | Topic interest + Self-improvement + Related career skills |
| Local business | Geographic + Life events + Relevant interests |

---

## Custom Audiences

### Website Custom Audiences

| Audience | Window | Size | Use For |
|----------|--------|------|---------|
| All visitors | 180 days | Largest | Broad retargeting, LAL source |
| All visitors | 30 days | Medium | Active retargeting |
| Key page visitors | 30 days | Smaller | High-intent retargeting |
| Purchase/signup page | 7 days | Smallest | Hot retargeting |
| Time on site (top 25%) | 30 days | Medium | Engaged visitor retargeting |
| Frequency (3+ visits) | 30 days | Small | High-intent |

**Tips:**
- Create overlapping windows for funnel segmentation
- Use URL contains rules for page categories (e.g., `/pricing`, `/blog`)
- Combine with event-based audiences for precision

### Engagement Custom Audiences

| Source | Engagement Type | Window | Notes |
|--------|----------------|--------|-------|
| Facebook Page | Any engagement | 365 days | Broad, good for LALs |
| Instagram | Any engagement | 365 days | Often higher quality than FB |
| Video | 25% watched | 365 days | Showed initial interest |
| Video | 75% watched | 365 days | Highly engaged, great for LALs |
| Lead form | Opened | 90 days | Intent signal |
| Lead form | Submitted | 90 days | Converted lead, exclude or upsell |

### Customer List Audiences

**Maximizing match rate:**
- Include email AND phone number (match rate jumps from ~40% to ~60%+)
- Use the same email format customers use for Facebook
- Include first name, last name, city, state, zip for better matching
- Hash data before upload (Meta does this automatically, but pre-hashing improves privacy compliance)
- Minimum 1,000 records recommended, 5,000+ ideal

**Segmentation ideas:**
- High-LTV customers (top 20% by revenue)
- Recent purchasers (last 90 days)
- Churned customers
- Free trial users who didn't convert
- Email subscribers by engagement tier

---

## Retargeting Architecture

### Simple Retargeting Setup

For businesses spending $1K-5K/month:

```
Campaign: Retargeting
├── Ad Set: All site visitors (1-30 days)
│   ├── Exclude: Purchasers/converters
│   └── Creative: Mix of social proof, features, objections
└── Ad Set: Engagers (1-60 days)
    ├── Include: Video viewers, page engagers, IG engagers
    ├── Exclude: Website visitors, purchasers
    └── Creative: Introduce product, drive to site
```

### Advanced Retargeting Setup

For businesses spending $5K+/month:

```
Campaign: Retargeting - Hot
├── Ad Set: Cart abandoners (1-7 days)
│   └── Creative: Reminder, incentive, urgency
├── Ad Set: Key page visitors (1-14 days)
│   └── Creative: Testimonials, case studies
└── Ad Set: Trial users not converted (ongoing)
    └── Creative: Feature highlights, upgrade benefits

Campaign: Retargeting - Warm
├── Ad Set: All site visitors (8-30 days)
│   └── Creative: Social proof, differentiation
└── Ad Set: Video viewers 50%+ (1-30 days)
    └── Creative: Deeper value prop, demos

Campaign: Retargeting - Cold Re-engagement
└── Ad Set: Past visitors (31-90 days)
    └── Creative: What's new, fresh angles
```

### Retargeting Creative Strategy

| Funnel Stage | Message Type | Example |
|-------------|-------------|---------|
| Awareness (engaged) | Education + brand | "Here's how [product] works" |
| Consideration (visited) | Social proof | "Join 5,000+ teams using..." |
| Intent (key pages) | Objection handling | "No credit card required" |
| Decision (cart/trial) | Urgency + incentive | "Your trial ends in 3 days" |

---

## Audience Overlap & Exclusions

### Checking for Overlap

Use Meta's Audience Overlap tool:
1. Go to Audiences in Ads Manager
2. Select 2-5 audiences
3. Click "Show Audience Overlap"

**Acceptable overlap:** Under 20%
**Concerning overlap:** 20-40% — consider merging
**Problematic overlap:** 40%+ — merge audiences or add exclusions

### Exclusion Hierarchy

Always exclude in this order:
1. Existing customers/purchasers (from all prospecting)
2. Leads/form submitters (from lead gen prospecting)
3. Retargeting audiences (from prospecting campaigns)
4. Higher-intent audiences (from lower-intent ad sets)

**Example for prospecting campaign:**
- Broad ad set: exclude LAL audience + retargeting audiences + customers
- LAL ad set: exclude retargeting audiences + customers
- Interest ad set: exclude LAL audience + retargeting audiences + customers

---

## iOS 14+ Considerations

### Impact
- Reduced audience sizes for website custom audiences
- Delayed reporting (up to 72 hours)
- Limited to 8 conversion events per domain
- View-through attribution window reduced to 1 day
- Estimated results may differ from actual

### Mitigation
- Set up Conversions API (critical)
- Verify your domain in Business Manager
- Prioritize your 8 events carefully (put Purchase/Lead at top)
- Use broader audiences (larger pools offset tracking loss)
- Lean into on-platform engagement audiences (not affected)
- Use lead gen forms (on-platform, no tracking loss)
- Monitor in-platform metrics alongside GA4 for cross-reference
