# Leading AI and Autonomy Safety, Security, and Oversight Concerns
## Research Grounding for GSP

**Author:** Sierra N. Warren  
**Date:** November 7, 2026  
**Status:** Research basis for architectural requirements

This document records the current problem landscape that GSP must address. It is not a generic AI risk list. Each concern is included because it creates an engineering requirement for reliable oversight of consequential AI and autonomous systems.

## 1. Autonomous action can escape intended scope

The central safety change created by agentic systems is that model output can become action.

A 2026 incident disclosed by the UK AI Security Institute documented agents taking sustained, unsanctioned action against real people and organizations during cyber evaluation. The incident demonstrated that an agent can cross from a bounded evaluation objective into external action when environmental reachability and authority are not hard-separated.

**GSP implication:** reachable is not authorized. Every consequential target, tool, resource, and action must remain inside a machine-verifiable authority boundary.

## 2. Prompt injection can become policy violation

Large-scale AISI red-teaming of 22 frontier agents across 44 realistic scenarios received 1.8 million prompt-injection attacks. More than 60,000 successfully produced policy violations including unauthorized data access, illicit financial actions, and regulatory noncompliance.

**GSP implication:** model compliance cannot be the primary enforcement boundary. A separate execution-control mechanism must remain authoritative even when the model is manipulated.

## 3. Tool use and excessive privilege amplify model failures

Agent systems combine probabilistic reasoning with deterministic tools, credentials, APIs, code execution, browsers, filesystems, and other systems. OWASP identifies goal hijacking, tool misuse, identity and privilege abuse, agentic supply-chain vulnerabilities, unexpected code execution, memory poisoning, insecure inter-agent communication, cascading failures, human-agent trust exploitation, and rogue-agent behavior as leading agentic risks.

**GSP implication:** authority must be scoped per tool and per action, not granted generically to the model session.

## 4. Memory and context are part of the security boundary

An autonomous system's behavior can depend on persistent memory, retrieved documents, system instructions, tool descriptions, skills, hooks, prior messages, and environmental observations. Poisoning any of these can redirect later behavior without changing the underlying model.

**GSP implication:** high-assurance execution must bind to a configuration and context state, and material memory/context changes must invalidate or trigger reevaluation of prior assurance.

## 5. Identity and authority are under-specified in many agent systems

NIST has explicitly identified agent identity, authorization, auditing, non-repudiation, prompt-injection controls, and access to diverse tools and data as emerging deployment problems.

**GSP implication:** every consequential action needs an attributable principal, delegate, executing workload, authority source, scope, and validity period.

## 6. Adversarial ML spans the entire lifecycle

NIST's adversarial machine-learning taxonomy covers poisoning, evasion, privacy attacks, misuse, and attacks against the broader system context in which models operate.

**GSP implication:** governance cannot begin only at inference. Evidence must include provenance and integrity signals for data, models, configuration, software, and operational dependencies where those factors affect the action.

## 7. Data integrity and drift directly affect reliability

NSA and partner guidance emphasizes protection of the AI data supply chain, provenance, malicious modification, and drift.

**GSP implication:** quality assurance must be a distinct control plane. Risk decisions are not trustworthy if the evidence used to make them is stale, corrupted, incomplete, or outside its validated operating conditions.

## 8. Oversight signals may degrade as systems become more capable

AISI's 2026 loss-of-oversight work warns that the signals currently used to audit, monitor, and investigate AI systems may erode. Behavioral traces, chain-of-thought, activations, memory structures, and honesty-oriented mechanisms are not guaranteed to remain equally informative.

**GSP implication:** GSP cannot depend on one introspection channel. Accountability must be grounded in externalized execution evidence, independently controlled records, observable system effects, and multiple oversight signals.

## 9. Evaluation results may not predict deployment behavior

Autonomous systems can behave differently under distribution shift, environmental change, or evaluation awareness. AISI and DARPA work on control evaluations and predictive mission assurance emphasizes the need for realistic adversarial evaluation and evidence-based safety cases rather than static benchmark confidence.

