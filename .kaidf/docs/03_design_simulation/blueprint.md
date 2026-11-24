---
id: docs/03_design_simulation/blueprint.md
title: Blueprint — the RhinoOps target design
document_class: core-doc
phase: 03_design_simulation
visibility: internal
status: draft
---

# Pipeline (the weekly cycle as a loop)

1. **Collect** — n8n gathers the week's inputs from the registered sources
   (ops/sources.md): market data, central-bank calendars, the editorial calendar.
2. **Preflight** — before drafting, the environment is assembled: source pack +
   editorial policy + channel format + the week's contract. No draft starts
   without its environment (the model-environment principle, K-AIDF #163).
3. **Draft** — the local model drafts each post inside its channel's format and
   the 2,000-character discipline. Analysis conclusions belong to the analysts;
   the model structures, summarizes and checks — it never issues a call.
4. **Approve** — drafts wait in the approval queue (#fila-aprovacao). A human
   approves, edits or rejects; the decision is recorded.
5. **Publish** — webhooks post per channel. If automation is down, the same
   approved text is pasted by hand: the operation never depends on the pipeline.
6. **Measure** — posts, approvals and member activity feed the monthly scorecard;
   `kob audit` scores this repository's governance.

# Contracts (seed set, created through the kob flow)

- **relaunch-gate** — the member approval: parties, what is being approved
  (operation model, roles, red lines), evidence of consent, exit criteria.
- **weekly-cycle** — the standing contract of the editorial week: deliverables
  per channel, owners, approval rule, measurement.

# Apps (seed set)

- **approval-queue** (persistent, web) — the drafts awaiting decision, with the
  source pack attached to each draft.
- **briefing** (ephemeral) — assembles the morning briefing from the source pack.

# Bot (later phase, only if the simple path proves insufficient)

RinoBot with least privilege: no administrator, no DMs, read/write only in its
channels, every action logged in #logs-equipe. The V1 decision stands: invite +
webhooks first; a bot is earned, not assumed.

# Security

Configuration as code in this repository; secrets only in the vault; an incident
plan (revoke webhooks first, rotate, announce in #geral); a monthly Rhino Audit
of permissions and published content against the editorial policy.
