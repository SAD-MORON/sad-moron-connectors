# Connector Contract

## Purpose

This contract defines the minimum governance contract every future SAD Moron connector must satisfy before implementation.

## Required Contract Elements

Every connector contract must define:
- connector name
- governing declared source
- institutional purpose
- temporal boundary
- intended record class
- known limitations
- compliance obligations to the framework

## Connector Obligations

A connector must:
- inherit governance from `sad-moron-framework`
- declare its source boundary
- remain limited to institutional use
- avoid unrestricted collection
- remain interpretable for later audit

## Exclusions

This contract does not define executable interfaces or implementation details.

## Summary

No connector should move into implementation until this governance contract is satisfied.
