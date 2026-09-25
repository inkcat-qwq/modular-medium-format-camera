# Revision History

> **Document type:** Historical revision index  
> **Status:** Living document  
> **Last updated:** September 2026  
> **Public documentation note:** This index describes publicly documented development milestones and may intentionally lag behind private internal development.

This document records historical revision identifiers used during development of the Modular Medium Format Camera project.

The naming system evolved organically during early development. Historical identifiers are preserved here so that older simulations, notes, diagrams, and design decisions remain traceable.

This document does not imply that all revisions reached the same level of maturity.

---

## Revision Status Definitions

Historical items may be described using the following states:

- `CONCEPT` — exploratory idea
- `SIMULATION` — evaluated primarily through simulation
- `CANDIDATE` — retained for further development
- `REJECTED` — investigated but not retained
- `SUPERSEDED` — replaced by a later direction
- `CURRENT` — part of the currently published development direction
- `RETAINED MILESTONE` — historically important direction retained as a basis for later work
- `RETAINED CANDIDATE` — candidate retained within a development path
- `ALTERNATIVE CANDIDATE` — retained comparator rather than the primary documented candidate
- `DEVELOPMENT STUDY` — structured investigation used to define or compare subsystem architecture
- `HOLD` — work intentionally not advanced to freeze or release pending further evidence

---

## Body Architecture

### REV03

**Area:** Camera body / structural architecture  
**Status:** SUPERSEDED

Early structural body revision.

This revision contributed to the transition from a conventional camera-body concept toward a more clearly modular architecture.

---

### REV04

**Area:** Camera body / structural architecture  
**Status:** SUPERSEDED

Further development of the central body and module arrangement.

The architecture continued to separate the digital-back structure from the central camera body.

---

### REV04A

**Area:** Camera body / structural architecture  
**Status:** SUPERSEDED

Development variant derived from REV04.

This stage further explored the load-bearing structure and front mounting architecture.

---

### BODY2_REV05

**Area:** Camera body / structural architecture  
**Status:** CANDIDATE / SUPERSEDED BY LATER DETAIL DEVELOPMENT

A more mature body architecture in which the central structural core became the primary reference structure for the camera system.

This revision strongly influenced the current platform architecture.

---

## Rear Interface Development

### B2-IF01

**Area:** Rear digital-back interface  
**Status:** CANDIDATE / SIMULATION

Interface study focused on digital-back attachment, seating, and mechanical compatibility.

This work contributed to the current emphasis on repeatable positioning and controlled seating.

---

## Viewfinder Packaging Studies

### SIDE01

**Area:** Viewfinder placement  
**Status:** REJECTED / SUPERSEDED

Early side-mounted viewfinder packaging study.

Used primarily to evaluate camera width, eye position, and ergonomic interference.

---

### SIDE02

**Area:** Viewfinder placement  
**Status:** CANDIDATE / SUPERSEDED BY LATER DEVELOPMENT

Refined side-mounted finder study.

This stage improved packaging and ergonomic compatibility and contributed to the retained side-shoulder viewfinder direction.

---

## Optical Viewfinder Development

### VF3B

**Area:** Optical viewfinder  
**Status:** REJECTED

Optical bench architecture investigated during early viewfinder development.

Testing and simulation exposed limitations in usable eye position and field performance.

---

### OPT02

**Area:** Optical viewfinder  
**Status:** REJECTED / DEVELOPMENT STEP

Optical configuration developed to improve field coverage and corner performance.

Results were improved relative to earlier concepts but remained insufficient for the intended viewing requirements.

---

### OPT03

**Area:** Optical viewfinder  
**Status:** REJECTED

Further optical development focused on eye-box and field performance.

The configuration did not provide sufficient viewing tolerance.

---

### OPT04

**Area:** Optical viewfinder  
**Status:** SUPERSEDED

More advanced optical configuration incorporating additional correction.

Performance improved, but remaining limitations and optical complexity motivated continued architectural exploration.

---

## Optical Bench Studies

### BENCH02A

**Area:** Viewfinder / optical bench  
**Status:** DEVELOPMENT STUDY

Bench configuration used to evaluate practical optical components, packaging, and assembly paths.

---

### BENCH02A_1

**Area:** Viewfinder / optical bench  
**Status:** DEVELOPMENT STUDY

Refinement of BENCH02A.

Used to explore assembly and removal constraints within the developing camera architecture.

---

## Direct-View Finder Development

### VF9_DIRECT01

**Area:** Optical viewfinder  
**Status:** RETAINED MILESTONE

Major transition toward a direct-view optical finder architecture.

This direction reduced dependence on more complex relay systems and became the basis for later direct-view finder development.
---

### D3

**Area:** Direct-view optical configuration  
**Status:** RETAINED CANDIDATE

