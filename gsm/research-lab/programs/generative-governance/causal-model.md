---
layout: default
title: Generative Governance - Causal Model
parent: Generative Governance
grand_parent: GSM Research Lab
nav_order: 3
---

> **Status:** Exploratory and non-normative.

## 1. Research intent and scope

This workstream owns organization, purpose, function, and viability
evaluations. It asks which relations a generative systemics model must
represent — including whether current GSM elements are sufficient,
excessive, or incomplete — and how those relations compose.

It does not own governance-chain role topology
([Governance Chain](governance-chain.md)) or DNA production occurrence
([DNA Production](dna-production.md)). It does not assume generative,
operational, impact, or viability causalities as organizing kinds. An
explicit governance chain may trace generation and concern (`H-GC-11`);
that trace is not a causal-axis taxonomy. Current GSM is the starting
inventory, not a closed vocabulary.

An arrow records a hypothesis that one term conditions, constrains, produces,
transforms, transmits, evaluates, or otherwise contributes to another. It does
not assert that all arrows have the same semantics.

## 2. Current state of knowledge

This baseline records only what the current authoritative GSM model and schemas
explicitly represent or make derivable. “Represented” does not imply that every
reference implementation has completed the corresponding runtime behavior.

| Element | Current GSM representation | Status in current knowledge | Causal relevance already stated or derivable |
| --- | --- | --- | --- |
| Purpose | `Structure.purpose` | Explicit core property | Why a Structure exists; its identity and governance address |
| Structure | `Structure` | Explicit core primitive | Organization or boundary in which Mechanisms, purpose, governance, and effects relate |
| Function | `Mechanism.function` | Explicit core property | Contribution expected from a Mechanism relative to purpose |
| Mechanism | `Mechanism` | Explicit core primitive | Logical causal unit whose Rule is realized through Effectors and Receptors |
| Rule | `Mechanism.rule` | Explicit core property | Transformation logic and source from which ports are derived |
| Effector | `Effector` | Explicit core primitive; derived from Rule syntax | Typed emitting boundary |
| Interaction | `Interaction` | Explicit core primitive | Explicit coupling between an Effector and a Receptor |
| Receptor | `Receptor` | Explicit core primitive; derived from Rule syntax | Typed receiving boundary |
| Archetype | `Archetype` | Explicit core primitive | Governed type, qualifier, and data schema used by causal relations |
| Directive | `Directive` | Explicit core primitive | Constitutive or directional governance statement |
| Norm | `Norm` | Explicit core primitive | Evaluable governance constraint with activation and temporal semantics |
| Ascription | Definition-to-Archetype governed snapshot and lifecycle | Explicit core lifecycle construct; not one of the eight primitives | Governed version-specific statement of a Definition |
| Governance | `gsm.puml` names Governance as the loop operation for Directives; Directive fields name governor and governed | Named loop operation and explicit Directive relation; Mechanism role signature not represented | Directive establishes a governance relation and scope between Structures |
| Regulation | `gsm.puml` names Regulation as the loop operation for Norms | Named loop operation; Mechanism role signature not represented | See gap inventory |
| Supervision | `gsm.puml` names Supervision as the loop operation for Ascriptions and as the observation path for Quality | Named loop operation; Mechanism role signature not represented | See gap inventory |
| Compliance | Norm assertions represent constraints; Compliance role is not named as a primitive | Assertion semantics explicit; role not represented | Norm evaluation yields satisfaction or violation over configured tolerance semantics |
| Value | Purpose fulfilment in the Quality account | Explicit derived systemic semantic | Degree to which a System fulfils its purpose |
| Cost | Operating burden in the Quality account | Explicit derived systemic semantic | Resources and overhead associated with defining, realizing, and operating Value |
| Risk | Residual uncertainty in the Quality account | Explicit derived systemic semantic | Uncertainty introduced or retained while operating Value |
| Quality | Viability balance expressed through qualifier Archetypes and Norms | Derived GSM semantics | Evaluation of purpose fulfilment across relevant viability dimensions |
| Viability | Qualifier Archetypes and governed constraints represent viability dimensions | Derived GSM semantics | Capacity to persist within beneficial and adverse constraints |

## 3. Phenomena and research problems

Comparison between the baseline and the intended explanatory scope exposes
research problems rather than additional baseline facts.

- `P-CM-01`. Causal possibility is modeled, but occurrence, attribution, and
  evidential warrant are not one represented relation.
- `P-CM-02`. Value, Cost, Risk, Adverse condition, and Quality share a
  consequence vocabulary without an established common referent or composition
  law.
- `P-CM-03`. A condition, an evaluation that change is justified, and a
  governance response are easily collapsed into one pipeline.
- `P-CM-04`. Current GSM treats Structure as a primitive with unique purpose
  and exclusive Mechanism membership. Source hypotheses distinguish what a
  Structure is as organization (`SH-01`) from whether a Mechanism may belong
  to several Structures or to none (`SH-04`).

The following candidate elements enter because of those gaps. Absence from
core GSM is not evidence that they must be added to core GSM. Operator,
Measure, and Evidence role signatures are investigated where they constrain
relation kind; their topology belongs to [Governance Chain](governance-chain.md)
and [DNA Production](dna-production.md).

