# Sierra — Briefing
*As of 9 Nov 2026 · AI customer-service agents for enterprises (sierra.ai — not Sierra Space or other "Sierra" companies)*

## TL;DR
- Builds AI agents that handle customer service (chat, voice, email) for large companies, and is moving into longer tasks like loan origination and insurance pre-authorisation.
- **$400M+ ARR** (30 Oct 2026, company blog), doubling roughly every five months. It added $150M+ in Q3 2026 alone.
- **~$15.8B valuation** from a $950M Series E (May 2026), led by Tiger Global and GV. That's ~40x today's ARR.
- **Moat:** it does **not** train its own core models. It rents 15+ LLMs (OpenAI, Anthropic, Google, Meta), so its moat is the platform, the integrations, outcome-based pricing and Fortune-50 relationships.
- **Biggest risks:** dependence on frontier labs that could become competitors; CEO Bret Taylor also chairs OpenAI's board; costly, slow enterprise deployments; a crowded market (Decagon, Salesforce Agentforce + Fin).
- **Asia is a real priority:** offices in Tokyo, Singapore (regional HQ), Sydney and Seoul. SoftBank is its exclusive partner in Japan, and Singtel and LINE MAN Wongnai are live customers.

## Snapshot
| | |
|---|---|
| Founded | 2023 (public launch Feb 2024) |
| Founders / CEO | Bret Taylor (CEO; ex-Salesforce co-CEO, Facebook CTO; chair of OpenAI's board) and Clay Bavor (ex-Google VP) |
| HQ | San Francisco (SoMa) |
| Other offices | New York, London, Paris, Madrid, Toronto, Tokyo, Singapore, Sydney, Seoul (lists vary by source) |
| Employees | ~500–1,000+ (2025–26 aggregator estimates; growing fast) |
| Stage | Private; Taylor says no IPO plans for now |
| Latest primary round | **Series E, $950M at ~$15.8B post, May 2026**, led by Tiger Global and GV |
| Latest valuation mark | Same (no tender found) |
| Total raised | ~$1.6B; $1B+ cash on hand after the Series E |
| Revenue / ARR | **$400M+ ARR (Oct 2026, company)**; $200M (May 2026); $100M (Nov 2025, 21 months after launch) |

## What it does
Sierra sells "agents" that talk to a company's customers and actually resolve issues: changing a subscription, processing a return, troubleshooting a device. They connect to the company's systems (CRM, billing, order management) and run on chat, phone and email in 30+ languages. Sierra builds and tunes each deployment with the customer.

| Product | What it does | Who buys |
|---|---|---|
| Agent OS / platform | Runtime, guardrails, monitoring and simulation for customer-facing agents | Enterprise CX teams |
| Agent Studio + Ghostwriter | No-code builder; Ghostwriter builds an agent from SOPs, transcripts or a plain-language goal | CX ops, business teams |
| Agent SDK | Developer toolkit for custom agents | Enterprise engineering |
| Voice (incl. Voice Personas) | Phone agents with configurable voice and behaviour | Contact centres |
| Horizon (Jul 2026, via Takeoff acquisition) | Long-running agents that pursue goals over days or weeks (e.g. originating a loan, healthcare prior authorisation) | Financial services, healthcare |
| Anon acquisition (Nov 2026) | Lets agents log in to websites and finish tasks where there's no API | Extends Horizon |

## How it makes money
- **Outcome-based pricing.** Customers pay mainly per *resolved* conversation. Escalations to humans generally aren't billed. Some contracts mix in per-conversation or volume pricing for simple interactions.
- **Price points** (third-party estimates, not confirmed): ~$1–2.50 per resolution; year-one budgets ~$200K–350K+; 3–7 months to deploy.
- **Customers:** large enterprises. Sierra says it serves almost 50% of the Fortune 50 (some sources say 40%+).
- No self-serve tier; it's sales-led and high-touch.

## Biggest revenue stream
**Enterprise customer-service agent contracts, billed per resolution.** This is effectively all of revenue today. Sierra doesn't split it by channel (voice vs chat) or industry. Horizon (long-running agents in finance and healthcare) is the next leg but too new to show up in the numbers.

## Funding & backers
| Round | Date | Amount | Valuation | Lead | Notable participants |
|---|---|---|---|---|---|
| Series E | May 2026 | $950M | ~$15.8B post | Tiger Global, GV | Benchmark, Sequoia, Greenoaks |
| Strategic | Dec 2025 | Undisclosed | — | SoftBank Vision Fund 2 | Tied to Japan expansion |
| Series D | Sep 2025 | $350M | $10B | Greenoaks | — |
| Series C | Oct 2024 | $175M | $4.5B | Greenoaks | — |
| Seed / A / B | 2023–Feb 2024 | $110M | — | Sequoia, Benchmark | — |

Strategic signal: **GV (Google)** co-leading means Google is a backer *and* a model supplier. **SoftBank** is an investor *and* the exclusive sales partner in Japan.

## Competitive landscape
| Layer | Competitor | Where they beat Sierra | Where Sierra wins |
|---|---|---|---|
| Direct pure-play | **Decagon** ($4.5B, Jan 2026) | Faster deployment; reportedly runs ~80% of traffic on its own fine-tuned models (🟡) → potentially better margins; lower valuation multiple (~45x vs Sierra’s ~79x ARR at their rounds, est.) | Bigger enterprise logos, deeper integrations, 2x+ the funding, founder brand |
| CRM / helpdesk incumbents | **Salesforce Agentforce** (+ **Fin**, formerly Intercom; Salesforce reportedly closed the acquisition Sep 2026 🟡), **Zendesk AI** | Already own the customer data and helpdesk; bundled pricing (Fin ~$0.99/resolution; Zendesk ~$1.50–2) | Vendor-neutral across CRMs; higher resolution on complex workflows; strategic "AI front door" positioning |
| Contact-centre / conversational AI | Kore.ai, Cognigy (NICE), PolyAI, Ada, Cresta, Yellow.ai | Long contact-centre relationships, telephony depth, lower price | Modern agent architecture, outcome pricing, speed of product shipping |
| Frontier labs | **OpenAI**, **Anthropic**, **Google** (enterprise agent platforms) | Own the models; could sell agents directly to the same enterprises | Multi-model neutrality, CX domain expertise, hands-on deployment |
| BPOs / outsourcers | Concentrix, Teleperformance, transcosmos | Own the human contact-centre contracts; adding AI themselves | Sierra replaces the cost base they're defending |
| Asia-local | 🇯🇵 ZEALS, Karakuri, Flyle (Series A Oct 2026); 🇰🇷 Channel Talk (ALF agent), Sendbird | Local language, culture, pricing, existing SMB/mid-market base | Large enterprise, global brands, SoftBank/Singtel distribution |

**Frenemies:** **OpenAI** (core supplier; Taylor chairs its board; could build competing agents), **Google** (investor, model supplier, competing agent platform), **Salesforce** (where many customers' data lives, and a direct rival).
**Market direction:** consolidating fast. Incumbents are buying (Salesforce–Fin, NICE–Cognigy), and pure-plays are racing for Fortune-500 lock-in. The winners will be decided by resolution rates and enterprise trust, not by models.

## Moat deep dive *(analysis)*
**Tech stack — what's owned vs rented**
| Layer | Owned / Rented | Detail |
|---|---|---|
| Core LLMs | **Rented** | 15+ third-party models from OpenAI, Anthropic, Google and Meta, plus open source. It routes by task, cost and provider capacity; ~10–15 model calls per conversation turn (🟡). Possible proprietary fine-tunes (🟡, single source). |
| Voice (STT/TTS) | **Rented** | Uses several providers; native voice-to-voice is a small share of traffic (🟡) |
| Orchestration, guardrails, evaluation | ✅ **Owned** | Agent OS, simulation/testing, its "agent development lifecycle", Ghostwriter |
| Integrations & long-running tasks | ✅ **Owned** (partly bought) | Enterprise system connectors; Horizon (Takeoff); browser log-in (Anon) |
| Data | **Owned (per customer)** | Conversation and resolution data from each deployment improves its playbooks; it uses support volume as a learning loop (🟡 Sacra) |
| Compute | **Rented** | Via model APIs; no own GPU fleet found |
| Distribution | ✅ **Owned** | Founder network into the Fortune 50, SoftBank in Japan, partner ecosystem |

So: **an application-layer company on top of frontier labs.** That's not a weakness by itself (it gets every model upgrade for free), but the moat has to come from everything *around* the model.

**Keystone clients**
| Client | Relationship | Why it matters |
|---|---|---|
| WeightWatchers, SiriusXM, Sonos | ✅ Launch customers (2024) | Proof cases that drove early credibility |
| ADT, Rocket Mortgage, Cigna, Sutter Health, SoFi, Ramp, Rivian | 🟡 Named customers | Spread across home security, mortgage, health and fintech — high-volume, regulated support |
| Uber, Hyatt, Gap, Santander, CLEAR | 🟡 Listed on Sierra's customer/partner pages and job posts | Global consumer brands; Santander opens European banking |
| **SoftBank Corp.** | ✅ Exclusive Japan sales partner (from 14 Jul 2026) + Vision Fund investor | Entry to Japan's enterprise market through Japan's biggest telco group |
| **Singtel** | ✅ "Shirley" assistant; live in 10 weeks, 70%+ resolution | Asian telco reference case |
| ~40–50% of the Fortune 50 | Company claim | Logo density = credibility, but also concentration |
No revenue share per customer is disclosed.

**Switching costs & network effects**
- Each deployment is wired into billing, CRM and order systems and tuned for months, so ripping it out is expensive.
- Outcome-based pricing aligns Sierra with the buyer's goals, which makes it hard for a cheaper "per seat" tool to win on value.
- Cross-customer learning on what resolves issues (🟡) improves new deployments over time.

**Bear case**
- Frontier labs (OpenAI, Anthropic, Google) sell agent platforms directly and price below Sierra.
- Salesforce bundles Agentforce + Fin into existing CRM contracts.
- Decagon matches it on quality with better margins thanks to its own models.
- Agent-building gets commoditized. Ghostwriter-style tools exist everywhere, and the hands-on deployment work doesn't scale like software.

**Moat rating:** **Moderate.** It rests on enterprise relationships, deep integrations and execution speed, not on proprietary technology. Strong for now, but it has to be re-won as models and incumbents catch up.

## Risks & dependencies *(analysis)*
| Category | Risk | Severity | Evidence |
|---|---|---|---|
| People | **Key-person and governance:** Bret Taylor is CEO *and* chair of OpenAI's boards; he says he recuses himself where they overlap | High | Fortune/Benzinga 2024 interviews; no independent account of how recusal has worked since |
| Culture & org | In-office 4–5 days, demanding pace; scaling headcount and ~10 offices quickly; Glassdoor sample tiny (4.0 on 13 reviews, aggregator) | Medium | Careers page, job posts, aggregator ratings |
| Cost & unit economics | Pays for every model call, but only gets paid when the agent resolves. Failed conversations are pure cost. Heavy deployment work (3–7 months) adds services cost. AI-native benchmark gross margin is ~52% vs 75–80% for SaaS (ICONIQ, not Sierra-specific) | High | Pricing analyses; margin undisclosed |
| Foundational infrastructure | 100% reliant on third-party LLMs and voice providers; mitigated by routing across 15+ models | Medium | Tech-stack analyses (🟡) |
| Customer concentration | Fortune-50-heavy; big contracts, long sales cycles | Medium | Company Fortune-50 claim; no breakdown |
| Legal & regulatory | No lawsuits found. Liability when an agent gives wrong answers or takes wrong actions; Horizon pushes into regulated loans and healthcare; EU AI Act | Medium | CISO hire, AIUC-1 certification (Sep 2026) show it's investing in trust |
| Valuation & capital | ~40x current ARR — fine at 2x every 5 months, painful if growth slows; $1B+ cash is a cushion | Medium | Company ARR + Series E |

## Asia footprint
| Market | Presence | Revenue signal | Customers & partners | Local rivals |
|---|---|---|---|---|
| 🇯🇵 Japan | ✅ Tokyo office; acquired Tokyo AI startup **Opera Tech** (Mar 2026), whose co-founders now lead Sierra Japan | Not disclosed | ✅ **SoftBank Corp.** exclusive sales partner (Jul 2026); ✅ SoftBank Vision Fund 2 investor | ZEALS, Karakuri, Flyle; BPOs like transcosmos |
| 🇸🇬 Singapore / SEA | ✅ **Regional HQ in Singapore** (Nov 2025); Sierra Summit Singapore 17 Nov 2026 | Not disclosed | ✅ **Singtel** ("Shirley"); ✅ **LINE MAN Wongnai** (Thailand, strategic partner for multiple agents) | Yellow.ai, local BPOs |
| 🇦🇺 Australia | ✅ Sydney office | Not disclosed | Not found | — |
| 🇰🇷 Korea | ✅ Seoul office; 🔍 hiring Regional VP Sales + engineers (Aug 2026) | Not disclosed | Not found | Channel Talk, Sendbird |
| 🇮🇳 India | Nothing found | — | — | — |
| 🇨🇳 China / HK / 🇮🇩 Indonesia | Nothing found | — | — | — |

**Verdict:** Asia is an early but deliberate bet. Sierra is using big telcos (SoftBank, Singtel) as its distribution channel and has a regional HQ in Singapore. Japan is the market to watch. India is a gap, which may be intentional given lower support-labour costs there.

## Recent developments
- **5 Nov 2026** — Acquires Anon (browser agents that can log in to websites).
- **3 Nov 2026** — Sierra Summit keynote; redesigned Agent Studio around Ghostwriter; new CISO (Kyle Randolph).
- **30 Oct 2026** — $400M+ ARR; added $150M+ in Q3.
- **Sep 2026** — AIUC-1 agent-security certification.
- **Jul 2026** — Horizon launch + Takeoff acquisition; SoftBank becomes exclusive Japan partner.
- **May 2026** — $950M Series E at ~$15.8B.
- **Mar 2026** — Acquires Opera Tech (Japan); Singtel partnership; Madrid office.

## If you're considering joining
**Strategy & moat**
- If OpenAI, Anthropic or Google sell enterprise agents directly, why do customers still pick Sierra? What's the evidence in recent win/loss data?
- How do you handle Bret's OpenAI role in practice — is there a written recusal process, and has it ever affected a deal or model decision?
- Is there a plan to train or fine-tune your own models (as Decagon reportedly does) to protect margins?
- How do you compete when Salesforce bundles Agentforce + Fin into existing contracts?

**Business health**
- What's gross margin, and how much of each deployment is services work vs software?
- What's the average resolution rate across customers, and how much model cost goes into conversations you don't get paid for?
- Net revenue retention, and how concentrated is revenue in the top 10 customers?
- How much of the $400M ARR is live and billing vs contracted but still deploying?

**People & culture**
- What does "in office most days" mean for my team? How strict is it in Asia offices?
- What are typical working hours and pace during a big customer launch?
- How much time do Bret and Clay spend on the business day to day?
- Attrition in the last 12 months, especially among agent engineers and deployment teams?

**The role**
- Is this role building the product, or deploying it for customers (agent engineer / forward-deployed)? How is time split?
- What does success look like at 6 and 12 months?

**Equity & compensation**
- What valuation is my grant priced off — the $15.8B Series E or a newer 409A?
- Has there been any employee tender, and is one planned?
- Vesting, cliff, and how long I get to exercise after leaving.
- Liquidation preference stack after $1.6B raised.

**Asia**
- How independent is Sierra Japan (ex-Opera Tech team) vs SoftBank's role as exclusive partner? Who owns the customer relationship?
- Headcount and revenue targets for Singapore, Tokyo, Seoul, Sydney over the next 12 months?
- Is India on the roadmap?
- How are language quality and local data rules (Japan APPI, Korea PIPA, Singapore PDPA) handled?

**Check yourself**
- Glassdoor / Blind — small sample, so ask ex-employees directly.
- LinkedIn: tenure of people who left in 2026 and where they went (Decagon? OpenAI?).
- Talk to a Sierra customer's CX team if you can — resolution rates are the whole business.
- Watch OpenAI's governance news for anything touching Taylor's dual role.

## Open questions
- Gross margin and how much of each deployment is services work.
- Revenue split by region, channel (voice vs chat) and industry.
- Whether Sierra fine-tunes its own models, and how much.
- Status of Salesforce's reported acquisition of Fin (formerly Intercom) — single-type sources.
- Korea and Australia named customers.

## Sources
**Funding & revenue**
- [CNBC — Sierra raises nearly $1B (May 2026)](https://www.cnbc.com/2026/05/04/bret-taylor-sierra-fundraise-openai.html)
- [Bret Taylor on X — $950M round](https://x.com/btaylor/status/2051313954312331411)
- [Tech Startups — $950M at $15.8B](https://techstartups.com/2026/05/04/bret-taylors-ai-startup-sierra-raises-950m-at-15-8b-valuation-as-demand-for-ai-agents-surges/)
- [Sierra blog — $400M+ ARR](https://sierra.ai/blog/our-customers-ambition-is-accelerating-our-growth)
- [Sacra — Sierra revenue, valuation & funding](https://sacra.com/c/sierra/)
- [Axios — SoftBank investment and Japan expansion](https://www.axios.com/2025/12/04/sierra-ai-softbank-investment-japan)
- [Fortune — $110M from Sequoia and Benchmark (2024)](https://fortune.com/2024/02/13/bret-taylor-clay-bavor-ai-startup-sierra-110-million-funding-sequoia-benchmark/?stream=top)
- [The Bridge — $100M ARR in 21 months](https://thebridge.jp/2025/11/sierra-ai-100m-arr-achievement)
- [CMSWire — $950M, beyond customer support](https://www.cmswire.com/customer-experience/sierra-raises-950m-at-15b-valuation-eyes-transformation-beyond-customer-support/)

**Business model & product**
- [Falkster — Sierra and outcome-based pricing](https://falkster.com/blog/the-sierra-playbook)
- [Fin — Sierra AI pricing (competitor)](https://fin.ai/learn/sierra-ai-pricing)
- [Featurebase — Sierra AI pricing](https://www.featurebase.app/blog/sierra-ai-pricing)
- [CMSWire — Takeoff acquisition, Horizon](https://www.cmswire.com/customer-experience/sierra-buys-takeoff-launches-horizon-agent-platform/)
- [Sierra blog — acquires Anon](https://sierra.ai/blog/sierra-acquires-anon)
- [Sierra blog — Summit recap 2026](https://sierra.ai/blog/summit-recap-2026)
- [Pulse — Ghostwriter](https://www.pulse.bot/saas/news/sierra-unveils-ghostwriter-ai-platform-that-builds-saas-agents-for-enterprises-3fa47f98-515f-490f-8aa1-d70522c8a929)

**Tech stack**
- [ZenML — production-grade CX agents at enterprise scale](https://www.zenml.io/llmops-database/building-production-grade-customer-experience-agents-at-enterprise-scale)
- [ZenML — voice and multi-modal agents](https://www.zenml.io/llmops-database/building-production-scale-voice-and-multi-modal-customer-experience-agents)
- [Contrary Research — Sierra report](https://research.contrary.com/report/sierra)
- [Sacra — support volume as moat](https://sacra.com/chat/h/1e0b8de1-c524-4b7d-9924-db5214914ac2)

**Competition**
- [Atlan — Sierra AI alternatives](https://atlan.com/know/ai-agent/ai-agent-applications/sierra-ai-alternatives/)
- [Fin — Sierra alternatives (competitor)](https://fin.ai/learn/sierra-alternatives)
- [Dragapp — Decagon vs Sierra](https://www.dragapp.com/blog/decagon-vs-sierra/)
- [AgentMarketCap — Decagon $4.5B Series D](https://agentmarketcap.ai/blog/2026/04/17/decagon-250m-series-d-4-5b-valuation-support-agent-vertical)
- [New Market Pitch — Is Sierra worth $15.8B?](https://newmarketpitch.com/blogs/news/agentic-ai-sierra-overvalued)
- [The Bridge — Flyle Series A](https://thebridge.jp/en/2026/10/flyle-an-ai-agent-for-contact-center-operations-raises-%c2%a51-88-billion-in-series-a-funding-ai-operator-to-launch-officially-in-november)
- [MT (Korea) — Channel Talk in Japan](https://www.mt.co.kr/en/future/2026/06/07/2026060711434842883)
- [Venture Square — Sendbird Agent Steward](https://www.venturesquare.net/?p=1097301)

**People, culture & risk**
- [Fortune — Taylor promises to recuse on OpenAI overlap](https://fortune.com/2024/02/13/openai-chair-bret-taylor-interview-promises-recuse-whenever-potential-overlap-ai-startup-sierra/)
- [Benzinga — Taylor dismisses conflict concerns](https://benzinga.com/news/24/02/37147866/openais-chair-bret-taylor-dismisses-concerns-about-his-ai-chatbot-startup-competing-with-chatgpt-par)
- [Sierra careers](https://sierra.ai/careers)
- [ZeroG Talent — company culture at Sierra](https://zerogtalent.com/blog/company-culture-at-sierra-ai)
- [Autobound — executive changes](https://www.autobound.ai/companies/sierra/executive-changes)

**Asia**
- [Sierra — launches in Japan](https://sierra.ai/blog/sierra-in-japan)
- [SoftBank Corp. — strategic partnership with Sierra](https://www.softbank.jp/en/corp/news/press/sbkk/2026/20260714_01/)
- [Sierra — Singapore regional HQ](https://sierra.ai/blog/singapore)
- [Sierra — Australia](https://sierra.ai/blog/sierra-comes-to-australia)
- [Sierra — launches in Korea](https://sierra.ai/blog/sierra-launches-in-korea)
- [Sierra — LINE MAN Wongnai](https://sierra.ai/kr/customers/line-man-wongnai)
- [Sierra Summit Singapore 2026](https://sierra.ai/sierra-summit-2026-singapore-register)
