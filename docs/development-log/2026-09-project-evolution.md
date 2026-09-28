# Project Evolution — September 2026

> **Document type:** Development history  
> **Current phase:** P1 Functional Prototype Development  
> **Date:** September 2026

This document summarizes the major publicly documented architectural evolution of the Modular Medium Format Camera project up to the current published stage.

It is intended to preserve the reasoning and progression of the project rather than provide manufacturing specifications.

---

> **Reading this chronology:** Sections 1–13 preserve the earlier public development account. Their present-tense descriptions and proposed next steps are historical context. Sections 14–19 record the later BODY3 / shutter / P1 transition.

## 1. Initial Concept

The project began with the idea of creating a custom medium-format digital camera that would not be permanently tied to a single camera body, digital back, lens system, or viewfinder configuration.

Early exploration focused primarily on:

- overall camera proportions
- digital-back integration
- interchangeable front modules
- lens-system flexibility
- basic body packaging
- possible focusing and viewing systems

At this stage, the architecture was still highly exploratory.

---

## 2. Early Body Revisions

Several early body revisions were created to investigate how the digital back, structural core, and front optical system could be packaged together.

These revisions gradually shifted the project away from a conventional fixed camera body and toward a modular structural architecture.

Early development exposed several recurring problems:

- excessive dependence between subsystems
- unclear mechanical reference surfaces
- difficult module replacement
- limited room for optical and ergonomic changes
- uncertainty in how the digital back should be repeatedly positioned

These issues influenced later architecture decisions.

---

## 3. Structural Core Development

Later revisions introduced a more clearly defined central structural core.

The core increasingly became responsible for:

- maintaining front-to-rear alignment
- supporting interchangeable modules
- carrying the viewfinder structure
- providing reference geometry
- separating the camera structure from specific digital-back hardware

This represented an important transition from a camera-body concept toward a camera-platform concept.

---

## 4. Rear Interface Development

The removable digital-back interface became a major engineering focus.

Initial interface concepts revealed that simply attaching a digital back securely was not sufficient.

A precision camera interface must also control:

- position
- orientation
- axial seating
- repeatability after removal
- clamping-induced movement

This led to the current design principle of separating positioning, seating, and clamping functions where practical.

See:

- [DD-002 — Separate Positioning, Seating, and Clamping Functions](../design-decisions/DD-002-separate-positioning-seating-clamping.md)

---

## 5. Viewfinder Placement Studies

Multiple viewfinder arrangements were explored.

Early concepts investigated different positions relative to the main camera body, including configurations that created packaging or ergonomic conflicts.

These studies demonstrated that optical design could not be considered independently from:

- eye position
- camera width
- user ergonomics
- internal packaging
- mechanical structure

The viewfinder therefore developed into a dedicated subsystem rather than a simple accessory.

---

## 6. Optical Viewfinder Experiments

Several optical architectures were investigated through simulation.

Some concepts used more complex relay arrangements in an attempt to achieve the desired field coverage and packaging.

These experiments exposed problems including:

- insufficient usable eye box
- poor off-axis viewing
- corner visibility limitations
- optical packaging complexity
- sensitivity to eye position

Rejected optical configurations were retained as useful engineering evidence rather than discarded.

Development eventually shifted toward a simpler direct-view optical architecture.

---

## 7. Direct-View Architecture

The direct optical viewfinder became the primary development direction after earlier relay-based concepts showed significant limitations.

The current direction emphasizes:

- compact optical packaging
- comfortable eye position
- useful field coverage
- reduced optical complexity
- integration into the camera structure

Several candidate optical configurations have been studied.

The current optical design remains a simulation candidate and has not yet been physically validated.

---

## 8. Tolerance and Repeatability Simulation

As the mechanical architecture became more mature, tolerance analysis became increasingly important.

BODY2_TOL01 introduced a reproducible assumed-input Monte Carlo and analytical error-chain study spanning the removable front module, structural core, rear adapter, and digital-back interface.

