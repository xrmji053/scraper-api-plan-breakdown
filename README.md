# Scraper API Complete Guide: How to Choose a Web Scraping API, Which Plan Fits Your Project, and Is ScraperAPI Worth It? (With Full Plan Breakdown and Real Cost Examples)

If you've ever typed "scraper api" into Google more than once this month, you already know the frustration. Every tool claims to be the easiest, the cheapest, the most reliable — and almost none of them tell you upfront what a single scrape actually costs once you factor in JavaScript rendering, CAPTCHA bypass, or hitting a target like Amazon or LinkedIn. You're not just looking for "an API." You're looking for one that won't quietly burn through your budget the moment a target site turns on bot protection.

That's the gap this article tries to close. We'll walk through what a modern scraper api actually needs to do, how the credit-based pricing model really works (because the headline credit number is rarely the whole story), and where ScraperAPI — one of the most widely used options in this space — fits in. The goal isn't to sell you on anything. It's to give you enough real information to make a decision you won't regret three billing cycles later.

## What You Should Actually Expect From a Scraper API

Before we get into plans and prices, it helps to define what "good" looks like. Most comparison articles skip this part and jump straight to a pricing table, which is why people end up surprised later. A solid scraper api should handle a few things without you having to think about them:

- **Proxy rotation** so a single IP address doesn't get flagged and blocked after a handful of requests. This is table stakes, not a premium feature.
- **JavaScript rendering** for sites that load content dynamically and won't return usable HTML to a plain HTTP request. A lot of modern sites fall into this category.
- **CAPTCHA and anti-bot bypass** for sites running Cloudflare, Datadome, PerimeterX, or similar protection. This is where most cheap APIs quietly fall short.
- **Geotargeting** so you can fetch region-specific pricing, search results, or localized content. If you're doing price comparison or SERP tracking, this matters more than you'd expect.
- **Predictable, usage-based billing** — ideally credit-based rather than flat bandwidth pricing, so you're not penalized for large pages.
- **A free tier or trial** to test integration before committing a credit card.

That's the checklist most people running a "scraper api" comparison search are working from, whether they realize it or not. The reason it matters: a lot of APIs look cheap on the surface because they gate the expensive features (JS rendering, CAPTCHA bypass, geotargeting) behind higher tiers. An entry-level plan that can't actually scrape your real target site isn't cheap — it's wasted money.

## How ScraperAPI Approaches the Problem

ScraperAPI is built around a single-endpoint model. You send a URL, it returns the rendered HTML, and it handles proxy rotation, retries, and anti-bot logic on the backend. Instead of charging by bandwidth, it uses a **credit-based system**, which is one of the more straightforward pricing structures in this space — once you understand how credit costs scale by target difficulty.

Here's the part that actually matters for budgeting, and it's the part most "scraper api" articles get wrong: **not every page costs the same number of credits.**

> A standard page costs 1 credit. Amazon costs 5 credits. Google and Bing (including subdomains) cost 25 credits. LinkedIn costs 30 credits. Sites protected by Cloudflare, Datadome, or PerimeterX add 10 extra credits per request when the bypass succeeds.

That tiered cost structure means a plan with "100,000 credits" doesn't translate to a flat 100,000 page scrapes. It could be 100,000 simple pages, or as few as ~3,300 LinkedIn pulls, depending on what you're actually targeting. There's a Domain Cost Estimator in the dashboard for checking this per-URL, and you can set a `max_cost` parameter per scrape so a single request can't blow past your intended budget.

This is the single most important thing to understand before you compare any scraper api on price alone. The headline credit number is a ceiling, not a guarantee.

### The Parameter Cost Layer

On top of the per-domain cost, certain request parameters add extra credits:

| Parameter | Extra Cost |
| --- | --- |
| `premium=true` | 10 credits/req |
| `render=true` | 10 credits/req |
| `screenshot=true` | 10 credits/req |
| `ultra_premium=true` | 30 credits/req (paid plans only) |
| `premium=true + render=true` | 25 credits/req |
| `ultra_premium=true + render=true` | 75 credits/req (paid plans only) |

Parameters like `country_code`, `session_number`, `device_type`, `output_format`, and `autoparse=true` add no extra cost. So a "simple" scrape of a standard page with `render=true` actually costs 11 credits, not 1. Run that math against your real workload before you commit to any plan.

## Free Trial and Entry-Level Access

For anyone testing whether a scraper api is even the right approach (versus a no-code scraper or a DIY script), ScraperAPI offers a genuinely usable on-ramp:

