---
layout: default
title: Milestones & Versions
nav_order: 5
---

# Milestones & Versions

{: .no_toc }

This page is the **single, canonical reference** for every delivery statement in Poesis content — on this site and on [poesis.cloud](https://poesis.cloud). Wherever a page mentions a milestone tier or a version, this page defines what it means.

> **The clause.** Milestones and versions express **ordered intent and implementation reality — not delivery commitments and not dates**. Ordering may change; unshipped items may be re-scoped or dropped. The only dated target Poesis publishes is the GSM specification publication (≈ October 2026).

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Version semantics

Each **product** carries its own version line (solutions are not versioned):

- **0.x** — pre-GA. Each minor is a named feature batch. Anything may change.
- **1.0 — GA / production-ready**: commercially supportable, documented, covered by the product's stated quality gates.
- **1.x minors** — post-GA feature batches, backward compatible.
- **Majors ≥ 2** — breaking or architectural shifts only.

## Milestone vocabulary

| Marker | Meaning |
| --- | --- |
| **Shipped (✓ vX.Y)** | implemented today, delivered in the version shown |
| **v1.0 (MVP/GA)** | the first-release scope — production-ready, commercially supportable |
| **v1.x** | post-GA feature batches; unordered unless stated |
| **Unversioned** | exploratory / research-tier; may never ship |

The ITIP Web Application catalogue also uses **v1 / v2**: **v1** is the v1.0 (MVP/GA) scope; **v2** is the v1.x scope.

## Product version milestones

Versions are ordered, not scheduled. Each line below is one product's version timeline; the filled segment and dots mark what has shipped or reached GA.

{% include roadmap_timeline.html %}

## How versions depend on each other

1. **GSM Specifications are at 1.0** — SIE products conform to it; their GA is gated on hardening, not on the standard.
2. **Definition Blackboard Manager GA gates the Code Sourcer GA** — the sourcer needs a stable server contract.
3. **The Agentic Harness is at 1.0** — the Organization and Workspace version against its stable CLI contract; their GA is gated on their own scope, not the harness.
4. **ITIP GA does not gate on SIE GA** — ITIP 1.0 may ship against SIE 0.x.
5. **Definition Blackboard Manager GA also gates the SAF SIE Bridge GA** — the same stable server contract the ITIP sourcer depends on.
