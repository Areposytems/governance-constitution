# Agentic Software Governance Mapping v0.1

## Purpose

This mapping explains how the Agentic Software Systems Domain Profile relates to repository governance, AI coding agents, CI/CD, developer platforms, software supply-chain concerns, and institutional software operations.

It is intentionally high-level and should be updated as technical capabilities, platform rules, security requirements, institutional policies, and software governance practices evolve.

## Mapping table

|Current concern|Agentic software governance response|
|-|-|
|AI-generated pull requests|Require scoped authorization, evidence references, human review, and non-delegated maintainer responsibility before merge|
|Agent modifies files outside task scope|Require explicit repository, branch, file path, module, tool, action-class, and expiry boundaries|
|Agent changes tests to fit its own code|Classify test modification as consequential and require review, evidence references, and scope checks|
|Agent modifies CI/CD or review gates|Treat workflow changes as high-risk and require formal authorization and heightened review|
|Agent touches security-sensitive code|Require narrow authorization, security review, proof-carrying records, and accountable human approval|
|Agent prepares deployment or release|Require explicit authorization, review trail, rollback conditions, and responsible release authority|
|Agent uses tools or APIs beyond intended scope|Require permitted and prohibited tool boundaries in authorization artifacts|
|Successful tests mistaken for legitimacy|Clarify that tests provide evidence but do not authorize action|
|Human approval becomes a rubber stamp|Require meaningful review and identifiable accountability before merge, release, or deployment|
|Responsibility disappears into automation|Require final accountable human person, team, office, or institution|
|Policy or workflow drift|Record policy, schema, workflow, and state changes through proof-carrying change records|
|Commercial or production adoption|Require appropriate licensing, institutional review, and local implementation governance where applicable|

## Operational translation

An institution using agentic software systems should be able to answer:

1. Was an AI agent used?
2. What was it used for?
3. Was the output exploratory, assistive, repository-modifying, workflow-modifying, security-sensitive, operational, or deployment-related?
4. Was the output merely proposed, or was it acted on?
5. Who authorized it?
6. What repository, branch, file path, tool, or environment was in scope?
7. What evidence supported the action?
8. What policy or institutional rule applied?
9. Was a Legitimacy Binding Artifact required?
10. Was a proof-carrying state transition required?
11. Who reviewed the change?
12. Who remains responsible?
13. When does the authorization expire or require review?
14. What happens if the action is absent, expired, revoked, or out of scope?

## Boundary

This mapping does not certify software safety, cybersecurity, legal compliance, production readiness, or institutional adequacy.

It gives institutions a structured way to discuss whether agentic software workflows can prove authorization, scope, evidence references, reviewability, expiry, and accountable responsibility before consequential action occurs.
