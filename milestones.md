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

Feature catalogues on this site use five tiers, which map to versions canonically:

| Tier | Meaning |
| --- | --- |
| **Foundation** | shipped in the product's current 0.x (implemented today) |
| **Near-term** | the product's next minor |
| **Mid-term** | a later 0.x minor (ordered after Near-term) |
| **Future** | a 1.x post-GA batch |
| **Exploratory** | unversioned — research-tier; may never ship |

The ITIP Web Application catalogue uses **v1 / v2**: **v1** is the 1.0 (GA) scope; **v2** is the 1.x scope.

## Product version milestones

Versions are ordered, not scheduled. ✅ marks shipped batches.

### ITIP

**Web Application** — current 0.0 (active design)

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 | Definition authoring core: Registry & Inventory; Structures; Archetypes; Directives; Norms; Mechanisms; Interactions; Ascription lifecycle |
| 0.2 | Frameworks management: Catalog; Framework detail; Stack Composer |
| 0.3 | Truth sourcing management: Sources; Source detail; Sync Jobs |
| 0.4 | Deliverables: Templates; Template Editor; Generated & Jobs · Admin: Users; Integrations |
| **1.0 (GA)** | All v1 capabilities, hardened (auth, tenancy, WCAG 2.1 AA) |
| 1.x | v2 capabilities: dashboards; Evaluation (bilateral appraisal-indicator classes); Lenses; Simulation; Review; Guided Workflows; Activity; Sessions |

**Definition Blackboard Code Sourcer** — current 0.1

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 ✅ | Blackboard contribution posting; confidence / provenance envelopes; sealed byte-stable streams |
| 0.2 | Core sourcing pipeline: inventory & classification; hybrid deterministic + LLM extraction; merge / dedupe; GSM-JSON output with provenance |
| 0.3 | IT-domain source adapters: git repositories; API contracts (OpenAPI / gRPC / AsyncAPI); infrastructure (Helm / Dockerfile / Terraform) |
| **1.0 (GA)** | Pipeline + IT-domain adapters production-ready against a GA Definition Blackboard Manager |
| 1.x | Legal & regulatory adapters (EUR-Lex); standards adapters (ISO/IEC, NIST CSF, CIS) |

### SIE

**Definition Manager** — current 0.1

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 ✅ | GSM Definitions management RESTful API; 8-primitive GSM core + DNA authoring; Ascription lifecycle state machine; retention/versioning |
| 0.2 | Descriptive analytics; assurance & safety; system presets |
| 0.3 | Prescriptive analytics (remediation, homeostasis, LLM-assisted DNA bootstrap) |
| 0.4 | Diagnostic + predictive analytics (root-cause, anomaly, forecasting, blast-radius, what-if) |
| **1.0 (GA)** | Conformant implementation of GSM specification 1.0; production multi-tenant hardening |
| unversioned | Emergence & cross-domain inference (Exploratory) |

**Operator** — current 0.1

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 ✅ | GSM Norms evaluation API; GSM Mechanisms execution API; sandboxed rule runtime; typed effect dispatch |
| 0.2 | Closed-loop control maturation with the Definition Manager analytics batches |
| **1.0 (GA)** | Conformant runtime for GSM specification 1.0; reproducible-verdict guarantees documented |

**Definition Blackboard Manager** — current 0.1

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 ✅ | OPEN → SEALED → BYTE_STABLE lifecycle + isolation invariant; schema validation against Panels; append-only audit ledger; confidence / provenance envelopes |
| 0.2 | Promotion path maturation (blackboard → governed Definitions in the Definition Manager) |
| **1.0 (GA)** | Production-ready collaborative sourcing service; stable client contract for sourcers |

### GSM

**Specifications** — current 0.1 (Working Draft, publication pending)

| Version | Milestone |
| --- | --- |
| 0.2 | Public publication of the document set on this site (target ≈ October 2026) |
| 0.x | Draft revisions from implementation feedback and early adopters |
| **1.0** | The standard's GA: normative content frozen for implementations; conformance catalog ID-stable; ready for neutral-stewardship submission |

**Frameworks** — current 0.1 (261 sourced schemas published)

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 ✅ | Domain / standard / legal vocabularies as typed Archetypes; evaluable legal Directives & Norms with clause provenance |
| 0.2 | Catalogue documentation + sourcing-method & provenance rules; executable standard Mechanisms |
| **1.0 (GA)** | Versioned, maintained catalogue with a stability contract on `$id` namespaces |

### SAF

**Agentic Harness** — current 0.1

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 ✅ | Deterministic workflow & step resolution; skill/instruction injection; LLM routing; artifact validation; step authorization; session ledger |
| 0.2 | Additional host adapters behind the same adapter contract |
| **1.0 (GA)** | Stable eleven-function CLI contract; multi-host parity |

**SAFe Agentic Organization** — current 0.1

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 ✅ | Three orchestrators + specialist bench; SAFe ceremony workflows; artifact schemas & templates; GitHub Copilot bundle |
| 0.2 | Ceremony/workflow coverage expansion; harness-conformance hardening |
| **1.0 (GA)** | Complete SAFe layer coverage on a GA harness |

**Agentic Workspace** — current 0.1

| Version | Milestone — feature batch |
| --- | --- |
| 0.1 ✅ | Workspace data plane: committed state = workspace state; one validated write = one commit |
| 0.2 | Installer (wires harness + organization + artifacts into a working tree) |
| 0.3 | CI/CD artifact pipelines (same deterministic checks as local) |
| **1.0 (GA)** | Turnkey governed workspace: install once, deliver governed, gates in CI |

## How versions depend on each other

1. **GSM 1.0 gates SIE GA** — the Definition Manager and the Operator reach 1.0 only against a frozen GSM 1.0.
2. **Definition Blackboard Manager GA gates the Code Sourcer GA** — the sourcer needs a stable server contract.
3. **Agentic Harness GA gates the Organization and Workspace GA** — both version against the harness's stable CLI contract.
4. **ITIP GA does not gate on SIE GA** — ITIP 1.0 may ship against SIE 0.x; its compliance-evaluation batches (1.x) track the Definition Manager analytics batches.