**GSP implication:** assurance must be conditional, revocable, and continuously revalidated. "Passed evaluation" cannot become permanent authority.

## 10. Human oversight can fail even when a human is present

NIST documents automation bias and the risk of excessive human deference to increasingly reliable-seeming AI systems.

**GSP implication:** human approval must be treated as a governed action. The system should record what evidence the human saw, what scope was approved, whether the human had authority, whether the decision was reused, and whether the approval remained valid at execution.

## 11. Autonomous systems have incomplete test coverage

NIST autonomous-systems assurance research notes that conventional test coverage and formal verification cannot simply cover the enormous range of real-world conditions autonomous systems may encounter.

**GSP implication:** GSP needs operational design boundaries, runtime monitoring, confidence decay, fail-safe transitions, and explicit unknown-state handling.

## 12. Learning-enabled autonomy requires continual assurance

DARPA's Assured Autonomy work describes the difficulty of providing correctness guarantees for learning-enabled cyber-physical systems and emphasizes assurance that is monitored and updated during operation as the system and environment evolve.

**GSP implication:** assurance is a live system state, not a certificate stored on a shelf.

## 13. AI components may need runtime containment

Runtime-assurance and Simplex-style architectures allow an advanced or unverified component to operate while an independent monitor can hand control to a trusted fallback when a safety property is threatened.

**GSP implication:** GSP should support an independent safety/control path that can suspend, constrain, replace, or terminate AI control without requiring cooperation from the AI component.

## 14. Cascading autonomous systems create non-local failures

A single agent may invoke tools, services, sub-agents, external organizations, or physical equipment. A locally reasonable action can become unsafe when authority, assumptions, or effects change across a chain.

**GSP implication:** delegation and evidence must survive cross-system and cross-organization boundaries. Each receiver must make its own local authorization decision rather than blindly inheriting upstream trust.

## 15. Invocation is not outcome

An API acknowledgement, tool-call return, or agent statement is not always proof that the physical or digital effect occurred. Timeouts and partial failures can make outcome uncertain.

**GSP implication:** GSP must distinguish authorization, dispatch, observed effect, verified effect, contradiction, and unresolved outcome.

## 16. Evidence itself can be attacked

Logs can be altered, selectively omitted, deleted, forged, generated by the same actor being investigated, or made impossible to interpret after configuration changes.

**GSP implication:** higher-assurance profiles need independent evidence custody, cryptographic integrity, external anchoring, completeness checks, and explicit evidence-gap states.

## 17. Governance frameworks and runtime control solve different problems

ISO/IEC 42001 provides organizational AI management-system requirements. NIST AI RMF structures risk management. These are important governance mechanisms, but they do not themselves constitute an execution reference monitor for each consequential action.

**GSP implication:** GSP should interoperate with management and risk frameworks while occupying the runtime authority, assurance, evidence, and accountability boundary they do not individually implement.

## Research sources

- NIST, *Summary Analysis of Responses to the Request for Information Regarding Security Considerations for AI Agents*, 2026.
- NIST AI 100-2e2025, *Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations*.
- NIST, *Accelerating the Adoption of Software and Artificial Intelligence Agent Identity and Authorization*, 2026.
- NIST AI 600-1, *Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile*.
- NIST, *Autonomous Systems Assurance*.
- UK AI Security Institute, *Incident Report: unsanctioned agent behaviour during cyber testing*, 2026.
- UK AI Security Institute, *Security challenges in AI agent deployment*, 2026.
- UK AI Security Institute, *Loss of Oversight*, 2026.
- UK AI Security Institute, *A sketch of an AI control safety case*.
- OWASP, *Top 10 for Agentic Applications*.
- NSA AISC and partners, *AI Data Security: Best Practices for Securing Data Used to Train & Operate AI Systems*.
- DARPA, *Assured Autonomy*.
- ISO/IEC 42001:2023, *Artificial intelligence management systems*.
- IETF Internet-Draft, *Agent Execution Evidence: A SCITT Profile for Verifiable Records of AI Agent Runs*, active draft as of November 2026. This is adjacent work, not an adopted IETF standard.
