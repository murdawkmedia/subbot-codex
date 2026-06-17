# Codex Integration

This branch tracks a Codex-first retooling path for `subbot`.

The current production app scans Gmail through browser OAuth, builds subscription groups in the frontend, and saves aggregate scan results through the Go API. The Codex adaptation keeps that source intact while adding an external MurphyOS skill that uses the Gmail connector for read-first inbox triage and approval-gated cleanup.

Canonical MurphyOS skill:

```text
D:\Users\Murphy\Documents\MurphyOS\codex-skills\gmail-inbox-operator\SKILL.md
```

The skill is intentionally outside this source repo so MurphyOS operational rules, private mailbox routing, and connector workflow guidance do not get mixed into the upstream application code. Future repo changes can add an import/export bridge if the web dashboard should display scans produced by Codex.
