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

### Front Module / Closure

**Status:** HOLD / DEVELOPMENT STUDY

Front-module architecture has progressed through integrated closure, retention, preload, safety, and lens-envelope studies.

The latest published integration study did not achieve digital closure. Several mechanical and service-path conflicts remain unresolved, so the front-module mechanism is intentionally held before any release or body-revision promotion.

Further progress requires targeted physical or supplier-backed evidence rather than additional parameter tuning alone.

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

A direct optical viewfinder architecture remains the primary publicly documented viewing direction.

Current work now includes two distinct layers:

- the retained direct-view optical finder
- a staged frameline / cue architecture study

A fixed optical frameline path has been retained for independent principle validation, while dynamic correction and more complex electronic framing remain later-stage options.

The combined finder and frameline system has not yet been physically bench-validated.

### Tolerance Analysis

**Status:** SIMULATION / SENSITIVITY STUDY

BODY2_TOL01 now provides a reproducible assumed-input Monte Carlo and analytical study of the front-module, core, rear-adapter, and digital-back error chain.

The study is useful for identifying sensitive interface responsibilities, calibration limits, seating assumptions, and removal / reinstallation effects.

It does not provide real manufacturing yield, a released GD&T scheme, or optical focus acceptance. The next step is to replace assumed inputs with measured mechanical evidence.

### Electronics / System Control

**Status:** ARCHITECTURE / SOFTWARE SIMULATION

Control, communication, power, I/O, user-interface, and interface-control studies have now been developed as coordinated system-level architecture tracks.

Executable software models are being used to evaluate states, degraded modes, power behavior, interconnect responsibilities, and user flows.

No PCB, connector, bus standard, battery system, or digital-back protocol is frozen, and no system electronics have yet been physically validated.

## Major Open Questions

- final rear-interface geometry
- locking and clamping mechanism
- manufacturing repeatability
- direct-view and frameline physical eye-box performance
- real frameline / combiner optical behavior
- front-module closure, retention, and real-lens compatibility
- digital-back synchronization and electrical boundary
- real power, contact, and harness behavior
- environmental sealing
- physical prototype validation

## Next Development Gate

The next major goal is to move selected simulated subsystems toward physical interface and bench validation.

Priority validation areas include:

- digital-back mechanical and synchronization evidence
- direct-view finder and fixed-frameline bench testing
- real eye-position and packaging checks
- front-module / closure physical validation
- real power, contact, and interconnect tests

See the [Physical Validation Roadmap](physical-validation-roadmap.md) for the public evidence sequence and exit criteria.

---

This document describes the current development state only.

Values and architectures described throughout the repository should not be considered manufacturing specifications unless explicitly marked `FROZEN` or `VALIDATED`.


## Related Documents

- [Subsystem Status Matrix](subsystem-status.md)
- [Physical Validation Roadmap](physical-validation-roadmap.md)
- [System Architecture Overview](../architecture/system-overview.md)
- [Electronics & Control Architecture](../architecture/electronics-control-overview.md)
- [VF13_FRAME_ARCH01 — Frameline Architecture Study](../development-log/vf13-frameline-architecture.md)
- [BODY2_REV05 — Architecture Integration](../development-log/body2-rev05-architecture-integration.md)
- [BODY2_TOL01 — Mechanical Tolerance and Repeatability Study](../development-log/body2-tol01-mechanical-tolerance-study.md)
- [FM2_CLOSURE03 — Digital Closure Review](../development-log/fm2-closure03-digital-closure-review.md)
- [Revision History](../development-log/revision-history.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
