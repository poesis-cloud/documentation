---
layout: default
title: GSM
nav_order: 3
has_children: true
---

# GSM — the standard

{: .no_toc }

The **Generative System Model (GSM)** is the vendor-neutral systemic standard at the foundation of Poesis. It is not a product you deploy — it is the shared model that every Poesis product implements: the **[SIE]({% link sie/index.md %})** engine hosts and enforces it, and domain applications such as **[ITIP]({% link itip/index.md %})** translate it into their domain.

GSM is to the **THINK** side of IT — *defining and governing* systems — what OpenTelemetry is to the **RUN** side: one vendor-neutral standard, so governed definitions are portable across tools instead of trapped in proprietary silos. It turns governance from prose that *describes* systems into definitions that *generate* them: typed, versioned, and machine-evaluable.

GSM is a pre-1.0 working draft, source-available under **BUSL-1.1** and developed as a candidate for contribution as an open standard. BUSL-1.1 is a source-available license, not an Open Source license.

## What GSM fixes

- **DNA — the governance grammar.** Every governed concern is expressed as a **Directive** (strategic intent), a **Norm** (a tactical, machine-evaluable assertion), and an **Ascription** (the versioned, lifecycle-managed binding of a definition to its subject).
- **Eight primitives.** Structure, Mechanism, Effector, Receptor, Interaction, Archetype, Directive, Norm — a deliberately small, fixed core.
- **Archetypes — the shared semantics.** Typed domain schemas that carry meaning (vocabulary, grammar, and constraints) so it travels with the type rather than living in prose.

## Products

- **Specifications** — the core spec: eight primitives, DNA grammar, Archetyping, and the systemic lifecycle, prepared as a CNCF-style document set. *Publication pending — the specification document set is being finalized for release.*
- **[Frameworks]({% link gsm/frameworks/index.md %})** — domain, standard, and legal vocabularies sourced into GSM, ready to enforce. *Documentation in construction.*
  - [Features]({% link gsm/frameworks/features.md %}) — the capability catalogue with milestones

GSM also has an academic-publication track (a paper and a book); that track is separate from this documentation site and from the normative Specification above.
