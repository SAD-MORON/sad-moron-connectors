# AI Agent Guide

## Purpose

This document provides guidance for AI agents reading or operating around
`SAD-MORON-CONNECTORS`.

It exists to clarify which documents are authoritative, which connector
boundaries must be preserved, and which safety rules apply before any
interpretation, planning, or implementation work proceeds.

## Authoritative Documents

Current repository authority lives primarily in:
- `docs/`
- `contracts/`
- connector pack governance documents under `connectors/`
- framework governance references inherited from `sad-moron-framework`

Reports are evidence and history, not current governance authority.

AI agents must not treat reports, audits, or older review artifacts as current
authority when more recent `docs/`, `contracts/`, or connector pack documents
define the active rule set.

## Runtime And Permission Boundaries

AI agents must not infer runtime permissions from governance documents.

Connector contracts and governance packs do not grant:
- runtime permission
- deployment approval
- credential access
- connector authorization
- operational write authority

AI agents must not treat connector contracts as production connectors.

## Source And Access Boundary

AI agents must not invent source access.

No AI agent should:
- assume live source reachability
- infer institutional mappings
- infer authorization from documentation presence
- propose operational execution without declared authority

AI agents must not create operational connectors without:
- declared source
- declared boundary
- relevant authorization
- documented sensitive-data handling
- accountable human review path

## Sensitive Exposure Rule

AI agents must not expose:
- IDs
- endpoints
- credentials
- tokens
- institutional mappings
- deployment secrets

If a task would reveal or operationalize sensitive material, the safe
classification is `REVIEW` or `BLOCKED` unless explicit authority and safe
handling boundaries are already documented.

## Uncertainty Classification

When uncertainty exists, classify the situation as:
- `REVIEW`
- `BLOCKED`

Use `REVIEW` when meaning is mostly clear but governance, scope, or authority
still requires confirmation.

Use `BLOCKED` when authority, source boundary, authorization, or sensitive-data
handling is missing or undefined.

## Janus Core Wording Rule

This repository inherits governance principles from Janus Core.

It does not depend on the full Janus runtime ecosystem unless a separate
repository explicitly documents that dependency for operational implementation.

## Summary

Do not infer runtime permissions, do not treat connector contracts as production
connectors, do not invent source access, and do not expose IDs, endpoints,
credentials, or institutional mappings. When uncertain, classify `REVIEW` or
`BLOCKED`.
