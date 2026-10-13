# Web Application Bug Reproduction & Triage Reports

A workbench for reproducing reported defects in a staging web application and handing engineering actionable, evidence-backed triage reports.

This repository is a reporting scaffold. It contains no verified defect reports yet. Create one report per defect from `triage-reports/REPORT-TEMPLATE.md`, and attach sanitized evidence as described in `evidence/README.md`.

## Standalone report builder

Open or download [`index.html`](https://raw.githubusercontent.com/JohnPiansay/skillgrid-web-bug-triage/main/index.html) to use the single-file workbench. It runs in a browser without a server or external dependencies, and generates a Markdown report for download. Form entries are not uploaded. The workbench documents findings; it does not test a staging application. Review each report for accuracy and redact sensitive evidence before sharing.

## Per-defect deliverables

Each report should include:

- Minimal, numbered reproduction steps.
- Expected and actual behavior.
- Reproduction status and the environment used, including when a defect could not be reproduced.
- Affected area and user impact.
- Links to console/network evidence or screenshots captured during reproduction.
- A concise engineering handoff with relevant context.

## Workbench layout

- `index.html` — standalone browser-based report builder that exports a Markdown report.
- `triage-reports/` — one Markdown report per defect, plus the report template.
- `evidence/` — sanitized screenshots and exported console/network evidence.
- `DELIVERY-NOTES-TEMPLATE.md` — summary for a delivery or release handoff.
- `ACCEPTANCE-CHECKLIST.md` — verification checklist for this scope.
- `SUBMISSION-REVIEW.md` — evidence-based answers and verification status for submission.
- `HANDOVER-AND-RELEASE-NOTES.md` — architecture, dependencies, verification record, and handover procedure.

## Getting started

1. Record the staging URL, build/version, browser and operating system in each report. Do not include credentials, session cookies, personal data, or unredacted tokens in committed evidence.
2. Reproduce one reported defect at a time. Record the exact steps and observed result; do not invent expected behavior when the product requirement is unclear.
3. Save supporting evidence under `evidence/` with a defect-specific name, then link it from that defect's report.
4. Mark reports that could not be reproduced with the status `Not reproduced` and explain what was tried and what environment was used.
5. Complete the checklist only when there is evidence for each checked item.

## Scope boundary

This workbench organizes reproduction and triage. It does not itself fix application defects or establish that the staging application meets a quality or accessibility standard. Findings must be based on observed behavior in the specified staging environment.
