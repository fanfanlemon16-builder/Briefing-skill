---
name: company-briefing
description: Produce a one-page investor-style briefing on a company (especially AI-native or new-business-model startups) from just its name. Covers what it does, how it makes money, HQ, latest funding round and backers, moat, biggest revenue stream, and its Asia footprint (offices, revenue, customers, partners). Use when the user gives a company name and asks for a briefing, profile, rundown, "tell me about X", or "who is X".
---

# Company Briefing

Turn a company name into a sourced, skimmable briefing. The reader wants to understand the company inside out in ~3 minutes, with a dedicated look at Asia.

## Workflow

1. **Disambiguate.** Confirm which company is meant (e.g. "Eleven Labs" vs "ElevenLabs"). If two plausible companies share the name, ask once; otherwise pick the obvious one and state it in the header.
2. **Research in parallel.** Run the searches in `references/research-playbook.md` — send them in one batch. Do at least one search per section. Prefer the last 12 months; today's date matters, so put the year in queries.
3. **Reconcile.** Numbers from startups conflict constantly. Apply the rules below before writing.
4. **Write** using the template in `references/template.md`. Keep it to roughly one screen per section; tables over prose where data is list-shaped.
5. **Close** with the "Open questions" and "Sources" sections. Never skip sources.

## Reconciliation rules (learned from the ElevenLabs test run)

- **Date every number.** "$600M ARR (Sep 2026, CEO to TechCrunch)" — never a bare figure.
- **ARR ≠ revenue.** Say which one it is, and that private-company ARR is self-reported/unaudited.
- **Primary round vs secondary.** Separate new money raised (Series X) from employee tender offers / secondary sales. A tender can set a higher valuation without new cash entering the company. Report both: "Latest primary round" and "Latest valuation mark".
- **Lead vs participants.** Name the lead(s) first, then notable new and returning backers. Note strategic investors (e.g. NVIDIA, a telco) separately — they often signal partnerships.
- **HQ can be ambiguous.** Distinguish legal/registered HQ, operational HQ, and where the founders/R&D sit. If sources disagree, show the split rather than picking silently.
- **Revenue streams.** If the company doesn't disclose a split, give the best available proxy (e.g. "enterprise 55%+ vs self-serve") and label estimates from third parties (Sacra, Latka, etc.) as estimates.
- **Moat is judgment.** Label it as analysis, list the evidence for it, and give the strongest counter-argument (who could commoditize it).
- **Asia: confirmed vs signals.** Tag each Asia item as one of:
  - ✅ **Confirmed** — company announcement, signed partner, named customer, local entity.
  - 🟡 **Reported** — credible press, not confirmed by the company.
  - 🔍 **Signal** — job postings, events, localized pages. Useful but not proof of business.
- **Prefer primary sources** (company blog/newsroom, filings, partner press releases) over aggregators. When only aggregators exist, say so.
- **Don't invent.** If a field can't be found, write "Not disclosed" and add it to Open questions.

## Asia section — what to cover

Go market by market for the markets where anything exists. Check at minimum: Japan, South Korea, India, Greater China (incl. Hong Kong/Taiwan), Singapore & Southeast Asia, Australia/NZ. For each:

- Presence: local entity / office / country lead / none
- Revenue: any disclosed figure or ranking (e.g. "India is #2 market by revenue")
- Customers and partners: named, with type (customer, reseller/channel, tech integration, government, investor)
- Regulatory or competitive notes if material (e.g. China access limits, local champions)

End with a one-line verdict: how meaningful Asia is to the company today, and where it's heading.

## Output

Default: markdown in chat, following `references/template.md`. If the user asks for a file, save to `briefings/<company-slug>-<YYYY-MM-DD>.md`.

See `examples/elevenlabs.md` for a completed briefing at the target level of depth.
