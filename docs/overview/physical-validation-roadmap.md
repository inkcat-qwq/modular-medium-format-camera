# Physical Validation Roadmap

> **Project stage:** Pre-prototype / Simulation  
> **Roadmap type:** Evidence-gathering and validation sequence  
> **Scope:** Publicly documented next-step work  
> **Last updated:** September 2026

This roadmap describes the physical evidence needed to move the Modular Medium Format Camera project from architecture and simulation toward increasingly credible subsystem validation.

It is **not** a project schedule, manufacturing release, procurement plan, or commitment to a particular supplier, component, or final mechanism.

The public repository may intentionally lag behind private internal development. Exact private dimensions, forces, coordinates, optical prescriptions, electrical pin budgets, and detailed tolerance values are intentionally omitted here.

---

## Roadmap Principle

The next stage should reduce uncertainty before adding complexity.

The preferred order is:

1. establish real physical reference data
2. validate removable-interface behavior
3. validate optical / ergonomic principles
4. validate front-module mechanics
5. validate electrical and synchronization boundaries
6. feed measured evidence back into the system baseline
7. only then consider a new integrated body revision

A successful test should close a clearly defined question. A failed test should still be preserved if it narrows the design space.

---

## 1. Digital-Back Mechanical Interface

**Current evidence:**  
The rear interface has a defined architectural role, but the real digital-back seating geometry, locking behavior, installation path, and physical clearances are not yet fully established.

**Unresolved question:**  
What geometry actually determines the digital back's position and imaging relationship when installed on the camera?

**Minimum physical evidence needed:**

- measured seating and contact references
- documented installed orientation
- observed locking / retention behavior
- installation and removal path
- relevant local protrusions and operating clearances
- repeatable reference for the imaging-plane relationship

**Exit criterion:**  
The project can describe the rear interface using measured physical references rather than placeholder or inferred geometry, with remaining unknowns explicitly separated.

---

## 2. Rear-Interface Repeatability and Datum Chain

**Current evidence:**  
BODY2_TOL01 shows that locating, seating, calibration, and removal / reinstallation behavior can materially affect the mechanical error chain, but its inputs remain largely assumed.

**Unresolved question:**  
Does the removable rear interface return to a sufficiently repeatable mechanical state, and which physical features actually control that state?

**Minimum physical evidence needed:**

- repeated install / remove / reinstall measurements
- measurable XY positioning reference
- measurable axial seating reference
- support / contact behavior under normal retention
- variation across repeated cycles
- a traceable front-to-rear datum chain

**Exit criterion:**  
Repeatability is described by measured distributions tied to real datums and contact features, allowing the assumed-input tolerance model to be replaced or revised.

---

## 3. Right-Eye, Face-Clearance, and Real Packaging

**Current evidence:**  
The direct-view finder architecture and several packaging studies use assumed eye and face references. These are useful for screening but do not demonstrate real ergonomic clearance.

**Unresolved question:**  
Can the intended right-eye viewing position coexist with the real camera body, digital back, controls, and removable optical modules?

**Minimum physical evidence needed:**

- real viewing posture and eye-position observations
- brow / nose / cheek clearance checks
- digital-back access checks
- battery / control access where relevant
- finder service / removal clearance
- representative hand and operating postures

**Exit criterion:**  
A documented viewing and operating envelope exists using real physical observations, and no critical hard interference remains in the intended use posture.

---

## 4. Direct-View Finder and Fixed-Brightline Bench

**Current evidence:**  
The direct-view finder is a retained simulation candidate. VF13 identifies a fixed optical brightline as the preferred first framing-information principle test.

**Unresolved question:**  
Can the direct scene and fixed frameline be viewed together with acceptable visibility, focus impression, eye-position tolerance, and manageable stray reflections?

**Minimum physical evidence needed:**

- direct-view optical bench or representative prototype
- fixed-brightline visibility check
- frameline focus / apparent-distance check
- intended eye-position sweep
- full-frame visibility check
- brightness / contrast observations
- ghost and stray-reflection observations
- alignment / re-alignment demonstration

**Exit criterion:**  
The fixed-brightline concept is physically demonstrated across the intended viewing region, with known failure modes and a credible alignment / service strategy.

Dynamic frameline correction should remain deferred unless this simpler architecture proves physically viable.

---

## 5. Front-Module Clamp, Safety, and Serviceability

**Current evidence:**  
FM2_CLOSURE03 integrated holding, retention, preload, safety, service, and lens-envelope concepts but remained on HOLD because digital closure was not achieved.

