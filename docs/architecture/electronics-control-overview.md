# Electronics and Control Architecture Overview

> **Status:** ARCHITECTURE / SOFTWARE SIMULATION  
> **Development stage:** Pre-prototype  
> **Hardware validation:** Not yet performed  
> **Last updated:** September 2026

This document summarizes the currently published electronics, control, power, user-interface, and interconnect architecture of the Modular Medium Format Camera project.

The work described here is architectural and software-simulated. It does not represent a released PCB, connector standard, wiring harness, battery design, or digital-back protocol.

---

## Scope

The electronics work is intended to support the modular mechanical platform without making the camera dependent on one permanently integrated electronic architecture.

Current studies cover:

- body control responsibilities
- module identity and calibration ownership
- user controls and status presentation
- exposure coordination
- power and protection architecture
- modular interconnect responsibilities
- system-interface control

---

## Control and Communication

The body-level controller is currently modeled as responsible for:

- discovering and identifying attached modules
- validating calibration state
- evaluating focus-position validity
- managing user input
- coordinating exposure-related states
- issuing display or frameline requests
- entering defined degraded modes when information is invalid

The body is not intended to perform digital-back image processing.

Communication links remain architectural candidates. No final bus, connector, pinout, MCU, or physical signaling standard has been selected.

---

## Digital-Back Boundary

The digital back remains a separately powered subsystem.

The camera body may eventually coordinate selected synchronization or readiness functions, but the real electrical boundary has not yet been validated.

The current public architecture therefore treats back communication and synchronization as an interface problem rather than an implemented feature.

No public document should be interpreted as a wiring guide for a specific back.

---

## Power Architecture

Power studies have been used to compare relative load classes, operating states, future actuator reservations, and protection behavior.

These studies are useful for architecture sizing, but they do not define:

- a battery chemistry
- battery capacity
- rail voltages
- regulator selection
- charging architecture
- final thermal behavior
- actual measured runtime

The current mechanical design should therefore preserve serviceable space for logic, protection, and power functions without freezing exact hardware envelopes.

---

## Interconnect Architecture

The interconnect study separates several functional interface classes rather than forcing all modules onto one universal connector.

The current principles include:

- removable serviceable contact structures where practical
- protection boundaries between subsystems
- separate treatment of power and data responsibilities
- controlled behavior during module insertion and removal
- isolation of future actuator loads from sensitive sensing or logic paths
- maintenance access that does not disturb precision mechanical datums

Final connector geometry, conductor count, pin sequence, cable construction, and EMC strategy remain unresolved.

---

## User Interface

A compact physical-control approach is currently being studied.

The public design intent is to keep core operation understandable even when optional electronic features are unavailable.

The retained principles include:

- mechanical camera functions should remain distinct from software-only state
- invalid or unavailable information should be shown as unavailable rather than silently substituted
- exposure coordination should fail safe rather than trigger a delayed or ambiguous capture
- external status presentation should remain simple
- finder electronics should supplement, not replace, the direct optical scene

No industrial-design control layout, button geometry, screen opening, or display technology is frozen.

---

## System Interface Baseline

A system-level interface-control baseline has now been established internally to coordinate:

- mechanical responsibilities
- optical responsibilities
- electrical responsibilities
- calibration ownership
- module state and data ownership

The baseline is primarily a consistency and traceability tool.

It does not represent a design freeze, and no system hardware requirement is currently considered physically verified.

---

## Validation Level

Current evidence includes:

- executable software state models
- fault and degraded-mode scenarios
- power and energy models
- interconnect fault models
- user-flow simulations
- interface-control and traceability documents

Physical validation has not yet covered:

- real digital-back synchronization
- real harnesses or contacts
- EMC / ESD behavior
- short-circuit tolerance
- battery and regulator behavior
- thermal performance
- control ergonomics
- hardware timing
- connector durability

---

## Current Direction

Electronics are now a defined parallel architecture track rather than a purely future placeholder.

However, the mechanical and optical platform remains the primary physical-validation focus.

The current development strategy is therefore:

1. maintain clear electronic subsystem responsibilities
2. keep hardware choices replaceable
3. validate real external interfaces before freezing electronics
4. avoid allowing unverified electronics assumptions to drive precision mechanical geometry

---

## Related Documents

- [System Architecture Overview](system-overview.md)
- [Current Project State](../overview/current-state.md)
- [VF13_FRAME_ARCH01 — Frameline Architecture Study](../development-log/vf13-frameline-architecture.md)
- [Revision History](../development-log/revision-history.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
