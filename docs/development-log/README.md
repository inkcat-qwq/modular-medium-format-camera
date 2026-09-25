# Development Log

This directory records the development history of the Modular Medium Format Camera project.

The purpose of the development log is to preserve major architectural changes, experiments, rejected concepts, simulation milestones, and changes in design direction.

These records are not intended to represent manufacturing specifications.

Public documentation may intentionally lag behind private internal development. See the [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md).

## Documents

- [BODY2_REV05 — Architecture Integration](body2-rev05-architecture-integration.md)  
  Public architecture-integration review covering the transition toward the current structural, viewfinder, and rear-interface direction.

- [VF13_FRAME_ARCH01 — Frameline Architecture Study](vf13-frameline-architecture.md)  
  Sanitized public summary of the fixed-brightline, cue, and later dynamic-frameline architecture study.

- [Project Evolution — September 2026](2026-09-project-evolution.md)  
  Narrative overview of how the project evolved from early concepts to the current architecture.

- [Revision History](revision-history.md)  
  Historical index of body, interface, viewfinder, optical, and tolerance-study revision identifiers.

## Log Structure

Development records may include:

- architecture revisions
- mechanical interface studies
- optical experiments
- simulation milestones
- rejected concepts
- prototype results
- major changes in design direction

Detailed engineering decisions should be recorded separately in the
[Design Decisions](../design-decisions/) directory.

## Development Phases

### Early Architecture Exploration

The project began as an investigation into a modular medium-format digital camera architecture.

Early work focused on:

- camera core proportions
- digital-back integration
- front-module concepts
- mechanical packaging
- basic viewfinder placement

Multiple structural configurations were explored before the current platform architecture emerged.

### Structural Architecture Development

Later work focused on defining a central structural core and separating the camera into major functional modules.

Development increasingly emphasized:

- repeatable module positioning
- independent adapter structures
- structural reference surfaces
- separation of locating and clamping functions

This work formed the basis of the current mechanical architecture.

### Viewfinder Development

Several optical viewfinder architectures were investigated.

Development included:

- finder placement studies
- packaging and ergonomic studies
- relay optical concepts
- field-of-view studies
- eye-position tolerance
- candidate direct-view optical systems

Several configurations were rejected due to optical or ergonomic limitations.

The currently published direction uses an integrated direct optical viewfinder architecture.

### Tolerance and Repeatability Studies

Tolerance simulation was introduced before physical manufacturing in order to evaluate:

- module alignment
- seating repeatability
- removal and reinstallation behavior
- sensitivity to manufacturing variation

These studies continue to inform the mechanical interface architecture.

### Current Phase

The project is currently in the:

**Simulation / Pre-prototype**

stage.

The immediate objective is to move selected subsystem concepts toward physical validation while continuing architecture and simulation work.

Current publicly documented parallel tracks now include frameline principle validation and system-level electronics / control architecture.

## Philosophy

Failed experiments are intentionally preserved.

A rejected design may still contain useful information about:

- constraints
- trade-offs
- packaging limits
- optical limitations
- mechanical failure modes

The development history is therefore considered part of the project documentation rather than temporary working material.
