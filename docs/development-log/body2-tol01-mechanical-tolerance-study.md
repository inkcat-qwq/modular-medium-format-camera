# BODY2_TOL01 — Mechanical Tolerance and Repeatability Study

> **Status:** SIMULATION / SENSITIVITY STUDY  
> **Development stage:** Pre-prototype  
> **Validation:** Assumed-input Monte Carlo and analytical geometry  
> **Date:** September 2026

BODY2_TOL01 studies how mechanical variation may propagate through the removable front-module, structural core, rear adapter, and digital-back chain.

This public document is a sanitized summary. Detailed tolerance values, coordinates, interface dimensions, sample distributions, and internal result tables remain outside the public repository.

---

## Purpose

The study was created to answer a limited engineering question:

> If the current modular architecture is subjected to plausible but still unverified mechanical variation, which parts of the interface chain appear most sensitive, and which assumptions most urgently require physical measurement?

It is therefore an **error-budget and sensitivity study**, not a manufacturing-yield prediction.

The study does not establish:

- production capability
- real assembly repeatability
- infinity-focus acceptance
- image-quality acceptance
- a released GD&T scheme
- a physically verified camera interface

---

## Error Chain

The study models an axial error chain spanning the front and rear interfaces.

At a high level, the modeled contributors include:

- core / body reference variation
- front support and module seating variation
- adapter and rear-seat variation
- digital-back seating uncertainty
- focusing-position / mechanism variation
- removal and reinstallation effects

Relative plane tilt is tracked separately from the central axial budget.

The current model intentionally does **not** treat unknown nominal geometry as known zero error.

Where real geometry or interface responsibilities remain unknown, those quantities remain unresolved rather than being filled with convenient nominal values.

---

## What the Study Demonstrated

Several useful qualitative conclusions emerged.

### Calibration can remove a static central bias, but not the whole problem

A modeled central axial calibration can greatly reduce the same-assembly central error under the assumptions used in the study.

However, that compensation does not automatically remove:

- relative tilt
- backlash / approach-direction effects
- removal and reinstallation variation
- unknown nominal interface offsets
- unmodeled rotational / Abbe effects

The study therefore treats calibration as one tool inside the interface architecture, not as a substitute for repeatable mechanics.

### Reinstallation remains a separate problem

The same manufactured parts can return to a different state after removable interfaces are disturbed.

This makes removal / reinstallation behavior a first-class requirement rather than a secondary assembly detail.

### Rear support geometry needs a clearer physical definition

A multi-point rear seating arrangement does not automatically form one rigid plane.

The study therefore compares conditional support models instead of assuming perfect simultaneous contact.

Real conclusions require:

- contact stiffness
- preload
- seating sequence
- surface condition
- repeatability measurements

### Locating and clamping responsibilities remain important

The study reinforces the project principle that positioning, seating, and clamping should not be treated as interchangeable functions.

Clear XY location and axial seating responsibilities are especially important at removable interfaces.

### Long mechanical lever arms can magnify small guide errors

Guide / bushing clearance can produce larger displacement at a remote reference surface.

This does not by itself prove that the existing mechanism is unacceptable, but it identifies another area where real geometry, loading, and constraint definition matter.

---

## Statistical Interpretation

The study uses assumed bounded input distributions to explore sensitivity.

Alternative distribution shapes and selected correlation assumptions were also compared.

The important public conclusion is:

> The numerical ranking depends strongly on the assumed input model.

For that reason:

- percentile results are not worst-case limits
- simulated percentiles are not production yield
- sample maxima are not guaranteed physical maxima
- correlation assumptions are not measured manufacturing correlation
- changing the assumed distribution can change the apparent sensitivity ordering

The analysis is therefore useful for deciding what to measure next, not for declaring process capability.

---

## Model Boundaries

The study includes analytical and Monte Carlo treatment of selected axial, tilt, locating, seating, and guide-clearance effects.

It does not yet provide a complete six-degree-of-freedom assembly solution.

Important omitted or conditional items include:

- complete 3D contact and collision behavior
- real GD&T verification
- elastic fastener and interface deformation
- loading and gravity effects
- thermal behavior
- wear and durability
- full guide-system constraint behavior
- real optical conjugates and imaging performance
- validated lens-to-sensor focus criteria
- real digital-back seating measurements
- some conditional Abbe / rotational coupling terms

These omissions are intentional and documented.

---

## Current Engineering Interpretation

The strongest outcome of BODY2_TOL01 is not a specific tolerance number.

It is the identification of several interface responsibilities that must be physically resolved before a real tolerance budget can become credible.

The highest-priority areas are:

- rear-adapter XY positioning
- rear seating / support definition
- removable-module repeatability
- a measurable front-to-rear datum chain
- real guide and mechanism behavior
- real digital-back seating geometry

The correct next step is therefore **measurement**, not simply tightening every assumed tolerance.

---

## Next Gate

A future tolerance revision should replace assumed inputs with measured or supplier-backed evidence.

Priority work includes:

- define the real rear positioning and seating architecture
- establish measurable reference datums
- measure removal / reinstallation repeatability
- measure real contact and seating variation
- characterize guide / mechanism behavior
- connect mechanical displacement to an explicit optical acceptance model only after the geometry is physically defined

Only then should the project consider a manufacturing-oriented tolerance budget.

---

## Related Documents

- [DD-002 — Separate Positioning, Seating, and Clamping Functions](../design-decisions/DD-002-separate-positioning-seating-clamping.md)
- [Current Project State](../overview/current-state.md)
- [Subsystem Status Matrix](../overview/subsystem-status.md)
- [System Architecture Overview](../architecture/system-overview.md)
- [BODY2_REV05 — Architecture Integration](body2-rev05-architecture-integration.md)
- [Revision History](revision-history.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
