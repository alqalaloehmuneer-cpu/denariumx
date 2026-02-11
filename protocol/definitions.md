Definitions
1. Purpose

This section defines the formal terminology used throughout the DenariumX protocol specification.

All capitalized terms defined herein are normative and binding within the scope of this protocol.

2. Core Temporal Terms
Atomic Time Source

An externally verifiable and authoritative time reference independent of validators, nodes, or local system clocks.

The protocol assumes that atomic time is externally anchored and not subject to validator manipulation.

Protocol Time

The time value recognized by the DenariumX protocol after anchoring to the Atomic Time Source.

Protocol Time MUST NOT be derived solely from local node clocks.

Time Window

A deterministic and predefined interval of elapsed real time that MUST pass before issuance eligibility is satisfied.

Example:

Minimum issuance interval ≥ 60 seconds

Temporal Deviation (ε)

The maximum permissible difference between:

Observed external atomic time

Candidate block timestamp

Any deviation exceeding ε constitutes a Temporal Violation.

Temporal Violation

Any condition in which:

A block is created before the required time window has elapsed

A timestamp deviates beyond ε

Retrospective or forward-dated issuance is detected

A Temporal Violation results in automatic invalidation.

3. Monetary Terms
Valid Block

A block that satisfies ALL of the following:

Time Window requirement

Temporal Deviation constraint

Validator quorum (≥ 2/3)

Structural integrity rules

Failure in any condition results in invalidation.

Issuance Event

The creation of new monetary units as a deterministic function of elapsed real time.

Issuance MUST NOT occur:

Retroactively

Preemptively

Discretionarily

Burn

The permanent destruction of a block resulting from a Temporal Violation.

Burn:

Is automatic

Is irreversible

Is not a monetary policy mechanism

4. Validator Terms
Validator

A protocol participant responsible for verifying temporal conformity and structural validity.

Validators do NOT:

Define time

Override time

Modify issuance rules

Validators only verify compliance.

Quorum

A minimum approval threshold of ≥ 2/3 validators required for block acceptance.

Quorum does not override temporal rules; it confirms compliance.

5. Compliance

An implementation is considered compliant only if it enforces all mandatory temporal rules defined in this specification.

Any system allowing discretionary temporal overrides is non-compliant.