| Candidate element | Current representation gap | Research role |
| --- | --- | --- |
| Operator | No general GSM role signature for a Mechanism that produces definitions or subjects | Relation of production to definition identity; occurrence owned by DNA Production |
| Measure | Measurable signals are named; no general Measure signature is established | Magnitude used in evidential and evaluative relations |
| Evidence | Description-plane evidence is referenced; no general causal-evidence signature is established | Warrant for causal, conformity, or consequence claims |
| Need | No established relation among purpose, condition, affected subject, and required transformation | Candidate evaluation, not a presumed primitive |
| Impact | No established common representation for realized or possible consequences | Candidate common referent for evaluations |
| Adverse condition | No formal representation of an experienced or persistent detrimental condition | Perspective-relative evaluation of a condition or Impact |
| Requirement | No general GSM distinction between a required outcome and a Directive, Norm, or implementation constraint | Candidate design conclusion after a Need is justified |

Other elements may be required. This inventory is not a closed vocabulary.

## 4. Research questions

- `Q-CM-01` from `P-CM-01`. Which predicates distinguish defined possibility,
  observed occurrence, evaluation, and warranted attribution?
- `Q-CM-02` from `P-CM-02`. Can Impact serve as a common referent for Value,
  Cost, Risk, Adverse condition, Quality, and viability without becoming a
  subtype hierarchy?
- `Q-CM-03` from `P-CM-03` (`SH-15`). How should Need, Requirement, Value,
  Cost, Risk, Quality, and Adverse condition be represented relative to
  Impact and purpose?
- `Q-CM-04` from `P-CM-04` (`SH-01`). Beyond purpose, what is a Structure as
  organization?
- `Q-CM-05` from `P-CM-04` (`SH-04`). May a Mechanism belong to several
  Structures, or to none?

## 5. Candidate classifications and hypotheses

Live hypotheses are tested with predicates, not with a family taxonomy. The
predicates under test are: produces, constrains, warrants, evaluates, and
enables.

- `H-CM-01` answers `Q-CM-01`. Defined possibility, observed occurrence,
  evaluation, and warranted attribution are distinct predicates. Falsifier: a
  single GSM field that represents all four without loss of accountability.
- `H-CM-02` answers `Q-CM-02` (`SH-15`). Impact is a common referent for
  Value, Cost, Risk, Adverse condition, Quality, and viability, not a parent
  type. Falsifier: a case in which Value or Quality must exist with no
  consequence-like referent, or that cannot share one Impact across opposed
  evaluations.
- `H-CM-03` answers `Q-CM-03` (`SH-15`). Need is a justified necessity for
  transformation relative to purpose, condition, and affected subject.
  Falsifier: a case in which Need adds no justificatory work beyond Impact
  plus purpose.
- `H-CM-04` answers `Q-CM-04` (`SH-01`). A Structure is a purposed
  organization of Mechanisms that governs their operability and Quality, and
  that organization may not reduce to purpose plus Mechanism list.
  Falsifier: every accountability and Quality effect is derivable from
  purpose and Mechanism membership alone.
- `H-CM-06` answers `Q-CM-05` (`SH-04`). A Mechanism may belong to several
  Structures, or to none. Falsifier: an accountability or Quality effect
  that cannot be stated unless each Mechanism has exactly one owning
  Structure.
- `H-CM-05` merged into `SH-15`. That the viability cluster belongs to this
  inquiry is the source claim. `H-CM-02` and `H-CM-03` are the live tests.

The condition-to-governance sequence is not a taught GSM path. It is a
candidate design narrative under `Q-CM-03`. CASE-03 tests opposed
evaluations of one Impact; it does not close Need.

Relation-family names formerly listed here are retired as chapter structure.
Whether any family name survives is a method question (`GOV-M01`), not an
object-level decision.

Teleology is applied as a test: if purpose changes and the justified
evaluation does not change, purpose is not doing causal or evaluative work.
CASE-03 is that test. The `Purpose -> Function -> Rule` decomposition remains
a GSM baseline relation; its composition with Impact is open.

Quality form, including any product expression, is quarantined to `GOV-D32`.
No formula is used in this chapter until a dimensional example exists.

## 6. Method and evidence

- `E-CM-01`. [CASE-03](cases.md#case-03-one-impact-two-opposed-evaluations).
- `E-CM-02`. Quality account in `gsm.puml`: Value, Cost, Risk, and Quality as
  derived viability semantics, without Impact or Need as primitives.
- `E-CM-03`. Baseline predicates available today: defined possibility
  (Interaction, Rule), evaluation (Norm assertion), and derived Quality.

Stop condition for `H-CM-03`: three independent cases in which Need adds no
justificatory work beyond Impact plus purpose.

## 7. Findings and representation implications

- `F-CM-01`. CASE-03 does not force Need to be a distinct Impact. Value and
  Adverse condition can share one Impact. `H-CM-03` remains open as an
  evaluative hypothesis (`SH-15`). It is not rejected and not promoted.
- `F-CM-02`. `H-CM-02` survives CASE-03. Opposed Value and Adverse condition
  can share one Impact. Placement is not decided.
- `F-CM-03`. `H-CM-01` is not yet settled. CASE-02 in DNA Production shows
  production occurrence without activation, which is consistent with distinct
  predicates but is not a complete evidence suite.
- `F-CM-04`. `H-CM-04` and `H-CM-06` are unrested. Organization of a
  Structure (`SH-01`) and Mechanism membership (`SH-04`) remain distinct.

These findings do not pass the promotion gates.

## 8. Decisions and dependencies

Active on this chapter: `GOV-D31`, `GOV-D32`, `GOV-D35`.

Dependencies and parked forks: `GOV-D01`, `GOV-D08`, `GOV-D09`, `GOV-D11`,
`GOV-D18`, `GOV-D23`–`GOV-D29`. Method items `GOV-M01`–`GOV-M03` are not
object-level decisions. Source hypotheses: `SH-01`, `SH-04`, `SH-15`.
