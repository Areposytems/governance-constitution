# Agentic Software Adoption Checklist v0.1

Use this checklist when assessing whether an agentic software workflow is ready for responsible use.

## 1. Scope

* [ ] The agentic software use case is clearly defined.
* [ ] The expected users, maintainers, reviewers, or operators are identified.
* [ ] The affected repositories, branches, file paths, modules, tools, workflows, or environments are identified.
* [ ] The workflow is classified as assistive, repository-modifying, workflow-modifying, security-sensitive, operational, deployment-related, or exceptional.
* [ ] The affected persons, customers, services, systems, or institutions are identified where relevant.
* [ ] Local equivalent terms, roles, permissions, and responsible teams are mapped.

## 2. Human or institutional responsibility

* [ ] A responsible human person, team, office, or institution is identified.
* [ ] AI is not treated as the accountable maintainer, reviewer, release authority, security authority, or responsible decision-maker.
* [ ] The human reviewer understands the limits of the AI system.
* [ ] Final responsibility remains non-delegated.
* [ ] Escalation pathways are defined for uncertainty, error, dispute, or exceptional use.

## 3. Authorization

* [ ] The action class is identified.
* [ ] The workflow defines whether an LBA is required.
* [ ] Any required authorization record is created before consequential action.
* [ ] The authorization defines permitted repositories, branches, file paths, tools, environments, and action types.
* [ ] The authorization defines prohibited actions.
* [ ] The authorization has expiry, review, withdrawal, or renewal conditions.
* [ ] The workflow denies absent, expired, revoked, or out-of-scope authorization.

## 4. Evidence references

* [ ] The issue, ticket, requirement, incident, policy, or design reference is recorded.
* [ ] Source materials or source references are preserved where appropriate.
* [ ] Test results, CI output, security review notes, or logs are attached where relevant.
* [ ] Evidence references are distinguishable from authorization.
* [ ] Any uncertainty, limitation, or unresolved review issue is documented.

## 5. Change integrity

* [ ] Code changes are reviewable.
* [ ] Test changes are reviewable.
* [ ] Configuration changes are reviewable.
* [ ] Dependency changes are reviewable.
* [ ] CI/CD or workflow changes receive heightened review.
* [ ] Security-sensitive changes receive heightened review.
* [ ] Production or deployment-related changes receive explicit accountable approval.
* [ ] Changes to policy, schema, workflow, tool, or institutional practice are recorded.

## 6. Review, merge, release, and deployment

* [ ] Human review is required before merge where consequential action is involved.
* [ ] Human review is required before release or deployment where externally consequential action is involved.
* [ ] Review is not treated as a rubber stamp.
* [ ] The workflow defines who may approve merge, release, or deployment.
* [ ] Rollback, recovery, or pause conditions are defined.
* [ ] The workflow remains legitimate only within its defined scope.

## 7. Exit criteria

* [ ] The workflow can be paused, withdrawn, corrected, revoked, or escalated if errors are discovered.
* [ ] The use case has review or expiry conditions.
* [ ] The authorization trail can be inspected later.
* [ ] Proof-carrying state transitions are available where required.
* [ ] The system does not allow hidden execution paths or silent scope expansion.
