# Web Application Bug Reproduction & Triage Reports

A workbench for reproducing reported defects in a staging web application and handing engineering actionable, evidence-backed triage reports.

This repository is a reporting scaffold. It contains no verified defect reports yet. Create one report per defect from `triage-reports/REPORT-TEMPLATE.md`, and attach sanitized evidence as described in `evidence/README.md`.

## Per-defect deliverables

Each report should include:

- Minimal, numbered reproduction steps.
- Expected and actual behavior.
- Reproduction status and the environment used, including when a defect could not be reproduced.
- Affected area and user impact.
- Links to console/network evidence or screenshots captured during reproduction.
- A concise engineering handoff with relevant context.

## Workbench layout

- `triage-reports/` — one Markdown report per defect, plus the report template.
- `evidence/` — sanitized screenshots and exported console/network evidence.
- `DELIVERY-NOTES-TEMPLATE.md` — summary for a delivery or release handoff.
- `ACCEPTANCE-CHECKLIST.md` — verification checklist for this scope.

## Getting started

1. Record the staging URL, build/version, browser and operating system in each report. Do not include credentials, session cookies, personal data, or unredacted tokens in committed evidence.
2. Reproduce one reported defect at a time. Record the exact steps and observed result; do not invent expected behavior when the product requirement is unclear.
3. Save supporting evidence under `evidence/` with a defect-specific name, then link it from that defect's report.
4. Mark reports that could not be reproduced with the status `Not reproduced` and explain what was tried and what environment was used.
5. Complete the checklist only when there is evidence for each checked item.

## Scope boundary

This workbench organizes reproduction and triage. It does not itself fix application defects or establish that the staging application meets a quality or accessibility standard. Findings must be based on observed behavior in the specified staging environment.
