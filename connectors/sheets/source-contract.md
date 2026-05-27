# Google Sheets Source Contract

## Purpose

This document defines the source contract requirements that must be satisfied before a Google Sheets source can support bounded implementation planning.

## Status

This document is governance-specification only.

It does not define API clients, Apps Script behavior, extraction mechanics, or runtime execution.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Required Source Elements

A governed Google Sheets source contract must define:
1. source name
2. institutional origin
3. spreadsheet or sheet-family boundary
4. document or record class
5. intended governance use
6. temporal relevance
7. known limitations
8. boundary note

## Source Constraints

### Rule 1: Institutional intelligibility

The source must be institutionally intelligible, not merely technically reachable through spreadsheet access.

### Rule 2: Bounded worksheet scope

The contract must state which tabs, ranges, or worksheet segments are in scope when mixed-purpose sheets exist.

### Rule 3: Mutable-source caution

The contract must acknowledge that Sheets are mutable working records and may not preserve full historical state by default.

### Rule 4: Allowed and excluded fields

Allowed and excluded fields, structures, or conventions must be declared before implementation handoff is contemplated.

### Rule 5: Audit reconstruction compatibility

The source contract must not block later audit reconstruction through ambiguity about source identity, scope, cadence, or bounded period.

## Summary

Google Sheets sources can support connector planning only when their institutional boundary, intended use, and mutable-source limitations are explicitly declared.
