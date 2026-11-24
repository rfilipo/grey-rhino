# Automation — the n8n pipeline

The designed pipeline (RhinoOps V1). Workflows, in order:

1. **morning-briefing** — collects the registered sources, assembles the source
   pack of the day, and opens the briefing app.
2. **post-drafter** — for each item in the weekly cycle, builds the preflight
   environment (source pack + editorial policy + channel format) and drafts
   with the local model.
3. **approval-router** — files drafts into the approval queue and notifies the
   operators; records approvals, edits and rejections.
4. **publisher-webhooks** — publishes approved items through one webhook per
   channel. **Webhook URLs are secrets: they live in the vault, never here.**
   This file names workflows and channels only.

## Dependencies and failure behaviour

- **Blocker (2026-11-24):** the n8n TLS certificate expired on 2026-11-13.
  Renewal (with auto-renewal confirmed) is a precondition of the execution phase.
- If n8n is down, the cycle runs by hand with the same approvals. Automation
  accelerates the operation; it is never its single point of failure.
- Every automated action lands in #logs-equipe (designed) or the ops scorecard.
