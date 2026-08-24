---
layout: default
title: Archetype Referential Model
parent: GSM Research Lab
grand_parent: GSM — the standard
nav_order: 1
---

> **Status:** Exploratory and non-normative.
>
> **Hypothesis:** Archetype identity is namespaced and version-pinned.
> Schema `$ref` and `allOf` edges are references, not GSM Interactions, and
> retiring a referenced Archetype does not reverse-cascade onto dependents.

## 1. Research problem

Using an Archetype `title` as a global key does not scale to independently
authored vocabularies. It cannot identify one governed version and makes
namespace-bearing references lossy when a processor resolves only their final
path segment.

Archetype composition depends on this identity contract. An Archetype is a
static composite whose JSON Schema may reference other governed Archetypes.
The meaning and lifecycle of those edges cannot be specified independently
from versioned identity.

The referential model therefore needs:

- namespace ownership without a flat global title registry;
- exact version addressing and stable reference meaning;
- coherence between human-readable names and machine identity;
- explicit evolution through the Ascription lifecycle;
- reference discovery and lifecycle eligibility;
- a strict distinction between static composition and operational causality.

## 2. Candidate identity

```text
$id = gsmarc://{authority}/{namespacePath}/{title}/v{version}
   +---------------- Archetype stem ----------------+ + version +
```

The candidate model has four semantic invariants:

1. `title` equals the path segment immediately before `/v{version}`.
2. All Ascriptions of one Archetype Definition retain the same stem.
3. One Definition owns a stem permanently; another Definition cannot
   republish the URI family after rejection, abandonment, deprecation, or
   retirement.
4. A full `$id` becomes canonical only when its Ascription receives its
   governed version through lifecycle approval.

`title` remains identity-bound and human-readable, but becomes a local name
inside a namespace rather than a global lookup key.

## 3. Candidate-to-canonical lifecycle

An author may claim a candidate full `$id` while drafting. Before proposal,
the candidate version is checked against the next governable version for that
Definition. Competing proposals may exist. Approval convergence selects one
winner and establishes the canonical version according to ordinary lifecycle
semantics.

This preserves statement immutability: the processor governs and confirms the
claimed identity rather than silently minting a different `$id` into an
authored statement.

## 4. Version-pinned references

- External Archetype references use full, version-pinned `$id` values.
- Local fragment references remain internal to the same schema document.
- Typing, qualifier, and port-data references expose `$id` at interchange
  boundaries and may use processor-local identifiers internally.
- Equality for an identity-bound Archetype reference compares the referenced
  Definition or stem, allowing deliberate re-pinning within the same
  Definition without switching identity.
- CEL applicability may use `ref("$id")` because URIs are not valid bare CEL
  identifiers.
- Mechanism rule declarations and dispatch need an unambiguous equivalent for
  exact Archetype references.

A floating reference whose meaning changes when another version becomes active
would make validation time-dependent. Adopting a new referenced version is a
governed change to the dependent definition.

## 5. Static composition is not operational composition

The following analogy aids analysis but is not an isomorphism:

| Operational plane | Static type plane |
| --- | --- |
| Structure | Archetype schema |
| Mechanism | Named property or schema capability |
| Interaction | External schema relation |
| Ports derived from a rule | References declared by a schema |

A GSM Interaction couples an Effector to a Receptor and expresses operational
causality. A schema edge constrains the shape or interpretation of statements.
It remains a reference in the type plane, not an Interaction and not a ninth
primitive.

## 6. Reference is not cascade

An external schema reference establishes that one Archetype depends on another
for interpretation or validation. It may participate in ordinary Referee
consistency checks when a dependent Ascription advances through its lifecycle.

That dependency does not imply a reverse cascade. Existing governed snapshots
retain their version-pinned references when a target is later deprecated,
suspended, or retired. New authoring and activation decisions are controlled by
an explicit eligibility policy rather than by rewriting historical dependents.

## 7. Lifecycle eligibility

Readability, authoring, typing, approval, and activation need not admit the
same target statuses:

- historical canonical versions may remain readable after retirement;
- typing may permit active and deprecated versions during governed evolution;
- authoring may need deprecated pins for reproducible historical composition;
- activation may require a stricter live-target policy.

GSM needs one explicit matrix for these surfaces. The matrix must distinguish
historical resolvability from permission to create or activate a new dependent.

## 8. Candidate outcomes

1. Keep composition in JSON Schema and derive references by walking governed
   statements.
2. Standardize a non-normative derived composition view for impact analysis.
3. Add normative conformance requirements for reference discovery and
   lifecycle eligibility without adding primitives.

Persisted property rows, relation rows, indexes, and query APIs remain
processor choices.

## 9. Normative integration surface

The selected identity, reference, expression, lifecycle, and interchange
semantics must be integrated across at least:

- the Archetype base schema and identity requirements;
- canonical interchange references;
- lifecycle and Referee semantics;
- CEL and Starlark reference profiles;
- conformance requirements.

Storage columns, indexes, locks, repository lookups, and HTTP errors are
implementation concerns.

## 10. Open decisions

- `ARCH-D01`: Which statuses are eligible for reading, authoring, typing,
  approval, and activation?
- `ARCH-D02`: How are authority and namespace claims governed?
- `ARCH-D03`: At which lifecycle edge does a candidate `$id` become externally
  resolvable?
- `ARCH-D04`: Which JSON Schema keywords create external GSM references?
- `ARCH-D05`: Can a portable derived composition vocabulary avoid prescribing
  persistence?
