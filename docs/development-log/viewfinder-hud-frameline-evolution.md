# Viewfinder, HUD, and Frameline Evolution

> **Document type:** Development history  
> **Scope:** Publicly documented viewfinder-information architecture  
> **Development stage:** Pre-prototype / Simulation  
> **Date:** September 2026

This document summarizes the transition from the retained direct-view finder architecture through several HUD integration studies and into the current staged frameline / cue direction.

It is a sanitized public history. Detailed optical prescriptions, dimensions, tolerance distributions, packaging coordinates, and internal numerical results remain outside the public repository.

---

## Starting Point — Direct-View Finder

The project first converged on a direct optical finder as the main scene-viewing architecture.

That decision separated the essential viewing path from optional framing and information overlays.

The direct-view scene therefore became the baseline that later information-display concepts had to preserve rather than replace.

---

## VF10_D3_ENGINEERING01 — Retain D3, Delay HUD

**Public status:** RETAINED MILESTONE

VF10 subjected the retained D3 direct-view candidate to deeper engineering review.

The important architectural result was not a completed HUD.

Instead, the study concluded that the D3 scene-viewing path remained worth continuing while HUD integration should be delayed.

VF10 identified two different classes of risk:

- optical / manufacturing sensitivity within the D3 assembly
- packaging and integration risk introduced by adding a combiner and HUD branch

A thin combiner concept did not, by itself, invalidate the D3 scene path, but the complete HUD branch still lacked a credible mechanical and ergonomic integration.

The public takeaway from VF10 is therefore:

> **Keep the direct-view finder; do not make HUD completion a prerequisite for the next body architecture.**

---

## VF11_HUD_PACK01 — Independent HUD Packaging Remains on HOLD

**Public status:** HOLD / DEVELOPMENT STUDY

VF11 explored whether a more compact independent HUD branch could be packaged around the retained D3 finder.

Several injection / folding topologies were compared.

The study showed that shortening the nominal projector optics did not solve the central problem.

The real difficulty was the coupling between:

- injection direction
- wide field coverage
- eye-position range
- projector aperture
- physical hardware volume
- face and camera-body clearance

One folded architecture remained the most useful direction for further study because it could move the source hardware in a more favorable direction, but the tested geometry still interfered with the scene path, optical hardware, or face-reference space.

No candidate provided a credible released HUD volume for the camera body.

The correct outcome was therefore to retain the evidence and keep HUD packaging on HOLD.

---

## VF12_SHARED_HUD01 — Shared-Aperture Architecture Also Remains on HOLD

**Public status:** HOLD / DEVELOPMENT STUDY

VF12 tested a different premise:

Instead of treating the HUD as a largely independent branch, could more of the existing viewfinder optical path be shared?

The study demonstrated that shared optical transfer was mathematically possible.

However, moving the injection point did not eliminate the system-level packaging problem.

The bottleneck shifted toward:

- the aperture required by the wide scene field
- available space around the existing finder optics
- compatibility with the camera body and digital-back region
- output-wavefront consistency
- physical projector implementation

The more compact diagnostic cases did not become valid camera-level candidates, while the configurations that preserved more of the required field became too difficult to package credibly.

VF12 therefore did not release a HUD interface for the next camera revision.

Its most important engineering contribution was to show that **sharing the optical path did not automatically make a full-field HUD compact or practical**.

---

## Architecture Reframing

VF10, VF11, and VF12 progressively changed the question.

The project moved away from:

> “How do we fit a full HUD into the existing finder?”

toward:

> “What is the minimum framing information actually required, and which parts truly need electronics?”

This reframing separated three functions that had previously been coupled:

1. direct scene viewing
2. visible framing boundaries
3. optional status or correction cues

That separation created the basis for VF13.

---

## VF13_FRAME_ARCH01 — Staged Frameline / Cue Architecture

**Public status:** RETAINED MILESTONE / PRINCIPLE-VALIDATION CANDIDATE

VF13 compared:

- fixed optical framelines
- later movable or profile-selectable framelines
- small local electronic cue regions

The retained public direction is staged.

The first physical experiment should focus on a fixed optical brightline system.

Small directional or status cues may be added later.

Dynamic correction remains a later-generation option only if physical validation shows that the added complexity is justified.

This direction preserves the direct optical scene while reducing the amount of information that must be carried by an active electronic optical branch.

---

## Development Chain

```text
VF9_DIRECT01 / D3
  ↓
Direct-view scene architecture retained
  ↓
VF10_D3_ENGINEERING01
  ↓
GO D3 — HUD deferred
  ↓
VF11_HUD_PACK01
  ↓
Independent HUD packaging HOLD
  ↓
VF12_SHARED_HUD01
  ↓
Shared-aperture HUD HOLD
  ↓
Architecture scope reduced
  ↓
VF13_FRAME_ARCH01
  ↓
Fixed brightline first
  ↓
Small cues later
  ↓
Dynamic frameline correction only if justified
```

---

## Current Interpretation

The repeated HUD holds should not be interpreted as failed work with no result.

They established several important project boundaries:

- the direct optical scene path should remain independent of optional display complexity
- reducing focal length alone does not solve wide-field HUD packaging
- sharing existing optics does not automatically produce a compact full-field HUD
- eye-box, aperture, packaging, and human-clearance requirements must be considered together
- optional electronic information should be added only where it provides enough value to justify its optical and mechanical cost

The current frameline direction is therefore not a disconnected new idea.

It is the direct result of progressively reducing the scope of the information-overlay problem after earlier architectures exposed their system-level costs.

---

## Next Gate

The next public validation gate is an independent fixed-brightline principle prototype.

The experiment should answer basic physical questions before any return to complex HUD development:

- Can the full frameline be seen comfortably across the intended eye positions?
- Does the frameline appear at an acceptable visual focus?
- Are brightness and contrast usable?
- Are ghosting and stray reflections manageable?
- Can the frameline module be aligned and serviced without disturbing the direct-view finder?

Only after those questions are answered should more complex movable or electronic framing architectures be reconsidered.

---

## Related Documents

- [VF13_FRAME_ARCH01 — Frameline Architecture Study](vf13-frameline-architecture.md)
- [System Architecture Overview](../architecture/system-overview.md)
- [Current Project State](../overview/current-state.md)
- [Subsystem Status Matrix](../overview/subsystem-status.md)
- [Revision History](revision-history.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
