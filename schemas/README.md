# Schemas

This directory contains machine-checkable structural definitions associated with the Governance Constitution.

## Available schemas

* [`lba.schema.json`](lba.schema.json) — structural schema for a Legitimacy Binding Artifact.
* [`pcsu_transition.schema.json`](pcsu_transition.schema.json) — structural schema for a Proof-Carrying State Update transition record.

## Purpose

The schemas define the required structure, field types, permitted values, basic formats, and closed-object boundaries of constitutional artifacts.

They support interoperable validation and help prevent silent field expansion, malformed records, missing required properties, and structurally ambiguous artifacts.

## Validation boundary

> **Schema-valid does not automatically mean constitutionally legitimate.**

JSON Schema validation establishes structural conformity only.

Depending on the artifact and adopting system, structural validation may confirm:

* required fields are present;
* values have the required JSON types;
* identifiers and strings meet declared length or pattern constraints;
* objects contain no undeclared properties where `additionalProperties` is false;
* enumerated values are within the permitted set;
* timestamp strings use a recognised date-time format;
* `non_delegation` is set to `true` where required;
* signature objects contain their required fields.

Structural validation does not by itself establish:

* that an action is authorized;
* that an approver possessed the relevant authority;
* that an approval threshold was met;
* that a signature is cryptographically valid;
* that an identifier or hash resolves to the intended immutable artifact;
* that evidence references are accurate, sufficient, or reliable;
* that an action falls within the permitted scope;
* that an authorization is currently applicable;
* that an artifact has not been revoked or superseded;
* that an action is safe, correct, lawful, ethical, compliant, or institutionally approved;
* that the Governance Constitution, mMRM specification, applicable policy snapshot, lane schema, and local institutional requirements have been satisfied.

## LBA validation layers

A conforming implementation should distinguish at least the following validation layers.

### 1. Structural validation

Validate the artifact against `lba.schema.json`.

### 2. Canonicalization and identifier validation

Apply the implementation’s declared canonicalization method and verify that the LBA identifier or content-hash reference corresponds to the intended artifact.

### 3. Signature validation

Verify each signature using the declared algorithm and applicable key material.

A structurally present signature is not necessarily a valid signature.

### 4. Approver and threshold validation

Verify that:

* the listed approvers were authorized for the use case and action class;
* the required approval threshold was satisfied;
* separation-of-duties requirements were preserved; and
* participation, assistance, review, or evidence production was not mistaken for approval.

### 5. Temporal validation

Verify that:

* `expires_at` is later than `issued_at`;
* the authorization has not expired;
* any applicable review or renewal period remains valid; and
* the evaluation uses an appropriate trusted time source.

### 6. Revocation and supersession validation

Verify whether the LBA:

* has been revoked;
* has been explicitly superseded;
* overlaps with another LBA; or
* is subject to declared precedence rules in the applicable policy snapshot or lane schema.

### 7. Scope validation

Verify that the proposed action matches:

* the use-case identifier;
* the action-class identifier;
* the applicable policy snapshot;
* the applicable lane schema;
* the explicit allow list;
* the explicit deny list;
* the relevant system, workflow, repository, environment, or institutional boundary; and
* any other declared scope restriction.

### 8. Constitutional and institutional validation

Verify that the action remains consistent with:

* the Governance Constitution;
* the mMRM Legitimacy Kernel Specification;
* applicable constitutional schemas;
* the relevant domain profile where used;
* applicable policy and lane definitions; and
* external legal, professional, technical, security, regulatory, and institutional requirements.

## PCSU validation layers

A conforming implementation should distinguish structural validation of a PCSU transition record from validation of the transition itself.

In addition to validation against `pcsu_transition.schema.json`, an implementation may need to verify:

* that `prev_state_hash` identifies the actual prior state;
* that `next_state_hash` identifies the resulting state;
* that triggering events exist and are properly ordered;
* that the selected ordering clock is interpreted correctly;
* that vector data is present and coherent when vector-clock semantics are used;
* that freshness timestamps satisfy local temporal and ordering rules;
* that the transition has not expired before application or reliance;
* that the reason code is permitted by the applicable policy;
* that the proof bundle exists and supports the transition;
* that applicable policy and lane-schema references resolve correctly;
* that signatures are valid and made by authorized signers; and
* that reconciliation, schema supersession, and state-transition rules are satisfied.

## Relationship to legitimacy

The schemas support proof-carrying governance but do not themselves bind legitimacy.

Where Action Lane legitimacy is at issue, legitimacy remains governed by the Governance Constitution, the mMRM Legitimacy Kernel Specification, an applicable unexpired LBA, the relevant immutable policy and lane-schema references, and any required external institutional authority.

Schema validation is one necessary control where a schema applies. It is not a substitute for authorization, review, signature verification, policy evaluation, evidence assessment, or accountable responsibility.

## Examples

Files in the repository’s `examples/` directory are illustrative only.

An example may be structurally valid while remaining intentionally unsuitable for operational use because it contains placeholder identifiers, example signatures, fictional authorities, expired timestamps, or non-operational policy references.
