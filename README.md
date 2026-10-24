# ScrapingBee Pricing: What Each Plan Really Costs, the Credit Multipliers Nobody Mentions, and a ScraperAPI Alternative to Compare First

ScrapingBee's pricing starts at **$19/month for the Hobby plan** and tops out at **$599/month for Business+**, with a $99 Startup plan in the middle that most growing projects land on. That's the short version. The longer version matters more: those numbers are for *API credits*, and one credit only covers a plain, no-JavaScript fetch. Turn on JavaScript rendering and the same credits buy you five times fewer pages. If you're searching for ScrapingBee's pricing because you're budgeting a scraping project, the sticker price alone will mislead you by a factor of 5 to 75.

This article walks through every plan, converts credits into actual pages, flags the limits that only show up in the documentation, and compares the numbers against ScraperAPI, another credit-based scraping API you should have on the same spreadsheet.

> **Quick take:** If you're scraping simple, JavaScript-free pages, ScrapingBee's Hobby plan at $19/month for 75,000 credits is a cheap way to test the waters. If your targets need rendering or sit behind anti-bot systems, do the math on real per-page cost first — and check ScraperAPI's pricing alongside it, since its plans bundle JS rendering and premium proxies into every tier. 👉 [Check ScraperAPI's current plans and pricing](https://www.scraperapi.com/pricing?fp_ref=coupons)

## ScrapingBee's Plans and Prices

ScrapingBee publishes five self-serve plans on its pricing page, all billed monthly, all priced in USD, and all listed excluding VAT. Here's the full lineup as shown on the official page:

| Plan | Monthly Price | API Credits | Concurrent Requests |
| --- | --- | --- | --- |
| Hobby | $19 | 75,000 | 25 |
| Freelance | $49 | 250,000 | 50 |
| Startup | $99 | 1,000,000 | 100 |
| Business | $249 | 3,000,000 | 200 |
| Business + | $599 | 8,000,000 | 400 |

Above Business+, ScrapingBee offers Enterprise plans by quote. The pricing page also advertises a **1,000 free API credit trial** with no credit card required, and a "cancel anytime, no questions asked" policy.

One thing the pricing page doesn't show: an annual billing option. Unlike several competitors, ScrapingBee's public pricing page lists monthly prices only — there's no displayed yearly discount to factor in, and no discount codes are promoted beyond the free trial credits.

## The Credit Multiplier: Why 75,000 Credits Isn't 75,000 Pages

This is the part most pricing summaries skip, and it changes which plan makes sense. ScrapingBee charges different credit rates depending on how hard the request is:

- Plain fetch (datacenter proxy, no rendering): **1 credit**
- JavaScript rendering: **5 credits**
- Premium proxy: **10 credits**
- Premium proxy + rendering: **25 credits**
- Stealth proxy (for heavily defended sites): **75 credits**

Since JavaScript rendering is the setting most scraping jobs leave on, the practical page counts look like this:

| Plan | Credits | Rendered Pages (at 5 credits) | Cost per 1,000 Rendered Pages |
| --- | --- | --- | --- |
| Hobby | 75,000 | 15,000 | $1.27 |
| Freelance | 250,000 | 50,000 | $0.98 |
| Startup | 1,000,000 | 200,000 | $0.50 |
| Business | 3,000,000 | 600,000 | $0.42 |
| Business + | 8,000,000 | 1,600,000 | $0.37 |

So the $19 Hobby plan gets you roughly 15,000 rendered pages a month, and the $49 Freelance plan gets you 50,000. If you estimated your budget off the raw credit numbers, you're off by 5x.

The multipliers bite harder at the top end. Routing a request through the Stealth proxy costs 75 credits, which means the entire Hobby plan's monthly allowance covers about **1,000 stealth requests** — effectively $19 per 1,000 requests for hard targets. On Business+ the same request type costs $5.62 per 1,000. If heavy anti-bot sites are your main use case, the entry plans won't survive contact with them.

> If your targets are Amazon, Google, or Walmart, note that ScrapingBee's dedicated endpoints have their own rates: Google costs 15 credits per request, Amazon 5–15, Walmart 10–15, YouTube 5. The Startup plan and above also includes an Agentic Search API at a flat 3,750 credits per call — on Hobby that's only 20 calls a month.

## Which ScrapingBee Plan Actually Fits Your Volume

Per-credit cost drops in steps, not smoothly, and one step is notably better than the others. Upgrading from Freelance to Startup costs $50 more per month but buys 750,000 additional credits at a marginal rate cheaper than even the Business+ plan's average price — the steepest value jump in the whole ladder.

There's a catch, though: the Startup plan only beats Freelance on effective per-credit cost once you use more than roughly **505,000 credits a month** (about 101,000 rendered pages). Below that threshold, the $49 Freelance plan is the smarter spend, and the $99 upgrade is just buying headroom.

A few rules of thumb based on the verified numbers:

- **Under ~15,000 rendered pages/month:** Hobby at $19 covers it, with nothing to spare.
- **~15,000–50,000 rendered pages/month:** Freelance at $49 is the practical entry point. Scrapeway's independent review put it bluntly: the $49 tier works out to about $0.30 per 1,000 credits, which isn't competitive until you climb higher.
- **Over ~101,000 rendered pages/month:** Startup at $99 wins on rate; Business and Business+ are for teams that need 200+ concurrent requests or steady high-volume rendering.
- **Heavy stealth-proxy work:** budget from Startup up; Hobby's allocation runs dry after about a thousand stealth requests.

Also worth knowing before you commit: per a third-party analysis of ScrapingBee's credit policy, failed requests aren't billed (successful attempts get 30 seconds of retries), but **credits don't roll over** to the next month — unused allowance expires at each billing cycle. One independent reviewer (Scrapeway) has also observed blocked requests occasionally being charged, which differs from the official "only successful requests are billed" policy; treat the official policy as the promise and the review as a data point from real usage.

## ScraperAPI's Plans: The Other Credit System to Put Next to ScrapingBee

Since you're pricing out a scraping API, ScraperAPI deserves a spot on the same comparison, partly because its entry point and billing quirks differ in ways that matter. ScraperAPI runs on credits too, but its plans bundle JavaScript rendering, premium residential and mobile proxies, CAPTCHA handling, and automatic retries into **every tier** — there's no per-feature credit multiplier to track.

| Plan | Monthly | Annual (per month) | API Credits | Concurrent Requests |
| --- | --- | --- | --- | --- |
| Hobby | $49 | $44.10 | 100,000 | 20 |
| Startup | $149 | $134.10 | 1,000,000 | 50 |
| Business | $299 | $269.10 | 3,000,000 | 100 |
| Scaling | $475 | $427.50 | 5,000,000 | 200 |
| Professional | $975 | $877.50 | 10,500,000 | 300 |
| Advanced | $1,975 | $1,777.50 | 21,500,000 | 500 |
| Enterprise | Custom | Custom | 22,000,000+ | 500+ |

Every paid plan carries a **10% discount on annual billing**, and ScraperAPI's all-in feature set means 99.9% uptime, unlimited bandwidth, custom headers and sessions, and geo-targeting come standard. Its proxy pool spans 40M+ IPs across 50+ countries, and the company reports serving over 11 billion requests in the past 30 days for 10,000+ companies.

The trade-off shows up in the credits-per-site math. A standard page costs 1 credit, but Amazon pages cost 5, Google and Bing cost 25, LinkedIn costs 30, and bypassing Cloudflare, Datadome, or PerimeterX protection adds 10 credits per request. Unlike ScrapingBee's parameter-based multipliers, ScraperAPI's pricing is domain-based — and it hands you tools to manage it: a Domain Cost Estimator in the dashboard shows the exact cost of any URL before you scrape it, and a `max_cost` parameter caps what any single request can burn.

Overage handling is also more forgiving than pausing and waiting: if you exceed your plan, requests come back with a 429 and no extra charge. Hobby, Startup, Business, and Scaling plans can opt into auto-upgrade to bump you to the next tier automatically when credits run out; Scaling and above can switch to pay-as-you-go at a fixed per-credit rate with a monthly cap you set.

If you'd rather test before picking a tier, ScraperAPI offers a **7-day trial with 5,000 credits, no credit card required**, plus a free plan with 1,000 credits at 5 concurrent connections. 👉 [Start the free 7-day ScraperAPI trial](https://www.scraperapi.com/signup?fp_ref=coupons)

## ScrapingBee vs. ScraperAPI: Side by Side

Here's how the two stack up on the dimensions that drive real cost, based on current official pricing pages. (ScrapingBee's own plans have no links here; only ScraperAPI entries are clickable.)