1. **1,000 free API credits per month**, capped at 5 concurrent connections — enough to validate that your target site can actually be scraped reliably before paying anything.
2. **5,000 free requests during the first 7 days** after signup, for heavier testing.
3. No credit card lock-in required to explore the basic dashboard and Domain Cost Estimator.

If you need more testing volume than that, support can extend additional credits on request — a more flexible policy than tools that hard-cut you off the moment the free tier is exhausted.

👉 [Start with 1,000 free API credits and test against your real targets](https://www.scraperapi.com/?fp_ref=coupons)

## Full Plan Breakdown: Every Tier, Side by Side

This is the section most comparison pages either skip or get wrong by quoting outdated numbers. Based on the most recent pricing data from the official documentation and pricing page, here's the full lineup of ScraperAPI plans, the concurrency limits attached to each, and what they're built for:

| Plan | Monthly Price | Annual Price (per mo) | API Credits / Month | Concurrent Threads | Best For | Get This Plan |
| --- | --- | --- | --- | --- | --- | --- |
| **Free** | $0 | $0 | 1,000 (+5,000 in first 7 days) | 5 | Testing & validation | [Start Free](https://www.scraperapi.com/?fp_ref=coupons) |
| **Hobby** | ~$49 | ~$44 | 100,000 | 20 | Side projects, small scrapers | [Get Hobby](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Startup** | ~$149 | ~$134 | 1,000,000 | 50 | Growing apps, regular scraping jobs | [Get Startup](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Business** | ~$299 | ~$269 | 3,000,000 | 100 | Production workloads, country-level geotargeting | [Get Business](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Professional** | ~$475+ | ~$427 | 5,000,000 | 200 | High-volume scraping, Pay-As-You-Go overflow | [Get Professional](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Enterprise** | Custom | Custom | 10,000,000+ | Custom | Large-scale operations, dedicated account manager | [Request Enterprise Quote](https://www.scraperapi.com/contact-sales?fp_ref=coupons) |

A few notes worth flagging, since pricing pages change without much warning:

- Annual billing consistently saves roughly 10% across every tier compared to paying monthly.
- **Hobby, Startup, and Business** plans don't include Pay-As-You-Go by default — if you exceed your credits, you're prompted to upgrade to the next tier or arrange a custom plan with support.
- **Professional, Advanced, and Enterprise** plans include Pay-As-You-Go, letting you keep scraping past your limit at a fixed per-credit rate, with an optional monthly spending cap so you don't get an unpredictable bill.
- Since prices and credit allotments do get adjusted periodically, it's worth confirming the live numbers on the pricing page itself rather than trusting any single screenshot.

👉 [View current ScraperAPI pricing](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## What's Included on Every Paid Plan

One thing that consistently comes up in third-party reviews: ScraperAPI doesn't gate its core anti-bot features behind the higher tiers. Every paid plan — not just Enterprise — includes:

- Automatic proxy rotation across a large IP pool
- JavaScript rendering for dynamic, JS-heavy pages
- CAPTCHA handling and bypass for common bot-protection systems (Cloudflare, Datadome, PerimeterX, Cloudflare Turnstile)
- Structured/auto-parsed data extraction for select targets like Amazon, Google, and Walmart
- SDKs for Python, JavaScript, Ruby, PHP, and Node.js
- A scheduling tool (called DataPipeline) for recurring scrape jobs, billed at additional credit cost

This matters because some competing scraper api options reserve JS rendering or CAPTCHA bypass for their top-tier plans, which can make an entry-level plan look cheaper on paper while being functionally useless for real-world targets.

### A Quick Python Example

If you're wondering how the integration actually looks, it's about as simple as it gets. The official Python SDK works like this:

python
from scraperapi_sdk import ScraperAPIClient

client = ScraperAPIClient("<API-KEY>")

# regular get request
content = client.get('https://example.com')

# with parameters
content = client.get(
    'https://example.com',
    render=True,            # JS rendering (+10 credits)
    country_code='us',      # geotargeting (no extra cost)
    autoparse=True          # auto-parsed JSON (no extra cost)
)


That's the whole integration. No proxy management, no browser pool, no retry logic on your side. Whether that simplicity is worth the credit cost depends entirely on your project.

## Where ScraperAPI Falls Short

No honest article skips the downsides, so here's what shows up consistently in independent reviews and benchmarks:

- **Entry price isn't the cheapest in the category.** At roughly $49/month for the lowest paid tier, it sits in the same range as competitors like ScrapingBee and Oxylabs rather than undercutting them.
- **Credits don't roll over.** Unused credits at the end of a billing cycle simply expire, so inconsistent usage patterns can mean paying for capacity you don't fully use some months.
- **Geolocation coverage on entry tiers is limited.** Lower plans are generally restricted to US and EU regions, with broader country-level geotargeting reserved for Business tier and above.
- **Reliability has been described as inconsistent by some users** — smooth for stretches, then intermittent timeouts on certain targets. This is a fairly common pattern across the credit-based scraper api category overall, not unique to one provider.

If your use case is highly latency-sensitive or you need broad geolocation coverage on a budget plan, it's worth weighing these tradeoffs against the convenience of the single-endpoint model.

## Real User Reviews: What People Actually Say

Aggregating the public review data tells a fairly consistent story:

- **Trustpilot**: 4.5/5 based on 42+ reviews, with ~93% five-star ratings. Users repeatedly mention ease of setup and reliability on common targets.
- **G2**: 4.4/5 based on 16+ reviews. Praise centers on clean documentation and straightforward API design. Criticism clusters around pricing at scale and occasional timeouts on harder targets.
- **Capterra**: Reviewers highlight the simplicity and reliability for standard scraping needs, with some noting the credit consumption on protected sites can be higher than expected.

A representative positive sentiment from Trustpilot: *"ScraperAPI was extremely easy to use out of the box. We are able to get around website blocks easily."*

A representative critical sentiment from G2: users flagging "pricing issues" and "API limitations" as the main disadvantages, particularly for teams whose credit usage spikes unpredictably when targets add bot protection mid-cycle.

The pattern is clear: people who scrape standard or moderately-protected sites at predictable volume tend to be very happy. People who scrape heavily-protected targets at unpredictable volume tend to feel the credit cost more acutely.

## How to Decide If This Is the Right Scraper API for Your Project

A practical way to filter through the noise:

1. **If you're just testing feasibility** — use the free 1,000-credit tier first. Run your actual target URLs through the Domain Cost Estimator before assuming any plan's credit count will cover your real usage.
2. **If you're scraping mostly standard pages** (blogs, listings, simple product pages) — Hobby or Startup will likely stretch much further than the credit number suggests, since standard pages only cost 1 credit each.
3. **If you're scraping Amazon, Google, Bing, or LinkedIn regularly** — budget accordingly. These targets cost 5–30 credits per request, which eats through lower tiers fast.
4. **If your targets sit behind Cloudflare, Datadome, or PerimeterX** — factor in the +10 credit surcharge per successful bypass, and consider Business or Professional tiers where Pay-As-You-Go protects you from a sudden plan upgrade.
5. **If you're running production infrastructure at scale** — Professional, Advanced, or a custom Enterprise plan will give you the concurrency and PAYG flexibility to avoid getting capped mid-cycle.

## Common Questions About Scraper API

**Is there a free tier?**
Yes. 1,000 API credits per month with 5 concurrent connections, plus 5,000 free requests during the first 7 days after signup. No credit card required.

**Do unused credits roll over?**
No. Credits reset at the start of each billing cycle. If your usage is bursty, this is worth factoring into your plan choice.

**Can I cancel anytime?**
Yes. You can cancel from the dashboard or by contacting support, and there's a 7-day no-questions-asked refund policy on paid plans.

**What happens if I run out of credits mid-cycle?**
On Hobby, Startup, and Business, you're prompted to upgrade or arrange a custom plan. On Professional, Advanced, and Enterprise, Pay-As-You-Go kicks in at a fixed per-credit rate, with an optional spending cap.

**Does it support JavaScript rendering?**
Yes, on every paid plan via the `render=true` parameter. It costs an additional 10 credits per request.

**Which countries are supported for geotargeting?**
US and EU are available on lower tiers. Broader country-level geotargeting opens up at the Business tier and above.

## Final Thoughts

The search for the best scraper api rarely has one universal answer — it depends entirely on what you're scraping, how often, and how sensitive that target is to bot detection. What ScraperAPI does well is make the cost structure transparent enough (via credit weighting and the cost estimator) that you can actually model your spend before committing, and it backs that up with a free tier generous enough to test against your real targets rather than a sanitized demo.

If you've been bouncing between tabs trying to compare scraping APIs on price alone, the more useful move is to actually test the credit cost against your specific target sites first — pricing only tells half the story until you know how many credits your real workload will burn.

👉 [Get 1,000 free API credits and test ScraperAPI against your own targets](https://www.scraperapi.com/?fp_ref=coupons)
