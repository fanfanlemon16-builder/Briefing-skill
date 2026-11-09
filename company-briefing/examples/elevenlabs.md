# ElevenLabs — Briefing
*As of 9 Nov 2026 · Voice AI platform (speech models + voice agents)*

## TL;DR
- Builds AI voice models (text-to-speech, speech-to-text, dubbing, music) and a platform for **voice agents** that answer calls and chats for businesses.
- **~$600M ARR** (Sep 2026, CEO to TechCrunch), up from ~$350M at end-2025. Self-reported, unaudited.
- **$22B valuation** from a $300M employee tender (closed 30 Sep 2026), double the $11B Series D in Feb 2026.
- Enterprise is now the bigger half of revenue (**55%+**), driven by voice agents for customer support and sales.
- **Moat:** trains its own speech models, but rents the agents' "brain" (Gemini, Claude, GPT) and all compute from Google — a supplier that also competes.
- **Biggest risks:** price pressure from OpenAI/Google voice, compute costs, and voice-data lawsuits (Illinois biometric-privacy class action, May 2026).
- **Asia matters a lot:** India is reportedly its **#2 market by revenue**, and it has local teams in Japan, Korea and Australia.

## Snapshot
| | |
|---|---|
| Founded | 2022 |
| Founders / CEO | Mati Staniszewski (CEO), Piotr Dąbkowski (CTO) — Polish, ex-Google / Palantir |
| HQ | New York (corporate, per most sources); London is the European HQ; R&D roots in Warsaw. Some directories list London as HQ. |
| Other offices | London, Warsaw, San Francisco, Dublin, Tokyo, Bangalore (India status mixed — see Asia) |
| Employees | ~900–1,350 (Mar–Sep 2026, Revelio/Autobound estimates) |
| Stage | Private; CEO has discussed IPO ambitions |
| Latest primary round | **Series D, $500M at $11B, Feb 2026**, led by Sequoia |
| Latest valuation mark | **$22B**, $300M employee tender, 30 Sep 2026 (secondary — no new cash to company) |
| Total raised (primary) | ~$780–800M+ (estimates vary) |
| Revenue / ARR | ~$600M ARR (Sep 2026, company); >$500M (Apr 2026, company blog) |

## What it does
ElevenLabs makes software that generates and understands human-sounding speech in dozens of languages. Developers call it through an API; creators use the web app; enterprises deploy it as voice agents on phone lines and apps.

| Product | What it does | Who buys |
|---|---|---|
| Text to Speech / voice cloning | Lifelike speech from text; clone or design voices | Creators, media, developers |
| ElevenAgents (Conversational AI) | Real-time voice agents that handle interruptions, connect to telephony and tools | Enterprises (support, sales, ops) |
| Dubbing | Translate video audio while keeping the speaker's voice | Media, studios, enterprises |
| Speech to Text | Transcription | Developers, enterprises |
| Music & sound effects | Generated audio | Creators, ad/media |
| Voice Library | Marketplace where voice owners earn when their voice is used | Creators (supply side) |

## How it makes money
- **Self-serve subscriptions** — tiered monthly plans (free → ~$990/mo) priced on credits/characters; overages and add-ons.
- **Usage-based API** — developers pay per character / minute.
- **Enterprise contracts** — custom pricing, platform fees, volume commitments, forward-deployed engineers for large rollouts.
- Mix: ~50/50 enterprise vs self-serve in Sep 2025 → **55%+ enterprise** by Sep 2026; company targets 60% by end-2026. The rest is SMBs, developers and creators.

## Biggest revenue stream
**Enterprise contracts, led by voice agents.** Enterprise is 55%+ of ARR and the fastest-growing part; reporting attributes the 2026 surge mainly to conversational agents for customer support, sales and internal ops. Named enterprise customers include Revolut (agents for 4M+ customers in UK/EU), Cisco, NVIDIA, Adobe, Epic Games. Self-serve TTS for creators is still large but a shrinking share.

