# Research playbook

Run batch 1 in parallel; then run batch 2 for any section that is still thin. Replace `{Co}` with the company name and `{YYYY}` with the current year.

## Batch 1 — core facts

| # | Section | Query |
|---|---------|-------|
| 1 | Funding | `{Co} funding round {YYYY} valuation lead investor` |
| 2 | Funding | `{Co} tender offer OR secondary valuation {YYYY}` |
| 3 | Revenue | `{Co} ARR revenue {YYYY}` |
| 3b | Filings | `{Co} accounts turnover loss Companies House OR ACRA OR ASIC` (for non-US private companies) |
| 4 | Business model | `{Co} pricing business model enterprise vs self-serve revenue split` |
| 5 | Products | `{Co} products launch {YYYY}` |
| 6 | HQ & founders | `{Co} headquarters founders CEO` |
| 7 | Asia overview | `{Co} Asia Pacific expansion office` |
| 8 | Japan / Korea | `{Co} Japan partnership customers` · `{Co} Korea launch` |
| 9 | India | `{Co} India revenue customers partners` |
| 10 | SEA / ANZ / China | `{Co} Singapore Australia` · `{Co} China` |
| 11 | Latest news | `{Co} news {current month} {YYYY}` |

## Batch 2 — depth

| # | Section | Query |
|---|---------|-------|
| 12 | Competition | `{Co} competitors {YYYY}` · `{Co} vs {top rival}` · `{Co} alternatives` |
| 13 | Competition (Asia) | `{Co} competitor Japan OR Korea OR India local` |
| 14 | Tech stack | `{Co} own model OR in-house model OR trained` · `{Co} uses OpenAI OR Anthropic OR Gemini` |
| 15 | Tech stack | `{Co} docs changelog LLM` (docs often reveal which third-party models power the product) |
| 16 | Infra & cost | `{Co} cloud provider GPU compute partnership` · `{Co} gross margin compute costs` |
| 17 | Keystone clients | `{Co} largest customers case study partnership {YYYY}` |
| 18 | People | `{Co} executive hire OR departure {YYYY}` · `{Co} chief revenue officer OR CTO` |
| 19 | Culture | `{Co} culture CEO interview` · `{Co} Glassdoor` · `{Co} employees headcount` |
| 20 | Legal & regulatory | `{Co} lawsuit` · `{Co} regulation EU AI Act` |

## Where to look first

- **Company newsroom/blog and docs/changelog** — funding, launches, which LLMs or vendors power the product.
- **Partner press releases** — often the only source for Asia deals (search in the local language if needed).
- **Tier-1 press** — Bloomberg, Reuters, TechCrunch, The Information, FT; regional: Nikkei, Economic Times/Business Today, Korea Herald, Sifted, DealStreetAsia.
- **Founder podcasts** (20VC, a16z, Lenny's, etc.) — culture, org design, hiring philosophy.
- **Data aggregators** — Sacra, Crunchbase, PitchBook, CB Insights, Dealroom, Revelio. Cross-checks only; label as estimates.
- **Court records / legal press** (Law360, dockets) — lawsuits.
- **Careers page / job boards** — hiring locations, team build-outs (🔍 signal).

If a section is still thin after batch 2, use `extended` search mode once before marking it "Not disclosed".
