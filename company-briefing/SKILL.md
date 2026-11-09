---
name: company-briefing
description: Produce an investor-style briefing on a company (especially AI-native or new-business-model startups) from just its name. Covers what it does, how it makes money, HQ, funding and backers, biggest revenue stream, competitive landscape, a deep moat analysis (own models vs built on frontier labs, keystone clients), risks and dependencies (people, culture, cost, infrastructure, legal), Asia footprint, and questions to ask if considering joining. Use when the user gives a company name and asks for a briefing, profile, rundown, "tell me about X", "who is X", or "should I join X".
---

# Company Briefing

Turn a company name into a sourced, skimmable briefing. The reader wants to understand the company inside out — as an investor, partner, or potential employee — with a dedicated look at Asia.

## Workflow

1. **Disambiguate.** Confirm which company is meant. If two plausible companies share the name, ask once; otherwise pick the obvious one and state it in the header.
2. **Research in parallel.** Run the searches in `references/research-playbook.md` in one batch, then a second batch for thin sections. Do at least one search per section. Put the current year in queries.
3. **Reconcile.** Apply the rules below before writing.
4. **Write** using `references/template.md`. Tables over prose where data is list-shaped.
5. **Close** with "Open questions" and "Sources". Never skip sources.

## Reconciliation rules

- **Date every number.** "$600M ARR (Sep 2026, CEO to TechCrunch)" — never a bare figure.
- **ARR ≠ revenue.** Say which one it is, and that private-company ARR is self-reported.
- **Primary round vs secondary.** Separate new money (Series X) from tender offers / secondary sales. Report "Latest primary round" and "Latest valuation mark" separately.
- **Lead vs participants.** Lead(s) first, then notable new and returning backers. Call out strategic investors — they often signal partnerships or dependencies.
- **HQ can be ambiguous.** Distinguish legal HQ, operational HQ, and where R&D sits.
- **Estimates are labelled.** Third-party numbers (Sacra, Latka, Revelio, blogs) are marked as estimates.
- **Analysis is labelled.** Moat, risk ratings, and competitive judgments are marked *(analysis)* and backed by evidence.
- **Confidence tags** for any claim that isn't a company announcement or tier-1 report:
  - ✅ **Confirmed** — company announcement, filing, partner press release, tier-1 press.
  - 🟡 **Reported** — single source or secondary press, not confirmed by the company.
  - 🔍 **Signal** — job postings, docs, changelogs, localized pages. Useful but not proof.
- **Don't invent.** If a field can't be found, write "Not disclosed" and add it to Open questions.
- **Watch for name collisions.** Common names (e.g. "Sierra") pull in unrelated companies with their own funding news. Check every number belongs to the right company, and say which company it is in the header.
- **Use the latest ARR for multiples.** Fast growers change monthly. Compute valuation ÷ ARR with the *newest* ARR, and say if the round was priced on an older figure (e.g. "~79x at the round, ~40x on today's ARR").
- **Company blog beats aggregators for ARR.** Search `{Co} ARR {current month}` and check the company's own blog before trusting Latka/Sacra figures.

## Official filings beat data sites (learned from FINBOURNE)
Many private companies outside the US must file accounts publicly. Check these **before** trusting aggregator revenue figures, which can be off by 2–4x:
- 🇬🇧 UK — Companies House (free; Endole and similar sites summarise it)
- 🇮🇪 Ireland — CRO · 🇩🇪 Germany — Unternehmensregister · 🇫🇷 France — Pappers/Infogreffe
- 🇸🇬 Singapore — ACRA · 🇭🇰 Hong Kong — Companies Registry · 🇦🇺 Australia — ASIC · 🇯🇵 Japan — official gazette (kanpō) balance-sheet notices
From filings, report turnover, profit/loss, cash, net assets, and any going-concern note. Mark the filing period, since filed accounts can be 6–18 months old.

## Classify the company first
State in the header whether it is **AI-native** (product is built around models it trains or deeply depends on), **AI-application** (built on rented frontier models), or **AI-adopter** (an established software/fintech product adding AI features). This sets how to read the moat and the risks.

