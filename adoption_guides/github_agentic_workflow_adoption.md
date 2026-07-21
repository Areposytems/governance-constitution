# GitHub Agentic Workflow Adoption Guide v0.1

Status: Early draft  
Type: Non-normative adoption guide

## Purpose

This guide outlines how a GitHub-style repository, software team, open-source project, or enterprise developer platform could begin assessing AI coding-agent workflows through the Agentic Software Systems Domain Profile.

## Step 1: Inventory agentic software uses

Identify where AI agents are used or may be used:

* issue triage or summarisation;
* code explanation;
* branch creation;
* source-code edits;
* test generation or modification;
* documentation updates;
* dependency update proposals;
* pull request creation;
* CI/CD configuration changes;
* workflow automation;
* release preparation;
* deployment support;
* security-sensitive code changes;
* production or customer-facing workflow changes.

## Step 2: Classify action categories

Classify each use as:

* low-risk assistive support;
* medium-risk repository support;
* high-risk workflow or security use;
* high-risk operational use;
* prohibited or exceptional use.

## Step 3: Define authorization requirements

For each category, identify:

* whether a Legitimacy Binding Artifact is required;
* who may issue or approve the authorization;
* what repository, branch, file path, module, tool, or environment may be in scope;
* what action class is permitted;
* what actions are expressly denied;
* when the authorization expires;
* when authorization must be revoked, renewed, or narrowed.

## Step 4: Define evidence references

For consequential agentic actions, record where appropriate:

* issue, ticket, requirement, or incident reference;
* source documents or design notes;
* policy version;
* related pull request, branch, or commit reference;
* test results or CI output;
* security review notes;
* responsible reviewer or maintainer;
* applicable authorization record;
* expiry, review, withdrawal, or renewal conditions.

## Step 5: Define review and denial paths

Identify how the workflow handles:

* absent authorization;
* expired authorization;
* revoked authorization;
* out-of-scope file changes;
* out-of-scope tool calls;
* attempts to modify CI/CD or review gates;
* attempts to self-approve;
* security-sensitive changes;
* production or deployment-related changes;
* rollback, recovery, or escalation.

## Step 6: Start narrow

Begin with low-risk or medium-risk workflows in non-production repositories.

Do not begin with autonomous merge, deployment, security-sensitive changes, permission changes, secrets handling, or production-impacting workflows.

## Step 7: Review and iterate

Review the workflow regularly and update policies, schemas, authorizations, and controls through explicit change records.

Agentic software governance should expand only after its authorization, reviewability, expiry, denial, and accountability paths have been tested.
