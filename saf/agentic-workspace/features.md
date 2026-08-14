---
layout: default
title: Features
parent: Agentic Workspace
grand_parent: SAF
nav_order: 1
---

# Agentic Workspace Features
{: .no_toc }

Capability catalogue for the Agentic Workspace.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Milestones

- **Foundation** — implemented today.
- **Near-term** — prioritized next (P0, feasibility now).
- **Mid-term** — planned (P1, feasibility next).
- **Future** — projected (P2–P3, later).
- **Exploratory** — research-tier; may evolve substantially or not ship.

Milestones express prioritization and engine reality — not delivery commitments.

---

## Capabilities

| Functional component | Representative features | Milestone |
|----------------------|-------------------------|-----------|
| Workspace data plane | Committed state (`HEAD`) *is* workspace state; agents stage writes, the harness validates and commits them — one validated write = one commit, attributed to the acting session | Foundation |
| Installer | Wires the harness, agents, skills, and workflows into a working tree | Near-term |
| CI/CD artifact pipelines | Validate and publish the artifacts agents produce, with the same deterministic checks that run locally | Near-term |
