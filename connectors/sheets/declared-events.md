# Google Sheets Declared Events

## Purpose

This document defines scaffold-level expected event families for Google Sheets sources in SAD Moron.

## Status

These remain scaffold-level event definitions, not production logic.

They exist to support connector planning and governance interpretation before any implementation exists.

## Event Families

### 1. Vacancy Publication

This event family covers spreadsheet records that indicate publication or listing of vacancies within a bounded institutional process.

Possible governance use:
- identifying whether a vacancy publication record appears in the declared sheet scope
- supporting bounded omission review over expected publication windows

### 2. Administrative Updates

This event family covers spreadsheet entries that reflect operational or administrative updates relevant to SAD Moron workflows.

Possible governance use:
- tracking that an expected administrative update was recorded
- distinguishing planned state from updated state within a bounded period

### 3. POFA Updates

This event family covers spreadsheet records related to POFA / POF-linked updates, supporting review of staffing or structural changes reflected in operational sheets.

Possible governance use:
- verifying that a POFA-related update was reflected in the bounded source
- cross-checking declared process expectations

### 4. Assignment Changes

This event family covers spreadsheet records that indicate changes in assignment state, allocation, or related operational handling.

Possible governance use:
- identifying whether an expected assignment change was recorded
- supporting reconstruction of sequence over a bounded period

### 5. Status Changes

This event family covers spreadsheet entries representing changes in workflow or record status.

Possible governance use:
- checking whether a status transition became visible in the declared source
- supporting review of progression or non-progression over time

### 6. Manual Correction Records

This event family covers spreadsheet updates that reflect human correction, amendment, or cleanup of prior entries.

Possible governance use:
- preserving awareness that operational spreadsheets may contain manual correction activity
- supporting interpretation of later ambiguity during audit reconstruction

## Event Boundary Rules

### Rule 1: Administrative meaning first

These event families describe institutional event expectations, not implementation triggers.

### Rule 2: Sheet visibility is not full truth

The appearance or absence of a sheet event does not automatically establish institutional truth without declared scope and further governance interpretation.

### Rule 3: Connector non-finality

The connector layer may define event families for planning, but it may not convert them into final governance verdicts by itself.

## Summary

These Sheets event families provide a bounded scaffold for future connector interpretation without creating production logic.