Primary optical candidate retained from the direct-view development path.

The design remains simulation-based and has not yet been physically validated.

---

### D4

**Area:** Direct-view optical configuration  
**Status:** ALTERNATIVE CANDIDATE

Alternative optical configuration retained for comparison with the primary candidate.

---

### VF13_FRAME_ARCH01

**Area:** Frameline / finder information architecture  
**Status:** RETAINED MILESTONE

Study comparing fixed optical framelines, later dynamic correction, and limited cue architectures.

The publicly retained path prioritizes an independent fixed-brightline principle test while leaving dynamic correction and packaging geometry unfrozen.

---

## Tolerance Development

### TOL01

**Area:** Mechanical tolerance analysis  
**Status:** SIMULATION

Tolerance study used to investigate:

- alignment variation
- assembly repeatability
- removal and reinstallation behavior
- effectiveness of calibration
- sensitivity of the mechanical datum architecture

This study reinforced the importance of repeatable reference geometry and controlled interface design.

---

## Front-Module Closure Development

### FM2_CLOSURE03

**Area:** Front-module closure / retention integration  
**Status:** HOLD

Integrated holding, retention, preload, safety, service, and lens-envelope concepts into a single digital candidate.

The study intentionally stopped without release after unresolved CAD-level conflicts, service-path issues, and lens-envelope risks remained.

Its engineering value is the explicit failure-to-close result rather than a completed front-module design.

---

## Electronics and System Integration

### SYS_ELEC01

**Area:** Control / communication architecture  
**Status:** DEVELOPMENT STUDY

Established software-simulated control responsibilities, degraded modes, and communication boundaries without freezing hardware.

---

### SYS_POWER01

**Area:** Power / energy architecture  
**Status:** DEVELOPMENT STUDY

Compared power, protection, and future-load scenarios without selecting a battery, rail architecture, or physical hardware.

---

### SYS_IO01

**Area:** Interconnect / harness architecture  
**Status:** DEVELOPMENT STUDY

Defined functional interface classes and protection responsibilities while leaving connectors, pinouts, and cable construction open.

---

### SYS_UI01

**Area:** User interaction architecture  
**Status:** DEVELOPMENT STUDY

Evaluated a compact physical-control and status model through software scenarios without freezing industrial-design geometry.

---

### SYS_ICD01

**Area:** System interface control baseline  
**Status:** RETAINED MILESTONE

Established a coordinated system-level baseline for mechanical, optical, electrical, calibration, and ownership responsibilities.

The baseline is a traceability and consistency milestone, not a design freeze; physical system verification remains open.

---

## Publicly Documented Direction

The currently published architecture is the result of several parallel development paths:

```text
Body Architecture

REV03
  ↓
REV04
  ↓
REV04A
  ↓
BODY2_REV05
  ↓
Current Structural Architecture


Viewfinder Development

SIDE Studies
  ↓
VF / OPT Relay Studies
  ↓
Optical Bench Studies
  ↓
VF9_DIRECT01
  ↓
D3 / D4 Candidate Evaluation
  ↓
VF13_FRAME_ARCH01
  ↓
Fixed-Brightline Principle Validation Candidate


Mechanical Interface Development

Early Interface Concepts
  ↓
B2-IF01
  ↓
Tolerance Analysis
  ↓
Current Datum / Seating / Clamping Architecture


Front-Module Development

Early Front-Module Concepts
  ↓
Integrated Closure Studies
  ↓
FM2_CLOSURE03
  ↓
HOLD — New Physical Evidence Required


System Electronics / Interface Development

SYS_ELEC01
  ↓
SYS_POWER01 / SYS_IO01 / SYS_UI01
  ↓
SYS_ICD01
  ↓
Published System Interface Baseline
```

---

## Naming Going Forward

Future revisions should use more consistent subsystem-based identifiers where practical.

Possible naming conventions include:

- `BODY-Rxx`
- `BACKIF-Rxx`
- `VF-Rxx`
- `VFOPT-Rxx`
- `LENSIF-Rxx`
- `TOL-Rxx`

Historical identifiers will not be renamed retroactively.

Instead, future public documents may reference both the historical identifier and a newer structured naming system when necessary.

---

## Related Documents

- [Project Evolution — September 2026](2026-09-project-evolution.md)
- [BODY2_REV05 — Architecture Integration](body2-rev05-architecture-integration.md)
- [FM2_CLOSURE03 — Digital Closure Review](fm2-closure03-digital-closure-review.md)
- [VF13_FRAME_ARCH01 — Frameline Architecture Study](vf13-frameline-architecture.md)
- [Electronics & Control Architecture](../architecture/electronics-control-overview.md)
- [Development Log Overview](README.md)
- [System Architecture Overview](../architecture/system-overview.md)
- [Current Project State](../overview/current-state.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
