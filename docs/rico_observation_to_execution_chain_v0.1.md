# RiCo Observation-to-Execution Chain v0.1

**Status:** Draft for joint review  
**Scope:** Private NeoMundi × RiCo exploratory pilot

## Purpose

This document records a proposed architectural boundary between NeoMundi runtime observation and RiCo runtime governance.

It is based on the initial private review of the representative observation cases and remains subject to joint validation.

The purpose is not to merge observation and authority.

The purpose is to establish how an observed runtime condition may become a governed, traceable and reconstructable input to a consequence-bearing decision.

---

## Core Separation

NeoMundi answers:

> What was observed under declared measurement conditions?

RiCo answers:

> Given that represented reality, what downstream consequence remains justified under present conditions?

Execution remains a decision exercised by an authority-bearing governance layer.

---

## Proposed Chain

```text
Runtime
↓
Observation
↓
Observation Receipt — NeoMundi
↓
Runtime Integrity Assessment — RiCo
↓
Admissibility
↓
Runtime Execution Boundary
↓
Execution
↓
Governance Receipt
↓
Reconstruction
