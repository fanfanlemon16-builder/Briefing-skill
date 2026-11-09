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
- **Watch for name collisions.** Common names pull in unrelated companies with their own funding news. Check every number belongs to the right company, and say which company it is in the header.
- **Use the latest ARR for multiples.** Fast growers change monthly. Compute valuation ÷ ARR with the *newest* ARR, and say if the round was priced on an older figure (e.g. "~79x at the round, ~40x on today's ARR").
- **Company blog beats aggregators for ARR.** Search `{Co} ARR {current month}` and check the company's own blog before trusting Latka/Sacra figures.

## Official filings beat data sites
Many private companies outside the US must file accounts publicly. Check these **before** trusting aggregator revenue figures, which can be off by 2–4x:
- 🇬🇧 UK — Companies House (free; Endole and similar sites summarise it)
- 🇮🇪 Ireland — CRO · 🇩🇪 Germany — Unternehmensregister · 🇫🇷 France — Pappers/Infogreffe
- 🇸🇬 Singapore — ACRA · 🇭🇰 Hong Kong — Companies Registry · 🇦🇺 Australia — ASIC · 🇯🇵 Japan — official gazette (kanpō) balance-sheet notices
From filings, report turnover, profit/loss, cash, net assets, and any going-concern note. Mark the filing period, since filed accounts can be 6–18 months old.

## Classify the company first
State in the header whether it is **AI-native** (product is built around models it trains or deeply depends on), **AI-application** (built on rented frontier models), or **AI-adopter** (an established software/fintech product adding AI features). This sets how to read the moat and the risks.

## Moat logic for application-layer companies
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

## Role mode (when the user names an open job)
If the user mentions a specific role (e.g. "Enterprise Sales Director APAC"):
1. **Use the posting to disambiguate.** Search `{Co} "{role title}"` first; the posting reveals which company it is (common names often match several firms).
2. **Check the posting itself:** location, pay if listed, required experience, reporting line, "first hire" language, posting date (flag if 6+ weeks old), and whether it appears on the company's own careers board or only on aggregators.
3. **Add "The role" section** after Asia footprint: posting facts, what the job really is (buyer, sales cycle, deal shape), green flags, red flags.
4. **Run an APAC readiness check for the role:** local entity/office, licences (for regulated products), named local customers, regional leader in place, in-region support. A founding role in an empty region is a very different job from joining an existing team.
5. **Tailor "Questions to ask"** to the role, starting with the riskiest gap found.
6. **Multiple roles → add a comparison file** (`briefings/apac-roles-comparison-<date>.md`) with a side-by-side table and a short read-out.
In role mode, keep each briefing compact (shorter tables, ~10–15 sources).

## Output

Default: markdown in chat. If the user asks for a file, save to `briefings/<company-slug>-<YYYY-MM-DD>.md`.

**Briefings are the user's private output.** Never add them to the skill folder, and never commit or push them. The repo's `.gitignore` excludes `briefings/`; keep it that way. If the user wants to share one, ask first.

See `examples/sample-briefing.md` for the target depth and format. It uses a **fictional** company; never copy its facts into a real briefing.
