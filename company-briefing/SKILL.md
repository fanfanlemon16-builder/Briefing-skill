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
- **People** — key-person dependence on founders, leadership gaps, recent senior hires/departures, hiring bottlenecks.
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

See `examples/elevenlabs.md` for a completed briefing at the target level of depth.
