---
id: docs/04_execution_instrumentation/runtime-notes.md
title: Execution notes — preparation mode and instrumentation
document_class: core-doc
phase: 04_execution_instrumentation
visibility: internal
status: draft
---

# Mode

**Preparation mode.** Design and governance artifacts are being built; nothing
runs against the live server. Execution unlocks in this order:

1. Member approval formalized (relaunch-gate contract).
2. Roles letter agreed and stored.
3. n8n certificate renewed, with auto-renewal confirmed.
4. Dry-run week inside the approval queue (zero publishing).
5. First governed week live.

# Instrumentation

- **Ops scorecard (monthly):** posts published vs planned, approval turnaround,
  active members, new members by invitation, incidents.
- **Governance score:** `kob audit` of this repository, monthly, recorded in the
  verification document with its remediation batches.
- **Editorial check:** every published post traceable to an approved draft and
  its source pack; any post that skipped the queue is an incident.

# Failure behaviour

Automation is an accelerator, never a single point of failure: with n8n down,
the cycle runs manually with the same approvals. A missed week is recorded as
a missed week — the scorecard tells the truth or it is worthless.
