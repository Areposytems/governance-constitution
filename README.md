# Governance Constitution

A **constitutional governance framework** for complex AI and cybernetic systems.

This repository defines a separation-of-powers architecture that makes **legitimacy explicit, sparse, and auditable**—without centralization, semantic authority, or vendor lock-in.

The design is intentionally **normative and minimal**. It specifies *what must be true* for action to be legitimate, not *how* to build any particular system.

License: See LICENSE.md

---

## What this is

* A **constitution**, not a product
* A **kernel of legitimacy**, not a risk bureaucracy
* **Implementation-neutral** (no runtime, no SDK required)
* Designed to survive federation, policy forks, audit saturation, and political pressure

If an action is claimed to be legitimate, this framework provides one simple test:

> **Show the artifact that authorizes it.**

If no such artifact exists, legitimacy does not.

---

## Repository structure

```text
.
├─ CONSTITUTION.md        # Governance Constitution v1.0 (normative)
├─ mMRM_SPEC.md           # Legitimacy Kernel Specification (normative)
├─ schemas/               # Machine-checkable artifact definitions
│  ├─ lba.schema.json     # Legitimacy Binding Artifact (LBA)
│  └─ pcsu_transition.schema.json
├─ domain_profiles/       # Optional non-normative domain translation profiles
│  ├─ legal/
│  ├─ medical/
│  ├─ economic/
│  └─ academic/
├─ adoption_guides/       # Non-normative implementation guidance
├─ examples/              # Illustrative artifacts and workflow examples
└─ CHANGELOG.md
```

---

## Core ideas (high level)

* **Separation of powers**: access control, legitimacy, recovery, and audit are never fused
* **Non-semantic governance**: no component judges truth, safety, or meaning
* **Sparse legitimacy**: only a small number of explicit events can authorize action
* **Proof-carrying change**: state and schema changes must be replayable and auditable
* **Federation without trust**: participation does not imply approval

---

## Domain profiles

Domain profiles translate the constitutional core into sector-specific language.

Current profile areas:

* **Legal**: courts, tribunals, legal practice, public law, legal-policy bodies, and legal AI workflows.
* **Medical**: clinical, hospital, patient safety, health administration, and care-related AI workflows.
* **Economic**: finance, public administration, procurement, credit, insurance, consumer protection, and model-risk workflows.
* **Academic**: education, research integrity, citation, assessment, authorship, and institutional knowledge systems.

Domain profiles do **not** amend the constitutional core.

They do **not** create legal, medical, financial, academic, or regulatory compliance by themselves.

They are translation layers that map domain-specific duties into the Constitution's shared governance architecture.

---

## What makes this different

Most governance systems rely on:

* continuous monitoring
* risk scoring
* centralized approval
* or interpretive audits

This framework relies instead on:

* **explicit authorization artifacts**
* **time-bounded legitimacy**
* **enumerability rather than interpretation**

It is designed so that:

* transparency cannot be weaponized by volume
* audits cannot be captured by narrative
* urgency cannot substitute for authority

---

## How to use this repository

You can adopt this framework at different levels:

* **As a standard**: align internal governance to the Constitution
* **As a kernel**: implement the legitimacy artifacts defined in `mMRM_SPEC.md`
* **As a reference**: evaluate whether an existing system can *prove* legitimacy
* **As a domain profile**: translate the Constitution into a sector-specific adoption pattern
* **As an adoption guide**: explore how an institution could begin applying the framework

No code is required to begin. The JSON Schemas allow structural validation when you choose to implement.

---

## What this repository does not do

* It does not provide executable code
* It does not certify systems or vendors
* It does not define risk scores or safety judgments
* It does not prevent misuse by malicious approvers
* It does not create compliance with domain-specific law or professional duties

Those concerns are intentionally left to **extensions**, domain profiles, and institutional adoption processes—not the constitutional core.

---

## Status

* Governance Constitution: **v1.0**
* Legitimacy Kernel (mMRM): **v1.0**
* Legal Domain Profile: **draft v0.1** (jurisdiction-neutral)
* Medical Domain Profile: **placeholder draft v0.1**
* Economic Domain Profile: **placeholder draft v0.1**
* Academic Domain Profile: **placeholder draft v0.1**

The framework is stable at the constitutional level. Extensions may evolve independently.

---

## Attribution

The Governance Constitution is maintained by Arepo Systems.

Institutions, researchers, developers, policymakers, and public bodies may study, critique, adapt, or build on this framework subject to the license terms. Public use, adaptation, or derivative work should preserve clear attribution and should not imply endorsement, certification, or approval by the maintainers unless expressly agreed in writing.

---

## License & contributions

This repository is intended for open discussion, critique, and implementation.

Contributions should:

* respect the separation of powers
* avoid adding semantic authority to the kernel
* prefer minimalism over completeness
* keep domain profiles clearly separated from the constitutional core

Discussion and critical review are encouraged.