## Funding & backers
| Round | Date | Amount | Valuation | Lead | Notable participants |
|---|---|---|---|---|---|
| Employee tender (secondary) | Sep 2026 | $300M | $22B | Wellington, T. Rowe Price | a16z, EQT (new), Goldman Sachs (new) |
| Series D (+ extension) | Feb 2026 (ext. disclosed May 2026) | $500M | $11B | Sequoia | a16z, ICONIQ, Lightspeed (new), Evantic (new); extension added BlackRock, Wellington, NVIDIA |
| Employee tender | Sep 2025 | $100M | $6.6B | — | — |
| Series C | Jan 2025 | $180M | $3.3B | a16z, ICONIQ | — |

Strategic signal: **NVIDIA** (compute/GPU partner and customer). Sequoia's Andrew Reed joined the board. In India, investment firm **Activate** invested with a mandate to grow the local ecosystem.

## Competitive landscape
| Layer | Competitor | Where they beat ElevenLabs | Where ElevenLabs wins |
|---|---|---|---|
| Frontier labs | **Google** (Gemini Live, Gemini TTS) | Price (~$15–18 vs ~$50–100 per 1M chars, third-party est.); end-to-end speech-native model; bundled with Google Cloud | Voice quality and range, voice cloning/library, multilingual polish, vendor-neutral |
| Frontier labs | **OpenAI** (Realtime API, gpt-4o-mini-tts) | Price (~$12–15 per 1M chars, est.); one model does listening + reasoning + speaking; huge developer base | Expressiveness, voice choice, enterprise agent tooling, telephony integrations |
| Speech specialists | **Cartesia** | Latency (claims sub-40ms), price | Quality, breadth of products, brand, enterprise footprint |
| Speech specialists | **Deepgram** | Speech-to-text heritage, latency, price | TTS quality, creator ecosystem |
| Speech specialists | Inworld, Hume, Resemble, WellSaid, Murf, PlayHT (status unclear) | Niche focus (gaming, emotion, studio voiceover), price | Scale and all-in-one platform |
| Agent / application layer | Customer-service agent platforms (e.g. Sierra, Decagon) and voice-agent builders *(analysis — not verified in this run)* | Own the customer workflow; can swap the voice vendor underneath | ElevenLabs sells agents directly *and* as the voice layer for others |
| Dubbing / video | HeyGen and AI-video tools | Video avatars + dubbing in one product | Audio quality, API depth |
| Music | Suno, Udio | Consumer music brand | Licensed deals (UMG, Sep 2026) reduce legal risk |
| Open source | Kokoro and self-hosted TTS | Near-zero marginal cost at scale | Quality, reliability, no ML team needed |

**Frenemies:** **Google** is ElevenLabs' cloud/GPU provider, the default LLM inside its agents, *and* a direct competitor. Customer-service platforms can be customers and rivals at the same time.
**Market direction:** voice is splitting in two — cheap "good-enough" speech bundled by frontier labs, and premium quality + enterprise agent platforms. ElevenLabs is betting on the second and pushing upmarket fast.