| Dimension | ScrapingBee | ScraperAPI |
| --- | --- | --- |
| Entry plan | $19/mo, 75,000 credits | $49/mo, 100,000 credits |
| Mid plan | $99/mo, 1M credits | $149/mo, 1M credits |
| JS rendering | 5 credits per request | Included on all plans |
| Premium/residential proxies | 10 credits per request | Included on all plans |
| Annual discount | Not displayed on pricing page | 10% off |
| Free trial | 1,000 credits, no credit card | 7-day trial, 5,000 credits, no credit card |
| Unused credits | Expire monthly | Annual plans can renew early for a fresh batch |
| Anti-bot bypass cost | Stealth proxy: 75 credits/request | +10 credits/request on protected sites |
| Cost transparency | Parameter-based multipliers | Per-domain cost table + max_cost cap |

What does this mean in practice? At the ~1M-credit level, ScrapingBee is $99 versus ScraperAPI's $149 monthly ($134.10 annual) — but ScrapingBee's credits only stretch that far if you keep rendering and premium proxies off. ScraperAPI's higher sticker price buys predictable per-page costs and no feature-based multipliers. For pure low-volume, no-render fetching, ScrapingBee's $19 Hobby is cheaper than anything ScraperAPI sells. For rendering-heavy workloads on moderately protected sites, run both through the per-page math for your specific target list before deciding — the winner flips depending on which domains you hit.

