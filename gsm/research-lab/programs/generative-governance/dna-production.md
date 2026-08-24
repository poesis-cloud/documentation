---
layout: default
title: Generative Governance - DNA Production
parent: Generative Governance
grand_parent: GSM Research Lab
nav_order: 5
---

> **Status:** Exploratory and non-normative.

## 1. Research intent and scope

This workstream owns autopoietic production of DNA and lifecycle handoff.
It asks what counts as producing a Directive or Norm candidate, and which
lifecycle actions a producer may perform or receive by delegation.

Target continuity and specialization remain in this chapter as source
hypotheses (`SH-06`, `SH-07`), not as adopted grammar. Chain roles belong
to [Governance Chain](governance-chain.md). Production, authorization,
scope, and activation are not assumed to be one relation.

## 2. Current state of knowledge

Mechanisms are GSM's logical causal units. Their Rules receive and emit typed
values through Receptors and Effectors. Mechanisms may operate on Ascriptions,
including producing governance DNA and being governed by DNA they produced.

Directive and Norm are explicit core primitives represented as governed
Ascriptions. A Directive identifies a governing Structure, qualifier, and
governed purpose. A Norm identifies the governed Structure and qualifier and
defines activation, assertion, and temporal evaluation semantics. Directive,
Norm, and Ascription operate at distinct governance tempos.

The current model does not establish a general identity for the production
occurrence, the producing Mechanism execution, or the Effector emission that
originated a DNA candidate. It also does not make production itself equivalent
to lifecycle approval or activation.

## 3. Phenomena and research problems

- `P-DP-01`. Causal origin of a Directive or Norm is not identified as a
  production occurrence.
- `P-DP-02`. Emitting a candidate, creating a draft, approving, and
  activating can be treated as one act.
- `P-DP-03`. Producer identity may name a Definition, Ascription, execution,
  or Effector, with different provenance guarantees.
- `P-DP-04`. Source hypotheses require DNA to reference its producing
  Mechanism and the Ascription it applies to, and specialize
  Directive-to-Structure and Norm-to-Mechanism.
- `P-DP-05`. If Governance and Regulation are generic Mechanisms, DNA
  production by those Mechanisms can be read as automatic emission, as
  optional derivation of the Mechanisms themselves, or as ordinary
  production that still requires lifecycle handoff.

## 4. Research questions

- `Q-DP-01` from `P-DP-01`. What constitutes a DNA production occurrence and
  product?
- `Q-DP-02` from `P-DP-02`. Which lifecycle actions may a producer perform or
  receive by delegation without collapsing production into activation?
- `Q-DP-03` from `P-DP-03`. Which producer identity is required for
  accountable provenance?
- `Q-DP-04` from `P-DP-04`. Must produced DNA reference its producer and its
  scoped Ascription, and are Directive-to-Structure and Norm-to-Mechanism
  mandatory?
- `Q-DP-05` from `P-DP-05`. If generic Governance or Regulation Mechanisms
  emit DNA, is that emission still a production occurrence distinct from
  activation and from derivation of the Mechanism itself?

## 5. Candidate classifications and hypotheses

One production topology under test:

```text
producing Mechanism -> Effector -> DNA candidate
DNA candidate -> Ascription lifecycle -> in-effect DNA
```

The first path is causal production. The second is lifecycle transition.

- `H-DP-01` answers `Q-DP-01` and `Q-DP-02`. Emission of a DNA candidate is
  the same relation as authorization or activation. Falsifier: CASE-02, a
  produced draft that is not in-effect.
- `H-DP-02` answers `Q-DP-02` and `GOV-D06`. A producer may emit a candidate
  without delegated approve or activate authority. Falsifier: a case in which
  a candidate cannot exist unless the producer also activates it.
- `H-DP-03` answers `Q-DP-03`. Stable Mechanism Definition identity is
  sufficient producer identity for all provenance. Falsifier: two executions
  of the same Definition that must be distinguished to attribute a candidate.
- `H-DP-04` answers `Q-DP-04` (`SH-05`). Produced DNA should reference the
  producing Mechanism. Falsifier: accountable production that cannot name a
  producing Mechanism.
- `H-DP-05` answers `Q-DP-04` (`SH-06`). DNA should reference the Ascription
  it applies to; scope is what a Directive directs and what a Norm
  evaluates. Falsifier: a coherent scope that never names an Ascription, or
  a case that requires targeting a Definition class instead.
- `H-DP-06` answers `Q-DP-04` (`SH-07`). A Directive applies to a Structure
  and a Norm applies to a Mechanism. Falsifier: a valid Directive whose
  governed subject is not a Structure, or a valid Norm whose governed
  subject is not a Mechanism.
- `H-DP-07` answers `Q-DP-05` (`SH-17`, `SH-19`). Emission of a Directive by
  a Governance Mechanism, or of a Norm by a Regulation Mechanism, is still a
  DNA production occurrence. It does not activate the candidate and it is
  not the same act as deriving the generic Mechanism. Falsifier: a derived
  Governance or Regulation Mechanism whose mere existence makes DNA
  in-effect, or a production that cannot be attributed to that Mechanism.

## 6. Method and evidence

- `E-DP-01`. [CASE-02](cases.md#case-02-produced-dna-that-is-not-activated).
- `E-DP-02`. Ascription lifecycle: `DRAFT` is not in-effect; `ACTIVE` and
  `DEPRECATED` are.
- `E-DP-03`. Baseline: no field identifies the producing execution or
  Effector of a Directive or Norm.
- `E-DP-04`. [CASE-04](cases.md#case-04-derived-generic-mechanisms-without-auto-activated-dna)
  is planned for `H-DP-07` with `H-GC-12`. It is not evidence yet.

## 7. Findings and representation implications

- `F-DP-01`. `H-DP-01` fails. CASE-02 shows a produced draft that is not
  in-effect. Production occurrence is not activation.
- `F-DP-02`. `H-DP-02` survives CASE-02. A producer may emit a candidate
  without delegated approve or activate authority.
- `F-DP-03`. `H-DP-03` is not settled. CASE-02 does not require distinguishing
  two executions of one Definition.
- `F-DP-04`. `H-DP-04`–`H-DP-07` are unrested source hypotheses. They remain
  on the map because they are original program inputs, not because they have
  passed a gate. CASE-02 already separates production from activation; it
  does not test derivation of a generic Mechanism (`H-GC-12`).

These findings do not pass the promotion gates. They reject collapsing
production into activation. They do not decide `H-DP-04`–`H-DP-07`.

## 8. Decisions and dependencies

Active on this chapter: `GOV-D06`, `GOV-D36`.

Parked: `GOV-D02`–`GOV-D04`, `GOV-D13`–`GOV-D15`, `GOV-D38`. `GOV-D08`
belongs to Causal Model. `GOV-D37` is merged into `GOV-D06`. Source
hypotheses: `SH-05`, `SH-06`, `SH-07`, `SH-14`, `SH-17`, `SH-19`.
