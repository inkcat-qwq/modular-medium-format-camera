# DD-003 — P1 Function First

> **Decision status:** CURRENT P1 DIRECTION  
> **Validation status:** Physical system verification incomplete  
> **Recorded:** September 2026

## Context

Whole-camera concept and compactness studies made the remaining functional gaps visible. Recovering native CAD delivery did not close portability, shutter implementation, real focusing, iris, lens or DM22 interface requirements. Optimizing the product before these functions were established risked treating packaging progress as camera validation.

## Decision

P1 is the single active functional-prototype mainline. First demonstrate the full shooting chain with BODY3, K3 / ACT-E, FOCUS-H2, a moving shared iris, one reference Optical Insert, D3, independent range assistance and DM22.

Function, adjustability, repeatability, safety and serviceability take priority over weight, industrial design and product packaging. Larger / heavier prototype construction, larger electronics or actuators, external development power and ordinary prototype materials may be considered with documented impacts. Safety, repeatability and fixed-datum responsibilities remain gates.

## Consequences

- Portability is DEFERRED PRODUCT OPTIMIZATION until after P1 validation, not an achieved lightweight product result.
- Magnesium, CFRP and hybrid structures remain possible future research requiring redesign and new evidence. No GEN1-L CAD is introduced.
- FM-C / Copal front development is superseded by H2 / iris / Optical Insert and the body shutter; historical records remain available.
- The sequence P1-01 through P1-07 is an evidence roadmap. The current shutter remains IMPLEMENTATION HOLD and NOT READY FOR CONTROLLED BENCH PLANNING.
- No manufacturing or physical camera release follows from this strategy decision.

## Review conditions

A fundamental incompatibility in the real reference lens / shared iris, DM22 synchronization or feasible shutter implementation can require an explicit architecture review. Weight alone does not undo the P1 strategy. Product optimization is reconsidered after functional evidence exists.

Source basis: CAMERA_P1_BASELINE01 system baseline, requirements, gate and development sequence; current shutter qualification from P1-01_SHUTTER_IMPL02.

- [P1 transition](../development-log/p1-functional-prototype-transition.md)
- [Evidence roadmap](../overview/physical-validation-roadmap.md)
- [Modularity principle](DD-001-modular-platform-architecture.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
