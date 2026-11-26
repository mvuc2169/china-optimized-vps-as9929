# China Optimized VPS: What AS9929 Actually Buys You, Which SixtyNet Plan Fits, and What $200 a Year Covers (Full Plan Table + Renewal Math)

SixtyNet's LAX-STARTER is the plan most people searching for a China optimized VPS should buy: 2 cores, 2 GB RAM, 40 GB NVMe, 5 TB of monthly traffic, DDoS protection included, listed at **$200/year against a $240 standard annual rate**. It runs on China Unicom Premium AS9929 out of Los Angeles, and it is the cheapest thing in the lineup that isn't a residential-IP product with ports 80 and 443 closed.

What follows covers three things the sales page doesn't spell out: what AS9929 is actually worth next to CN2 GIA, what that 17% saving means once renewal comes around, and how to avoid buying one of SixtyNet's residential plans by mistake when what you wanted was a web host.

> **Quick pick**
> - **Most readers:** LAX-STARTER, $200/year. 2 cores, 2 GB, 40 GB NVMe, 5 TB/month.
> - **Running a site on ports 80/443:** stay in the LAX series. The residential-IP plans block those ports.
> - **Measured a CPU or traffic ceiling:** LAX-MEDIUM at $800/year, 8 cores and 20 TB/month.
> - **Skip SixtyNet** if you need Hong Kong latency, a published refund window, or documented China Telecom CN2 GIA.
>
> 👉 [Check the LAX-STARTER annual price](https://sixtynet.net/aff.php?aff=39)

## What "China optimized" means, and what it means on this page

The phrase has no technical definition. What matters is the AS number behind it, and there are really five tiers in play.

China Telecom's cheapest transit is **AS4134**, also called ChinaNet or 163. It's inexpensive and heavily loaded, and peak-hour packet loss into mainland China routinely lands in the 20% to 30% range. That's the number behind the frozen video calls and dropped SSH sessions people complain about. **CN2 GT (AS4809 Global Transit)** used to be the upgrade, though since 2019 its congestion has crept close to 163 levels while the price stayed higher. **CN2 GIA (AS4809 Global Internet Access)** is the expensive tier, with transit reportedly quoted as high as $120 per megabit in some markets, which is why a full 1 Gbps commit is a six-figure monthly bill in theory. **CTGNet (AS23764)** is the newest China Telecom option and lands close to GIA on both price and performance.

Outside China Telecom, the names to recognize are **CMIN2 (AS58807)** for China Mobile, **China Unicom Premium (AS10099)**, and **AS9929**, China Unicom's premium backbone.

SixtyNet's product page labels its China routing as China Unicom Premium AS9929, and some configurations carry the line "AS9929 Optimize for China." That's a Unicom-side premium route. It is not CN2 GIA, and nothing on the order page claims it is.

A third-party review of the brand does claim CN2 GIA routing, and separately names AT&T Mobility as the residential IP provider, while more recent coverage identifies Cox Communications instead. Two reviews, two different upstream ISPs, two different China Telecom tiers. When a seller's marketing and a reseller's blog disagree, the AS number on the product page is the only thing you can check. Ask support to confirm in writing which AS paths your traffic takes before you pay, and treat any listing that won't name one as ordinary ChinaNet transit with nicer typography.

## SixtyNet's full lineup

SixtyNet sells three separate things from the same Los Angeles footprint, and only one of them is a normal VPS you can put a website on.

The LAX series is the mainstream product, priced annually with a displayed 17% reduction:

| Plan | Config | Traffic / network | Price | Order |
| --- | --- | --- | --- | --- |
| LAX-STARTER | 2 cores, 2 GB RAM, 40 GB NVMe, 12,500 IOPS | 5 TB/mo, 2G premium network, DDoS protection | $200/yr (list $240) | [Order LAX-STARTER](https://sixtynet.net/aff.php?aff=39) |
| LAX-MICRO | 4 cores, 4 GB RAM, 80 GB NVMe, 12,500 IOPS | 10 TB/mo, 4G premium network, DDoS protection | $400/yr (list $480) | [Order LAX-MICRO](https://sixtynet.net/aff.php?aff=39) |
| LAX-MEDIUM | 8 cores, 8 GB RAM, 160 GB NVMe, 25,000 IOPS | 20 TB/mo, 10G premium network, DDoS protection | $800/yr (list $960) | [Order LAX-MEDIUM](https://sixtynet.net/aff.php?aff=39) |
| LAX-LARGE | 8 cores, 16 GB RAM, 320 GB NVMe, 25,000 IOPS | 40 TB/mo, 10G premium network, DDoS protection | $1,600/yr (list $1,920) | [Order LAX-LARGE](https://sixtynet.net/aff.php?aff=39) |

The second line is the residential-IP series, sold on monthly terms. It's on the same page and easy to buy by accident:

| Configuration | Traffic | Notes |
| --- | --- | --- |
| 2 cores, 2 GB, 40 GB NVMe, 12,500 IOPS | 5 TB/mo | Residential IP |
| 4 cores, 4 GB, 80 GB NVMe, 12,500 IOPS | 10 TB/mo | Residential IP |
| 8 cores, 8 GB, 160 GB NVMe, 25,000 IOPS | 20 TB/mo | Residential IP |
| 16 cores, 16 GB, 320 GB NVMe, 25,000 IOPS | 40 TB/mo | Residential IP |

Two constraints apply to every residential plan. Ports 80 and 443 are closed for IP risk-control reasons, so no public website. And refunds go to your SixtyNet account balance rather than back to your card. A security-focused variant of these plans also rejects all external probes and scans, with access only through a port-forwarding panel and an IP whitelist.

The third item is not a VPS at all. The page also lists a China Unicom Premium AS9929 network product with free BGP session setup, 100M base bandwidth with 3x burst, and 95th-percentile billing at $2,500/year against a $3,000 list rate. That's for announcing your own IP space. Ignore it unless you already know what 95th-percentile billing means for your traffic pattern.

## What the first year costs against the second

Every LAX plan shows two numbers: a struck-through annual rate and a discounted one. The gap is exactly 17%, and SixtyNet doesn't publish what happens at renewal.

| Plan | Year 1 | Year 2 at list rate | Two-year total | Effective monthly, year 1 |
| --- | --- | --- | --- | --- |
| LAX-STARTER | $200 | $240 | $440 | $16.67 |
| LAX-MICRO | $400 | $480 | $880 | $33.33 |
| LAX-MEDIUM | $800 | $960 | $1,760 | $66.67 |
| LAX-LARGE | $1,600 | $1,920 | $3,520 | $133.33 |

If the 17% recurs, a two-year STARTER costs $400 instead of $440. If it doesn't, budget $440 and treat the difference as the real cost of the discount. The gap is $40 a year on the entry plan and $320 on LAX-LARGE, which is enough to matter when you're comparing across providers.

Monthly billing exists on the residential line and is the cheaper way to test the network, but it also forfeits the annual discount. For the LAX series, the annual price is the only one displayed, and there is no published trial.

Worth putting next to it: BandwagonHost's entry CN2 GIA-E plan is listed by third parties at $169.99/year for 1 GB RAM, 20 GB SSD and 1 TB of monthly transfer. SixtyNet's STARTER gives you double the RAM, double the disk and five times the traffic for $30 more per year, on a Unicom premium route rather than a Telecom one. Where SixtyNet loses is on flexibility: BandwagonHost lets you migrate that plan across a long list of datacenters for free, and SixtyNet has one location.

👉 [Start with the $200/year LAX-STARTER](https://sixtynet.net/aff.php?aff=39)

## Which plan fits which job

**A proxy, a personal site, or a small app with Chinese visitors.** LAX-STARTER covers it. 2 GB of RAM handles a LEMP stack and a modest database, 5 TB of monthly traffic is far more than a text-heavy site will use, and the DDoS protection is included rather than a paid add-on. This is the plan that matches the search intent behind "china optimized vps" for most people.

**An e-commerce store or a SaaS app serving mainland users.** Same starting point, but check the port situation first. You want the LAX series, not the residential one. Step up to LAX-MICRO at $400/year once you're running Redis or a heavier PHP stack, since 2 GB gets tight when MySQL, PHP-FPM and a cache all share the box.

**Real-time work: gaming, trading, live collaboration.** Configuration won't fix geography. SixtyNet is Los Angeles only, and the LAX-MEDIUM and LAX-LARGE plans add cores and bandwidth, not lower latency. If sub-50 ms to Shanghai is the actual requirement, you need a Hong Kong box, and those start around $89.99/month from BandwagonHost's Asia line for 2 GB. SixtyNet is the wrong purchase at any tier for that job.

**LAX-LARGE at $1,600/year.** Most readers will never need it. 16 GB of RAM and 40 TB of monthly traffic is a media or download-workload profile, and if you're not pushing that volume today you're paying for headroom you can add later.

## Limits worth knowing before you pay

The LAX plans list DDoS protection as a feature with no mitigation figures attached. Third-party coverage repeats a claim of handling 1000 Gbps of attack traffic, and SixtyNet's own page doesn't quantify it or describe the method. Ask what happens during an attack, specifically whether the response is nullrouting, because on premium China routes that's the usual answer and it takes you offline just as effectively as the attack.

The refund terms are the weaker spot. Residential products refund to account balance only, and no money-back window is published for the LAX plans. If a refund option affects your decision, get it confirmed in a ticket before ordering rather than assuming a 30-day policy exists.

Single location. Every product is in Los Angeles. There's no Hong Kong or Tokyo option to fall back on if the route degrades.

Virtualization is KVM throughout with AMD EPYC hardware, DDR4-3200 memory and NVMe storage, one IPv4 per instance, and no IPv6 on the residential line. Standard Linux installs are self-managed through a client area and a separate port-forwarding panel for the residential products. If you want a managed host that handles setup, this isn't it.

## How it compares

**BandwagonHost** runs CN2 GIA and CTGNet out of Los Angeles DC9 with CMIN2 and China Unicom Premium on the same box, plus Hong Kong and Japan locations, free migration across a long datacenter list, a 99.9% uptime guarantee and a 30-day refund. Entry CN2 GIA-E pricing sits around $169.99/year. Its China routes are not DDoS-tolerant either; attacks get nullrouted.

**DMIT** uses the same AS4809 CN2 GIA backbone with comparable latency to China, and carries a better reputation for handling attacks. Product range is narrower, there's no free migration equivalent, and prices run equal to or above BandwagonHost's premium tiers.

**RackNerd** sells plans under $20/year, and they route to China over ordinary ChinaNet/163. Cheap, but the peak-hour packet loss is the problem you came here to solve.

SixtyNet's position is the middle: Unicom premium routing and generous traffic allowances at annual prices below the CN2 GIA players, with one location and thinner published policy.

## FAQ

**Do I need an ICP license or Chinese real-name verification?**
No. The servers are in Los Angeles, outside mainland filing requirements. SixtyNet's pages don't mention identity verification for these plans; confirm at checkout if that matters to you.

**Can I pay with Alipay or UnionPay?**
The product pages don't list payment methods, and none of the coverage reviewed here confirms Chinese payment gateways. Ordering runs through a standard client area, and the available gateways appear at checkout. If Alipay is a hard requirement, ask before you commit.

**Will the price go up on renewal?**
The 17% is presented as a saving off the annual list rate, and renewal terms aren't published. Budget the list price for year two, and confirm the renewal invoice amount in the client area after your first order.

**What happens if the server gets DDoSed?**
The LAX plans advertise DDoS protection without specifying capacity or method. The residential plans reject external probes and scans by default and only accept whitelisted or port-forwarded traffic. Either way, ask support what the mitigation actually does.

**Hong Kong or Los Angeles?**
Not a choice here. SixtyNet is Los Angeles only. Hong Kong cuts round-trip time to the mainland substantially and costs several times more per month.

## Before you order

Match the plan to the port requirement first: a website on 80/443 means the LAX series, full stop. Then pick by measured load rather than ambition, because LAX-STARTER at $200/year handles a personal site, a proxy, or a small app, and the only reason to move up is a resource ceiling you've actually hit. Anything latency-critical belongs on a Hong Kong box from another provider.

Two things to confirm in a pre-sales ticket: the AS paths your traffic will use, and the refund terms in writing. Both are cheap questions now and expensive assumptions later.

👉 [See SixtyNet's current VPS plans and pricing](https://sixtynet.net/aff.php?aff=39)
