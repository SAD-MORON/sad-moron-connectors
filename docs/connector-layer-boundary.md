# Connector Layer Boundary

## Purpose

This document defines the boundary of the connector layer in SAD Moron.

## Scope

The connector layer defines:
- source boundary interpretation
- connector compliance expectations
- source-specific contract planning
- connector documentation structure

## Out of Scope

The connector layer does not currently define:
- executable connectors
- runtime services
- APIs
- Apps Script
- credential flows
- scraping logic
- synchronization behavior

## Boundary Rules

### Rule 1: No execution

This repository does not execute.

### Rule 2: No governance redefinition

Connector-layer artifacts must inherit governance from `sad-moron-framework`.

### Rule 3: No unrestricted source access

Every connector must stay within declared source boundary and institutional purpose.

### Rule 4: No production posture

Connector definitions remain pre-implementation until a later governed repository introduces bounded execution.

## Summary

The connector layer is a planning and contract layer, not an implementation layer.