The study focused on questions such as:

- How sensitive is the architecture to assumed mechanical variation?
- What can a central calibration remove, and what does it leave unresolved?
- How much can removal and reinstallation change the mechanical state?
- Which positioning and seating responsibilities need a clearer physical definition?
- How strongly do the conclusions depend on assumed distributions and correlations?

The study deliberately did not convert simulated percentiles into production yield or image-quality acceptance.

Its most important result was to move the next step away from “tighten every tolerance” and toward measurement: define a measurable datum chain, characterize real seating and guide behavior, and replace assumed inputs with physical evidence.

---

## 9. HUD Integration and Frameline Reframing

After the direct-view finder direction stabilized, development explored how framing and status information could be added without sacrificing the direct optical scene.

The sequence became progressively more constrained:

- **VF10_D3_ENGINEERING01** retained the D3 scene-viewing path but deferred HUD integration.
- **VF11_HUD_PACK01** tested compact independent HUD packaging and remained on HOLD because field, eye-position, and physical-volume requirements could not be closed together.
- **VF12_SHARED_HUD01** tested a shared-aperture approach. Optical transfer could be studied, but no credible camera-level HUD package or released body interface resulted.
- **VF13_FRAME_ARCH01** reframed the problem around the minimum information actually required.

The retained public direction now favors a fixed optical brightline as the first independent principle-validation step.

Small cues may be added later, while dynamic correction remains a later option rather than a prerequisite for the direct-view finder.

---

## 10. Front-Module Closure Study

Front-module development progressed from interface and packaging concepts toward an integrated closure candidate.

The study combined holding, retention, preload, safety, service, and lens-envelope concerns into one mechanical review.

The result remained on **HOLD**.

Several CAD-level and assembly-level issues were still unresolved, and the project intentionally stopped further parameter tuning rather than treating the remaining work as “only physical testing.”

The next useful inputs are real lens geometry, physical clamp / safety evidence, and measured or supplier-backed mechanical behavior.

---

## 11. Electronics and System-Control Development

Electronics developed from a future placeholder into a parallel architecture track.

Separate studies now address:

- body control and communication responsibilities
- power and protection behavior
- modular interconnect responsibilities
- user interaction
- system-level interface control and traceability

These studies currently rely on executable software models and interface documents rather than released hardware.

No PCB, connector system, battery architecture, digital-back protocol, or production control layout has been frozen.

---

## 12. Current Architecture at the Earlier Public Milestone (Historical)

The currently published project architecture consists of:

- a central structural core
- a modular rear digital-back interface
- interchangeable front / lens modules
- front-module closure and retention architecture currently on HOLD
- an integrated direct optical viewfinder
- defined positioning and seating architecture
- a staged frameline / cue subsystem
- coordinated electronics / control architecture

The project remains in the:

**Simulation / Pre-prototype**

stage.

No complete physical camera prototype has yet validated the system.

---

## 13. Current Development Direction at That Milestone (Historical)

The next major transition is from architecture and simulation toward selective physical validation.

Important future validation work includes:

- mechanical datum testing
- rear-interface repeatability testing
- direct-view finder and fixed-frameline bench validation
- real digital-back synchronization evidence
- real power, contact, and interconnect testing
- module removal and reinstallation testing
- structural prototype evaluation
- eventual imaging tests

The architecture may continue to change as physical test results become available.

---

## 14. Body-Shutter Transition and BODY3

The later architecture moves the shutter into the body and uses 645-class as the maximum optical scope, replacing the earlier 6×7 body ambition. BODY3 replaces BODY2 as the active body direction, retaining D3 and a fixed rear datum independent of the shutter, with a modular rear adapter. BODY3 architecture, structural packaging and frame studies have different local gates; none establishes complete physical camera readiness.

## 15. Flexible Focal-Plane Shutter and Electric Actuation

