# Aligner OS — UK-Branded Dental Aligner Operating System

**Documentation baseline:** 8 November 2026  
**Project stage:** Research, product architecture and pre-development only  
**Priority:** Deferred commercial launch until OPOS secures its first paying customer  
**Repository:** `zeeshankhanminhas/aligners` — currently a starter repository, with no product code verified

## Business model decision

The intention is to sell custom dental aligners to UK dental clinics under the **Aligner OS brand**, with Aligner OS acting as the **legal device manufacturer** and a contracted Pakistan laboratory or facility performing physical manufacture. This is more than a marketplace or coordination portal.

The UK dental practice remains responsible for patient assessment, prescription, clinical treatment decisions, approval and fitting. Aligner OS's intended manufacturer role includes controlling device specifications, its contracted manufacturing process, conformity evidence, traceability, quality release, complaints and post-market obligations. Exact legal roles and regulatory classification must be validated by qualified specialists before any commercial supply.

The Pakistan-side commercial firm and the physical manufacturer may be different entities. Do not assume a Pakistan coordinator has the production facility's quality system or registration.

## Non-negotiable privacy and clinical boundaries

1. **No directly identifying patient details to the Pakistan lab.** Keep names, addresses, contact data, identity-to-case mappings, unneeded photos and patient-record details out of laboratory workspaces and exports.
2. **No assumption that dental geometry is anonymous.** An STL/3D dental model or other patient-specific geometry may remain personal health data even without a name. Confirm the UK GDPR status and international-transfer requirements for the exact exported dataset.
3. **UK-controlled identity environment.** Physically/logically separate the clinic identity vault from the manufacturing workspace with role-specific access, authenticated exports, metadata minimisation and audit trails. Validate actual hosting/backup regions and processor agreements before production.
4. **Synthetic-data-only development and QA.** No real patient records, scans, photographs or clinical histories until privacy, cybersecurity, clinical and regulatory gates have passed.
5. **Clinical planning and approvals remain governed.** No plan or order may be released for manufacturing without the required qualified clinician's approved prescription/plan and the legal manufacturer's acceptance controls.
6. **No production use before expert review.** A technical prototype, Neon database or demo does not establish UK GDPR or MHRA compliance.

## Proposed system architecture

- **Clinic workspace:** identity/patient mapping, authorised prescription, treatment planning reviews, consent/legal notices and clinical sign-offs.
- **Case governance:** pseudonymous case ID; versioned prescriptions, approved treatment models and manufacturing releases.
- **Controlled export gateway:** selected manufacturing inputs only, stripped of unnecessary metadata; access checks and transfer authorisation before export.
- **Pakistan manufacturing workspace:** case reference, approved stage geometry and necessary specifications, materials/batches, job progress, defects, remake requests and QC evidence.
- **Manufacturer QA / release:** Aligner OS authorisation, product identity, traceability, technical documentation, device labels, retention and recall records.
- **Clinic fulfilment:** track packs, receipt, clinician fitting, issues, corrections and safety feedback.
- **Audit and safety:** all relevant access, approvals, releases, complaints, corrective actions and vigilance events.

Manufacturing geometry access is **not** automatically anonymous or exempt from international-transfer safeguards.

## Technology decisions

- **Database foundation:** Neon PostgreSQL is the current planned starting architecture, with distinct development/QA and production environments. Do not assume any particular Neon project or location is already provisioned.
- **Auth, storage, secrets and hosting:** to be designed and independently reviewed for regulated health-data use, including private object storage, access controls, encryption, recovery, deletion, DPAs and cloud sub-processors. Neon does not by itself supply every required service.
- **Isolation:** No shared operational database with OPOS, Barnama or The Second Read.
- **Current repo evidence:** Starter `.gitkeep` only; this README states plans and decisions, not implemented capabilities.

## Regulatory gate — must pass before placing devices on the GB market

Specialist UK medical-device and data-protection review is required to confirm:

- Whether the intended aligner product meets the **custom-made device** definition; a scan-derived personalised product is not automatically custom-made.
- Who the legal manufacturer and importer/distributor are, including the contractual role of each Pakistan entity.
- Applicable MHRA registration, custom-made statement, technical file, labelling, applicable conformity obligations, documented risk controls, quality system, supplier audits and process/material validation.
- Complaints, traceability, post-market surveillance, incident/vigilance and corrective-action processes.
- Product liability insurance and supply/import arrangements.
- Clinic–Aligner OS–laboratory controller/processor/sub-processor roles; applicable Article 28 contracts, DPIA, data mapping and security.
- Where applicable, a valid UK international-transfer mechanism (such as the IDTA), a transfer-risk/data-protection assessment and effective technical/contractual measures.

This document is a planning baseline, **not a compliance certification or legal opinion**.

## Open business decision

**Treatment planning split:** Determine whether the Pakistan partner also prepares digital stages, or whether planning is performed/approved in the UK and only approved manufacturing-ready models are exported. Clinical responsibility, allowed data exposure, quality checks and costs depend on this decision. No architecture should silently assume it is resolved.

## Phased delivery

### Phase 0 — Concept / no live data

- Validate partner capabilities, desired product family and actual manufacturing chain.
- Complete synthetic case workflow, proposed legal/data roles and pre-sprint dependency register.
- Obtain fixed-fee quotations for medical-device and privacy reviews when commercial validation justifies expenditure.
- Prototype identity isolation and controlled manufacturing exports without live patients.

### Phase 1 — Regulated readiness

- Specialist classification and manufacturer-role review.
- Supplier qualification, technical documentation, validated manufacturing and QC process, transfer agreements, DPIA/security and applicable MHRA registration.
- Insurance, labelling, import and safety reporting arrangements.
- Clinician-supervised pilot only when legally and clinically approved.

### Phase 2 — Commercial launch

- UK clinic onboarding, controlled case intake, clinician approval, verified manufacture, QA release, shipping and aftercare.
- Budgeted support, audit and post-market monitoring.

No calendar-based transition between phases; each requires verified evidence and owner approval.

## November sprint rule

During **9–22 November 2026**, Aligner OS is limited to **planning and synthetic prototype work**, if time remains after OPOS, delivery work and family commitments. It is not a commercial launch milestone.

Before each new sprint use the [Pre-Sprint Handover](docs/SPRINT_HANDOVER_2026-11.md). At the **23 November** review, decide whether to defer further development until the OPOS first-customer condition is met.

## Working safety rules

- Keep credentials and any patient-sensitive information out of GitHub and chat.
- Use isolated branches, reviewed schema changes, synthetic fixtures and clearly labelled demonstrations.
- Never claim legal, clinical, security or manufacturer readiness from code existence alone.
- Do not activate real payment, accept real patient submissions or share live scans overseas without the applicable authorisations.
