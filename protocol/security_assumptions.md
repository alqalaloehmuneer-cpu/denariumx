Security Assumptions
1. Purpose

This section defines the security assumptions, trust boundaries, and limitations of the DenariumX protocol.

DenariumX prioritizes temporal correctness over availability.
The protocol’s security model depends on external time integrity.

2. Atomic Time Integrity Assumption

DenariumX assumes that:

The Atomic Time Source is externally verifiable

It is resistant to coordinated manipulation

It reflects real-world elapsed time accurately

If the atomic time source is compromised, the protocol cannot guarantee temporal correctness.

DenariumX does not define how atomic time infrastructure is secured.

3. Validator Honesty Assumption

The protocol assumes:

≥ 2/3 of validators behave honestly

Validators correctly execute temporal verification

Validators do not collude to override protocol rules

Validators cannot alter time but could refuse to validate correctly.

The protocol mitigates this via quorum requirements but does not eliminate coordinated majority attacks.

4. Network Assumptions

DenariumX assumes:

Network latency does not systematically exceed ε

Temporary partitions may occur

Temporal validation is independent of network ordering

In cases of partition:

Competing candidate blocks may arise

Only temporally valid blocks may survive

No temporal compensation is allowed for delayed transmission.

5. Liveness Trade-Off

DenariumX explicitly prioritizes:

Correctness > Availability

If atomic time becomes unavailable:

Block production MUST halt

No fallback to local clocks is permitted

No retroactive issuance is allowed

Temporary halting is considered preferable to temporal compromise.

6. Attack Surface Overview

Potential attack categories include:

Atomic time spoofing

Coordinated validator collusion

Network delay exploitation

Timestamp manipulation attempts

Temporal rules are designed to minimize successful exploitation by:

External anchoring

Deterministic validation

Automatic burn enforcement

7. Non-Goals

DenariumX does NOT attempt to:

Guarantee economic stability

Prevent market volatility

Eliminate validator centralization risks

Replace external time infrastructure

The protocol enforces temporal validity only.

8. Compliance Boundary

Any implementation that:

Falls back to local clocks

Allows discretionary temporal override

Retroactively compensates missed windows

Reverses burn events

Is considered non-compliant.
