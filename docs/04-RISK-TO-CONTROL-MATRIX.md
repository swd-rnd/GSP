# GSP Risk-to-Control Matrix
## AI and Autonomous Systems

**Author:** Sierra N. Warren  
**Date:** November 7, 2026

| Leading concern | GSP engineering response | Primary enforcement point |
|---|---|---|
| Goal hijacking / prompt injection | Treat model intent as untrusted; independently authorize each consequential action | IGRM + constrained dispatcher |
| Tool misuse | Per-action capability scope; exact tool and target binding | Permit service |
| Identity / privilege abuse | Workload identity, principal/delegate chain, least authority, revocation | Identity + authority plane |
| Agentic supply-chain compromise | Signed manifests, provenance, approved component state, context digest | Quality + attestation plane |
| Unexpected code execution | Execution allowlists, containment domain, independent dispatch policy | Dispatcher + sandbox |
| Memory/context poisoning | Versioned context state, provenance, invalidation on material mutation | Context/quality plane |
| Insecure inter-agent communication | Authenticated peer identity, message provenance, local authorization on receipt | Federation boundary |
| Cascading failures | Consequence containment domains, quotas, circuit breakers, bounded delegation depth | Runtime monitor |
| Human-agent trust exploitation | Governed approvals, independent evidence, scope/expiry, anti-reuse | Human authority gate |
| Rogue/unsanctioned action | Target allowlists, egress controls, permit enforcement, emergency revocation | IGRM + network controls |
| Model drift / environment drift | Live assurance state, confidence decay, revalidation | Runtime assurance |
| Evaluation gaming / weak predictiveness | Conditional assurance, adversarial tests, operational monitoring | Assurance case |
| Data poisoning / low-quality evidence | Quality-before-risk gate, provenance, contradiction detection | Quality engine |
| Sensor failure | Calibration evidence, health state, redundant observation | Quality + outcome observer |
| Policy tampering | Signed/versioned policy, independent source, change invalidation | Policy resolver |
| TOCTOU | Dispatch-time revalidation and short-lived permits | Dispatcher |
| Replay | Nonce, one-time consumption, atomic reservation | Permit service |
| Parameter substitution | Exact-action commitment | Permit + dispatcher |
| Approval replay | Approval scope, expiry, nonce, action digest | Human authority gate |
| Revoked authority | Live revocation status and permit invalidation | Authority plane |
| Partial execution | Effect observation and reconciliation | Outcome plane |
| False success / false failure | Separate invocation from verified outcome | Reconciliation engine |
| Evidence deletion | External anchoring, independent custody, completeness status | Evidence graph |
| Log forgery | Signatures, causal linkage, independent witnesses | Evidence graph |
| Loss of oversight | Multiple oversight signals, externalized execution evidence, independent monitor | IGRM + evidence plane |
| Overreliance on model explanation | Do not use self-report as sole evidence | Evidence policy |
| Excessive autonomy | Consequence-class autonomy ceilings and adaptive downgrade | Runtime assurance |
| Cross-domain trust leakage | Local authorization at every domain | Federation layer |
| Unknown policy | Evidence challenge / fail closed for affected consequence | Policy plane |
| Unknown authority | Authority unresolved state; no inferred permission | Authority plane |
| Unknown outcome | OUTCOME_UNKNOWN; reconciliation required | Outcome plane |

## Design rule

No row is considered "covered" because documentation exists.

A control counts only when its enforcement location, failure behavior, evidence output, and adversarial test are defined.
