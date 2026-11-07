# GSP Bricolage Engineering Architecture
## Reliable AI, Liability Oversight, and Governing Systems

**Author:** Sierra N. Warren  
**Organization:** Sierra Warren Developments, LLC  
**Date:** November 7, 2026  
**Status:** Forward engineering architecture

## 1. Design position

I am developing GSP as a governing and assurance substrate for consequential AI and autonomous systems.

The engineering method is deliberate bricolage: selecting mechanisms that have proved useful in different technical disciplines, then recombining them around a single problem that none of those disciplines solve alone.

The problem is not simply whether an AI system is accurate.

The problem is whether an AI or autonomous system remains:

- legitimately authorized;
- inside its operating and legal boundaries;
- based on evidence of sufficient quality;
- resistant to manipulation;
- observable during operation;
- controllable when behavior diverges;
- unable to silently expand privilege;
- accountable for the exact action it causes;
- reconstructable after a failure; and
- governable across organizational and technical boundaries.

GSP therefore combines ideas from safety engineering, control theory, runtime assurance, formal methods, zero-trust security, identity and authorization, cryptographic evidence, fault containment, distributed systems, incident response, assurance cases, and liability reconstruction.

The objective is not to copy those disciplines.

The objective is to make them cooperate.

## 2. Core failure model

The forward GSP architecture assumes that any one of the following can fail:

- the model;
- the prompt;
- retrieved context;
- persistent memory;
- a tool;
- a connector;
- an identity claim;
- a credential;
- a policy source;
- an approval;
- a sensor;
- a human reviewer;
- a runtime monitor;
- a network path;
- an external service;
- an evidence store;
- a subordinate agent;
- a system integrator; or
- an institution.

GSP therefore does not place final trust in any single one of them.

## 3. The GSP closed-loop governing system

GSP should operate as a closed-loop control and accountability system.

The loop is:

**Sense → Establish State → Establish Authority → Verify Evidence Quality → Evaluate Risk and Constraints → Bind Exact Action → Authorize → Dispatch → Observe Effect → Reconcile → Update Assurance State → Preserve Evidence**

The cycle repeats for every consequential transition.

Governance is therefore continuous rather than episodic.

## 4. Bricolage Layer A: Runtime assurance + independent reference monitoring

### Borrowed engineering idea

Runtime assurance architectures allow a high-capability component to operate while an independent mechanism monitors safety properties and can constrain or replace control when required.

DARPA's Assured Autonomy program is built around continual assurance for learning-enabled cyber-physical systems as the system and environment evolve.

### GSP composition

GSP should contain an **Independent Governing Reference Monitor (IGRM)**.

The IGRM does not need to understand every internal reasoning step of a model.

It must understand the externally relevant contract:

- who is acting;
- what they are attempting;
- what resource will change;
- which authority applies;
- which constraints apply;
- what evidence is required;
- which limits cannot be crossed; and
- what transition is currently permissible.

The IGRM must be able to:

- permit;
- deny;
- challenge for additional evidence;
- reduce scope;
- require human authority;
- downgrade autonomy;
- route to a safe controller;
- suspend the workload;
- revoke credentials;
- isolate network access; or
- terminate execution.

The AI component must not own the only mechanism capable of stopping itself.

## 5. Bricolage Layer B: Zero trust + capability security + delegated authority

### Borrowed engineering idea

Zero-trust architecture assumes no implicit trust based on location. Capability systems bind authority to narrowly scoped permissions. Modern identity systems increasingly treat software agents as principals requiring explicit authorization.

NIST has identified agent identity, authorization, auditing, non-repudiation, prompt injection, and access to diverse tools and datasets as major deployment concerns.

### GSP composition

Every consequential GSP execution receives a bounded **Authority Capability**.

The capability identifies:

- principal;
- delegate;
- workload identity;
- permitted action;
- target;
- permitted parameters;
- resource scope;
- time-to-live;
- delegation depth;
- approval requirements;
- policy version;
- consequence class; and
- revocation source.

An agent never receives "general authority" merely because it is trusted.

Authority is issued for specific consequences.

## 6. Bricolage Layer C: Formal methods + runtime invariants

