# Known Limitations for 5650 / 900

## Purpose

This document records the known limitations of the `5650` / `900` spreadsheet workflow connector boundary at the current scaffold stage.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Current Limitations

### 1. Unconfirmed workflow coverage

The included SAD processes, such as Res. 5650, MAD, and any related workflows, are not yet formally bounded in the declared sources catalog.

### 2. Unconfirmed declared Google Sheets sources

The exact Google Sheets, tabs, ranges, or spreadsheet families that act as declared sources have not yet been formally specified.

### 3. Unknown process-specific field scope

Required and excluded fields cannot yet be stated definitively for each governed workflow.

### 4. Unknown Apps Script reuse boundary

The currently existing Apps Script functions, if any, and their reusable boundary across spreadsheet workflows remain undefined at the connector layer.

### 5. Unknown reconstruction behavior

Temporal reconstruction expectations remain undefined until workflow coverage and declared Google Sheets access are confirmed.

### 6. Unknown evidence surface

Audit and evidence expectations cannot yet be mapped to a sufficiently concrete spreadsheet record model.

### 7. Potential data ambiguity

Until workflow and source confirmation occur, duplication risk, schema drift, incomplete history, formatting ambiguity, and field ambiguity must all be treated as open limitations.

## Required Resolution Areas

Any future implementation path requires:
1. included resolutions or process families
2. declared Google Sheets source confirmation
3. institutional purpose
4. temporal reconstruction window
5. required fields by process
6. excluded fields
7. audit/evidence expectations
8. known data limitations
9. Apps Script reuse boundary

## Summary

The primary limitation of `5650` / `900` is that it remains an incompletely declared spreadsheet workflow specification, not yet a fully bounded Google Sheets administrative process surface.
