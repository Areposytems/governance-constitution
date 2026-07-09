# Governance Constitution v1.0.1

## Part I — Preamble

This Constitution defines a separation-of-powers governance framework for AI systems and their integrations. Its purpose is to enable interoperability, auditability, and risk containment **without centralization**, **without semantic authority**, and **without silent escalation**. Authority is deliberately fragmented so that no single component, operator, or vendor can silently create legitimacy.

This document is normative. Invariants stated herein **must always hold**.

---

### I-1. Constitutional Overview

This Constitution establishes a **separation-of-powers governance architecture** for complex AI and cybernetic systems. It is designed to survive adversarial pressure, federation, policy forks, audit saturation, and political capture **without centralization**.

The Constitution distinguishes between:
- **Legitimacy (constitutional authority)** — sparse, explicit, non-delegable
- **Operation (execution & mediation)** — non-semantic, non-authoritative
- **Observation (assurance)** — read-only, non-certifying

The system is constitutionally complete with the components defined in Part I. Additional governance functions may exist only as extensions defined in Part II.

---

### I-2. Separation of Powers (Ecosystem Invariants)

**ECO-1 — Separation of powers**  
No single component may simultaneously:
(a) decide access or execution,
(b) define or bind legitimacy,
(c) declare audit outcomes.

**ECO-2 — No shadow execution paths**  
Any path to action must be declared as an Action Lane and is subject to SPM-C mediation, mMRM legitimacy binding, and CAA observability.

**ECO-3 — Trajectory–Recovery Separation**  
Trajectory control (AAM) and recovery control (ARGL) must be implemented as distinct mechanisms. No component may both detect attractors and govern phase exit.

**ECO-4 — Proof-carrying change**  
Any state or schema change driven by inconsistent, delayed, or conflicting inputs must be proof-carrying and externally observable.

---

### I-3. Lane Model

All system behavior is classified into one of three explicit lanes:

- **Idea Lane** — exploration, hypothesis, alternatives
- **Evidence Lane** — validation artifacts, tests, measurements
- **Action Lane** — execution or externally consequential decisions

Lane definitions, transition criteria, and schemas are versioned artifacts referenced by immutable hashes.

No execution outside declared Action Lanes is legitimate.

---

### I-4. SPM-C — Selective Permission & Mediation (Conformance)

SPM-C governs **connections and interfaces only**. It applies declared rules without semantic interpretation or execution authority.

---

### I-5. AAM — Anti-Attractor Mechanism

AAM governs **trajectory awareness and repulsion**. It expands hypothesis space and detects unhealthy convergence without authority.

---

### I-6. ARGL — Ascent & Recovery Governance Layer

ARGL governs **recovery, hysteresis, and forward re-entry** after intervention. It prevents oscillation and paralysis.

---

### I-7. PCSU — Proof-Carrying State Updates

PCSU governs **how systems change state or schema honestly** when faced with inconsistent, delayed, missing, or conflicting inputs.

#### Role
PCSU enforces explicit, replayable, and auditable transitions. Silent accommodation or reinterpretation is prohibited.

#### Core Requirements
- Every state or schema transition must reference:
  - prior state hash
  - triggering event IDs
  - freshness/ordering metadata
  - reason code
  - proof bundle hash
- Schema changes must supersede, not overwrite, prior versions.
- Reconciliation sub-phases must be observable by assurance.

PCSU is non-semantic and non-authoritative.

---

### I-8. CAA — Continuous Artificial Assurance

CAA provides **read-only observability, capture detection, and external mirroring**. It does not certify, approve, or enforce.

---

### I-9. mMRM — Minimal Model Risk Management (Legitimacy Core)

#### Constitutional Role
mMRM is the **sole legitimacy-binding authority** in the system. It defines when Action is constitutionally authorized.

mMRM does not score risk, monitor continuously, interpret semantics, or execute actions.

Legitimacy here is constitutional/procedural authorization for Action Lane execution, not semantic correctness or legal validity.

#### Core Concept: Legitimacy-Critical Events (LCEs)
An LCE is any event whose occurrence authorizes or materially enables Action.

#### Legitimacy Binding Artifact (LBA)
All LCEs produce an immutable LBA containing:
- LBA ID (hash)
- use-case ID
- action class ID
- policy snapshot hash
- lane schema hash
- evidence references (IDs only)
- approver IDs (threshold)
- approval scope
- issuance time
- expiry time
- non-delegation flag
- optional supersession reference
- signatures

Absence of an applicable, unexpired LBA implies absence of legitimacy for that action.

---

### I-10. Governance Extensions (Optional)

