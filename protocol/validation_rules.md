Validation Rules
1. Purpose

This section defines the mandatory validation procedure for candidate blocks within the DenariumX protocol.

Validation is a multi-stage deterministic process.
Temporal conformity MUST be verified before structural or quorum checks.

No block may be accepted unless it satisfies all required validation stages.

2. Validation Order (Strict Sequence)

Each candidate block MUST undergo validation in the following order:

Temporal Eligibility Check

Temporal Deviation Check

Structural Integrity Check

Validator Quorum Confirmation

Failure at any stage results in immediate rejection.

Temporal validation always precedes consensus approval.

3. Temporal Eligibility Check

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

 = current protocol time

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


The candidate block MUST satisfy:

ΔT ≥ Minimum_Time_Window


If not satisfied:

→ Block MUST be rejected
→ No quorum vote may override this condition

4. Temporal Deviation Check

Let:

𝑇
𝑏
T
b
	​

 = candidate block timestamp

𝑇
𝑐
T
c
	​

 = externally anchored time

The block MUST satisfy:

|T_b - T_c| ≤ ε


If deviation exceeds ε:

→ Temporal Violation
→ Block MUST be invalidated
→ Burn procedure MUST be triggered

5. Structural Integrity Check

The candidate block MUST:

Reference the last valid block

Preserve state transition consistency

Follow deterministic issuance rules

Contain no retroactive state modification

Failure results in rejection.

6. Validator Quorum Confirmation

After successful temporal and structural validation:

Validators MAY vote to confirm compliance

Acceptance requires ≥ 2/3 quorum

Validators confirm correctness; they do not determine temporal validity.

If quorum is not reached:

→ Block is rejected
→ No alternative time interpretation is permitted

7. Automatic Enforcement

Validation rules MUST be enforced mechanically.

No actor may:

Override a temporal failure

Approve a non-compliant block

Retroactively validate a rejected block

Any implementation allowing discretionary override is non-compliant.

8. Rejection Consequences

If a block fails validation:

It MUST NOT be appended to the chain

It MUST NOT affect supply

If failure is temporal in nature → Burn procedure applies

Rejected blocks are permanently excluded.

9. Diagram Reference

The validation process is illustrated below:
