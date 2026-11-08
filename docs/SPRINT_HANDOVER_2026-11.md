# Aligner OS — Pre-Sprint Dependency & Regulatory Handover

**Baseline:** 8 November 2026  
**Commercial status:** Deferred until OPOS first paying customer and the separate regulatory readiness gates  
**Permitted present scope:** Architecture, supplier diligence and entirely synthetic prototypes.

## Dependency register

| Dependency | Status | Next action / decision |
| --- | --- | --- |
| GitHub | **Ready** | Starter `zeeshankhanminhas/aligners` repo; no application implementation verified |
| Manufacturer structure | **Intent recorded; legal review pending** | UK Aligner OS brand will be legal manufacturer; identify actual Pakistan facility versus coordinator |
| Planning vs fabrication | **Open decision** | Determine where treatment stages are designed and clinician-approved before manufacturing |
| UK clinical oversight | **Design gate** | Establish qualified clinician prescription, approval and fitting responsibilities |
| Medical-device classification | **Not verified** | Specialist confirms custom-made eligibility, UK device rules, device statements and required records |
| Regulatory registration / obligations | **Not completed** | Determine MHRA registration, labelling, technical file, QMS, post-market, vigilance and traceability |
| Manufacturing supplier qualification | **Not verified** | Supplier audit, process validation, material controls, QC, change notification and remake procedures |
| Data roles & UK GDPR | **Pending** | Controller/processor mapping, Article 28 contracts, DPIA, rights/retention and privacy notices |
| Pakistan transfer controls | **Pending** | Assess geometry identifiability, IDTA or other valid safeguard and required transfer/data protection test |
| UK identity-vault design | **Design only** | Patient identity and mapping never available to Pakistan lab; validate actual cloud locations and permissions |
| Neon and clinical services | **Not provisioned/verified** | Separate development database; future regulated deployment needs auth, storage, backup, logs and security review |
| Synthetic fixtures | **Needed** | Invented patient records and synthetic geometries; never use real patient scans in QA |
| Liability and importing | **Pending specialist review** | Verify insurer, manufacturer/importer contract, shipping and claims procedure |
| Budget approval | **Not granted** | Collect fixed-fee legal/regulatory quotes only at commercial readiness gate |

## Minimum technical safety controls to design

1. Isolate UK patient identity and clinic cases from lab-visible manufacturing case references.
2. Produce a **versioned, clinician-approved, minimum-necessary** manufacturing export.
3. Strip identifying fields and unneeded metadata; log exporter, recipient, legal basis and approval.
4. Use role-scoped permissions, private object storage, encryption, retention/deletion controls, audit logs and incident workflows.
5. Enforce manufacturing stage tracking, lot/material traceability, QA inspection, authorised release and rework control.
6. Never equate a name-free STL/3D file with anonymous data as a matter of policy.
7. Build and test only with fictional/synthetic information until appropriate expert reviews and authorisations are complete.

## Owner handover

- Confirm intended legal entities and which physical factory manufactures the aligners.
- Confirm who creates treatment stages and who approves the plan.
- Provide supplier capability documents through an approved secure channel when available.
- Set a budget ceiling before obtaining specialist quotes or subscribing to services.
- Review privacy, manufacturer, import and clinical approval gates before any real clinic pilot.
- Keep project deployment, secrets and storage isolated from other ventures.

## November milestone

Only an architecture/due-diligence brief and synthetic workflow may be proposed. The **23 November 2026** milestone gate should consider **Defer / Continue research / Approve synthetic prototype**; it must **not** declare the clinical business launched.

## No-go rules

No actual patient data, overseas transfer, real production order, clinical advice, device manufacture for patients or public device sales based solely on software completion. Obtain documented specialist regulatory/privacy clearance and validated quality arrangements first.
