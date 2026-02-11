Issuance Rules
1. Purpose

This section defines the deterministic conditions under which new monetary units may be created within the DenariumX protocol.

Issuance is strictly governed by elapsed real time.
No discretionary authority may accelerate, delay, or override issuance conditions.

2. Temporal Eligibility Condition

Let:

𝑇
𝑛
T
n
	​

 = timestamp of the last valid block

𝑇
𝑐
T
c
	​

 = current externally anchored protocol time

Δ
𝑇
=
𝑇
𝑐
−
𝑇
𝑛
ΔT=T
c
	​

−T
n
	​


A new issuance event is permitted only if:

ΔT ≥ Minimum_Time_Window


Where:

Minimum_Time_Window ≥ 60 seconds


Issuance MUST NOT occur if the required time window has not elapsed.

3. Deterministic Issuance Function

Issuance is defined as a deterministic function of elapsed real time:

Issuance = f(ΔT)


The function MUST:

Be predefined

Be non-discretionary

Be identical across compliant implementations

Issuance MUST NOT depend on:

Validator preference

Governance vote

Market conditions

Network congestion

Time alone determines eligibility.

4. Single-Issuance Constraint

Only one valid issuance event may occur per satisfied time window.

The protocol MUST prevent:

Multiple blocks within a single window

Artificial subdivision of time windows

Parallel issuance attempts

If multiple candidate blocks are proposed within the same valid window, only one may be accepted under validator quorum rules.

5. Prohibited Issuance Behaviors

The following are strictly forbidden:

Retroactive issuance

Forward-dated issuance

Issuance after extended delay with accumulated compensation

Manual intervention to adjust supply timing

Delayed issuance does not accumulate future entitlement.

If a valid window passes without block creation, that issuance opportunity is permanently lost.

6. Liveness vs Correctness

If issuance cannot occur due to:

Atomic time unavailability

Network failure

Insufficient quorum

The protocol MUST prioritize correctness over liveness.

No retroactive issuance may compensate for missed intervals.

7. Diagram Reference

The deterministic issuance flow is illustrated below:
