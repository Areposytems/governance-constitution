# Changelog

This changelog records substantive public changes to the Governance Constitution repository.

The constitutional core and mMRM legitimacy kernel remain versioned separately from optional domain profiles. Domain profiles are non-normative with respect to the constitutional core. Institutions may make them locally binding through their own lawful or institutional authority, but such adoption does not amend, expand, or create authority within the Governance Constitution itself.

---

## Governance Constitution License v1.1 — 2026-08-16

### Changed

- Clarified the boundary between non-production experimentation and operational use.
- Clarified restricted use across commercial, regulated, production, procurement-facing, and institutionally operational contexts.
- Clarified indirect institutional use through contractors, vendors, affiliates, and hosted services.
- Clarified the intellectual-property scope of the license.
- Added explicit non-exclusivity and anti-enclosure provisions.
- Added license-versioning rules to prevent silent retroactive license changes.

### Notes

- GCL-1.1 preserves free access for study, research, education, critique, and non-production experimentation.
- Operational, regulated, production, procurement-facing, or institutionally operational adoption remains subject to separate written licensing.
- Licensing does not transfer ownership, exclusive stewardship, certification authority, or exclusive control over the Governance Constitution.

---

## Constitutional Authority and Action-Boundary Clarification — 2026-08-16

### Added

- Added an explicit Action Lane boundary to the Agentic Software Systems Domain Profile.
- Defined agentic transition into the Action Lane through governed-state modification, protected or consequential capability invocation, changes to repositories or operational environments, and consequential institutional reliance.
- Added a distinction between exceptional high-authority automation and illegitimate authority bypass in the Agentic Software Systems Domain Profile.
- Added `.github/workflows/schema-validation.yml` to automatically validate illustrative Legal and Agentic Software LBA artifacts against the LBA JSON Schema on repository pushes and pull requests.

### Changed

- Clarified the constitutional completeness statement so that completeness applies specifically to the defined scope of constitutional legitimacy for Action Lane execution.
- Clarified mMRM as the sole constitutional legitimacy-binding mechanism rather than an originating source of institutional authority.
- Clarified that authority represented through an LBA must derive from the applicable human, institutional, legal, or governance structure external to mMRM.
- Clarified that mMRM binds and exposes authority but does not create the underlying authority it records, and that an implementation does not become authoritative merely because it validates or stores LBAs.
- Clarified the Agentic Software Systems Domain Profile so that isolated drafting, simulation, analysis, code suggestion, and proposal may remain within the Idea or Evidence Lane until a declared Action Lane boundary is crossed.
- Clarified that consequential agentic action requires applicable authorization, while capability, successful execution, urgency, participation, or self-authorization cannot create missing authority.
- Clarified the status of the Legal and Agentic Software Systems Domain Profiles: institutions may make profiles locally binding through their own lawful or institutional authority, but local adoption does not amend, expand, or create authority within the Governance Constitution.
- Changed the README adoption description from "As a standard" to "As a governance baseline" to avoid implying external standards-body recognition.
- Updated the README repository structure to include the schema-validation workflow.

### Validation

- The new GitHub Actions schema-validation workflow successfully validates the current Legal and Agentic Software LBA examples against `schemas/lba.schema.json`.
- Automated schema validation establishes structural conformity only. It does not establish constitutional legitimacy, authorization validity, institutional approval, safety, correctness, lawfulness, compliance, or certification.

### Notes

- No new governance component or independent source of constitutional authority was introduced.
- No LBA or PCSU schema fields were changed.
- No component gained additional execution, semantic, certification, monitoring, or legitimacy-originating authority.
- These changes narrow and clarify existing authority boundaries, Action Lane transitions, institutional adoption semantics, and authority provenance.
- Governance Constitution remains v1.0.1.
- mMRM Legitimacy Kernel remains v1.0.
- Legal Domain Profile remains draft v0.1.
- Agentic Software Systems Domain Profile remains draft v0.1.

---

## Repository Documentation and Alignment Update — 2026-07-25

### Added

- Added `schemas/README.md` to distinguish structural schema validation from constitutional legitimacy, authorization, signature validation, scope validation, and institutional approval.

### Changed

- Updated domain-profile compatibility references to Governance Constitution v1.0.1.
- Updated adoption-guide and example indexes for the Agentic Software Systems materials.
- Added explicit Domain Profile Contract alignment to the Agentic Software Systems Domain Profile.
- Clarified the relationship between profiles, supporting materials, adoption guides, and illustrative examples.

### Notes

- No constitutional requirements, component authorities, schema fields, validation rules, or governance semantics were changed.
- The updates are documentation and alignment changes only.

---

## Agentic Software Systems Domain Profile v0.1 — 2026-07-21

### Added

- Added the environment-neutral Agentic Software Systems Domain Profile.
- Added software-environment adaptation guidance.
- Added GitHub-style workflow guidance, governance mapping, risk-benefit matrix, adoption checklist, and illustrative agentic PR LBA.

### Notes

- No constitutional requirements, component authorities, schemas, or governance semantics were changed.
- The profile remains a non-normative translation layer.
- Detailed changes are recorded in `CHANGELOG_DOMAIN_PROFILES_v0.1.md`.
  
---

## Domain Profile Contract — 2026-07-14

### Added

- Added `DOMAIN_PROFILE_CONTRACT.md` to define the translation contract for domain profiles.
- Clarified how future profiles should preserve the constitutional core while translating domain-specific duties, roles, workflows, and adoption considerations.

### Notes

- No constitutional requirements, component authorities, invariants, schemas, or governance semantics were changed.
- Domain profiles remain non-normative translation layers unless separately adopted by an institution.

---

## Metadata and Formatting Update — 2026-07-09

### Changed

- Updated JSON Schema `$id` values from GitHub page URLs to raw repository-hosted schema URLs.
- Updated `CONSTITUTION.md` to `Governance Constitution v1.0.1`.
- Normalized Markdown heading hierarchy for the document title, Part I, Part II, numbered sections, and internal subsections.

### Notes

- No constitutional requirements, component authorities, invariants, schema fields, validation rules, or governance semantics were changed.

---

## Domain Profiles v0.1 — 2026-07-08

### Added

- Added the first domain-profile changelog: `CHANGELOG_DOMAIN_PROFILES_v0.1.md`.
- Added the Legal Domain Profile v0.1 as a jurisdiction-neutral legal translation profile.
- Added `domain_profiles/legal/jurisdictional_adaptation_note.md` for local legal-system translation.
- Added or updated supporting legal-domain materials, including the legal governance mapping, risk-benefit matrix, adoption checklist, court/tribunal adoption guide, and illustrative legal LBA example.

### Changed

- Revised the legal profile from common-law leaning terminology into broader jurisdiction-neutral language.
- Expanded legal-domain translation terms to cover adjudicative, administrative, regulatory, institutional, and rights-affecting contexts.
- Replaced narrower terms such as solicitor and affidavit with broader functional equivalents.
- Added due process, natural justice, attorney-client privilege, professional secrecy, administrative review, and equivalent local-law concepts.
- Added expiry, review, withdrawal, and renewal concepts to operational governance questions.

### Notes

- No amendment was made to the constitutional core.
- No amendment was made to the mMRM Legitimacy Kernel Specification.
- Domain profiles do not create legal, medical, financial, academic, or regulatory compliance by themselves.
- For detailed domain-profile changes, see `CHANGELOG_DOMAIN_PROFILES_v0.1.md`.
