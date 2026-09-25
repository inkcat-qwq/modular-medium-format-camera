# Current Project State

> **Status:** Pre-prototype / Simulation  
> Last updated: September 2026

This document provides a high-level snapshot of the currently published development state of the Modular Medium Format Camera project.

> **Public documentation note:** Private internal development may be ahead of the milestones described here.

## System Architecture

The project is currently based on a modular camera architecture consisting of:

- a central structural camera core
- a replaceable digital-back interface
- interchangeable front and lens modules
- an integrated direct optical viewfinder
- independent mechanical datum and clamping systems

The current architecture remains experimental and has not been frozen for manufacturing.

## Current Development Areas

### Camera Body

**Status:** CANDIDATE / SIMULATION

The current body architecture is being evaluated for structural layout, module integration, and interface repeatability.

### Digital Back Interface

**Status:** CANDIDATE / SIMULATION

Development currently focuses on:

- repeatable positioning
- axial seating
- independent clamping
- removable digital-back adapters

Physical interface geometry has not yet been fully validated.

### Optical Viewfinder

**Status:** CANDIDATE / SIMULATION

A direct optical viewfinder architecture is the primary publicly documented development direction.

Current work focuses on:

- field of view
- magnification
- eye position tolerance
- corner visibility
- optical packaging

The optical system has not yet been physically bench-tested.

### Tolerance Analysis

**Status:** SIMULATION

Tolerance studies are being used to evaluate mechanical alignment and repeatability before physical prototype manufacturing.

### Electronics / System Control

**Status:** EARLY SYSTEM DEVELOPMENT

Early system-level work is defining power, I/O, user-interface, and subsystem-interface responsibilities. Detailed implementation remains secondary to the current mechanical and optical validation work.

## Major Open Questions

- final rear-interface geometry
- locking and clamping mechanism
- manufacturing repeatability
- optical eye-box performance
- final front-module architecture
- environmental sealing
- physical prototype validation

## Next Development Gate

The next major goal is to move selected simulated subsystems toward physical interface and bench validation.

---

This document describes the current development state only.

Values and architectures described throughout the repository should not be considered manufacturing specifications unless explicitly marked `FROZEN` or `VALIDATED`.


## Related Documents

- [System Architecture Overview](../architecture/system-overview.md)
- [BODY2_REV05 — Architecture Integration](../development-log/body2-rev05-architecture-integration.md)
- [Revision History](../development-log/revision-history.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
