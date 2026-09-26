# Subsystem Status Matrix

> **Project stage:** Pre-prototype / Simulation  
> **Scope:** Publicly documented status only  
> **Last updated:** September 2026

This page provides a compact view of the current public development state of the Modular Medium Format Camera project.

The public repository may intentionally lag behind private internal work. A status such as `CANDIDATE`, `DEVELOPMENT STUDY`, or `HOLD` describes the published evidence level, not manufacturing readiness.

| Subsystem | Public status | Latest public milestone | Current validation level | Next gate |
| --- | --- | --- | --- | --- |
| Central body / structural core | **CANDIDATE / SIMULATION** | BODY2_REV05 architecture integration | CAD integration, packaging, and interface studies | Targeted structural and physical interface validation |
| Rear digital-back interface | **CANDIDATE / SIMULATION** | B2-IF01 / system interface baseline | Interface architecture and tolerance studies | Real seating, locking, installation-path, and repeatability evidence |
| Front module / closure | **HOLD / DEVELOPMENT STUDY** | FM2_CLOSURE03 | Integrated CAD review and analytical checks | Real lens geometry, physical clamp / safety evidence, and measured mechanical inputs |
| Direct optical viewfinder | **CANDIDATE / SIMULATION** | VF9_DIRECT01 / retained D3 path | Optical simulation, packaging, and architecture studies | Physical optical bench and real eye-position validation |
| Frameline / cue subsystem | **PRINCIPLE-VALIDATION CANDIDATE / SIMULATION** | VF13_FRAME_ARCH01 | Numerical architecture, registration, and optical-boundary studies | Independent fixed-brightline principle prototype |
| Mechanical datum / repeatability | **CANDIDATE / SIMULATION** | TOL01 | Tolerance and reinstallation simulation | Physical datum and repeated-removal measurements |
| Control / communication | **DEVELOPMENT STUDY** | SYS_ELEC01 | Executable software state and degraded-mode models | Validate real external synchronization and module electrical boundaries |
| Power / protection | **DEVELOPMENT STUDY** | SYS_POWER01 | Software energy, protection, and future-load studies | Measured loads, real power-path behavior, and thermal validation |
| I/O / interconnect | **DEVELOPMENT STUDY** | SYS_IO01 | Interface classification and logical fault studies | Real contacts, harnesses, protection, ESD / EMC, and durability tests |
| User interaction | **DEVELOPMENT STUDY** | SYS_UI01 | Software user-flow and failure-state scenarios | Physical control prototype and human-factors testing |
| System interface control | **RETAINED MILESTONE** | SYS_ICD01 | Cross-subsystem ownership, calibration, and traceability baseline | Update baseline with measured physical inputs; no design freeze implied |

---

## Status Interpretation

### CANDIDATE / SIMULATION

The subsystem has a retained architectural direction supported primarily by CAD, optical, tolerance, or interface simulation.

### PRINCIPLE-VALIDATION CANDIDATE / SIMULATION

The subsystem has a preferred architecture for a focused physical proof-of-principle, but the physical principle has not yet been demonstrated.

### DEVELOPMENT STUDY

The subsystem has structured analysis or executable models that help define responsibilities and trade-offs, but no released hardware implementation.

### HOLD

The current study intentionally stops before release because unresolved issues still require new evidence.

### RETAINED MILESTONE

The work establishes a durable system-level reference or development checkpoint, but does not imply a frozen or physically verified design.

---

## Cross-Subsystem Priorities

The most important next public validation gates are:

- real digital-back mechanical and synchronization evidence
- direct-view finder and fixed-frameline bench testing
- real eye-position and packaging checks
- front-module / closure physical evidence
- repeated mechanical interface measurements
- real power, contact, harness, and control-hardware tests

No subsystem in this matrix is currently production-released or manufacturing-frozen.

---

## Related Documents

- [Current Project State](current-state.md)
- [System Architecture Overview](../architecture/system-overview.md)
- [Electronics & Control Architecture](../architecture/electronics-control-overview.md)
- [BODY2_REV05 — Architecture Integration](../development-log/body2-rev05-architecture-integration.md)
- [FM2_CLOSURE03 — Digital Closure Review](../development-log/fm2-closure03-digital-closure-review.md)
- [VF13_FRAME_ARCH01 — Frameline Architecture Study](../development-log/vf13-frameline-architecture.md)
- [Revision History](../development-log/revision-history.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
