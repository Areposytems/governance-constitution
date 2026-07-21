# Software Environment Adaptation Note v0.1

## Purpose

The Agentic Software Systems Domain Profile is environment-neutral. This note helps adopting teams translate the profile into their local software environment without changing the constitutional core.

Different software environments use different platforms, roles, permissions, workflows, artifacts, review processes, deployment paths, and security controls.

## Core rule

Adopt the function, not merely the wording.

If a term in the profile does not match the local software environment, the adopting team should identify the equivalent local system, role, permission, workflow, artifact, or safeguard.

## Common translation pairs

|Environment-neutral term|Possible local equivalents|
|-|-|
|Repository|Project, codebase, workspace, monorepo, package, service directory, source-control project|
|Branch|Feature branch, working branch, change branch, workspace branch, patch branch, fork branch|
|Pull request|Merge request, change request, patch review, code review artifact, review request, proposed change record|
|Issue|Ticket, task, work item, story, bug report, incident, requirement, change request|
|Maintainer|Repository owner, project owner, code owner, technical lead, module owner, service owner|
|Reviewer|Code reviewer, security reviewer, approving engineer, release reviewer, governance reviewer|
|Release manager|Deployment owner, release owner, production approver, change manager, operations lead|
|CI/CD|Build pipeline, test pipeline, deployment pipeline, workflow automation, release automation|
|Workflow|Automation rule, pipeline, job, action, task sequence, orchestration path, toolchain step|
|Production environment|Live environment, customer-facing system, operational environment, regulated environment, protected environment|
|Tool call|API call, plugin action, shell command, workflow action, integration call, automation step|
|Agent|AI coding agent, tool-using model, autonomous workflow, assistant, automation worker, orchestration agent|
|Authorization record|Approval record, LBA, change ticket, delegated authority record, governance artifact, decision log|
|Proof-carrying state transition|PCSU, change record, signed transition, audit-linked state change, deployment record, workflow transition record|
|Scope boundary|Repository, branch, file path, module, service, environment, action class, tool boundary, time window|
|Denied action|Blocked action, prohibited tool call, restricted workflow, forbidden file path, disallowed escalation|
|Human review|Maintainer review, code review, security review, release approval, change advisory review, accountable sign-off|

## Local adaptation questions

Before adoption, the team or institution should answer:

1. Which local systems correspond to repository, branch, pull request, issue, workflow, CI/CD, and deployment?
2. Which roles correspond to maintainer, reviewer, approver, release manager, security reviewer, and accountable institution?
3. Which agentic actions are merely assistive?
4. Which agentic actions modify repositories, workflows, infrastructure, dependencies, permissions, or deployment state?
5. Which action classes require a Legitimacy Binding Artifact?
6. Which changes require a proof-carrying state transition record?
7. What local artifact proves authorization before the agent acts?
8. What evidence references must be attached before reliance, merge, release, or deployment?
9. Which repositories, branches, file paths, modules, tools, workflows, or environments are in scope?
10. Which actions must be denied even if technically possible?
11. When does authorization expire, require review, or require renewal?
12. Who remains accountable after the agent prepares, modifies, or proposes a change?
13. How can the authorization trail be inspected later?
14. How can the workflow be paused, revoked, rolled back, or escalated if the agent acts outside scope?

## Boundary

This note does not create software safety, cybersecurity, legal, regulatory, compliance, audit, certification, or production-readiness approval.

It supports translation between the Governance Constitution and local software environments.