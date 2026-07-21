# Agentic Software Systems Domain Profile v0.1

## 1. Status

Draft domain profile.  
Compatible with Governance Constitution v1.0.1.  
Non-normative unless explicitly adopted by an institution.

This version is written as an environment-neutral agentic software translation profile. It should be adapted through the technical architecture, repository rules, security requirements, development practices, deployment procedures, institutional policies, and terminology of each adopting software environment.

## 2. Purpose

This profile translates the Governance Constitution into agentic software systems language for institutions considering responsible AI governance in software, repository, automation, tool-use, and deployment workflows.

It is intended for discussion by software teams, repository maintainers, AI coding agent developers, enterprise platform teams, developer tooling providers, software governance teams, security reviewers, compliance teams, open-source maintainers, and institutions using AI agents in technical workflows.

This document is not a software safety certification, cybersecurity assurance, legal opinion, regulatory compliance scheme, audit approval, production-readiness assessment, or substitute for secure development practices.

## 3. Environment-neutral interpretation

This profile is intended to travel across software environments. Terms such as **repository**, **branch**, **pull request**, **issue**, **ticket**, **deployment**, **workflow**, **CI/CD**, **maintainer**, **reviewer**, **release manager**, **production environment**, **tool call**, and **agent** should be read according to the equivalent systems, roles, permissions, and safeguards in the adopting environment.

Where local terminology differs, institutions should preserve the functional requirement rather than the exact wording.

## 4. Agentic software-domain translation

|Governance Constitution concept|Agentic software-domain translation|
|-|-|
|Legitimacy|Recognised authority to perform or prepare a consequential software action|
|Action Lane|Externally or institutionally consequential software, repository, workflow, infrastructure, or deployment action|
|Evidence Lane|Source-grounded issue, ticket, requirement, policy, test, log, review, incident, or documentation material requiring verification before reliance|
|Idea Lane|Exploration, drafting, code suggestion, debugging hypothesis, design discussion, or non-applied prototype not yet relied on for consequential action|
|Non-delegation|Accountable human or institutional responsibility cannot be transferred to an AI agent, model, vendor, platform, workflow, or automated process|
|LBA|Time-bounded authorisation record for a scoped agentic software action class|
|PCSU|Proof-carrying record of code, configuration, schema, dependency, workflow, policy, infrastructure, release, or deployment state change|
|CAA|Read-only assurance and workflow observability, without certification or approval authority|
|No semantic authority|The kernel does not determine code correctness, security, safety, legality, production readiness, business value, or engineering adequacy|
|No silent escalation|AI assistance must not quietly become repository authority, deployment authority, security authority, release authority, or operational decision authority|

## 5. Agentic software-domain principles

### 5.1 Authorization before consequential action

AI agents should not perform or prepare consequential software actions without an applicable authorization artifact.

Consequential actions may include modifying repository files, opening or updating pull requests, changing tests, altering configuration, modifying dependencies, changing workflow rules, preparing deployment steps, or interacting with protected tools.

A general instruction such as "fix the repo," "improve the system," or "make the agent productive" should not be treated as sufficient authorization for broad consequential action.

### 5.2 Scope and expiry

Agentic software permissions should be scoped by relevant boundaries such as repository, branch, file path, module, issue, ticket, action class, tool, environment, and time.

Authorization should not silently expand from one task into adjacent files, workflows, tools, repositories, environments, or deployment pathways.

Agentic authorization should expire. Evergreen authorization is not appropriate for consequential software action.

### 5.3 Human or institutional accountability

AI agents may assist, draft, propose, summarize, test, refactor, classify, route, or prepare software changes.

They should not be treated as accountable maintainers, responsible reviewers, release authorities, security authorities, product owners, or substitutes for human or institutional responsibility.

Where a consequential action is merged, released, deployed, or relied on, the accountable person, office, team, or institution should remain identifiable.

### 5.4 Evidence-linked change

Agentic software actions should be linked to relevant source material, such as issues, tickets, requirements, incident reports, policies, test results, review records, logs, or design documents.

Evidence references support the action, but they do not themselves authorize action.

Tests, CI results, model confidence, static analysis, or successful execution should not be mistaken for legitimacy.

### 5.5 Proof-carrying state transitions

Where an agentic system prepares or performs a meaningful change to code, configuration, schema, dependency state, workflow rules, infrastructure, release artifacts, or deployment state, the change should be inspectable and connected to the applicable authorization record.

A proof-carrying record should help identify what changed, why it changed, which authorization applied, what evidence supported the change, who or what prepared it, who reviewed it, and whether it remained within scope.

### 5.6 Review before merge, release, or deployment

Agentic software systems should preserve meaningful human or institutional review before merge, release, deployment, production change, or other externally consequential action.

Review should not become a rubber stamp over agentic output.

High-risk changes should receive proportionate review, especially where they affect security, authentication, authorization, data handling, user rights, financial operations, regulated systems, safety-critical systems, or public-facing services.

## 6. Agentic software use categories

|Category|Examples|Governance posture|
|-|-|-|
|Low-risk assistive support|Issue summaries, code explanation, documentation suggestions, non-applied snippets, draft comments, test ideas|Light recordkeeping and ordinary supervision|
|Medium-risk repository support|Draft pull requests, source edits, test changes, documentation commits, small refactors, dependency suggestions|Scoped authorization, evidence references, human review, source retention|
|High-risk workflow or security use|CI/CD changes, deployment scripts, access control, authentication logic, dependency sources, secrets handling, audit or telemetry changes|Formal authorization, heightened review, proof-carrying transition records, narrow scope and expiry|
|High-risk operational use|Release preparation, production configuration, infrastructure-as-code, live service behaviour, user-facing workflow changes, regulated or rights-affecting systems|Explicit authorization, accountable human approval, review trail, rollback or recovery conditions|
|Prohibited or exceptional use|Autonomous merge, unsupervised production deployment, unauthorized permission escalation, secret access outside scope, self-approval, bypassing review gates|Not legitimate without explicit lawful or institutional authority, exceptional safeguards, reviewability, and non-delegated accountability|

## 7. Relationship to existing software governance, safety, and security

This profile does not replace software governance, cybersecurity, secure development practices, legal obligations, regulatory obligations, or institutional policy.

It is a structural translation layer intended to support, where applicable:

* secure development lifecycle practices;
* code review and maintainer responsibility;
* software supply-chain governance;
* change management;
* incident response;
* access control and permission management;
* deployment governance;
* auditability and recordkeeping;
* model, tool, vendor, and platform accountability;
* human review before consequential software action.

## 8. Adoption rule

An institution adopting this profile should define:

1. the local software terms that correspond to this profile's environment-neutral terms;
2. the agentic software use categories permitted, restricted, or prohibited in that institution;
3. the action classes that require a Legitimacy Binding Artifact;
4. the repositories, branches, files, tools, workflows, or environments that may be in scope;
5. the human roles that remain accountable;
6. the records required before merge, release, deployment, or other consequential action;
7. the denial process for absent, expired, revoked, or out-of-scope authorization;
8. the review, rollback, recovery, and expiry conditions that apply;
9. the process for updating the profile when tools, models, repositories, workflows, policies, or institutional practices change.

## 9. Closing statement

Software institutions should not discover agentic misuse only after systems, repositories, workflows, or production environments have already changed.

This profile asks institutions to move authorization, scope, evidence references, proof-carrying change, reviewability, expiry, and accountable responsibility upstream before AI-assisted software activity becomes consequential action.
