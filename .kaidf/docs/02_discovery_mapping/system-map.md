---
id: docs/02_discovery_mapping/system-map.md
title: System map — the server and its systems as they are
document_class: core-doc
phase: 02_discovery_mapping
visibility: internal
status: draft
---

# The server as-is

- **Grey Rhino (Rinoceronte Cinza)**, Discord, since November 2023.
- **Members (5):** monsenhor (Ricardo Filipo, host/editor), YunoEwig (Daniel Filipo,
  owner and chief analyst), and three reading members.
- **Channels:** #geral, #educativo, #analise-btc, #mercados-tradicionais,
  #analise-probabilistica, #cripto-oportunidades, #trads-oportunidades,
  #outros-assuntos, #international, plus a voice channel.
- **Current mode:** fully manual. Two publishers (Monsenhor, Yuno). No bots, no
  webhooks, no automation running today.

# Assets that already exist

- Launch kit: server structure, ready-to-paste blocks, anti-scam rules, Semana 1 plan.
- Plano V1 — RhinoOps architecture (approved 2026-11-13): pipeline, security, phases 0-4.
- Plano V2 — roles, remuneration in three tempos, growth design, weekly live format
  ("Mesa do Rinoceronte", Saturdays, 45 min, audio + charts, participation by choice).
- Roles letter Ricardo x Yuno (draft, 2026-11-14) — awaiting their review/signature.
- Semana 1 posts: Mon-Wed published (2026-11-16 to 18); Thu-Sun suspended with the server.

# Systems

- **Discord** — the surface. No connector in use; publishing today is manual,
  webhooks are the designed path.
- **n8n** (self-hosted, kobkob.org) — the automation engine of the design.
  **Blocker:** TLS certificate expired 2026-11-13; renewal owned by the team.
- **kob / K-AIDF** — method and governance; this repository is its scaffold.
- **Stripe** — planned only (Rhino Pro role), inside the V1 commercial design.
- **Local models (Ollama)** — drafting and briefings; no cloud in the loop.
