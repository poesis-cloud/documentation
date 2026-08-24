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

Versions are ordered, not scheduled. ✅ marks shipped.

### ITIP

**Web Application** — current **v0.1**

| Version | Milestone |
| --- | --- |
| 0.1 ✅ | First pre-GA increment — application & BFF foundation |
| **1.0 (MVP/GA)** | GSM Definitions management + GSM Frameworks management + RBAC/ABAC, hardened |
| 1.x | Truth sourcing management · IT artifact factory · IT compliance evaluation · IT impact simulation (unordered) |

**Definition Blackboard Code Sourcer** — current **v0.0**

| Version | Milestone |
| --- | --- |
| **1.0 (MVP/GA)** | GSM Definitions automatic sourcing from code repos |

### SIE

**Definition Manager** — current **v1.0**

| Version | Milestone |
| --- | --- |
| **1.0 (MVP/GA)** ✅ | GSM Definitions management RESTful API · lifecycle enforcement · retention |
| 1.x | GSM Definitions and tooling serving (MCP) |

**Operator** — current **v0.1**

| Version | Milestone |
| --- | --- |
| 0.1 ✅ | Basic Mechanism runtime |
| **1.0 (MVP/GA)** | GSM Norms evaluation API |
| 1.x | GSM Mechanisms execution API |

**Definition Blackboard Manager** — current **v1.0**

| Version | Milestone |
| --- | --- |
| **1.0 (MVP/GA)** ✅ | KS Contributions management RESTful API · lifecycle enforcement · retention |

### GSM

**Specifications** — current **v1.0** (normative content frozen; publication of the document set pending, target ≈ October 2026)

| Version | Milestone |
| --- | --- |
| 1.0 ✅ | Eight primitives · DNA grammar · Archetyping · systemic lifecycle — frozen |
| 1.1 | Enhanced Directives and Norms model |

**Frameworks** — current **v0.1**

| Version | Milestone |
| --- | --- |
| 0.1 ✅ | First frameworks sourced |
| **1.0 (MVP/GA)** | HTTP, TOGAF, and ITIP complete & validated |
| 1.x | Remaining protocol semantics · ISO 25010 · ISO 25012 · GDPR · NIS2 · SCAP · DORA · SAFe · ITIL · catalogue update stream (unordered) |

**Research Lab** — current **v1.0.0-beta.1**

| Version | Milestone |
| --- | --- |
| 1.0.0-beta.1 ✅ | Research product extracted — generative governance and archetype referential model |
| **1.0 (MVP/GA)** | Research protocol · published programs · promotion path into GSM Change Proposals |

### SAF

**Agentic Harness** — current **v1.0**

| Version | Milestone |
| --- | --- |
| **1.0 (MVP/GA)** ✅ | Workflow & step resolution · prompt injection · LLM resolution · artifact validation · authorization · logging |

**SAFe Agentic Organization** — current **v0.1**

| Version | Milestone |
| --- | --- |
| 0.1 ✅ | First pre-GA increment — framework scaffold |
| **1.0 (MVP/GA)** | Agents · skills · workflows · instructions · artifacts |

**Agentic Workspace** — current **v0.0**

| Version | Milestone |
| --- | --- |
| **1.0 (MVP/GA)** | Workspace data plane · installer · CI/CD artifact pipelines |

**SAF SIE Bridge** — current **v0.0**

| Version | Milestone |
| --- | --- |
| **1.0 (MVP/GA)** | Harness history sourcing into GSM contributions on the Definition Blackboard Manager |

## How versions depend on each other

1. **GSM Specifications are at 1.0** — SIE products conform to it; their GA is gated on hardening, not on the standard.
2. **Definition Blackboard Manager GA gates the Code Sourcer GA** — the sourcer needs a stable server contract.
3. **The Agentic Harness is at 1.0** — the Organization and Workspace version against its stable CLI contract; their GA is gated on their own scope, not the harness.
4. **ITIP GA does not gate on SIE GA** — ITIP 1.0 may ship against SIE 0.x.
5. **Definition Blackboard Manager GA also gates the SAF SIE Bridge GA** — the same stable server contract the ITIP sourcer depends on.
