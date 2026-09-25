# DD-001 — Modular Camera Platform Architecture

> **Decision status:** ACCEPTED — Current architectural direction  
> **Validation status:** PRE-PROTOTYPE  
> **Date:** September 2026

## Context

The project began with the goal of developing a medium-format digital camera without permanently tying the camera body to a single digital back, lens system, viewfinder configuration, or future electronic architecture.

Commercial medium-format systems often integrate many of these functions around proprietary mechanical and electronic interfaces.

For an experimental camera project, this can make redesign difficult when one subsystem changes.

The project therefore requires an architecture that can evolve while allowing individual subsystems to be redesigned, replaced, or validated independently.

## Decision

The camera will be developed as a **modular platform** rather than as a single fixed camera body.

The system will be divided into several major subsystems:

- central structural core
- rear digital-back interface
- front / lens module
- optical viewfinder system
- mechanical datum and clamping system
- electronics / system control

Each major subsystem should, where practical, have a clearly defined interface with the central camera structure.

The central core should provide the primary structural reference while avoiding unnecessary dependency on any one digital back, lens system, or viewfinder design.

## Design Goals

The modular architecture is intended to support:

- interchangeable digital-back adapters
- interchangeable front or lens modules
- independent development of the optical viewfinder
- easier mechanical experimentation
- electronic system expansion
- subsystem replacement without complete body redesign
- clearer tolerance and interface analysis
- preservation of experimental flexibility

## Alternatives Considered

### A. Fixed Integrated Camera Body

A conventional architecture could permanently integrate the digital back, lens interface, viewfinder, and structural body.

**Advantages:**

- potentially smaller
- potentially lighter
- fewer mechanical interfaces
- easier optimization around one final configuration

**Disadvantages:**

- major subsystem changes may require complete body redesign
- difficult to support multiple digital backs
- reduced experimental flexibility
- stronger dependency between mechanical and optical development

This approach was not selected for the current development phase.

### B. Highly Universal Modular System

Another option would be to make nearly every component universally interchangeable.

**Advantages:**

- maximum flexibility
- broad compatibility

**Disadvantages:**

- excessive interface complexity
- increased size and mass
- difficult tolerance control
- increased manufacturing requirements
- risk of modularity becoming more important than camera performance

This approach was also rejected.

## Selected Direction

The project therefore uses **controlled modularity**.

Only major functional subsystems are intended to be modular.

The central structural architecture remains responsible for maintaining alignment, rigidity, and repeatable reference geometry.

Modularity should not be introduced where it significantly compromises:

- rigidity
- alignment
- optical performance
- ergonomics
- manufacturability
- reliability

## Consequences

### Positive

- subsystems can evolve independently
- experimental digital backs can be supported through adapters
- optical and mechanical development can proceed separately
- failed concepts do not necessarily invalidate the entire camera architecture
- future upgrades become easier to incorporate

### Negative

- additional mechanical interfaces are required
- tolerance accumulation becomes more important
- locking and datum systems become critical
- the system may become larger than a fully integrated camera
- manufacturing complexity may increase

## Current Validation

The modular architecture has currently been evaluated through:

- CAD architecture development
- interface studies
- optical packaging studies
- mechanical tolerance simulation

A complete physical camera prototype has not yet validated the architecture.

## Revisit Conditions

This decision should be reconsidered if:

- modular interfaces prevent acceptable structural rigidity
- alignment repeatability cannot meet imaging requirements
- the resulting camera becomes impractically large or heavy
- physical prototype testing reveals unacceptable interface instability
- a later integrated architecture provides substantial performance advantages

## Related Documents

- [System Architecture Overview](../architecture/system-overview.md)
- [Current Project State](../overview/current-state.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