### Borrowed engineering idea

Formal methods provide mathematically explicit properties that must hold. They are powerful but cannot completely characterize open-world autonomous behavior.

### GSP composition

Instead of trying to formally verify the entire model, GSP formalizes the parts that can be made hard:

- an unauthorized actor MUST NOT dispatch a governed action;
- an expired permit MUST NOT execute;
- a materially modified action MUST NOT execute under an old permit;
- a revoked authority MUST invalidate dependent permits;
- a quality failure MUST invalidate dependent risk decisions;
- an unresolved policy conflict MUST NOT silently become approval;
- a one-time authority MUST NOT be consumed twice;
- an outcome MUST NOT be recorded as verified when only dispatch is known;
- a human approval MUST NOT be reused outside its scope;
- a lower-assurance mode MUST NOT silently replace a required higher-assurance mode.

These become runtime invariants enforced outside the model.

## 7. Bricolage Layer D: Safety engineering + fault containment

### Borrowed engineering idea

Safety-critical engineering assumes failures will occur and designs containment boundaries, hazard analysis, redundancy, degraded modes, and safe-state transitions.

### GSP composition

GSP introduces **Consequence Containment Domains**.

A containment domain defines:

- maximum permissible effect;
- reachable systems;
- accessible data;
- credential scope;
- network boundaries;
- physical operating envelope;
- monetary or resource limits;
- permitted duration;
- fallback controller; and
- emergency shutdown behavior.

A failure inside one domain should not automatically propagate into another.

This directly addresses cascading autonomous failure and excessive agency.

## 8. Bricolage Layer E: Data quality engineering + epistemic assurance

### Borrowed engineering idea

Quality engineering asks whether inputs are fit for purpose before downstream decisions rely on them.

### GSP composition

GSP introduces a distinct **Evidence Quality Gate** before risk authorization.

The Quality Gate evaluates evidence dimensions including:

- provenance;
- completeness;
- freshness;
- source authenticity;
- calibration;
- sensor health;
- model and software version;
- configuration integrity;
- drift;
- contradiction;
- missing mandatory sources; and
- known uncertainty.

A risk engine does not get to convert bad evidence into a precise-looking score.

If evidence quality is insufficient, the correct output is an evidence failure state.

## 9. Bricolage Layer F: Adversarial security + prompt/tool isolation

### Borrowed engineering idea

OWASP's 2026 agentic risk taxonomy identifies goal hijacking, tool misuse, identity and privilege abuse, supply-chain vulnerabilities, unexpected code execution, memory poisoning, insecure inter-agent communication, cascading failures, human trust exploitation, and rogue-agent behavior.

AISI testing has also demonstrated that prompt-injection attacks can successfully produce unauthorized data access, illicit financial actions, and other policy violations across modern agent systems.

### GSP composition

GSP treats model instructions as **untrusted control input** with respect to consequential execution.

Prompt injection may change what the model wants to do.

It must not change what the machine is authorized to do.

Tool access is therefore mediated through the IGRM.

Tool descriptions, MCP servers, plugins, retrieved documents, browser content, and inter-agent messages are not allowed to directly grant authority.

## 10. Bricolage Layer G: Memory integrity + temporal trust

### Borrowed engineering idea

Persistent memory creates long-lived security effects. A poisoned observation today can change behavior tomorrow.

### GSP composition

Material memory and context become versioned state.

For high-assurance actions, GSP binds authorization to a **Context State Digest** representing the material execution context.

The digest may include:

- active system policy;
- tool manifest;
- memory revision;
- retrieved evidence identifiers;
- agent configuration;
- software build;
- model identifier;
- external skill set; and
- environment attestation.

If a material element changes, the assurance state can be invalidated or reevaluated.

## 11. Bricolage Layer H: Control theory + assurance state

### Borrowed engineering idea

Control systems do not merely classify a system as "safe" once. They continuously estimate state and correct deviation.

### GSP composition

GSP introduces a **Live Assurance State**.

The assurance state is not a marketing rating.

It is a machine-readable representation of whether the conditions supporting authority and safe execution still hold.

Possible dimensions include:

