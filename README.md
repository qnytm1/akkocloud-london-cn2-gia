# London CN2 GIA VPS: What AkkoCloud Costs, Which Plan Is Enough, and Where the Spec Sheets Disagree (Full Plan Table + Route Notes)

AkkoCloud's London CN2 GIA plans start at **¥449 a year**, roughly US$5.60 a month averaged out, for a single-core unmanaged KVM box with CN2 GIA return routing to China Telecom, China Unicom and China Mobile. The **¥699 annual plan** (about US$8.71/month) is the one to look at if you want more RAM and around 1.2 TB of monthly traffic. Both are small machines with a UK IP address, and both sit at the cheap end of a London route that holds up during the Asian evening peak.

Below you'll find all eight London plans with prices, the three places where the provider's own pages and third-party listings give different numbers for the same plan, how London compares with the San Jose and Frankfurt nodes on the same network, and the two things worth confirming before you pay.

> **Quick pick**
> - Blog, small WordPress site, monitoring box, proxy endpoint: **¥449/year KVM-CN2-A2 mini** (≈US$5.60/month).
> - A few sites, a small database, more transfer: **¥699/year KVM-CN2-B1 mini** (≈US$8.71/month).
> - Want to test monthly billing first: **from ¥129.99/month**, but that's a larger box at a far higher yearly cost.
> 👉 [See the current London plan list and prices](https://bit.ly/akkocloud)

## All eight London plans, with prices

| Plan | vCPU / RAM | Price | Billing | Order |
| --- | --- | --- | --- | --- |
| KVM-CN2-A2 mini (annual special) | 1 / 768 MB–1 GB | ¥449.00 (≈US$5.60/mo) | Yearly | [Order the ¥449 plan](https://bit.ly/akkocloud) |
| KVM-CN2-B1 mini (annual special) | 1 / 1 GB | ¥699.00 (≈US$8.71/mo) | Yearly | [Order the ¥699 plan](https://bit.ly/akkocloud) |
| KVM-CN2-B1 | 1 / 1.5–2 GB | ¥129.99 (≈US$19.44/mo) | Monthly | [Order KVM-CN2-B1](https://bit.ly/akkocloud) |
| KVM-CN2-B2 | 1 / 2 GB | ¥299.99 (≈US$44.87/mo) | Monthly | [Order KVM-CN2-B2](https://bit.ly/akkocloud) |
| KVM-CN2-C1 | 1 / 2 GB | ¥459.99 (≈US$68.80/mo) | Monthly | [Order KVM-CN2-C1](https://bit.ly/akkocloud) |
| KVM-CN2-D1 | 2 / 4 GB | ¥699.99 (≈US$104.69/mo) | Monthly | [Order KVM-CN2-D1](https://bit.ly/akkocloud) |
| KVM-CN2-E1 | 4 / 8 GB | ¥1,049.99 (≈US$157.04/mo) | Monthly | [Order KVM-CN2-E1](https://bit.ly/akkocloud) |
| KVM-CN2-F1 | 4 / 8 GB | ¥1,399.99 (≈US$209.38/mo) | Monthly | [Order KVM-CN2-F1](https://bit.ly/akkocloud) |

Prices are in CNY; the USD figures are monthly averages converted from the listed cycle, not a payment currency. B2, C1, E1 and F1 look identical on paper in places because they're separated by traffic quota rather than by CPU, so read the next table before picking.

## Storage, traffic and port speed

| Plan | SSD | Monthly traffic (counted in both directions) | Port |
| --- | --- | --- | --- |
| KVM-CN2-A2 mini | 15 GB | 800 GB | Listed as 1 Gbps |
| KVM-CN2-B1 mini | 20 GB | 1.2 TB | Listed as 1 Gbps |
| KVM-CN2-B1 | 20 GB | 1.5 TB | Listed as 1 Gbps |
| KVM-CN2-B2 | 30 GB | 3 TB | Listed as 1 Gbps |
| KVM-CN2-C1 | 30 GB | 4 TB | Listed as 1 Gbps |
| KVM-CN2-D1 | 40 GB | 6 TB | Listed as 1 Gbps |
| KVM-CN2-E1 | 60 GB | 9 TB | Listed as 1 Gbps |
| KVM-CN2-F1 | 60 GB | 12 TB | Listed as 1 Gbps |

Traffic is counted bidirectionally, so 800 GB a month means about 400 GB up and 400 GB down. Budget accordingly if you're serving images or video.

The annual specials are a different product class from the monthly plans, not the same box at a discount. KVM-CN2-B1 bills at ¥129.99 a month, which is ¥1,559.88 over a year. The ¥699 B1 mini annual is less than half that, and it's also smaller: 1 GB of RAM instead of 1.5–2 GB, and 1.2 TB of traffic instead of 1.5 TB. The ¥449 A2 mini costs roughly what three and a half months of the cheapest monthly plan would, which is why most people who only need a UK foothold stop there.

## Three sources, three different spec sheets

This is the part that trips people up when they compare London CN2 GIA VPS listings across sites. The same ¥449 plan shows different numbers depending on where you look.

**Memory on the ¥449 plan.** The provider's homepage plan card and a directory listing verified against the official site in late October both say **768 MB**. A third-party plan table and the London order page both say **1024 MB**. Same plan code, two answers.

**Port speed.** Four figures are in circulation for the same plan family: **300 Mbps** (homepage card and directory listing), **500 Mbps** (a 2026 review of the London plans), and **1 Gbps** (third-party plan table and the order page). A 2022 review mentioned 300 Mbps as the starting point, which was accurate then and may not be now.

**A ¥299/year London plan.** One review lists a 512 MB London starter at ¥299/year. It doesn't appear in the current London list from either the order page or the directory snapshot, both of which start at ¥449. It may be an older promotion, a different location, or a stale figure. Don't plan a purchase around it.

None of this is sinister. Promo pages get updated at different speeds, and plan cards sometimes lag behind the cart. The practical answer is the same in every case: **the cart shows the configuration you're actually buying**, and that's the number that governs what gets provisioned and what you can complain about later.

👉 [Open the London plan list and check the live configuration](https://bit.ly/akkocloud)

## London vs San Jose vs Frankfurt

All three AkkoCloud locations ride CN2 back toward China, and all three advertise three-network return routing. The difference is geography and how much latency that adds.

| Location | Reported latency to mainland China | Best for |
| --- | --- | --- |
| San Jose (US West) | 160–170 ms | Chinese visitors, cross-border APIs, anything where China is the primary audience |
| Frankfurt | ~180 ms | European users, with a China route that beats a generic EU host |
| London | ~200 ms (review figure) | UK presence, EU customers, UK-specific testing |

The San Jose and Frankfurt figures come from user reports collected in a review; the London figure is from a separate review and is the least corroborated of the three. For reference, a generic European VPS typically lands around 230 ms to China, so London's advantage over a random UK host is real but modest, on the order of 30 ms. If your audience is in Shanghai and nowhere else, buy San Jose. London is for when you need the UK endpoint and want China access to not be terrible.

If you want to test before buying, San Jose publishes 45.9.10.146 as a test IP, and the London Looking Glass node responds on 185.217.110.10. The London product page is explicit that test IPs don't represent the address you'll be assigned.

Routing detail from the provider's own 2022 description of the London node: **three-network return via CN2 GIA, with Telecom and Unicom outbound also on GIA**. Return-path GIA doesn't mean every hop in both directions is GIA, and if full bidirectional GIA on Unicom matters to you, that's a question to put to another provider.

## Who this fits, and who should look elsewhere

The hardware is AMD EPYC with SSD in RAID10, and single-core Geekbench 6 scores reported around 1100–1200. That's fine for WordPress, small APIs, bots and light databases. It is not fine for anything CPU-bound: seven of the eight plans are single-core, so single-thread performance is the whole story.

Every plan is unmanaged. You handle patching, updates, hardening and backups. The control panel covers OS reinstall, reboot and bandwidth graphs, and that's about it; there's no library of one-click installers, and documentation leans Chinese. If you need a managed stack or a hand-held first server, this is the wrong product regardless of price.

Routing benefits vary by carrier. Telecom users get the most consistent result; Unicom and Mobile get optimized return paths but fluctuate more. A directory that tracks the brand rates it 3.9/5 and states plainly that the score is the directory's own, not an average of user reviews, so treat it as a rough signal rather than a verdict.

## Payment, support and the refund question

Alipay is the primary payment route and is confirmed on the provider's own pages. PayPal appears in two independent write-ups as an option for international buyers, but another review says Alipay only. If paying by PayPal is a hard requirement, confirm at checkout before you commit.

Provisioning usually happens within hours of payment, sometimes faster. Support runs on tickets plus a Telegram community, in Chinese. The published commitment is a reply within 24 hours and resolution within 48, during business hours listed as 12:00 to 22:00, so a 3am failure waits until morning.

Refunds are the item most worth reading twice. The London product page states that the terms of service do not allow refunds, and explicitly rules out refund requests on the grounds that the assigned IP isn't native. No trial period or money-back window appears anywhere in the public material. If trying before committing matters to you, the quarterly and monthly options are the only soft landing available.

## AkkoCloud vs MoeCloud on the London route

MoeCloud runs a comparable London CN2 GIA product, and it's the name that comes up most often in the same searches. Both listings below are as published; neither is a recommendation to go elsewhere.

|  | AkkoCloud London | MoeCloud London |
| --- | --- | --- |
| Entry annual price | ¥449/year | ¥299/year in one write-up, ¥499/year in a later one for what looks like the same 512 MB plan |
| Entry configuration | 768 MB–1 GB, 15 GB SSD, 800 GB traffic | 512 MB, 10 GB SSD, 0.5 TB traffic |
| Telecom / Unicom outbound | CN2 GIA (2022 provider statement) | CN2 GIA both directions |
| Return routing | All three networks via CN2 GIA | All three networks via CN2 GIA |
| Plan flexibility | No upgrade or traffic-reset restrictions stated on the published plan pages | Special plans cannot be upgraded; traffic cannot be reset |
| Streaming unlock | Not advertised | Not guaranteed, though the UK node tested as working |

Two differences matter for a buying decision. MoeCloud's published routing is stronger on outbound for Telecom and Unicom, since it claims GIA in both directions rather than on the return leg. AkkoCloud's entry plan gives you more RAM and more traffic for the money, and its plan pages don't carry the no-upgrade, no-traffic-reset clause. That's an absence of a stated restriction, not a promise that upgrades are available; ask support if you think you'll grow into a bigger box.

## FAQ

**Can I pay with Alipay or PayPal?**
Alipay, yes. PayPal is listed by two sources and contradicted by one. Check the payment step before you fill the cart.

**How quickly is the server online?**
Usually within hours of payment, occasionally faster. Nothing is instant-provisioned in the way a big cloud provider is.

**Is the IP native?**
Not guaranteed, and the London page says so directly. Don't buy this expecting a clean UK residential-grade IP for streaming services.

**Can I get a refund?**
The London product page states the terms of service don't allow refunds. Ask support in writing before paying if you need an exit option.

**Will the renewal price jump?**
No public renewal pricing exists in any source I could verify. The annual specials are the discount mechanism, and no working promo codes are circulating, so the listed price is the discount. Confirm the renewal line in the cart before checkout.

**Can I install Windows or a control panel?**
It's KVM, so an OS reinstall is one click, but with 768 MB to 1 GB of RAM on the entry plans, Windows Server isn't realistic. Anything above a basic panel install is your own work.

**Which plan for two small WordPress sites?**
The ¥699 annual. 1 GB of RAM and 1.2 TB of traffic leaves room for a database and a bit of headroom, and it's still under US$9 a month.

## What to do next

Match the plan to what you're actually running:

- One site, a bot, a proxy, or a dev box with a UK IP: **¥449/year**, and don't pay for more.
- Two or three sites, or more than 800 GB of monthly transfer: **¥699/year**.
- You need 2 cores and 4 GB: KVM-CN2-D1 at ¥699.99/month. At that monthly rate, the annual specials stop looking like the obvious answer and you should sanity-check what else that budget buys.
- Your users are in Germany, not the UK: buy the Frankfurt node instead. The London premium buys geography, not a better route.

Before paying, confirm two things in the cart: the RAM and port speed displayed for the exact plan you selected, since the published numbers differ by source, and the renewal price and refund terms attached to that plan code.

👉 [Compare the London annual specials and pick a plan](https://bit.ly/akkocloud)
