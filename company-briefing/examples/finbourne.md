# FINBOURNE Technology — Briefing
*As of 9 Nov 2026 · Cloud data platform for investment managers (LUSID) · Not AI-native: an established fintech now adding AI agents on top*

## TL;DR
- Builds **LUSID**, a cloud "single source of truth" for an investment firm's holdings, trades and valuations. It replaces old in-house and legacy systems at asset managers, pension funds and wealth firms.
- **Revenue is much smaller than data sites claim.** Figures drawn from its UK filings show **~£23.5M turnover (year to Dec 2025)**. Aggregators guess $47–100M.
- **Funding:** $70M (£55M) Series B in Jun 2024, led by Highland Europe and AXA Venture Partners; LSEG and Fidelity International are strategic investors. Valuation is undisclosed (estimates ~£320–400M).
- **Moat:** owns its core data engine, and once installed as a firm's system of record it's very hard to rip out. But it's small next to giants like BlackRock Aladdin, SimCorp and Clearwater.
- **Biggest risks:** thin balance sheet (negative net assets, ~£6M cash at end-2025, aiming for profit in 2026); headcount down ~25% from its 2024 peak (est.); weak employee reviews (Glassdoor 3.0/5).
- **Asia-Pacific = Australia so far.** AustralianSuper (A$438B) went live in Oct 2026. There's a Singapore hub with a regional sales head, but no named Asian client.

## Snapshot
| | |
|---|---|
| Founded | 2016 |
| Founders / CEO | Thomas McHugh (CEO; ex-quant/tech lead at RBS, UBS, Morgan Stanley); co-founders include Benedict Nielsen and Dermot Shortt (sources say 3–7 co-founders) |
| HQ | London |
| Other offices | Dublin, New York, Singapore, Sydney, Brisbane |
| Employees | ~235 (2025, Revelio est.), down from a ~318 peak in 2024; PitchBook ~230 |
| Stage | Private (UK company no. 10539696) |
| Latest primary round | **Series B, $70M (£55M), Jun 2024**, led by Highland Europe and AXA Venture Partners |
| Latest valuation mark | Not disclosed. Estimates: £317M (Tracxn) to ~$400M (Caplight) |
| Total raised | ~$107–186M equity (sources differ) + £30M debt facility from Kreos (Jan 2023) |
| Revenue | 🟡 **~£23.5M turnover, 12 months to 31 Dec 2025** (Endole, from Companies House filings). Aggregator estimates of $47–100M look wrong. |
| Balance sheet | 🟡 Cash ~£6.2M; total assets £28.4M vs liabilities £39.6M → **net assets about –£11.2M** (Dec 2025) |

## What it does
Investment firms hold data about their portfolios in many disconnected systems: trading, accounting, risk, custodians. FINBOURNE's LUSID pulls it all into one cloud platform with a full history of every change ("bitemporal" — you can see what the books said on any past date, and what you knew at the time). Clients use it as their official book of record and build reporting, analytics and now AI agents on top.

| Product | What it does | Who buys |
|---|---|---|
| **LUSID** | Cloud investment book of record: positions, transactions, valuations, accounting views, full audit trail; API-first | Asset managers, pension/super funds, insurers, wealth managers |
| **Luminesce** | Query and combine data across LUSID and other systems without moving it | Data and ops teams |
| **AI agents (Candela agentic layer)** | 30+ ready-made agents for investment operations; connects to Anthropic's Claude via MCP; agents have the same permissions and audit log as humans | Ops teams; 7 clients in production (Sep 2026) |
| **Yield Book in LUSID** (with LSEG) | LSEG's fixed-income analytics run inside LUSID (launch Q2 2026) | Fixed-income managers |
| Implementation / forward-deployed engineers | Help clients migrate and build solutions | All clients |

## How it makes money
- **SaaS subscriptions** on multi-year enterprise contracts (pricing private; also sold through AWS Marketplace).
- **Implementation and services** for migrations, which often take months to years.
- **Partner / embedded revenue:** LSEG uses LUSID inside its own wealth and investment products (since 2021).
- Customer types: asset managers (Baillie Gifford, Fidelity International, Seilern, TT International), asset owners (Railpen, AustralianSuper), insurers (Pension Insurance Corporation), market-data firms (LSEG, Thomson Reuters).

## Biggest revenue stream
**LUSID subscriptions from large investment firms.** No split is disclosed. The LSEG relationship is likely one of the largest single accounts, since it is client, partner and investor in one *(analysis)*. Turnover reportedly jumped sharply in 2025, but the prior-year comparison in the filings is unclear (may be a short accounting period).

