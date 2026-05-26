# Google Sheets Known Limitations

## Purpose

This document records the known governance-relevant limitations of Google Sheets sources in the SAD Moron connector layer.

## Limitations

### Human Editing Inconsistency

Spreadsheet content may be edited by different actors with different levels of consistency, producing variation in naming, update timing, and operational meaning.

### Schema Drift

Columns, tabs, headings, and structural assumptions may change over time without formal governance notice.

### Manual Entry Variability

Manual entry practices may introduce inconsistent abbreviations, missing values, mixed formatting, or uneven record granularity.

### Historical Incompleteness

Past sheet state may be difficult or impossible to reconstruct fully if earlier versions were overwritten, deleted, or not retained in a declared review context.

### Duplicated Records

Sheets may contain repeated, partially repeated, or manually copied rows that complicate interpretation and bounded reconstruction.

### Formatting Ambiguity

Color, layout, merged cells, comments, tab names, and informal visual conventions may carry operational meaning that is not stable enough to treat as fully governed structure by default.

## Interpretation Rule

These limitations must be treated as governance-relevant constraints on future connector interpretation, not as minor implementation noise.

## Summary

Google Sheets sources are operationally useful but structurally ambiguous, so future connector work must remain cautious, bounded, and audit-aware.
