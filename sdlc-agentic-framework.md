---
layout: default
title: SDLC Agentic Framework
nav_order: 6
has_children: true
---

# SDLC Agentic Framework

{: .no_toc }

**SDLC Agentic Framework** is the multi-agent SDLC orchestration layer for VS Code / GitHub Copilot.
It brings SAFe-shaped portfolio–program–iteration orchestration, a specialist bench, and
deterministic model routing directly into your IDE — used to build and evolve Poesis products.

Three orchestrator agents collaborate in a strict hierarchy:

| Agent | SAFe layer | Responsibility |
|---|---|---|
| `@vmo-orchestrator` | Portfolio (VMO) | Strategic Themes, Epic intake, Portfolio Kanban |
| `@rte-orchestrator` | Program / ART | Feature breakdown, PI Planning, Architecture gate, PR merge |
| `@sm-orchestrator` | Team / Iteration | Story grooming, pair-programming micro-cycle, PR gate prep |

All orchestrators are dispatched from a single entry point — `@vmo-orchestrator`.
No orchestrator writes production code; they delegate to `ai-team-dev`, `ai-team-qa`,
and the SE:\* specialist bench.

## In this section

- **[Quickstart]({% link sdlc-agentic-framework/quickstart.md %})** — install and run your first orchestrated PR in under 30 minutes