## What Independent Benchmarks Say

Independent test data is thin in this space, so the Scrapeway benchmark (September 2026, 11 target sites, 7 APIs) is worth a look — with the caveat that it's one tester's methodology and mostly measures tough, anti-bot-heavy targets.

In that benchmark, ScrapingBee scored a **33% overall success rate**, ranking 6th of 7, with an average response time of 2.8 seconds (well ahead of the 9.3s field average) and a cost of $1.51 per 1,000 requests (versus a $2.80 average). ScraperAPI scored **52% success**, 7.5 seconds average, at $4.05 per 1,000 requests. Neither led the field — Scrapfly topped it at 98% success but at $3.14 per 1,000 and 17.8 seconds. On target-specific results, ScrapingBee managed 29% on Amazon (at a low $0.31 per 1,000) and 18% on Booking.com.

Read together: in this benchmark, ScraperAPI succeeded more often but charged more per attempt; ScrapingBee was cheaper and faster but failed more often. Since ScrapingBee doesn't bill failed requests, the effective cost of *delivered* data can narrow that gap. Neither API is the pick if raw success rate on hostile targets is your only KPI, and benchmark conditions won't match every site on your list. On user reviews, ScrapingBee holds a 4.9 rating on Capterra (137 reviews); ScraperAPI's Capterra rating is 4.6 (62 reviews).

## FAQ

**Does ScrapingBee offer a discount code or annual plan?**
The official pricing page currently shows monthly pricing only, with no annual billing option or promo codes beyond the 1,000 free trial credits. Anyone claiming a ScrapingBee discount code beyond the trial is not pointing at something the pricing page supports.

**Do failed requests cost credits on either service?**
ScrapingBee's official policy: only successful requests are billed, with automatic retries built in. ScraperAPI's approach: requests over your concurrency limit return a 429 with no charge. Independent reviewers have occasionally observed blocked ScrapingBee requests being charged, so monitor your credit usage after the first billing cycle.

**What happens when I run out of credits?**
On ScrapingBee, scraping pauses until the next billing cycle unless you upgrade. On ScraperAPI, you can opt into auto-upgrade (Hobby through Professional) or pay-as-you-go overage (Scaling and above), and annual plans can renew early for a fresh batch of credits.

**Which is cheaper for Amazon scraping specifically?**
ScrapingBee's Amazon endpoint runs 5–15 credits per request, which on a $99 Startup plan works out to roughly $0.50–$1.50 per 1,000 requests. ScraperAPI charges a flat 5 credits per Amazon page, so 1M credits covers about 200,000 Amazon pages at $149 monthly. For high-volume Amazon work, ScraperAPI's flat rate is easier to budget; verify current rates on both pricing pages before committing, since endpoint pricing changes periodically.

## Before You Subscribe

Match the plan to your actual request profile, not to the headline credit number. If you're pulling plain HTML from friendly sites in low volume, ScrapingBee's $19 Hobby plan is the cheapest credible entry point in this pairing, and its 1,000 free credits will tell you quickly whether your targets cooperate. If you need JavaScript rendering or premium proxies on every request — which describes most commercial scraping — ScraperAPI's bundled pricing and annual discount (Startup at $134.10/month billed annually) tend to produce fewer billing surprises, and the 7-day trial lets you benchmark your real targets before paying anything.

Two checks before checkout: confirm your target domains' credit costs using ScraperAPI's Domain Cost Estimator, and set a monthly credit ceiling so a misconfigured crawler can't eat a whole plan in an afternoon. 👉 [Compare ScraperAPI plans and lock in the 10% annual discount](https://www.scraperapi.com/pricing?fp_ref=coupons)
