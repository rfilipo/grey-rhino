# Grey Rhino — a Discord community operated with K-AIDF

**Case #2 of the K-AIDF case series** (after [Vim-AI](https://github.com/rfilipo/vim-ai), the code case audited to 100/100).
Here the product is not code — it is an **operation**: the Grey Rhino (Rinoceronte Cinza) Discord server,
a small community about crypto, stocks, FX and money, running since November 2023 and published by
Monsenhor (Ricardo Filipo) and Yuno (Daniel Filipo).

This repository holds the operation *as code*: editorial policy, the weekly cycle, the automation
design, and the governance that binds them — planned, drafted and measured under the K-AIDF framework.

## The operation (RhinoOps)

```
sources -> n8n -> local-model drafts (preflight: market context + editorial policy)
        -> human approval queue -> webhooks per channel -> measure -> monthly audit
```

Nothing is published without a human decision. The model drafts, structures and summarizes;
humans own every conclusion and every post.

## Status: PREPARATION MODE

The server is **suspended since 2026-11-18, pending formal approval by its members**. This case is
being built in preparation mode: intent, mapping and design proceed now; execution (the live
pipeline) unlocks only with that approval — the case's gate contract. Two more dependencies are
recorded in the phase documents: the expired n8n TLS certificate (team) and the roles letter
(Ricardo x Yuno) awaiting signature.

## Red lines (non-negotiable, enforced as guardrails)

- **No investment recommendations or signals.** Education and scenarios only (CVM/SEC line).
- **Nobody is ever required to appear** — no lives, video or voice are a condition for any member.
- **Secrets live only in the vault** — webhook URLs and tokens never enter this repository.
- **Every publication passes a human gate.** Automation proposes; humans dispose.

## Layout

- `.kaidf/` — the K-AIDF scaffold: specs and the five phase documents of this case.
- `contracts/` — the operation's contracts (created through the kob flow; see its README).
- `apps/` — the operation's instant apps (approval queue, briefing).
- `ops/` — the working documents: editorial policy, weekly cycle, sources.
- `automation/` — the n8n pipeline design and the webhook map (names only, never URLs).

## How this case runs

Same method as Vim-AI: the mentor workflow walks the five phases with human acceptance at each
gate; `kob audit` (KAIDF-AMM) scores the governance of this repository; remediation proceeds in
reviewed batches. When the cycle completes, the story is written in `CASE.md` at this root.
