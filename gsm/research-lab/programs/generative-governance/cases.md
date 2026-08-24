---
layout: default
title: Generative Governance - Cases
parent: Generative Governance
grand_parent: GSM Research Lab
nav_order: 7
---

> **Status:** Exploratory and non-normative. These cases are executed
> discriminating examples. They are evidence, not promotion outcomes.

This corpus is the program's first method object. Each case states the
configuration, the hypothesis it tests, the result, and the finding it
supports. Further cases may be added; CASE-01 through CASE-03 start the
critical path. CASE-04 is a planned discriminator, not yet executed.

## CASE-01 Operationalization without a named Regulation role

**Tests:** `H-GC-01`, `GOV-D05`, `GOV-D17`

**Configuration.** Structure `G` issues Directive `D1` governing Structure
`S` on qualifier `Q`. Structure `S` has Norm `N1` whose `structure` is `S`
and whose qualifier is `Q`. No Mechanism is labeled Regulation. `N1`
activation and assertion are evaluable. No Supervision or Compliance
Mechanism is declared.

**Question.** Does the absence of a named Regulation role prevent
governance operationalization?

**Result.** `D1` still opens scope. `N1` still states an evaluable
constraint inside that scope. The DNA grammar functions. What is missing is
an accountable Mechanism that produced `N1`, adapted it, or returned
feedback. Governance is not empty; role topology is incomplete.

**Falsifier that did not occur.** A case in which no Norm can exist unless a
Mechanism carries the Regulation label.

**Consequence.** Missing Regulation is not, by itself, a DNA-grammar
failure. Treating it as normative conformance (`GOV-D17`) would require a
role signature that GSM does not yet have. `H-GC-01` is weakened: the
candidate chain is a useful analysis of accountability, not a necessary
condition for a Directive and Norm to exist.

## CASE-02 Produced DNA that is not activated

**Tests:** `H-DP-01`, `GOV-D06`, `GOV-D36`

**Configuration.** Mechanism `M` emits Norm candidate `N-cand` through an
Effector. An Ascription `A-draft` is created in `DRAFT`. No submit, approve,
or activate transition is performed by `M` or by any other authority. `N-cand`
is therefore not in-effect.

**Question.** Is emission of a DNA candidate the same relation as
authorization or activation?

**Result.** Causal origin is attributable to `M`. Lifecycle status remains
`DRAFT`. No governed constraint is in effect. Production occurred;
governance did not become effective.

**Falsifier that did not occur.** A model in which emitting a candidate
necessarily creates an in-effect Norm.

**Consequence.** Production occurrence and lifecycle authority are distinct
relations. `GOV-D06` cannot collapse them. A producer may emit a candidate
without receiving delegated approve or activate authority.

## CASE-03 One Impact, two opposed evaluations

**Tests:** `H-CM-02`, `H-CM-03`, `GOV-D31`, `GOV-D35`

**Configuration.** Operation of Mechanism `M` in Structure `S` changes
capacity available to subject `A` and subject `B`. From `A`'s purpose the
change is beneficial Value. From `B`'s purpose the same change is an
Adverse condition. No separate event is required to explain the two
evaluations.

**Question.** Are Value and Adverse condition distinct Impacts, or
evaluations of one Impact relative to purpose and subject?

**Result.** One consequence, two evaluations. Splitting the event into two
Impacts hides the common referent. Treating Value or Adverse condition as
the event itself cannot explain the disagreement.

**Falsifier that did not occur.** A case that requires Value to exist with
no consequence-like referent, or that cannot share one Impact across
opposed evaluations.

**Consequence.** Impact can serve as a common referent for opposed
evaluations (`H-CM-02` survives this case). Value, Cost, and Adverse
condition are not forced into a subtype hierarchy. Need remains an open
evaluative hypothesis (`H-CM-03`, `SH-15`): this case does not show that
Need is required, and it does not show that Need is unnecessary.

## CASE-04 Derived generic Mechanisms without auto-activated DNA

**Status.** Planned. Not evidence until executed.

**Tests:** `H-GC-10`, `H-GC-11`, `H-GC-12`, `H-DP-07`, `GOV-D38`

**Intended configuration.** Governor `G`, governed `S`, qualifier `Q`, and
`Directive.purpose == Norm.structure` are already present. No Governance,
Regulation, or Supervision Mechanism is declared. An implementation derives
generic Mechanisms from that information only.

**Question.** Can those derived Mechanisms make production and the concern
chain traceable without activating DNA and without inventing information not
already in GSM?

**Discriminators to record when executed.**

1. Derivation succeeds from present information only (`H-GC-12`).
2. Emission by a derived Governance or Regulation Mechanism remains a
   production occurrence, not activation (`H-DP-07`, CASE-02).
3. The concern path is recoverable from the derived chain (`H-GC-11`).
4. Supervision-as-evaluation does not settle Compliance (`H-GC-03`).

## Teleological test applied by these cases

The same topology can change its justified evaluation when purpose changes
(CASE-03). The same production topology can fail to govern when activation
is withheld (CASE-02). Teleology is used here as that test, not as a causal
category.