Additional governance functions may exist **only as extensions** layered atop mMRM. These include, but are not limited to:
- Risk scoring frameworks
- Model lifecycle management
- Sector-specific compliance
- Safety evaluation regimes
- Vendor certification programs

Extensions may reference LBAs but must not redefine legitimacy.
Extensions may not introduce new legitimacy-binding authorities.

---

### I-11. Federation & Interoperability

- Cross-system recognition requires explicit LBAs.
- Participation does not imply approval.
- Proof-carrying federation is mandatory.

---
## Part II — Normative Component Specifications


---

### II-1. SPM-C — Selective Permission & Mediation (Conformance)

#### Role
SPM-C mediates **who may connect to whom, under what declared capabilities, schemas, rates, and identities**. It does not judge meaning, truth, safety, or intent.

#### Invariants

**SPM-C-1 — No semantic authority**  
SPM-C must not classify content as true/false, safe/unsafe, allowed/disallowed based on meaning. Enforcement is limited to protocol, identity, rate, schema, and capability declarations.

**SPM-C-2 — No action execution**  
SPM-C must not execute downstream actions. It may only allow, deny, throttle, or shape connections and message formats.

**SPM-C-3 — Explicit deny reasons**  
Every deny or throttle decision must emit a structured reason code and a policy rule identifier traceable to a published rule set.

**SPM-C-4 — Policy immutability by hash**  
All enforcement decisions must reference an immutable policy snapshot ID. Silent policy drift is prohibited.

**SPM-C-5 — No unilateral escalation**  
SPM-C must not upgrade hypotheses or signals into evidence or action status. It gates lanes only according to predeclared rules.

**SPM-C-6 — Separation of duties for policy changes**  
Policy updates require multi-party approval. No single operator may unilaterally change enforcement rules.

**SPM-C-7 — Tamper-evident decision logging**  
All allow/deny/throttle events must be recorded in an append-only, hash-chained log.

**SPM-C-8 — Kill-switch transparency**  
Any fail-open or fail-closed mode must be explicitly logged with identity, timestamp, reason code, and renewal bounds.

**SPM-C-9 — Replay and ordering protection**  
Mediated lanes must include replay and ordering protections. Detected anomalies must be logged.

**SPM-C-10 — Identity and key lifecycle logging**  
Credential issuance, rotation, and revocation events must be immutably logged and surfaced to assurance.

---

### II-2. AAM — Anti-Attractor Mechanism

> **Control-theoretic note:** AAM governs *trajectory deviation* (detecting and countering unhealthy dynamics). It does not govern recovery or re-entry into forward motion. That function is handled by ARGL (defined below).

#### Role
AAM resists convergence toward narrow, captured, or power-seeking equilibria by maintaining diversity in hypothesis generation. It is explicitly **non-authoritative**.

#### Invariants

**AAM-1 — Advisory-only output**  
Outputs must be labeled as hypotheses or alternatives, never conclusions.

**AAM-2 — No direct path to action**  
AAM outputs must not feed directly into execution. Evidence Lane validation is mandatory.

**AAM-3 — Provenance tagging**  
Each output must include generation method ID, diversity parameters, and exploration mode.

**AAM-4 — Diversity floor reporting**  
A diversity metric must be computed and logged per run. Diversity collapse must raise a non-suppressible alert.

**AAM-5 — No goal steering**  
AAM must not optimize toward a preferred narrative. Any objective beyond diversity expansion must be declared and auditable.

**AAM-6 — Bounded perturbation**  
Operation must remain within declared bounds. Breaches must fail safely and be logged.

**AAM-7 — Non-suppressible warnings**  
Signals such as novelty collapse or repeated convergence must always be emitted to assurance channels.

**AAM-8 — No covert personalization**  
Personalization that materially alters outputs must be logged with feature flags and inputs.

---

### II-3. ARGL — Ascent & Recovery Governance Layer

#### Role
ARGL governs **phase-exit, recovery, and forward re-entry** after intervention. It prevents oscillation, hesitation, and clarification loops once a destabilizing attractor has been countered.

ARGL is neither semantic nor generative. It is a **control-layer governor** that ensures reasoning progresses *after* damping or intervention.

#### Invariants

**ARGL-1 — No semantic judgment**  
ARGL must not judge truth, correctness, or safety of content. It operates only on state, phase, and control signals.

**ARGL-2 — One-way phase exit**  
Once a system exits a dampened or intervention phase, ARGL must prevent re-entry into the same phase without new external evidence or state change.

**ARGL-3 — Anti-oscillation guarantee**  
ARGL must enforce hysteresis such that repeated clarification or reassurance loops are bounded and non-recursive.

