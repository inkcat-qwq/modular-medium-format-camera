# DD-002 — Separate Positioning, Seating, and Clamping Functions

> **Decision status:** ACCEPTED — Current mechanical design principle  
> **Validation status:** SIMULATION  
> **Date:** September 2026

## Context

Removable camera modules must return to a predictable position after installation, removal, and reinstallation.

This is particularly important for components that influence the imaging geometry, including:

- digital-back adapters
- sensor positioning
- front optical modules
- structural interface plates

A simple mechanical interface can use the same fasteners or surfaces to locate, seat, and clamp a component.

However, this can cause clamping forces, friction, manufacturing variation, and assembly sequence to influence the final position of the module.

For a modular camera architecture, repeatability is more important than simply holding the components together.

## Decision

Where practical, the mechanical interface architecture will treat the following functions separately:

1. **Positioning**
2. **Axial seating**
3. **Clamping**

The locating features should determine the in-plane position of a module.

The seating features should establish the primary axial reference.

The clamping mechanism should provide retention force without becoming the primary positioning mechanism.

## Positioning

Positioning features are responsible for controlling the lateral location and orientation of a module.

Their purpose is to produce repeatable alignment after repeated installation cycles.

Positioning elements should avoid unnecessary overconstraint where practical.

## Axial Seating

Axial seating establishes the reference plane between the camera core and attached module.

The seating system should provide:

- predictable contact
- stable reference geometry
- resistance to rocking
- repeatable axial position

The seating geometry should remain as independent as practical from the clamping mechanism.

## Clamping

The clamping system is primarily responsible for maintaining contact between the module and its reference surfaces.

The clamp should ideally:

- maintain sufficient preload
- avoid shifting the module during engagement
- distribute force appropriately
- avoid introducing unnecessary deformation

Clamping force should not be relied upon to correct poor positioning geometry.

## Alternatives Considered

### A. Fasteners as Both Location and Clamp

Bolts or screws could directly locate and clamp the module.

**Advantages:**

- simple construction
- low part count
- easy manufacturing

**Disadvantages:**

- clearance can affect repeatability
- tightening sequence can influence alignment
- clamp force may shift the module
- difficult to control repositioning accuracy

This approach is not preferred for precision interfaces.

### B. Fully Constrained Tight-Fit Interface

A tightly fitted interface could constrain the module through multiple closely toleranced surfaces.

**Advantages:**

- potentially high stiffness
- compact structure

**Disadvantages:**

- sensitive to manufacturing variation
- risk of overconstraint
- difficult assembly
- thermal expansion may influence fit
- wear may change positioning behavior

This approach is not currently preferred.

## Selected Direction

The preferred architecture uses intentionally defined reference features for positioning and seating, with an independent retention mechanism.

The exact geometry may change during development, but the separation of these mechanical functions should remain a guiding design principle.

## Expected Benefits

- improved reinstall repeatability
- clearer tolerance analysis
- reduced dependence on tightening sequence
- easier adapter development
- easier identification of alignment errors
- reduced risk of clamping-induced position changes

## Trade-offs

The approach also introduces additional design requirements:

- more deliberate interface geometry
- potentially greater manufacturing complexity
- tighter control of reference surfaces
- additional tolerance analysis
- wear and contamination of datum surfaces must be considered

## Current Validation

This principle has currently been evaluated through:

- interface architecture studies
- CAD development
- tolerance simulation
- repeated-removal simulation scenarios

Physical validation has not yet been completed.

## Revisit Conditions

This decision should be reconsidered if physical prototype testing shows that:

- repeatability is insufficient
- datum wear becomes excessive
- assembly becomes impractical
- clamping significantly deforms the interface
- a simpler architecture achieves equivalent repeatability

## Related Documents

- [DD-001 — Modular Camera Platform Architecture](DD-001-modular-platform-architecture.md)
- [System Architecture Overview](../architecture/system-overview.md)
- [Current Project State](../overview/current-state.md)
- [BODY2_REV05 — Architecture Integration](../development-log/body2-rev05-architecture-integration.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
