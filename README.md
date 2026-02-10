# DenariumX

**DenariumX** is a time-governed monetary protocol in which **temporal correctness is a prerequisite for monetary validity**.  
Unlike conventional monetary or blockchain systems, DenariumX treats time not as a parameter, but as an **enforceable constraint**.

Value cannot be created, validated, or preserved if time is violated.

---

## Core Idea

Most monetary systems tolerate:
- Delayed issuance
- Timestamp drift
- Retrospective validation

DenariumX rejects this model.

> **If time is violated, value must not survive.**

Blocks, issuance, and monetary state transitions are valid **only** when produced within strict protocol-defined time windows anchored to external atomic time sources.

---

## Key Principles

- **Time as a Validity Condition**  
  Monetary units are valid only if created at the correct time.

- **External Atomic Time Anchoring**  
  Time is sourced externally, not from validators or local clocks.

- **Deterministic Issuance**  
  Issuance follows fixed time intervals (e.g. ≥ 60 seconds).

- **Automatic Enforcement**  
  No discretionary overrides or governance intervention.

- **Burn as Penalty, Not Policy**  
  Block destruction is a response to temporal violation, not a supply tool.

---

enariumX

DenariumX is a time-governed monetary protocol in which temporal correctness is a prerequisite for monetary validity.

Unlike conventional monetary or blockchain systems, DenariumX treats time not as a configurable parameter, but as an enforceable protocol-level constraint.

Value cannot be created, validated, or preserved if time is violated.

Core Idea

Most monetary systems tolerate temporal inconsistencies such as:

Delayed issuance

Timestamp drift

Retrospective validation

DenariumX explicitly rejects this model.

If time is violated, value must not survive.

Blocks, issuance events, and monetary state transitions are considered valid only when produced within strict, protocol-defined time windows anchored to external atomic time sources.

Key Principles
Time as a Validity Condition

Monetary units are valid only if created at the correct, externally verifiable time.

External Atomic Time Anchoring

Time is sourced externally and independently — not from validators, miners, or local system clocks.

Deterministic Issuance

Issuance follows fixed and non-negotiable time intervals (e.g., ≥ 60 seconds).

Automatic Enforcement

Temporal rules are enforced mechanically by the protocol, without discretionary overrides or governance intervention.

Burn as Penalty, Not Policy

Block destruction is a direct response to temporal violation, not a monetary supply management tool.

How It Works (High-Level)

The system initializes and anchors itself to external atomic time.

A genesis block is created with an immutable timestamp.

For each subsequent block:

Elapsed real time since the previous block is calculated.

Block creation is permitted only if the protocol’s time window is satisfied.

Candidate blocks undergo:

Temporal deviation checks

Validator approval (≥ 2/3 quorum)

Any detected temporal violation results in:

Immediate block invalidation

Permanent block burn

Immutable logging of the violation
## Repository Structure


