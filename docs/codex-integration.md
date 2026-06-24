# Codex Integration

This branch tracks a Codex-first retooling path for `subbot`.

The current production app scans Gmail through browser OAuth, builds subscription groups in the frontend, and saves aggregate scan results through the Go API. The Codex adaptation keeps that source intact while adding an external Codex skill that uses the Gmail connector for read-first inbox triage and approval-gated cleanup.

Canonical local Codex skill:

```text
gmail-inbox-operator
```

The skill is intentionally outside this source repo so private mailbox routing and connector workflow guidance do not get mixed into the public application code. Future repo changes can add an import/export bridge if the web dashboard should display scans produced by Codex.
