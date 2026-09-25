# Project Evolution — September 2026

> **Document type:** Development history  
> **Project stage:** Simulation / Pre-prototype  
> **Date:** September 2026

This document summarizes the major publicly documented architectural evolution of the Modular Medium Format Camera project up to the current published stage.

It is intended to preserve the reasoning and progression of the project rather than provide manufacturing specifications.

---

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

Simulation began to focus on questions such as:

- How accurately does a module return after removal?
- How sensitive is alignment to manufacturing variation?
- Which reference features dominate positioning error?
- How much can calibration improve system accuracy?
- Does repeated assembly significantly change alignment?

These studies reinforced the need for clearly defined mechanical datums and independent clamping.

---

## 9. Current Architecture

The currently published project architecture consists of:

- a central structural core
- a modular rear digital-back interface
- interchangeable front / lens modules
- an integrated direct optical viewfinder
- defined positioning and seating architecture
- provision for evolving electronic systems

The project remains in the:

**Simulation / Pre-prototype**

stage.

No complete physical camera prototype has yet validated the system.

---

## 10. Current Development Direction

The next major transition is from architecture and simulation toward selective physical validation.

Important future validation work includes:

- mechanical datum testing
- rear-interface repeatability testing
- optical bench validation
- module removal and reinstallation testing
- structural prototype evaluation
- eventual imaging tests

The architecture may continue to change as physical test results become available.

---

## Development Principle

The project intentionally preserves rejected designs and failed experiments.

The development history is considered part of the engineering output because unsuccessful concepts document constraints that may otherwise need to be rediscovered later.