- identity confidence;
- authority validity;
- policy integrity;
- evidence quality;
- configuration integrity;
- behavioral deviation;
- monitoring health;
- containment integrity;
- outcome uncertainty;
- outstanding incidents; and
- revocation status.

The state can decay over time or after change.

It can also trigger automatic reduction of autonomy.

## 12. Bricolage Layer I: Independent evidence + distributed accountability

### Borrowed engineering idea

Security logging, transparency systems, cryptographic receipts, append-only records, remote attestation, and independent witnesses all reduce the ability of one party to rewrite history.

### GSP composition

GSP evidence should be **multi-source and independently checkable**.

A high-assurance execution may produce:

1. authority receipt;
2. policy receipt;
3. quality receipt;
4. risk decision receipt;
5. approval receipt;
6. execution permit;
7. dispatcher receipt;
8. environment attestation;
9. outcome observation;
10. reconciliation receipt;
11. revocation events; and
12. completeness status.

These artifacts form a causal evidence graph rather than a flat log.

The same component should not be the sole source of every claim about itself.

## 13. Bricolage Layer J: Incident response + autonomous circuit breaking

### Borrowed engineering idea

Cybersecurity incident response provides isolation, credential revocation, containment, recovery, and forensic preservation.

### GSP composition

GSP adds **Autonomy Circuit Breakers**.

Circuit breakers may trigger when:

- action rate changes unexpectedly;
- privilege increases;
- a target is outside the task boundary;
- a new communication channel appears;
- network egress deviates;
- policy conflicts emerge;
- evidence becomes unavailable;
- memory changes unexpectedly;
- execution diverges from the permit;
- the system resists interruption;
- an outcome cannot be reconciled; or
- a monitor detects a known high-severity pattern.

A circuit breaker can atomically:

- suspend new permits;
- revoke active permits;
- revoke credentials;
- disable network paths;
- isolate affected workloads;
- preserve volatile evidence; and
- transfer control to a safe mode.

## 14. Bricolage Layer K: Human factors + governed human intervention

### Borrowed engineering idea

Automation bias shows that a human can be present without providing meaningful oversight.

### GSP composition

Human intervention becomes its own governed transaction.

GSP records:

- reviewer identity;
- reviewer authority;
- information shown;
- known evidence gaps;
- decision requested;
- decision given;
- permitted scope;
- expiration;
- whether the model recommendation was visible;
- whether independent evidence was available; and
- whether the resulting action matched what was approved.

High-consequence workflows can require independent or multi-party approval.

## 15. Bricolage Layer L: Reliability engineering + uncertainty preservation

### Borrowed engineering idea

Reliable systems distinguish known failure from unknown state. They do not manufacture certainty.

### GSP composition

The protocol distinguishes:

- proposed;
- authorized;
- dispatched;
- acknowledged;
- effect observed;
- effect verified;
- effect contradicted;
- partial effect;
- outcome unknown; and
- reconciled.

Unknown is a valid state.

This prevents a timeout, missing callback, or self-report from being falsely interpreted as success or failure.

## 16. Bricolage Layer M: Assurance cases + liability reconstruction

### Borrowed engineering idea

Safety cases and assurance cases connect claims to evidence. Legal and incident investigations reconstruct responsibility from facts and causal chains.

### GSP composition

Every high-consequence system can maintain a **Machine Assurance Case**:

**Claim → Argument → Evidence → Current validity**

Examples:

- Claim: this workload may approve purchases below a defined threshold.
- Evidence: delegation document, role identity, policy version, signing authority.
- Claim: the active model environment satisfies the required security profile.
- Evidence: signed build provenance, attestation, approved tool manifest.
- Claim: the human intervention was valid.
- Evidence: reviewer identity, authority, evidence presented, signed decision.

When a claim loses supporting evidence, GSP marks the assurance case degraded rather than silently preserving the old conclusion.

## 17. Bricolage Layer N: Cross-domain governance federation

### Borrowed engineering idea

Distributed systems and federated identity allow independently administered domains to cooperate without requiring one global administrator.

### GSP composition

GSP should not require a universal central governance database.

Each organization can retain local authority.

