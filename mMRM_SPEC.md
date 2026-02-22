# mMRM Legitimacy Kernel Specification v1.0

## 0. Status
Normative. This specification defines the **minimal legitimacy kernel** (“mMRM”) required for constitutional governance of Action in complex systems.

mMRM (Minimal Model Risk Management) serves as the system’s minimal legitimacy kernel.

mMRM is intentionally small. Anything not needed to prevent legitimacy failure modes is out of scope.

## 1. Purpose (one sentence)
mMRM exists solely to define, bind, and expose **legitimacy-critical decisions** so they cannot be laundered, drowned, forked, or captured.

## 2. Non-goals
mMRM MUST NOT:
- score risk, classify safety, or judge correctness/meaning
- monitor continuously or run assurance/audit
- gate interfaces or execute actions
- certify systems, vendors, or organizations
- become a centralized authority by virtue of implementation

These functions belong to other layers (mediation, assurance, trajectory control, recovery, proof-carrying updates).

## 3. Definitions

### 3.1 Action Lane
A lane in which operations occur that are externally consequential (execution, deployment, irreversible change, binding decisions).

### 3.2 Legitimacy-Critical Event (LCE)
An event whose occurrence authorizes or materially enables Action Lane execution.
Examples include (non-exhaustive):
- granting or renewing an Action authorization
- overriding a previously imposed stop/hold
- recognizing a foreign policy snapshot for a use-case
- extending or narrowing authorization scope

### 3.3 Legitimacy Binding Artifact (LBA)
An immutable artifact that records a legitimacy decision for a specific use-case and action class, bound to:
- a policy snapshot hash
- lane schema hash
- evidence references
- threshold approvers
- time-bounded validity (expiry)

LBAs are sparse and enumerable. They are the only legitimacy source of truth.

### 3.4 Evidence Reference
A pointer to evidence artifacts (IDs only), not evidence content. Evidence is out of scope; only references are bound here.

## 4. Core Invariants (normative)

### mMRM-1 — Action requires an LBA
No Action Lane execution is legitimate without an **unexpired** LBA explicitly authorizing that action class for that use-case.

### mMRM-2 — Participation is not approval
Evidence production, federation participation, assistance, or verification does **not** constitute approval unless explicitly bound in an LBA.

### mMRM-3 — No implicit policy equivalence
Policy snapshots are not equivalent by default. Recognition/equivalence for a given use-case MUST be explicitly granted via an LBA.

### mMRM-4 — Legitimacy is sparse and enumerable
All LBAs active in a time window MUST be enumerable. If none exist, legitimacy is absent for that window.

### mMRM-5 — Legitimacy expires
Every LBA MUST expire. Evergreen legitimacy is prohibited.

## 5. Legitimacy Binding Artifact (LBA) Requirements

### 5.1 Required fields
An LBA MUST include:
- `lba_id` (content hash or canonical hash reference)
- `use_case_id`
- `action_class_id`
- `policy_snapshot_hash`
- `lane_schema_hash`
- `evidence_refs` (array of IDs; MAY be empty)
- `approver_ids` (array; MAY be empty only if policy explicitly allows zero-approver mode, which is discouraged)
- `approval_scope` (explicit allow + explicit deny/boundary text)
- `issued_at` (RFC3339)
- `expires_at` (RFC3339; must be > issued_at)
- `non_delegation` (boolean; MUST be true in mMRM)
- `signatures` (array of signature objects)

Optional:
- `supersedes_lba_id` (for explicit replacement)
- `revoked_at` and `revocation_reason_code` (if you support revocation; recommended)

### 5.2 Validity rules
An LBA is valid if:
- signatures meet threshold policy defined by the system’s governance (external to this spec, but verifiable)
- `expires_at` has not passed
- it references immutable hashes for `policy_snapshot_hash` and `lane_schema_hash`
- it is not revoked (if revocation is supported)

### 5.3 Supersession rules
Supersession MUST be explicit:
- a new LBA that supersedes MUST reference `supersedes_lba_id`
- supersession does not erase the prior LBA; both remain enumerable
- if two LBAs overlap in scope/time, precedence rules MUST be declared in the lane schema or policy snapshot

## 6. Minimal Interfaces (implementation-neutral)
Implementations MAY be a service, an append-only log, a ledger, or a file-based registry.

These interfaces are illustrative and do not prescribe an API, protocol, or deployment model.

mMRM MUST support at least:

### 6.1 `EnumerateLBAs(time_window)`
Return all LBAs issued/active in the window (issued, active, expired, revoked) with stable ordering.

### 6.2 `GetLBA(lba_id)`
Fetch LBA by ID.

### 6.3 `ValidateAction(use_case_id, action_class_id, policy_snapshot_hash, lane_schema_hash, now)`
Return:
- `allowed: true/false`
- `reason_code` (e.g. NO_LBA, EXPIRED, SCOPE_MISMATCH, HASH_MISMATCH, SIGNATURE_INVALID)
- `matched_lba_id` (if any)

mMRM MUST NOT execute the action. It only returns legitimacy status.

## 7. Federation Rules (minimal)
Cross-system recognition MUST NOT be implied. To rely on a foreign snapshot/policy:
- an LBA MUST explicitly bind recognition for the use-case/action class
- evidence refs MAY include foreign artifacts, but do not imply approval

Participation across orgs does not create legitimacy unless LBA-bound.

## 8. Observability Requirements
mMRM MUST emit enough information for read-only assurance systems to verify:
- LBAs exist (or not) for a window
- which snapshot and lane schema were bound
- which approvers signed
- expiry bounds

mMRM MUST remain compatible with proof-carrying state update logging (PCSU), but PCSU is out of scope here.

## 9. Security & Abuse Considerations (brief)
This kernel is designed to prevent:
- action-by-default
- approval laundering via participation
- policy-fork equivalence narratives
- mirror fog via audit saturation
- mirror capture via “true but misleading” reporting

It does not prevent:
- malicious approvers signing bad LBAs (requires separation-of-duties governance outside mMRM)
- semantic misuse of action classes/use-case IDs (must be defined in lane schema/policy)

## 10. Versioning
- This spec is versioned.
- LBAs MUST include `spec_version` or be implicitly versioned by the referenced schema hash.
- Silent changes are prohibited; migration paths must be explicit.
