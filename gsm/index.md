---
layout: default
title: GSM
nav_order: 1
has_children: true
---

# GSM — the open standard
{: .no_toc }

The **Generative System Model (GSM)** is the open systemic standard at the foundation of Poesis. It is not a product you deploy — it is the shared model that every Poesis product implements: the **[SIE]({% link sie-definition.md %})** engine hosts and enforces it, and domain applications such as **[ITIP]({% link itip/index.md %})** translate it into their domain.

GSM is to the **THINK** side of IT — *defining and governing* systems — what OpenTelemetry is to the **RUN** side: one open, vendor-neutral standard, so governed definitions are portable across tools instead of trapped in proprietary silos. It turns governance from prose that *describes* systems into definitions that *generate* them: typed, versioned, and machine-evaluable.

## What GSM fixes

- **DNA — the governance grammar.** Every governed concern is expressed as a **Directive** (strategic intent), a **Norm** (a tactical, machine-evaluable assertion), and an **Ascription** (the versioned, lifecycle-managed binding of a definition to its subject).
- **Eight primitives.** Structure, Mechanism, Effector, Receptor, Interaction, Archetype, Directive, Norm — a deliberately small, fixed core.
- **Archetypes — the shared semantics.** Typed domain schemas that carry meaning (vocabulary, grammar, and constraints) so it travels with the type rather than living in prose.

## In this section

The GSM open standard is published as a CNCF-style document set:

- **[Manifesto]({% link gsm/manifesto.md %})** — what GSM is, why it must exist, and the ten principles it commits to.
- **[Primer]({% link gsm/primer.md %})** — a non-normative introduction that builds intuition for the model with a running example, before the formal rules.
- **[Specification]({% link gsm/specification.md %})** — the normative open standard: the eight primitives, the DNA governance grammar, the Archetype type system, the Ascription lifecycle, the expression-language profiles, the canonical JSON interchange, and conformance.
- **[Conformance]({% link gsm/conformance.md %})** — the testable requirement catalog with stable assertion IDs and conformance profiles.
- **[Charter]({% link gsm/charter.md %})** — the proposed project governance (mission, roles, decision-making, licensing).
- **[CNCF Sandbox Proposal]({% link gsm/cncf-sandbox-proposal.md %})** — the draft application proposing GSM to the CNCF at the Sandbox maturity level.

GSM also has an academic-publication track (a paper and a book); that track is separate from this documentation site and from the normative Specification above.