When an action crosses domains, it carries evidence sufficient for the next domain to make an independent decision.

Upstream approval is evidence.

It is not a command.

This preserves local sovereignty and prevents trust from becoming transitive by accident.

## 18. System architecture

The forward GSP reference architecture consists of:

### A. Principal and Authority Registry
Maintains authoritative grants, scopes, delegation, expiration, and revocation.

### B. Workload Identity and Attestation Verifier
Determines which model, agent, service, or device is actually requesting execution.

### C. Policy Resolver
Retrieves authenticated, versioned rules applicable to the target action.

### D. Evidence Quality Engine
Determines whether the evidence basis is adequate.

### E. Consequence and Risk Engine
Evaluates consequence and required controls.

### F. Independent Governing Reference Monitor
Evaluates hard GSP invariants and produces the execution decision.

### G. Permit Service
Produces narrowly scoped, expiring, non-replayable execution permits.

### H. Constrained Dispatcher
Executes only actions that exactly match valid permits.

### I. Runtime Assurance Monitor
Watches live system and environment state.

### J. Autonomy Circuit Breaker
Stops execution and revokes authority when assurance falls below required conditions.

### K. Outcome Observer
Obtains independent evidence of the resulting effect.

### L. Reconciliation Engine
Determines whether the outcome matches the authorized action.

### M. Evidence Graph
Preserves causal receipts and completeness state.

### N. Assurance Case Engine
Maintains claims, supporting evidence, validity, and confidence decay.

### O. Liability Reconstruction Interface
Allows authorized investigators to reconstruct the authority-to-effect chain without allowing the interface itself to decide legal liability.

## 19. Governing state machine

A consequential GSP transition should progress through explicit states:

PROPOSED  
→ IDENTITY_VERIFIED  
→ AUTHORITY_VALIDATED  
→ POLICY_RESOLVED  
→ QUALITY_CLEARED  
→ CONSEQUENCE_EVALUATED  
→ REQUIRED_APPROVALS_SATISFIED  
→ ACTION_BOUND  
→ PERMIT_ISSUED  
→ DISPATCH_REVALIDATED  
→ DISPATCHED  
→ EFFECT_OBSERVED  
→ RECONCILED  
→ CLOSED

Failure branches include:

- IDENTITY_FAILED
- AUTHORITY_MISSING
- AUTHORITY_REVOKED
- POLICY_MISSING
- POLICY_CONFLICT
- QUALITY_INSUFFICIENT
- RISK_LIMIT_EXCEEDED
- APPROVAL_REQUIRED
- CONTEXT_CHANGED
- PERMIT_EXPIRED
- REPLAY_DETECTED
- PARAMETER_SUBSTITUTION
- ASSURANCE_DEGRADED
- CIRCUIT_BREAKER_OPEN
- DISPATCH_FAILED
- PARTIAL_EFFECT
- OUTCOME_UNKNOWN
- OUTCOME_MISMATCH
- INCIDENT

## 20. Control objective

The central GSP control objective is:

**A consequential AI or autonomous action must remain inside a continuously valid chain of authority, assurance, constraint, execution, and evidence from proposal through verified outcome.**

Any break in that chain must become visible to the system.

High-consequence profiles must be able to convert that break into reduced autonomy, challenge, suspension, or refusal.

## 21. Why this architecture is different from a conventional governance framework

A governance framework usually tells an organization what it should manage.

GSP is being engineered to make selected governance properties executable.

A policy framework may say:

"Maintain human oversight."

GSP asks:

Which human?
With what authority?
What did they see?
What did they approve?
For how long?
Was the action changed afterward?
Was the approval reused?
Did execution occur under the same conditions?
What effect actually occurred?

A policy framework may say:

"Manage AI risk."

GSP asks:

Was the evidence fit for risk evaluation?
Which conditions were assumed?
Did those conditions remain true?
Which control fired when they did not?
Can that be proven after the fact?

## 22. Engineering principle

The protocol should assume that intelligence will improve faster than institutions can manually supervise it.

The answer is not to make oversight depend on humans reading more logs.

The answer is to move accountability into the execution architecture itself.

That is the direction of GSP.
