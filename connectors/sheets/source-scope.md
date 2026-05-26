# Google Sheets Source Scope

## Purpose

This document defines what qualifies as a governed Google Sheets source for SAD Moron connector planning.

## Governed Source Definition

A governed Google Sheets source is a spreadsheet or bounded spreadsheet workspace that:
- has an identifiable institutional origin
- serves a declared institutional use
- contains records relevant to SAD Moron operational or administrative review
- can be described within a declared source boundary

## Allowed Institutional Use

Allowed use includes bounded institutional contexts such as:
- operational tracking of administrative processes
- support records for vacancy-related publication workflows
- working coordination artifacts tied to declared SAD processes
- spreadsheet-based registries used to support administrative review

## Excluded Use

Excluded use includes:
- personal or informal spreadsheets without institutional standing
- unrestricted spreadsheet discovery
- opportunistic collection of unrelated operational data
- broad monitoring of all accessible Sheets content
- use of Sheets as an undefined general data lake

## Declared-Source Requirement

No Google Sheets connector should be treated as governed unless the target sheet or sheet family is tied to a declared source model under the SAD Moron governance framework.

At minimum, the declared source should make clear:
- institutional origin
- document or record class
- intended governance use
- temporal relevance
- known limitations
- source boundary note

## Boundary Rules

### Rule 1: Institutional intelligibility

The connector source must be institutionally intelligible, not merely technically reachable.

### Rule 2: Process-bound use

The source must be linked to a defined institutional process or administrative use case.

### Rule 3: No unrestricted ingestion

The connector must not treat all accessible spreadsheet content as in scope.

### Rule 4: Bounded worksheet interpretation

If a spreadsheet contains multiple tabs or mixed-purpose content, the governed scope must specify which parts are relevant and why.

## Summary

Google Sheets sources are governed only when they are institutionally declared, process-bounded, and restricted against unrestricted ingestion.