## Funding & backers
| Round | Date | Amount | Valuation | Lead | Notable participants |
|---|---|---|---|---|---|
| Series B extension (🟡) | Sep 2024 | ~$58.7M (CB Insights) | Not disclosed | — | CommerzVentures, HSBC (🟡) |
| Series B | Jun 2024 | $70M (£55M) | Not disclosed (est. £317M) | Highland Europe, AXA Venture Partners | Existing backers |
| Debt facility | Jan 2023 | £30M | — | Kreos Capital | — |
| Strategic | 2021 | Undisclosed | — | LSEG | — |
| Strategic | — | Undisclosed | — | Fidelity International Strategic Ventures | Pivot Investment Partners |

Strategic signal: **LSEG** and **Fidelity International** are both investors *and* clients. That gives credibility, but it also ties the company closely to a few large relationships.

## Competitive landscape
| Layer | Competitor | Where they beat FINBOURNE | Where FINBOURNE wins |
|---|---|---|---|
| Front-to-back incumbents | **BlackRock Aladdin** | Market standard; full front-to-back suite; huge client base | Open and modular; works alongside Aladdin (often integrated); no BlackRock lock-in |
| Front-to-back incumbents | **SimCorp** (Deutsche Börse, with Axioma) | Deep European asset-manager base; mature accounting | Cloud-native from day one; faster to change |
| Cloud consolidators | **Clearwater Analytics** (bought Enfusion for $1.5B in 2025, plus Beacon and BISTRO; 🟡 reported take-private by Permira/Warburg) | Scale, money, an integrated front-to-back suite | Data-layer focus; doesn't force a client to swap everything |
| Custodian platforms | **BNY** (Eagle), **State Street Alpha** (with Charles River), **SS&C** | Bundled with custody and fund admin; existing relationships | Independent of any custodian |
| Data-platform specialists | **Arcesium** (D.E. Shaw-backed; markets itself as a LUSID alternative), FundGuard, Limina | Arcesium: hedge-fund depth and operations services | Bitemporal data model, open APIs, asset-owner wins |
| DIY | Snowflake / Databricks + in-house build | Flexibility; may already be in the client's stack | Ready-made investment data model |
| Asia-local | 🇯🇵 e.g. NRI (Japanese asset-management systems) *(analysis, not verified this run)* | Local language, regulation, incumbency | — (no Asian wins found) |

**Frenemies:** **LSEG** (investor, client, data partner; could build or buy its own platform), **BlackRock Aladdin** (integration partner and the system FINBOURNE often competes against).
**Market direction:** consolidation. Big players are buying to offer one front-to-back suite (Clearwater–Enfusion, SimCorp–Axioma). Independent data-layer vendors like FINBOURNE either become the "open" alternative or an acquisition target.

## Moat deep dive *(analysis)*
**Tech stack — what's owned vs rented**
| Layer | Owned / Rented | Detail |
|---|---|---|
| Core platform (LUSID data engine) | ✅ **Owned** — built in-house | Bitemporal investment data model, API-first, multi-tenant SaaS. Described as "open-source architecture" in client quotes, but no confirmation that code is open-source licensed. |
| AI / LLMs | **Rented** | Agents use Anthropic's Claude via MCP; Candela is FINBOURNE's own agentic layer on top. It doesn't train models. |
| Data | **Client-owned + partner data** | Holds clients' data; market data from partners like LSEG (Yield Book). No proprietary dataset. |
| Compute / cloud | **Rented** | AWS |
| Distribution | Owned + partner | Direct enterprise sales by region; LSEG channel; AWS Marketplace |

So: **a real software platform it owns**, not an AI wrapper. AI is a feature on top, using rented models.

**Keystone clients**
| Client | Relationship | Why it matters |
|---|---|---|
| **LSEG** | ✅ Client (2021), investor, and partner (Yield Book integration, 2025–26) | Biggest credibility anchor; a distribution channel |
| **AustralianSuper** (A$438B) | ✅ Whole-of-fund book of record, **live Oct 2026** | Flagship Asia-Pacific win; proves it at one of the world's largest pension funds |
| **Baillie Gifford** | ✅ Book of record for global operations (2021) | Large UK manager reference |
| **Fidelity International** | ✅ Client + strategic investor | Global asset-manager reference |
| Railpen, Pension Insurance Corporation | ✅ Book of record / data platform | UK asset owners and insurers |
| Seilern, TT International, Thomson Reuters, OMBA | ✅ / 🟡 | Mid-size managers; OMBA is the AI-agent reference |
| Northern Trust | 🟡 Third-party database only | Would be big if confirmed |
Most named wins date from 2021–23. Few new logos were announced in 2025–26 apart from AustralianSuper.