**ARGL-4 — Forward-motion constraint**  
After an intervention, ARGL must bias the system toward a declared forward lane (Idea, Evidence, or Action) rather than indefinite stabilization.

**ARGL-5 — No action authority**  
ARGL must not trigger execution. It only governs eligibility to re-enter forward lanes.

**ARGL-6 — Explicit phase signaling**  
All phase transitions (damped → recovery → forward) must be explicitly signaled and logged.

**ARGL-7 — Bounded recovery window**  
Recovery and stabilization phases must be time- or step-bounded. Silent stalling is prohibited.

**ARGL-8 — Non-overlap with AAM**  
ARGL must not perform attractor detection or diversity expansion. Its sole function is recovery governance.

---

### II-4. CAA — Continuous Artificial Assurance

#### Role
CAA provides continuous, read-only observation, capture detection, and audit evidence. It does not enforce policy or grant approval.

#### Invariants

**CAA-1 — Read-only posture**  
CAA must not modify production systems, policies, or gates.

**CAA-2 — Minimum non-redactable telemetry set**  
CAA must receive guaranteed telemetry, including policy snapshot hashes, allow/deny counts, override events, lane transitions, and drift metrics.

**CAA-3 — Tamper-evident audit log**  
All outputs must be written to an append-only, hash-chained log.

**CAA-4 — Alert integrity**  
Alerts are uniquely identified, stateful, and non-deletable. Closure requires justification.

**CAA-5 — Independent verification hooks**  
CAA must expose verifiable proofs of execution scope, policy snapshot, and time window.

**CAA-6 — Capture detection triggers**  
Explicit, versioned triggers must exist for suspicious patterns, including silence or asymmetric behavior.

**CAA-7 — Externalized escalation channel**  
At least one escalation path must exist outside the operator’s control domain.

**CAA-8 — No certification language**  
CAA must not emit “compliant,” “certified,” or “approved” statements.

**CAA-9 — Telemetry absence is an incident**  
Missing required telemetry beyond a threshold must raise a non-closable alert without external sign-off.

---

### II-5. mMRM — Minimal Model Risk Management (Legitimacy Core)

#### Role
mMRM is the legitimacy core of the governance architecture. It binds sparse, explicit, and time-bounded legitimacy for Action Lane execution through Legitimacy Binding Artifacts (LBAs).

mMRM does not execute actions, judge semantic correctness, certify systems, score risk, or monitor continuously. It determines only whether an applicable, unexpired, and properly authorized LBA exists for a claimed Action Lane execution.

#### Invariants

**mMRM-1 — Action requires an LBA**  
No Action Lane execution is legitimate without an unexpired LBA.

**mMRM-2 — Participation is not approval**  
Evidence, assistance, or federation does not constitute approval unless explicitly bound by an LBA.

**mMRM-3 — No implicit policy equivalence**  
Policy snapshots are not equivalent unless explicitly bound by an LBA.

**mMRM-4 — Legitimacy is sparse and enumerable**  
All LBAs active in a time window must be enumerable. Absence implies no legitimacy.

**mMRM-5 — Legitimacy expires**  
All LBAs must expire. Evergreen legitimacy is prohibited.

mMRM is non-delegable and non-centralizing by design.

---

### II-6. IAM — Interpretive Advisory Mechanisms

#### Role

The system may include non-binding interpretive advisory mechanisms that generate epistemic, ethical, or oversight signals to support system self-awareness and human understanding.

Interpretive Advisory Mechanisms operate in a parallel interpretive plane. They do not bind legitimacy, authorize action, mediate access, or override governance layers.

#### Invariants

**IAM-1 — Advisory-only status**  
IAM outputs are advisory only. They must not be treated as conclusions, approvals, certifications, or legitimacy-binding artifacts.

**IAM-2 — No legitimacy dependency**  
IAM outputs must never be required conditions for legitimacy, lane transitions, SPM-C mediation, or Action Lane execution.

**IAM-3 — Assurance observability**  
IAM outputs must be observable by assurance systems and auditable when used to support system self-awareness, oversight, or human understanding.

**IAM-4 — Separate specification boundary**  
A reference specification for Interpretive Advisory Mechanisms may be maintained separately, but it does not alter the constitutional authority model.

---

### II-7. Amendment Process

Amendments to this Constitution require:
- versioned change proposals,
- multi-party approval,
- public diff publication,
- and explicit migration paths.

This amendment process applies to all parts of this Constitution, including normative component specifications.

Silent amendment is prohibited.

---

### Status

This document constitutes **Governance Constitution v1.0.1**. It is intended as a living but tightly controlled foundation for refinement, formalization, and conformance testing.

