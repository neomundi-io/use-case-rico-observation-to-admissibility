# RiCo Observation-to-Execution Chain v0.2

**Status:** Draft for joint review  
**Scope:** Private NeoMundi × RiCo exploratory pilot

---

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

```
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
```

---

## Architectural Principles

### 1. Observation is not authority

A NeoMundi observation payload represents runtime conditions, signals and measurement limits.

It does not itself authorise, prohibit, suspend or execute an action.

---

### 2. Representation is not consequence

A represented reality may be accurate and still be insufficient to justify a requested downstream consequence.

Conversely, an unfavourable observation does not automatically prohibit execution.

Admissibility depends on the relationship between:

- the represented reality;
- the requested consequence;
- the applicable authority;
- the available controls;
- the required evidence and receipts.

---

### 3. Positive observation does not enlarge authority

A favourable runtime observation does not itself justify a more consequential use, broader scope or higher-risk execution.

The authority and policy context remain decisive.

---

### 4. Negative observation does not automatically prohibit execution

A risk signal may require restriction, replay, review, acceptance of a documented gap, additional authority or enhanced controls.

It does not automatically determine that execution must stop.

---

### 5. Incomplete measurement is part of the represented reality

A known evidence gap is not the same as a negative observation.

It must nevertheless remain visible in the admissibility assessment because it may limit what consequence can be justified.

---

### 6. Runtime admissibility is continuously evaluated

Runtime conditions evolve.

Observation may change.

Authority may change.

Dependencies may change.

Environmental conditions may change.

Human decisions may change.

RiCo therefore treats admissibility as a continuously evaluated runtime property rather than a decision established only at system initiation.

Execution may continue only while sufficient authority, evidence, policy and runtime integrity remain admissible under present conditions.

Operational continuity alone does not preserve execution legitimacy.

Admissibility must persist.

---

## What the Pilot Tests

For each representative NeoMundi observation payload, the pilot should determine whether RiCo can produce:

1. a runtime integrity assessment;
2. an admissibility posture;
3. an execution boundary;
4. a documented governance rationale;
5. a lightweight governance receipt;
6. sufficient material to reconstruct the relationship between observation, authority, consequence and outcome.

---

## Expected Boundary

| NeoMundi | RiCo |
|----------|------|
| Observes runtime conditions | Assesses integrity and admissibility |
| Records measurement limits | Determines whether a consequence is justified |
| Produces an observation receipt | Produces a governance receipt |
| Does not claim authority | Connects authority, controls and execution boundaries |
| Does not execute | Supports governed execution and reconstruction |

---

## Open Questions

- What minimum fields are required in an observation receipt for RiCo to assess admissibility?
- How should incomplete observation be represented in a governance receipt?
- What authority must be explicit before an execution boundary can be altered?
- Which conditions require replay, review, escalation or documented acceptance?
- What is the minimal reconstructable record across the full chain?

---

## Next Step

Review this draft jointly against the five representative payloads and identify:

1. missing continuity fields;
2. missing authority fields;
3. required receipt attributes;
4. the smallest executable mapping from observation to admissibility assessment.

The objective of the pilot is not to automate governance.

The objective is to determine whether runtime observation, admissibility assessment and governed execution can remain continuously reconstructable as operating conditions evolve.
