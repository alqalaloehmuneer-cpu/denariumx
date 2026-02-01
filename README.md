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

## How It Works (High-Level)

1. The system initializes and anchors to atomic time.
2. A genesis block is created with an immutable timestamp.
3. For each new block:
   - Elapsed real time since the last block is calculated.
   - Block creation is allowed **only if the time window is satisfied**.
4. Candidate blocks undergo:
   - Temporal deviation checks
   - Validator approval (≥ 2/3 quorum)
5. Any temporal violation results in:
   - Block invalidation
   - Permanent block burn
   - Immutable logging of the violation

---

## Repository Structure