SHUTTER01 retained K3 flexible dual curtains as the primary research direction. SHUTTER02 exposed mechanical closure gaps. SHUTTER03 selected ACT-E direct closed-loop electric drive over the active ACT-S route to simplify the normal braking, capture and reset chain, while leaving hardware / safe closing on HOLD. SHUTTER04 introduced realistic actuator, power, support and service constraints without closing those gates.

## 16. Focus and Lens Architecture Redesign

FOCUS-H2 replaces FM-C as the front direction. A large manual focus ring moves a non-rotating optical cage whose actual q must be measured directly. A shared Universal Iris travels with the cage. The user-replaceable Optical Insert becomes a lensboard-like optical carrier rather than a complete per-lens focusing / shutter system. Only one reference lens is planned initially, with real optical geometry and compatibility still open.

## 17. Whole-Camera Concept Integration

CAMERA_GEN1_CONCEPT01 brought BODY3, H2, the shared iris and the reference insert into a whole-camera concept. Its native delivery limitation was recorded rather than hidden. D3 retained optical scene viewing, while electronic frameline, three small focus cues and independent ranging became the intended assistance layer; a full HUD was not reopened.

## 18. Portability Review and Native Recovery

CAMERA_GEN1_COMPACT01 recovered native CAD delivery and recorded more explicit mass, envelope and service evidence. It did not close the product portability gate or demonstrate physical camera function. Structural variants and modelled mass reductions did not prove real mechanisms, stiffness, lens compatibility or DM22 registration.

## 19. P1 Functional Prototype Transition

CAMERA_P1_BASELINE01 made P1 the active function-first mainline: first establish the complete shooting chain, then optimize the product. Weight and packaging are DEFERRED PRODUCT OPTIMIZATION. Larger prototype hardware and external development power may be considered while function, safety, repeatability and service gates remain required. Magnesium / CFRP / hybrid structures remain possible post-P1 research, with no GEN1-L CAD introduced.

P1-01_SHUTTER_IMPL01 and IMPL02 continued implementation. The latest IMPL02 retains a right-side drive arrangement and an optical / coded direct bar reference candidate, but remains **IMPLEMENTATION HOLD — NOT READY FOR CONTROLLED BENCH PLANNING**. Main-power-loss closing is under study; total-energy-loss autonomous mechanical closing is **NOT CLOSED / NOT VALIDATED**.

H2 motion / q sensing, the actual iris, insert locking / real reference-lens data, DM22 registration / synchronization, physical D3 assistance / ranging and electronics / power / UI remain open. P1 is a development phase, not a completed prototype. The current [evidence roadmap](../overview/physical-validation-roadmap.md) follows P1-01 through P1-07.

These additions summarize the reviewed source milestones without inventing exact calendar dates. See [P1 transition](p1-functional-prototype-transition.md), [BODY3 development](body3-development.md) and [shutter development](shutter-architecture-development.md) for evidence scope.

---

## Development Principle

The project intentionally preserves rejected designs and failed experiments.

The development history is considered part of the engineering output because unsuccessful concepts document constraints that may otherwise need to be rediscovered later.


---

## Related Documents

- [BODY2_REV05 — Architecture Integration](body2-rev05-architecture-integration.md)
- [BODY2_TOL01 — Mechanical Tolerance and Repeatability Study](body2-tol01-mechanical-tolerance-study.md)
- [FM2_CLOSURE03 — Digital Closure Review](fm2-closure03-digital-closure-review.md)
- [VF13_FRAME_ARCH01 — Frameline Architecture Study](vf13-frameline-architecture.md)
- [Viewfinder, HUD, and Frameline Evolution](viewfinder-hud-frameline-evolution.md)
- [Electronics & Control Architecture](../architecture/electronics-control-overview.md)
- [Revision History](revision-history.md)
- [System Architecture Overview](../architecture/system-overview.md)
- [Current Project State](../overview/current-state.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
