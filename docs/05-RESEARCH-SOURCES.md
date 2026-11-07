# Research Sources Grounding the Forward GSP Architecture

**Compiled by:** Sierra N. Warren  
**Date:** November 7, 2026

This source ledger supports the current GSP restructuring. Inclusion does not imply endorsement, equivalence, or that any external source defines GSP.

## AI agent security and autonomy

### UK AI Security Institute

**Incident Report: unsanctioned agent behaviour during cyber testing**  
https://www.aisi.gov.uk/blog/incident-report-unsanctioned-agent-behaviour-during-cyber-testing

AISI disclosed sustained, unsanctioned agent action directed at real people and organizations during a cyber evaluation. This supports GSP requirements for independent authority boundaries, egress control, containment, revocation, and emergency stop mechanisms.

**Security challenges in AI agent deployment: Insights from a large scale public competition**  
https://www.aisi.gov.uk/research/security-challenges-in-ai-agent-deployment-insights-from-a-large-scale-public-competition

AISI reports 1.8 million prompt-injection attacks against 22 frontier agents across 44 realistic scenarios, with more than 60,000 successful policy violations. This supports moving consequential enforcement outside the model itself.

## Agentic threat taxonomy

### OWASP GenAI Security Project

**OWASP Top 10 for Agentic Applications 2026**  
https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/

Relevant risk classes include agent goal hijacking, tool misuse, identity and privilege abuse, agentic supply-chain vulnerabilities, unexpected code execution, memory and context poisoning, insecure inter-agent communication, cascading failures, human-agent trust exploitation, and rogue agents.

**GenAI and Agentic AI Exploit Roundup Q3 2026**  
https://genai.owasp.org/2026/10/08/genai-and-agentic-ai-exploit-roundup-q3-2026/

Used as incident-oriented evidence for excessive agency, privilege expansion, unapproved communication paths, persistent-memory manipulation, and the need for independent network, identity, and execution controls.

## Identity, authorization, and agent security

### National Institute of Standards and Technology

**New Concept Paper on Identity and Authority of Software Agents**  
https://www.nist.gov/news-events/news/2026/02/new-concept-paper-identity-and-authority-software-agents

NIST identifies agent identification, authorization, auditing, non-repudiation, access to tools and data, and prompt-injection defenses as important deployment concerns.

**Summary Analysis of Responses to the Request for Information Regarding Security Considerations for AI Agents (NIST 800-5)**  
https://www.nist.gov/publications/summary-analysis-responses-request-information-regarding-security-considerations-ai

The analysis reports broad agreement that AI agents introduce novel security threats and that existing cybersecurity practices require adaptation.

**Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations (NIST AI 100-2e2025)**  
https://csrc.nist.gov/pubs/ai/100/2/e2025/final

Used to ground lifecycle-level concerns including poisoning, evasion, privacy attacks, and misuse.

**Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile (NIST AI 600-1)**  
https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf

Used for human factors, confabulation, automation bias, information-integrity, and lifecycle risk context.

## Continual assurance and autonomous systems

### DARPA

**Assured Autonomy**  
https://www.darpa.mil/research/programs/assured-autonomy

DARPA defines continual assurance as safety and functional-correctness assurance established provisionally at design time and continually monitored, updated, and evaluated during operation as the system and environment evolve.

This directly informs GSP's Live Assurance State and conditional/revocable assurance model.

## AI data and system integrity

### NSA Artificial Intelligence Security Center and partners

**AI Data Security: Best Practices for Securing Data Used to Train & Operate AI Systems**  
https://www.nsa.gov/Press-Room/Press-Releases-Statements/Press-Release-View/Article/4209451/nsa-and-partners-release-guidance-on-ai-data-security/

Used to ground GSP requirements for provenance, integrity, data-supply-chain controls, drift awareness, and quality-before-risk.

## Adjacent execution-evidence work

### IETF / SCITT

**Agent Execution Evidence: A SCITT Profile for Verifiable Records of AI Agent Runs**  
https://datatracker.ietf.org/doc/draft-emirdag-scitt-ai-agent-execution/

This is active Internet-Draft work, not an adopted IETF standard. It is tracked as adjacent work concerning verifiable post-execution evidence. GSP should compose with applicable standards where useful while preserving its wider pre-execution reliability, authority, quality, runtime-assurance, and liability-reconstruction scope.

## Management-system context

### ISO

**ISO/IEC 42001:2023 Artificial intelligence management systems**  
https://www.iso.org/standard/81230.html

ISO/IEC 42001 addresses organizational AI management systems. GSP treats management-system governance and runtime technical enforcement as distinct but complementary layers.

## Research rule

External work is used to define the problem, discover mature mechanisms, identify overlap, and sharpen GSP's contribution.

Existing mechanisms are not relabeled as GSP inventions.

The GSP contribution is evaluated at the level of architecture, system composition, control semantics, and the resulting authority-to-outcome accountability model.
