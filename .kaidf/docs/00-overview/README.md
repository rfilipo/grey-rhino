---
id: docs/00-overview/README.md
title: Grey Rhino operations case — overview
document_class: core-doc
phase: root
visibility: internal
status: draft
---

# Overview

This repository is the operations home of the Grey Rhino case: a Discord community
(crypto, stocks, FX, money) operated under the K-AIDF framework. It is the second
case of the series — Vim-AI governed *code*; this one governs an *operation*:
planning, strategic management, automation and content generation with general AI.

The operation design is RhinoOps (approved 2026-11-13): sources feed a self-hosted
n8n; a local model drafts under a preflight environment (market context + editorial
policy); a human approval queue decides; webhooks publish per channel; a monthly
KAIDF-AMM audit of this repository scores the governance.

The case runs in preparation mode until the server's members formally approve the
relaunch (suspension of 2026-11-18). The phase documents carry the real state:
intent and constraints (01), the as-is map (02), the target design (03), execution
notes and instrumentation (04), and the verification evidence list (05).