**Switching costs & network effects**
- As a firm's book of record, LUSID sits under reporting, compliance and risk. Replacing it means a multi-year migration, so it's very sticky.
- Regulators and auditors rely on its audit trail, which makes leaving even harder.
- There are few network effects. Each client's data is separate.

**Bear case**
- Incumbents bundle "good-enough" data platforms with front-office and accounting, which makes a separate data layer a hard sell.
- Long sales cycles and big implementations strain a company with ~£6M cash at year-end.
- LLMs plus Snowflake/Databricks could make DIY data layers easier for large firms.
- It could be acquired (LSEG is the obvious candidate) before it reaches scale.

**Moat rating:** **Moderate.** Strong lock-in once installed, with technology it owns. But it's small and has few new wins, against deep-pocketed incumbents.

## Risks & dependencies *(analysis)*
| Category | Risk | Severity | Evidence |
|---|---|---|---|
| Cost & capital | Negative net assets (–£11.2M), ~£6.2M cash at Dec 2025; needs to hit its 2026 profitability goal or raise again | **High** | Endole (Companies House data, 🟡); Financial News on 2026 profitability aim |
| People | Headcount down ~25% from the 2024 peak (est.); 2025 redundancies mentioned in reviews; several leadership changes (new CTO, CPO, COO, regional sales heads) | High | Revelio; Glassdoor; A-Team / Asset Servicing Times people moves |
| Culture & org | Glassdoor **3.0/5 (38 reviews)**, ~22% below the IT average; complaints of top-down decisions, low transparency and an office mandate; positives on tech and colleagues; management says it's "strengthening leadership" | High | Glassdoor reviews 2024–25 |
| Customer concentration | LSEG (client + investor + partner) and a handful of large clients likely make up much of revenue | Medium | No split disclosed |
| Foundational infrastructure | AWS-only hosting; AI layer relies on Anthropic | Low–Medium | AWS Marketplace; Claude/MCP integration |
| Competitive | Consolidating rivals with far more money (Clearwater, Aladdin, SimCorp) | High | Clearwater–Enfusion $1.5B; SimCorp–Axioma |
| Legal & regulatory | No lawsuits found. As a critical vendor to regulated firms, it faces operational-resilience rules (EU DORA, UK critical third parties, Australia's APRA CPS 230) | Medium | Regulatory context *(analysis)* |
| Valuation | Est. £320–400M on ~£23.5M revenue ≈ 14–17x, less stretched than AI natives. A down-round is possible if growth stalls. | Medium | Estimates only |

## Asia footprint
| Market | Presence | Revenue signal | Customers & partners | Local rivals |
|---|---|---|---|---|
| 🇦🇺 Australia / NZ | ✅ Sydney + Brisbane offices; ANZ head of sales Marianne Antonicelli (2024); part of 24/7 follow-the-sun support | Not disclosed; AustralianSuper is likely a major contract | ✅ **AustralianSuper** (live Oct 2026) | SimCorp, Aladdin, custodians |
| 🇸🇬 Singapore / SEA | ✅ Singapore office (since 2022); Asia head of sales **Peter Edwards** (ex-BNY Eagle) based there | Not disclosed | None named | Custodian platforms, Aladdin |
| 🇯🇵 Japan | Nothing found | — | — | NRI and local vendors *(analysis)* |
| 🇭🇰 Hong Kong | Nothing found | — | — | — |
| 🇰🇷 Korea / 🇮🇳 India / 🇨🇳 China | Nothing found | — | — | — |

**Verdict:** Asia-Pacific is an **Australia story** for now, led by pension (super) funds, where AustralianSuper is a strong reference. Singapore is a sales hub with no announced wins. North Asia (Japan, HK) is untouched.

## Recent developments
- **27 Oct 2026** — AustralianSuper goes live with a whole-of-fund book of record on LUSID.
- **11 Sep 2026** — OMBA runs FINBOURNE AI agents in production (≥20% less operational work); 7 clients live with AI; 30+ agents available to all clients.
- **2026** — CEO says AI lets the firm avoid big hiring in engineering and ops; targeting profitability in 2026 (Financial News).
- **Q2 2026** — LSEG Yield Book fixed-income analytics launch inside LUSID.
- **Nov 2025** — LSEG partnership expanded.
- **Jun 2025** — Claude integration via MCP.

## If you're considering joining
**Strategy & moat**
- How many new logos did you sign in 2025–26 besides AustralianSuper? What's the pipeline?
- Where do you win against Aladdin, SimCorp and Clearwater, and where do you lose?
- How important is LSEG to revenue, and what happens if LSEG builds or buys its own platform?
- Is a sale (to LSEG or a consolidator) part of the plan?

**Business health**
- 2025 turnover was ~£23.5M with negative net assets. What's ARR today, how much cash is left, and how many months of runway?
- Are you on track to be profitable in 2026? If not, when is the next raise, and could it be a down-round?
- What share of revenue is software vs implementation services?
- Net revenue retention and gross margin?

**People & culture**
- Headcount fell from ~318 to ~235. What drove that, and is restructuring finished?
- Glassdoor reviews mention top-down decisions and cancelled town halls. What has changed since 2025?
- How many leadership roles changed in the last 18 months, and why?
- What's the office policy now?

**The role**
- Is the role product engineering, client implementation, or forward-deployed AI work?
- What does success look like at 6 and 12 months, and how is it tied to the profitability goal?

**Equity & compensation**
- What type of options (e.g. UK EMI) and at what strike? What valuation is used?
- How do liquidation preferences after ~$100–190M raised affect common shares in a modest exit?
- Any secondary or tender history?

**Asia**
- What's the Asia plan beyond Australia? Target clients in Singapore, Japan, Hong Kong?
- How big is the Singapore team, and does it have its own implementation and support staff?
- Revenue target for APAC in 2027?

**Check yourself**
- Download the latest filed accounts free from Companies House (company 10539696): revenue, losses, cash, going-concern note.
- Read Glassdoor reviews from the last 6 months; check whether management replies match changes on the ground.
- LinkedIn: where recent leavers went, and senior tenure.
- Ask an AustralianSuper or Baillie Gifford contact how the implementation went.

## Open questions
- Exact 2025 loss, and the reason for the big jump from the prior-year turnover figure.
- Valuation at the Series B and extension (both undisclosed).
- Confirmation of the Sep 2024 extension and of HSBC as investor.
- Northern Trust as a client (third-party database only).
- Any Asian (non-Australian) clients.

## Sources
**Funding & financials**
- [TechCrunch — FINBOURNE taps $70M (Jun 2024)](https://techcrunch.com/2024/06/17/finbourne-taps-70m-for-tech-that-turns-financial-data-dust-into-ai-gold)
- [A-Team Insight — raises £55m to fund overseas expansion](https://a-teaminsight.com/blog/finbourne-raises-55m-to-fund-overseas-expansion/)
- [Finextra — raises $55 million](https://www.finextra.com/newsarticle/44321/investment-data-management-platform-finbourne-raises-55-million)
- [FINBOURNE — £30M Kreos debt facility](https://www.finbourne.com/finbourne-partners-with-kreos-capital-securing-a-30-million-debt-facility-to-fuel-future-growth-plans/)
- [Endole — company profile (Companies House data)](https://open.endole.co.uk/insight/company/10539696-finbourne-technology-limited)
- [Tracxn — company profile](https://tracxn.com/d/companies/finbourne-technology/__2GxAYpuZXF2fcpW9CnZ_iuiwMD47k2JPmIUoE_rVW3o)
- [Caplight — valuation & funding history](https://www.caplight.com/company/finbourne)
- [CB Insights — financials](https://www.cbinsights.com/company/finbourne-technology/financials)
- [PitchBook — profile](https://pitchbook.com/profiles/company/221696-47)
- [GetLatka — revenue claim (unreliable)](https://getlatka.com/companies/finbourne-technology)
- [Revelio Labs — headcount](https://www.reveliolabs.com/companies/finbourne-technology/employees)
- [Financial News — turns to AI to limit hiring (mirror)](https://fnlondon-spa-stg.sc.onservo.com/articles/lseg-backed-fintech-finbourne-turns-to-ai-to-limit-hiring-fa2149fa?mod=home)

**Product, AI & tech**
- [The TRADE — integrates with Anthropic's Claude](https://www.thetradenews.com/finbourne-integrates-with-anthropics-claude-to-provide-ai-agent-offering/)
- [A-Team Insight — agentic AI via MCP](https://a-teaminsight.com/blog/finbourne-integrates-agentic-ai-via-mcp-to-enable-secure-real-time-investment-operations/)
- [A-Team Insight — more humans in the loop](https://a-teaminsight.com/blog/finbourne-puts-even-more-humans-in-the-loop-to-build-client-confidence-and-business/)
- [TechIntelPro — OMBA cuts ops burden by 20%](https://techintelpro.com/news/ai/enterprise-ai/omba-runs-finbourne-agentic-ai-to-cut-ops-burden-by-20)
- [AWS Marketplace — LUSID listing](https://aws.amazon.com/marketplace/pp/prodview-4ixywcdp2lxws)
- [FINBOURNE — LSEG fixed income analytics partnership](https://www.finbourne.com/finbourne-and-lseg-extend-partnership-to-deliver-integrated-fixed-income-analytics/)

**Clients**
- [A-Team Insight — LSEG selects FINBOURNE](https://a-teaminsight.com/blog/lseg-selects-finbourne-platform-to-power-wealth-and-investment-solutions-businesses)
- [Finextra — Baillie Gifford selects LUSID](https://www.finextra.com/pressarticle/90148/baillie-gifford-selects-finbournes-lusid-platform-to-boost-investment-data-management)
- [Asset Servicing Times — Railpen selects LUSID](https://www.assetservicingtimes.com/assetservicesnews/dataservicesarticle.php?article_id=12522)
- [A-Team Insight — Pension Insurance Corporation](https://a-teaminsight.com/blog/pensions-insurance-corporation-selects-finbourne-cloud-native-data-management-platform/?brand=dmi)
- [The TRADE — Seilern selects FINBOURNE](https://www.thetradenews.com/seilern-investment-management-selects-finbourne-technology-to-support-growth/)
- [The TRADE — TT International](https://www.thetradenews.com/tt-international-taps-finbourne-technology-to-bolster-data-ecosystem/)
- [Apps Run The World — customer database](https://www.appsruntheworld.com/customers-database/products/view/finbourne-lusid-operational-data-store-ods)

**Competition**
- [Global Trading — Clearwater to acquire Enfusion](https://www.globaltrading.net/clearwater-analytics-to-acquire-enfusion-as-am-tech-provider-contest-heats-up/)
- [The TRADE — Clearwater completes Enfusion acquisition](https://www.thetradenews.com/clearwater-analytics-completes-acquisition-of-enfusion-for-1-5-billion/)
- [Arcesium — LUSID alternative (competitor page)](https://www.arcesium.com/finbourne-lusid-alternative)
- [CB Insights — alternatives & competitors](https://www.cbinsights.com/company/finbourne-technology/alternatives-competitors)
- [WatersTechnology — buy side seeks to unify data](https://www.waterstechnology.com/emerging-technologies/7928511/one-view-to-rule-them-all-buy-side-firms-seek-to-unify-their-data)

**People & culture**
- [City AM — McHugh interview](https://www.cityam.com/?p=2242809)
- [Highland Europe — Thomas McHugh story](https://www.highlandeurope.com/stories/thomas-mchugh/)
- [Glassdoor — FINBOURNE reviews](https://www.glassdoor.co.nz/Reviews/Finbourne-Technology-Reviews-E5346375.htm)
- [Asset Servicing Times — Evans appointed CPO](https://www.assetservicingtimes.com/assetservicesnews/peoplemovesarticle.php?article_id=17252)
- [A-Team Insight — new COO](https://a-teaminsight.com/people/finbourne-appoints-new-chief-operating-officer)

**Asia-Pacific**
- [Asset Servicing Times — AustralianSuper goes live](https://www.assetservicingtimes.com/assetservicesnews/industryarticle.php?article_id=18498)
- [ai-CIO — AustralianSuper launches new data platform](https://www.ai-cio.com/news/australiansuper-launches-a-new-data-platform-for-307-1b-portfolio/)
- [A-Team Insight — new sales head to lead Asia expansion](https://a-teaminsight.com/people/finbourne-appoints-new-sales-head-to-lead-asia-expansion)
- [Finextra — Antonicelli head of sales ANZ](https://www.finextra.com/pressarticle/102050/finbourne-appoints-marianne-antonicelli-as-head-of-sales-for-australia-and-new-zealand)
- [FINBOURNE — CTO appointment and APAC expansion](https://www.finbourne.com/finbourne-technology-appoints-robert-byrne-as-cto-as-it-expands-into-north-america-and-asia-pacific/)
