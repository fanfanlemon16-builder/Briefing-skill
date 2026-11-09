# Briefing-skill

A Claude skill that turns a company name into a sourced briefing: what it does, how it makes money, HQ, latest funding and backers, moat, biggest revenue stream, and its **Asia footprint** (offices, revenue, customers, partners).

Built for keeping up with AI-native and new-business-model companies.

## Layout
```
company-briefing/
  SKILL.md                       # instructions + reconciliation rules
  references/research-playbook.md  # search queries and source priorities
  references/template.md         # output format
  examples/elevenlabs.md         # worked example
```

## Install
Copy `company-briefing/` into `~/.claude/skills/` (Claude Code) or upload it as a skill in Claude.ai. Then ask: *"Brief me on ElevenLabs"*.