**Unresolved question:**  
Can the front module be retained, released, adjusted, and serviced safely without hidden interference, loose-part risk, or dependence on unverified elastic behavior?

**Minimum physical evidence needed:**

- representative clamp / retention prototype
- preload / release behavior
- positive safety sequence
- captured-part behavior
- repeated opening / closing cycles
- tool and finger access
- module removal / installation sequence
- observed wear or instability during repeated use

**Exit criterion:**  
A physical mechanism demonstrates a complete service sequence with no unresolved hard interference, no uncontrolled loose-part path, and repeatable retention behavior suitable for continued integration work.

---

## 6. Real Lens Envelope and Control Motion

**Current evidence:**  
Digital lens-envelope studies identified conflicts and showed that nominal barrel diameter alone is not enough to define compatibility.

**Unresolved question:**  
What real geometric and operational envelope must the front-module architecture support for the intended first lens or lens family?

**Minimum physical evidence needed:**

- measured external lens geometry
- actual mounting / register references
- focus travel
- shutter / aperture / release-control protrusions where applicable
- control-motion paths
- rear-element and internal-clearance information
- representative service and handling access

**Exit criterion:**  
At least one real lens configuration can be described by a measured compatibility envelope that can be checked against the front-module and finder architecture.

The project should avoid claiming universal lens compatibility from this milestone.

---

## 7. Power, Contacts, Harness, and Protection

**Current evidence:**  
SYS_POWER01 and SYS_IO01 define architectural responsibilities and software-simulated failure behavior, but no released electrical hardware exists.

**Unresolved question:**  
Can the camera's modular electrical interfaces operate safely and predictably with real contacts, wiring, loads, and power transitions?

**Minimum physical evidence needed:**

- representative contact / connector hardware
- real continuity and insertion / removal behavior
- measured subsystem loads
- power-up / power-down behavior
- fault-current / protection observations
- contact-misalignment or partial-engagement checks
- basic harness routing and serviceability
- thermal observations under representative use

Where relevant, later testing should also cover ESD / EMC and durability.

**Exit criterion:**  
A representative low-voltage hardware chain demonstrates stable power and data behavior under normal use and defined fault cases without relying solely on software assumptions.

---

## 8. Digital-Back Synchronization Boundary

**Current evidence:**  
The electronics architecture treats digital-back synchronization as an external interface boundary. Current software models do not prove a real protocol or electrical implementation.

**Unresolved question:**  
What external readiness, wake, synchronization, or exposure-completion behavior is actually available and safe to use with the real digital back?

**Minimum physical evidence needed:**

- authoritative interface documentation where available
- non-destructive observation of real synchronization behavior
- timing observations
- clear separation between proven signals and assumed software events
- defined behavior for unavailable / invalid / timeout conditions
- isolation or protection evidence where an electrical interface is used

**Exit criterion:**  
The project has a documented, physically observed synchronization boundary that can be represented in the system interface baseline without inventing unsupported signals or timing guarantees.

---

## Integration Gate After Physical Evidence

The roadmap does not end when individual bench tests pass.

Measured results should be fed back into:

- system interface control
- calibration ownership
- mechanical tolerance models
- body packaging
- service architecture
- electronics responsibilities

A later integrated body revision should be considered only when the evidence is strong enough to replace major placeholder assumptions in several subsystems at once.

At minimum, a new integration gate should require:

- measured digital-back references
- measured rear-interface repeatability
- a physically demonstrated direct-view / frameline path
- a physically credible front-module retention concept
- at least one measured lens envelope
- a defined power / contact strategy
- a physically supported synchronization boundary

Passing one workstream does not automatically validate the full camera.

---

## What This Roadmap Does Not Authorize

This document does not authorize:

- production
- manufacturing drawings
- procurement
- public release of private engineering source
- final optical prescriptions
- final connector / pinout selection
- final battery or power architecture
- final lens compatibility claims
- final digital-back compatibility claims
- safety certification
- commercial use claims

---

## Related Documents

- [Current Project State](current-state.md)
- [Subsystem Status Matrix](subsystem-status.md)
- [System Architecture Overview](../architecture/system-overview.md)
- [Electronics & Control Architecture](../architecture/electronics-control-overview.md)
- [BODY2_TOL01 — Mechanical Tolerance and Repeatability Study](../development-log/body2-tol01-mechanical-tolerance-study.md)
- [FM2_CLOSURE03 — Digital Closure Review](../development-log/fm2-closure03-digital-closure-review.md)
- [VF13_FRAME_ARCH01 — Frameline Architecture Study](../development-log/vf13-frameline-architecture.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