## Moat deep dive *(analysis)*
**Tech stack — what's owned vs rented**
| Layer | Owned / Rented | Detail |
|---|---|---|
| Core speech models (TTS, STT, dubbing, music) | ✅ **Owned** — trained in-house | Research-led company; Eleven v3 TTS, Scribe STT, music model. 🟡 An end-to-end realtime agent model ("Eleven Realtime") reportedly rolled out Oct 2026. |
| LLM / reasoning (the agent's "brain") | **Rented** | Agents run on third-party LLMs. Docs/changelog (🔍) show the default is Google Gemini Flash, with Claude and GPT options, an NVIDIA Nemotron model hosted by ElevenLabs, or bring-your-own LLM. |
| Data | **Mixed** | Licensed voices via Voice Library (owners paid per use) and licensing deals (UMG). Some historical training data is contested in court (see Risks). |
| Compute / cloud | **Rented** | Google Cloud (GKE) on NVIDIA GPUs, including Blackwell clusters. |
| Distribution | ✅ **Owned** | Large self-serve funnel, developer API, enterprise sales, local Asia teams. |

So: **not a wrapper on a frontier lab for speech** — the voice layer is proprietary. But the agent product depends on frontier-lab LLMs for reasoning, and everything runs on Google.

**Keystone clients**
| Client | Relationship | Why it matters |
|---|---|---|
| Deutsche Telekom | ✅ Deep partnership since early 2025; ElevenLabs engineers on-site in Germany; contact centre + network-level AI features | Telco reference customer — proves voice agents at carrier scale; template for other telcos (incl. Asia) |
| Revolut | ✅ ElevenAgents for customer support, 4M+ customers in UK/EU (Jan 2026) | Flagship fintech agent deployment |
| Meta, Epic Games, Salesforce, Harvey, MasterClass | 🟡 API customers (apps reaching 1B+ users combined) | Big-brand developer validation |
| Cisco, NVIDIA, Adobe | 🟡 Enterprise customers; NVIDIA is also an investor | Strategic tie-ins with infra and creative software |
| Universal Music Group | ✅ Multi-year music licensing deal (Sep 2026) | Licensed data for music; contrasts with rivals being sued |
| Klarna, Square, Ukrainian government | 🟡 Named customers | Breadth across fintech and public sector |
No single-customer revenue share is disclosed, so concentration can't be judged.

**Switching costs & network effects**
- Agents get wired into call centres, CRMs and telephony (Twilio-style providers, Exotel/Plivo in India) — ripping them out is painful.
- Custom and cloned voices become a brand asset that lives on ElevenLabs.
- Voice Library is two-sided: more voice owners → more choice → more users → more payouts.

**Bear case**
- Frontier labs make speech a free feature of their models, and price is 3–8x lower.
- The LLM layer of agents belongs to Google/OpenAI/Anthropic, who can bundle their own voice.
- Customer-service platforms keep the customer relationship and treat voice as a swappable part.

**Moat rating:** **Moderate–Strong.** It rests on proprietary speech models plus enterprise integration depth. The weak spot is that the agent's reasoning and all compute are rented from companies that also compete.

## Risks & dependencies *(analysis)*
| Category | Risk | Severity | Evidence |
|---|---|---|---|
| People | Founder dependence: the two co-founders still interview every hire; the commercial leadership is new | Medium | First CRO (Ashley Kramer, ex-OpenAI enterprise sales) hired only Sep 2026; plans to roughly double sales headcount (+120 reps) |
| Culture & org | No job titles and ~20 micro-teams of 5–10 people worked at ~250–400 staff; now ~900–1,350 (estimates) — strain as it adds a big sales org | Medium | CEO and Sifted on the no-titles model; Revelio/Autobound headcount estimates; no reliable Glassdoor data found |
| Cost & unit economics | Compute-heavy, gross margin undisclosed (third-party est. ~70–75%); price pressure from OpenAI/Google | High | ElevenLabs engineer: "not enough GPUs"; third-party price comparisons |
| Foundational infrastructure | Single cloud (Google) and frontier-lab LLMs in agents — suppliers that also compete | High | Google Cloud/NVIDIA partnership; agent docs default to Gemini |
| Customer concentration | Not disclosed; enterprise is 55%+ and rising, so large accounts matter more | Unknown | No breakdown published |
| Legal & regulatory | Illinois biometric-privacy (BIPA) class action (May 2026) over voice data; earlier voice-actor suit settled; EU AI Act disclosure rules (Aug 2026); voice-cloning fraud and reputation risk | High | Law360, court filings coverage; Consumer Reports 2025 found weak consent barriers across cloning tools |
| Valuation & capital | $22B on ~$600M ARR ≈ 37x ARR — needs sustained high growth to justify | Medium | Tender and ARR figures above |

## Asia footprint
| Market | Presence | Revenue signal | Customers & partners |
|---|---|---|---|
| 🇮🇳 India | Local leadership + team; Bangalore listed as an office, though an Apr 2026 report said a dedicated office was still being evaluated | ✅ Company says India is its **#2 market by revenue**; target **$100M** India revenue (Feb 2026) | 🟡 Physics Wallah, Havells, Razorpay (customers) · ✅ Karnataka state govt (public services) · ✅ Ozonetel, Exotel, Plivo (telephony integrations) · ✅ Activate (investor/ecosystem partner) |
| 🇯🇵 Japan | ✅ ElevenLabs Japan G.K. (Tokyo) — first international subsidiary, APAC hub (2025); GM Hajime Tamura | Not disclosed | ✅ To-in (Jun 2026, enterprise multilingual dubbing reseller) · 🟡 OpenHome (featured voice partner in Japan developer program) |
| 🇰🇷 Korea | ✅ Official launch; country lead Sangwon Hong (Japan GM also covers Korea) | Not disclosed | ✅ MBC C&I, SBS (broadcast), Krafton (gaming), ESTsoft |
| 🇦🇺 Australia / NZ | ✅ Expanding local business; plans to triple team (May 2026) | Not disclosed | Not found |
| 🇸🇬 Singapore / SEA | 🔍 APAC roles listed for Singapore; Singapore named as possible next hub | Not disclosed | Not found |
| 🇨🇳 China | 🔍 Job listings mention China; no confirmed operations | Not disclosed | Not found |

**Verdict:** Asia is already material — India alone is the #2 revenue market — and ElevenLabs is building it market-by-market through local leads, broadcasters/gaming in Korea, channel partners in Japan, and telephony + government in India. Watch Singapore as the likely next hub.

## Recent developments
- **30 Sep 2026** — $300M employee tender closes at $22B.
- **Sep 2026** — CEO: $600M ARR, 55%+ enterprise; calls for businesses to disclose when AI answers calls.
- **Jun 2026** — Japan partnership with To-in for enterprise dubbing.
- **May 2026** — Series D extension adds BlackRock, NVIDIA; ARR passes $500M; ANZ expansion; Activate invests for India.
- **Feb 2026** — $500M Series D at $11B (Sequoia); India $100M revenue goal announced.

## If you're considering joining
**Strategy & moat**
- How much of agent revenue would survive if Google or OpenAI bundled comparable voice for free? What's the plan if they do?
- What's the roadmap for the LLM layer — keep renting, or move to the in-house realtime model? How many agent customers use it today?
- How do you manage being dependent on Google as cloud provider, LLM supplier and competitor?

**Business health**
- What is gross margin today, and how has it moved as enterprise grew? What's compute spend as % of revenue?
- How does ARR convert to recognized revenue? What's net revenue retention for enterprise vs self-serve?
- What does the top-10 customer share of revenue look like?
- Is there an IPO timeline, and what milestones have to be hit first?

**People & culture**
- With no titles, how are levels, pay bands and promotions decided?
- Do the founders still interview every hire? What happens to that as you double the sales team?
- What's attrition been in the last 12 months, especially among early employees and in sales?
- How does the remote-first model work across time zones — how much happens in hubs?

**The role**
- What does success look like at 6 and 12 months? Which micro-team would I sit in, and who decides my priorities?
- How has this role changed since the CRO joined (for commercial roles)?

**Equity & compensation**
- What's my strike price / grant value vs the $11B Series D and the $22B tender? Which one is used to value my grant?
- Vesting, cliff and exercise window after leaving?
- Have tenders been offered regularly (Sep 2025, May 2026, Sep 2026)? Who was eligible and how much could people sell?
- Any liquidation preferences that sit ahead of common stock?

**Asia**
- How much autonomy do the Japan/Korea/India leads have on hiring, pricing and partners?
- What are the revenue targets per market (e.g. India $100M), and is Singapore the next hub?
- How do you handle local data-residency and AI rules (India, Japan, Korea)?

**Check yourself**
- Glassdoor / Blind reviews, filtered to the last 12 months.
- LinkedIn: tenure of people who left in 2026, and where they went.
- Back-channel with an ex-employee from your target team.
- Status of the Illinois BIPA case (court docket).

## Open questions
- Recognized (GAAP) revenue and gross margin — only ARR is disclosed.
- Share of agent traffic on the in-house realtime model vs third-party LLMs.
- Customer concentration.
- Local Asian competitors (e.g. Korean/Japanese/Indian voice AI players) — not researched in this run.
- Revenue split by product (agents vs TTS vs dubbing) — not broken out.
- Japan / Korea revenue size.
- Whether Bangalore is a full office or a distributed team.
- Series D lead details differ slightly across reports.

## Sources
- [TechCrunch — $500M from Sequoia at $11B (Feb 2026)](https://techcrunch.com/2026/02/04/elevenlabs-raises-500m-from-sequioia-at-a-11-billion-valuation/)
- [Bloomberg — valuation triples to $11B](https://www.bloomberg.com/news/articles/2026-02-04/ai-startup-elevenlabs-more-than-triples-valuation-to-11-billion)
- [ElevenLabs blog — $500M ARR and new investors](https://elevenlabs.io/blog/500m-arr-and-new-investors)
- [Pulse 2.0 — BlackRock, NVIDIA join](https://pulse2.com/elevenlabs-500-million-arr-reached-as-ai-voice-platform-adds-blackrock-nvidia-and-jamie-foxx-as-investors/)
- [Unite.AI — $300M tender at $22B](https://unite.ai/elevenlabs-closes-300m-employee-tender-offer-at-22b-valuation)
- [Sifted — valuation doubles to $22B](https://sifted.eu/articles/elevenlabs-doubles-valuation-to-22bn-with-tender-offer/)
- [Music Business Worldwide — $22B vs Suno](https://www.musicbusinessworldwide.com/elevenlabs-valuation-doubles-to-22b-four-times-that-of-ai-music-rival-suno/)
- [AI Musicpreneur — $600M ARR, IPO, AI disclosure](https://www.aimusicpreneur.com/ai-tools-news/elevenlabs-600-million-arr-ceo-ipo-ai-disclosure-2026/)
- [Sacra — revenue, valuation & funding](https://sacra.com/c/elevenlabs/)
- [Crypto Briefing — enterprise revenue surpasses consumer](https://cryptobriefing.com/elevenlabs-enterprise-revenue-surpasses-consumer/)
- [ElevenLabs — Japan subsidiary](https://elevenlabs.io/blog/elevenlabs-establishes-japanese-subsidiary-elevenlabs-gk)
- [ElevenLabs — Korea expansion](https://elevenlabs.io/de/blog/expanding-into-korea)
- [ElevenLabs — Australia & NZ](https://elevenlabs.io/ja/blog/elevenlabs-expands-presence-in-australia-new-zealand)
- [Business Today — India $100M revenue goal](https://www.businesstoday.in/technology/news/story/elevenlabs-bets-big-on-india-with-100-million-revenue-goal-major-hiring-push-517299-2026-02-20)
- [Business Today — Activate invests](https://www.businesstoday.in/technology/story/activate-invests-in-elevenlabs-bets-big-on-indias-voice-ai-opportunity-531498-2026-05-14)
- [ElevenLabs — Voice AI for India scale](https://elevenlabs.io/fr/blog/voice-ai-for-india-scale)
- [CIO Elets — India office evaluation](https://cio.eletsonline.com/?p=76018)
- [To-in × ElevenLabs Japan dubbing](https://aeo.washinmura.jp/ai/%E6%A0%AA%E5%BC%8F%E4%BC%9A%E7%A4%BE%E5%8D%81%E5%8D%B0/en/news/2026-06-16-%E5%A4%9A%E8%A8%80%E8%AA%9E%E7%BF%BB%E8%A8%B3%E3%81%AE%E5%8D%81%E5%8D%B0-%E3%82%A4%E3%83%AC%E3%83%96%E3%83%B3%E3%83%A9%E3%83%9C%E7%A4%BE%E3%81%A8%E6%8F%90%E6%90%BA%E3%81%97-ai%E9%9F%B3%E5%A3%B0%E3%82%92%E6%B4%BB%E7%94%A8%E3%81%97%E3%81%9F%E4%BC%81%E6%A5%AD%E5%90%91%E3%81%91%E5%A4%9A%E8%A8%80%E8%AA%9E%E5%90%B9%E3%81%8D%E6%9B%BF)
- [01net — OpenHome × ElevenLabs Japan](https://www.01net.it/openhome-and-elevenlabs-partner-to-grow-voice-ai-development-in-japan/)
- [CB Insights — company profile](https://www.cbinsights.com/company/eleven-labs)
- [CMSWire — ElevenLabs vs Big Tech](https://www.cmswire.com/customer-experience/will-elevenlabs-survive-big-techs-dominance-in-conversational-ai)

**Competition**
- [Inworld — ElevenLabs alternatives (competitor blog)](https://inworld.ai/resources/elevenlabs-alternatives)
- [Activepieces — ElevenLabs alternatives 2026](https://www.activepieces.com/blog/best-elevenlabs-alternatives-in-2026-compared)
- [HeyGen — ElevenLabs alternatives](https://www.heygen.com/blog/elevenlabs-alternatives)
- [OrcaRouter — Gemini Live vs ElevenLabs](https://www.orcarouter.ai/blog/gemini-3-8-live-vs-elevenlabs)

**Tech stack & infra**
- [ElevenLabs docs — custom LLM](https://elevenlabs.io/docs/eleven-agents/customization/llm/custom-llm)
- [ElevenLabs changelog](https://elevenlabs.io/docs/changelog)
- [SpeechTech — Google Cloud + NVIDIA Blackwell partnership](https://www.speechtechmag.com/Articles/News/Speech-Technology-News/ElevenLabs-Partners-with-Google-Cloud-for-Cloud-Services-and-NVIDIA-Blackwell-GPUs-173734.aspx)
- [ZenML — GPU infrastructure case study](https://www.zenml.io/llmops-database/scaling-voice-ai-with-gpu-accelerated-infrastructure)
- [Air Street Press — "compute scarcity is an engineering problem"](https://press.airstreet.com/p/angelos-perivolaropoulos-elevenlabs)
- [Sacra — quality vs cheaper rivals](https://sacra.com/chat/h/d449f40a-cdec-45d3-aa74-471443e6d434)

**Keystone clients**
- [ElevenLabs — Deutsche Telekom](https://elevenlabs.io/blog/deutsche-telekom)
- [ElevenLabs — Series D post](https://elevenlabs.io/de/blog/series-d)
- [Tech Times — UMG licensing deal](https://www.techtimes.com/articles/327314/20260911/elevenlabs-signs-first-lawsuit-free-ai-music-deal-umg-fans-get-remix-platform.htm)

**People, culture & legal**
- [ElevenLabs — CRO announcement](https://elevenlabs.io/blog/cro)
- [The Next Web — Ashley Kramer joins as CRO](https://thenextweb.com/news/elevenlabs-ashley-kramer-chief-revenue-officer-openai-ai-act-article-50)
- [Sifted — no job titles at ElevenLabs](https://sifted.eu/articles/no-job-titles-elevenlabs)
- [AOL/Business Insider — 20 micro-teams, CEO interviews every hire](https://www.aol.com/articles/elevenlabs-ceo-says-startup-runs-060611326.html)
- [Revelio Labs — headcount estimate](https://www.reveliolabs.com/companies/eleven-labs/employees)
- [Pulse — hiring 120 sales reps](https://www.pulse.bot/entrepreneurship/news/elevenlabs-to-hire-120-new-sales-reps-doubling-team-amid-500m-funding-91371665-d839-4ea9-a8cc-d3bca354dd32/)
- [Law360 — voice-training suits](https://www.law360.com/articles/2476478/google-meta-hit-with-suits-over-use-of-voices-for-ai)
- [The Voice Realm — ElevenLabs lawsuit](https://www.thevoicerealm.com/blog/a-look-into-the-elevenlabs-lawsuit/)
- [Wikipedia — ElevenLabs](https://en.wikipedia.org/wiki/ElevenLabs)
