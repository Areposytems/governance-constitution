# Governance Constitution

A **constitutional governance framework** for complex AI and cybernetic systems.

This repository defines a separation‑of‑powers architecture that makes **legitimacy explicit, sparse, and auditable**—without centralization, semantic authority, or vendor lock‑in.

The design is intentionally **normative and minimal**. It specifies *what must be true* for action to be legitimate, not *how* to build any particular system.

License: See LICENSE.md

---

## What this is

- A **constitution**, not a product
- A **kernel of legitimacy**, not a risk bureaucracy
- **Implementation‑neutral** (no runtime, no SDK required)
- Designed to survive federation, policy forks, audit saturation, and political pressure

If an action is claimed to be legitimate, this framework provides one simple test:

> **Show the artifact that authorizes it.**

If no such artifact exists, legitimacy does not.

---

## Repository structure

```
.
├─ CONSTITUTION.md        # Governance Constitution v1.0 (normative)
├─ mMRM_SPEC.md           # Legitimacy Kernel Specification (normative)
├─ schemas/               # Machine‑checkable artifact definitions
│   ├─ lba.schema.json    # Legitimacy Binding Artifact (LBA)
│   └─ pcsu_transition.schema.json
└─ CHANGELOG.md
```

---

## Core ideas (high level)

- **Separation of powers**: access control, legitimacy, recovery, and audit are never fused
- **Non‑semantic governance**: no component judges truth, safety, or meaning
- **Sparse legitimacy**: only a small number of explicit events can authorize action
- **Proof‑carrying change**: state and schema changes must be replayable and auditable
- **Federation without trust**: participation does not imply approval

---

## What makes this different

Most governance systems rely on:
- continuous monitoring
- risk scoring
- centralized approval
- or interpretive audits

This framework relies instead on:
- **explicit authorization artifacts**
- **time‑bounded legitimacy**
- **enumerability rather than interpretation**

It is designed so that:
- transparency cannot be weaponized by volume
- audits cannot be captured by narrative
- urgency cannot substitute for authority

---

## How to use this repository

You can adopt this framework at different levels:

- **As a standard**: align internal governance to the Constitution
- **As a kernel**: implement the legitimacy artifacts defined in `mMRM_SPEC.md`
- **As a reference**: evaluate whether an existing system can *prove* legitimacy

No code is required to begin. The JSON Schemas allow structural validation when you choose to implement.

---

## What this repository does not do

- It does not provide executable code
- It does not certify systems or vendors
- It does not define risk scores or safety judgments
- It does not prevent misuse by malicious approvers

Those concerns are intentionally left to **extensions**, not the constitutional core.

---

## Status

- Governance Constitution: **v1.0**
- Legitimacy Kernel (mMRM): **v1.0**

The framework is stable at the constitutional level. Extensions may evolve independently.

---

## License & contributions

This repository is intended for open discussion, critique, and implementation.

Contributions should:
- respect the separation of powers
- avoid adding semantic authority to the kernel
- prefer minimalism over completeness

Discussion and critical review are encouraged.