## Moat logic for application-layer companies (learned from Sierra)
If the core models are rented, don't stop at "it's a wrapper". Explain where the moat comes from instead: orchestration and evaluation tooling, integrations into customer systems, deployment know-how, pricing model, data loop, and distribution. Also check:
- **Pricing-model risk** — e.g. outcome-based pricing means the company pays for model calls on failed attempts.
- **Services intensity** — long, hands-on deployments act as a moat but drag on margins.
- **Supplier-as-competitor** — the model provider could sell the same solution directly.

## Section guidance

### Competitive landscape
Map competitors **by layer**, not as one flat list. Typical layers for AI companies:
- **Direct specialists** — same product, same buyer.
- **Frontier labs / Big Tech** — OpenAI, Google, Anthropic, Meta, Microsoft, Amazon bundling a "good-enough" version.
- **Application-layer players** — companies selling the end solution, who may be customers *and* competitors.
- **Open source / self-hosting** — the price floor.
- **Asia-local rivals** — local champions in the markets covered in the Asia section.

For each main rival: where they beat the company, where the company wins. Flag **frenemies** (a supplier or partner who also competes). End with a one-line read on how the market is moving (consolidating, commoditizing, splitting by use case).

### Moat deep dive
Answer these explicitly:
1. **Tech stack ownership.** Layer by layer (core models, LLM/reasoning, data, compute/cloud, distribution): is it **built in-house**, **rented from a frontier lab/vendor**, or **open source**? This is the single most important question for an AI company — a wrapper on someone else's model has a very different moat from a company training its own.
2. **Data advantage.** Proprietary or licensed data, data flywheel from usage, rights/consent position.
3. **Keystone clients.** Named customers that anchor revenue, credibility, or a vertical. Note depth (pilot vs multi-year, on-site engineers, co-development) and any concentration risk.
4. **Switching costs & network effects.** What makes leaving painful once integrated.
5. **Distribution.** Brand, developer adoption, channel partners.
6. **Bear case.** Who could commoditize this, and how fast.

End with a moat rating *(analysis)*: **Strong / Moderate / Thin**, and one sentence on what it really rests on.

### Risks & dependencies
Cover each category; rate severity **High / Medium / Low** *(analysis)* with evidence:
- **People** — key-person dependence on founders, leadership gaps, recent senior hires/departures, hiring bottlenecks, and **founder outside roles or conflicts** (board seats at suppliers or competitors).
- **Culture & org** — structure, how it is scaling, employee sentiment (Glassdoor/Blind if found), remote model.
- **Cost & unit economics** — compute cost, gross margin, price pressure, burn.
- **Foundational infrastructure** — single cloud, GPU supply, reliance on third-party models/APIs, and whether suppliers are also competitors.
- **Customer concentration** — reliance on a few large clients or one channel.
- **Legal & regulatory** — lawsuits, IP/data rights, AI regulation (EU AI Act, US state laws, Asia rules), misuse/reputation.
- **Valuation & capital** — valuation multiple vs revenue, what has to go right.

### Asia footprint
Go market by market where anything exists. Check at minimum: Japan, South Korea, India, Greater China (incl. HK/Taiwan), Singapore & Southeast Asia, Australia/NZ. For each: presence, revenue signal, customers & partners (type: customer, reseller/channel, tech integration, government, investor), local competitors. End with a one-line verdict.

### If you're considering joining
Tailor to *this* company — no generic interview questions. Group into:
- **Strategy & moat** — the questions the risks and moat sections left open.
- **Business health** — revenue quality, margins, runway, path to IPO/exit.
- **People & culture** — how decisions get made, attrition, what the founders are like to work with.
- **The role** — scope, success in 6–12 months, who you'd report to.
- **Equity & compensation** — share type, strike vs latest valuation (primary *and* tender), vesting, liquidity/tender history, preference stack.
- **Asia** (if relevant) — local autonomy, headcount plans, revenue targets.

Add **"Check yourself"**: things to verify outside the interview (Glassdoor/Blind, LinkedIn tenure of recent leavers, back-channel with ex-employees, court records).

## Output

Default: markdown in chat. If the user asks for a file, save to `briefings/<company-slug>-<YYYY-MM-DD>.md`.

Completed briefings at the target depth:
- `examples/elevenlabs.md` — a company that trains its own models (voice AI).
- `examples/sierra.md` — an application-layer company on top of frontier labs (customer-service agents).
- `examples/finbourne.md` — an established fintech adding AI, with revenue from public filings (UK).
