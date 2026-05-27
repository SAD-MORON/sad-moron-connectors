# Compliance Rules for 5650 / 900

## Purpose

This document defines the compliance rules any future connector for spreadsheet-governed SAD administrative workflows associated with `5650` / `900` must inherit.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Compliance Requirements

Any future implementation path requires:
1. included resolutions or process families
2. declared Google Sheets source confirmation
3. institutional purpose
4. temporal reconstruction window
5. required fields by process
6. excluded fields
7. audit/evidence expectations
8. known data limitations
9. bounded Apps Script implementation handoff

## Rules

### Rule 1: No credential persistence

No credentials may be stored in repository content or connector documentation.

### Rule 2: No silent data mutation

A future connector must not present itself as governed while silently mutating source data.

### Rule 3: Append-only audit orientation

Connector behavior must remain explainable in later append-only evidence and audit interpretation.

### Rule 4: Governance inheritance

Any future connector must inherit governance from `sad-moron-framework` and cannot bypass framework change control.

### Rule 5: No governance override by connector logic

Connector logic must not override declared source meaning, evidence classification, temporal boundaries, or institutional decision authority.

### Rule 6: No misclassification by implementation pressure

This connector must not be reclassified as COBOL, legacy-system, or provincial-system integration merely because spreadsheet workflows may later exchange data with other systems.

### Rule 7: Implementation separation

Any later Google Sheets or Apps Script runtime implementation belongs in `sad-moron-appscript`, not in this repository.

## Implementation Block

This connector cannot move to implementation until the relevant spreadsheet workflows and their declared Google Sheets sources are formally described in the declared sources catalog.

## Summary

Compliance for `5650` / `900` is governance-first and blocks implementation until the spreadsheet workflows, declared Sheets surfaces, and implementation handoff boundary are institutionally defined.
