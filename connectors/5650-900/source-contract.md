# Source Contract for 5650 / 900

## Purpose

This document defines the source contract requirements that must be satisfied before spreadsheet-governed SAD administrative workflows associated with `5650` / `900` can support connector implementation planning.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Contract Requirements

The source contract must explicitly define:
1. included resolutions or process families
2. declared Google Sheets source identification
3. institutional purpose
4. temporal reconstruction window
5. required fields by process
6. excluded fields
7. audit/evidence expectations
8. known data limitations
9. reusable workflow boundary for later Apps Script implementation

## Interpretation Rules

### Rule 1: Spreadsheet workflow classification

`5650` / `900` must be treated as a spreadsheet-governed SAD workflow specification, not as a COBOL source connector and not as a direct legacy or provincial system connector.

### Rule 2: Institutional meaning first

The source contract must establish institutional purpose, included administrative processes, and declared Sheets boundaries before any future technical mapping.

### Rule 3: Field boundary required

Required and excluded fields must be declared by process before implementation is contemplated.

### Rule 4: Audit expectation required

The source contract must state how later audit and evidence interpretation can remain possible.

### Rule 5: Implementation separation required

Any later runtime execution belongs in `sad-moron-appscript`, not in this repository.

## Implementation Block

This connector cannot move to implementation until the relevant spreadsheet workflows and their declared Google Sheets sources are formally described in the declared sources catalog.

## Summary

The source contract for `5650` / `900` remains incomplete by design until the bounded spreadsheet workflows, declared Sheets surfaces, and process-specific fields are institutionally confirmed.
