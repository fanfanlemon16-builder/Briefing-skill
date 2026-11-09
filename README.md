# Briefing-skill

A Claude skill that turns a company name into a sourced briefing: what it does, how it makes money, HQ, latest funding and backers, biggest revenue stream, **competitive landscape**, a **moat deep dive** (own models vs rented, keystone clients), **risks & dependencies** (people, culture, cost, infra, legal), its **Asia footprint**, and **questions to ask if you are considering joining**. Name an open role and it adds a role section with an APAC readiness check; name several and it compares them.

Built for keeping up with AI-native and new-business-model companies.

## Layout
```
.claude/skills/company-briefing/
  SKILL.md                         # instructions + reconciliation rules
  references/research-playbook.md  # search queries and source priorities
  references/template.md           # output format
  examples/sample-briefing.md      # fictional worked example
```

## Install
- **Claude Code, in this repo:** nothing to do. The skill lives in `.claude/skills/`, so any Claude Code session opened on this repo loads it. Type `/company-briefing {company}` or just send the company name.
- **Claude Code, everywhere:** copy `.claude/skills/company-briefing/` into `~/.claude/skills/`.
- **Claude.ai (web, desktop, mobile):** zip the `company-briefing/` folder and upload it under Settings → Capabilities → Skills.

Then just send a company name, e.g. *"Acme"* or *"Acme — Enterprise AE APAC"*.

## Privacy
Briefings you generate are saved to `briefings/`, which is git-ignored, so they stay on your machine and are never pushed.
