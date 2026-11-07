# GSP Canon
## Protected Architectural Invariants

**Author:** Sierra N. Warren  
**Date:** November 7, 2026  
**Status:** Canonical research specification

The GSP Canon defines principles that later implementations, extensions, domain profiles, and certification schemes may strengthen but should not silently contradict.

## 1. Authority precedes consequential execution

Capability is not authority.

A model, agent, robot, service, workflow, or human-operated system may be technically capable of performing an action without possessing legitimate authority to perform it.

## 2. Governance belongs in the execution path

Retrospective logging is necessary but insufficient.

GSP distinguishes proposal, evaluation, authorization, dispatch, execution, observed outcome, and verified outcome. These states must not be collapsed into a single "success" event.

## 3. Quality precedes risk

A risk assessment performed on unreliable evidence is unreliable governance.

GSP treats evidence quality as a separate pre-risk control surface. Quality can include provenance, freshness, completeness, sensor health, calibration, configuration state, software integrity, model identity, source validity, and required contextual information.

## 4. Exact-action binding

The action evaluated must be the action dispatched.

Any parameter capable of materially changing the consequence must be bound into the authorization decision or its cryptographic commitment.

## 5. State matters

Authorization is contextual. Material changes in principal, delegate, workload, system configuration, policy version, evidence, time, target, environment, or prior state can invalidate an earlier decision.

## 6. Revocation must propagate to execution

Revoked, expired, superseded, suspended, or otherwise invalid authority must not remain effective solely because an earlier authorization artifact still exists.

## 7. Refusal is a first-class outcome

A governed system must be able to produce explicit states including authority unresolved, policy unresolved, evidence insufficient, quality failed, risk outside limits, approval required, state changed, permit expired, dispatch blocked, outcome unknown, and outcome mismatch.

Unknown remains unknown until evidence resolves it.

## 8. Human involvement must be attributable

"Human in the loop" is not sufficient as a control claim.

When human authority is required, GSP should identify who acted, what information was presented, what was approved or rejected, the scope of that decision, when it occurred, and whether it remained valid at dispatch.

## 9. The model is not the ultimate enforcement boundary

Model instructions, alignment, refusal behavior, or self-reported intent may contribute to safety but cannot be the only barrier protecting consequential execution.

## 10. Evidence must survive the subject of accountability

An actor should not be the only party capable of rewriting the evidence later used to evaluate that actor.

## 11. Outcome is distinct from invocation

Sending a command is not proof that the intended effect occurred.

## 12. Accountability follows causality, not merely chronology

A timestamped event stream is not a complete accountability model. GSP preserves causal relationships among authority, policy, evidence, decision, intervention, dispatch, machine state, external effect, and verification.

## 13. Liability reconstruction is evidence production, not automatic judgment

GSP can provide facts necessary for legal, contractual, regulatory, safety, security, insurance, or institutional determinations without pretending that the protocol itself is a court or legal factfinder.

## 14. Assurance is conditional and revocable

Assurance applies only while the identity, capability set, policy, configuration, evidence base, deployment conditions, and monitoring assumptions supporting it remain valid.

## 15. Oversight must not depend on one signal

No single reasoning trace, monitor, log, model explanation, or internal representation is assumed permanently sufficient for oversight.

## 16. Safe degradation must be explicit

A system may not silently downgrade from independently verified to self-asserted, fail-closed to fail-open, signed policy to unsigned policy, verified identity to anonymous identity, or observed outcome to assumed outcome.

## 17. Implementations may vary; invariants may not

GSP does not require one cloud, model, policy engine, hardware root, storage provider, or programming language.

## 18. Every normative control must become testable

Every normative requirement should eventually map to a machine-verifiable conformance condition, adversarial test, evidence requirement, or explicitly documented reason why it cannot yet be machine verified.
