# Subsystem Status Matrix

> **Current phase:** P1 Functional Prototype Development  
> **Updated:** 2026-09-28  
> **Overall evidence:** No complete physical camera verification or manufacturing release.

The system baseline is CAMERA_P1_BASELINE01. The latest applicable shutter update is P1-01_SHUTTER_IMPL02, retaining K3 flexible dual curtains and ACT-E direct closed-loop electric drive. A status denotes the next evidence need, not permission to manufacture or begin a bench test.

| Subsystem | Current status | Latest milestone / applicable basis | Validation level | Next gate |
| --- | --- | --- | --- | --- |
| BODY3 | READY_FOR_DETAIL | BODY3_FRAME01 → COMPACT01 → P1 baseline | Digital structural / host evidence; strength and joints unverified | P1-01 implementation effects, joints, process and datum retention |
| Rear Interface | REAL_DATA_REQUIRED | COMPACT01 / P1 baseline | Core-side adapter candidates; actual back interface open | P1-04 measured seating, locking, safe removal and reinstall repeatability |
| P1 Shutter | IMPLEMENTATION HOLD | P1-01_SHUTTER_IMPL02 | CAD and model studies; remaining interferences / service gaps | P1-01 drive, direct bar sensing, controlled close and assembly closure; NOT READY FOR CONTROLLED BENCH PLANNING |
| FOCUS-H2 | DETAIL_REQUIRED | COMPACT01 / P1 baseline | Structural / motion-envelope candidate; no working focusing mechanism | P1-02 actual motion pair, support, anti-rotation, retention and backlash evidence |
| Direct q Measurement | DETAIL_REQUIRED | P1 baseline | Actual cage-position measurement requirement; hardware / calibration open | P1-02 sensing integration; P1-05 calibrated data validity |
| Universal Iris | DETAIL_REQUIRED | GEN1 concept → P1 baseline | Moving aperture concept; blades / actuation / feedback incomplete | P1-03 actual mechanism, aperture behavior and service connections |
| Optical Insert | REAL_DATA_REQUIRED | COMPACT01 / P1 baseline | One reference-lens placeholder and retention candidates | P1-03 real lens / stop relationship, datums, locking and repeatability |
| D3 Finder | BENCH_REQUIRED | VF9 / VF10 history → P1 baseline | Direct-view candidate; historical optical configurations are not interchangeable measurements | Consistent optical configuration, alignment and physical viewing evidence |
| Frameline / Focus Cues | BENCH_REQUIRED | P1 baseline; VF13 historical principle reference | Electronic frameline and NEAR / OK / FAR concept; physical visibility unverified | P1-05 low-complexity optical implementation, eye-position and invalid-data behavior |
| Electronic Ranging | BENCH_REQUIRED | P1 baseline | Independent ranging responsibility; actual device / performance not established | P1-05 distance, target selection, validity / freshness and lens-profile pairing |
| DM22 Registration / Sync | REAL_DATA_REQUIRED | P1 baseline | Real mount / register / lock / electrical synchronization open | P1-04 measured registration, external sync and actual saved-image confirmation |
| Electronics | DETAIL_REQUIRED | P1 baseline; SYS studies retained as history | Functional responsibilities / older software models; physical hardware open | P1-05 controllers, harness, protection, faults and exposure transaction |
| Power | BLOCKED | P1 baseline + IMPL02 safety-power review | Main / reserve / loss-of-energy architectures under study | P1-01 load and safe-power boundary; P1-05 integrated power evidence |
| UI | READY_FOR_DETAIL | P1 baseline; SYS_UI01 historical | Control / transaction concepts; no physical usability validation | P1-05 body display, fresh release, fault / UNKNOWN behavior |
| System ICD | DETAIL_REQUIRED | P1 baseline supersedes conflicting SYS_ICD01 assumptions | Responsibility / calibration baseline; no hardware or interface freeze | Reconcile P1 interfaces with measured evidence before P1-06 integration |
| Portability / Lightweight Product Study | DEFERRED_PRODUCT_OPTIMIZATION | COMPACT01 gate reclassified by P1 baseline | Mass / envelope scenarios; no lightweight product validation | Post-P1 lightweight product redesign; no GEN1-L CAD |
| FM2 / FM-C and Copal front architecture | SUPERSEDED / HISTORICAL HOLD | FM2_CLOSURE03; replaced by BODY3 / H2 direction | Historical failed-to-close candidate | No active P1 front-development gate; retain as history |

## Status meaning

- **READY_FOR_DETAIL:** a direction or host exists for further detail; physical verification is still required.
- **DETAIL_REQUIRED:** an actual mechanism, connection or implementation remains incomplete.
- **REAL_DATA_REQUIRED:** real interface, lens or component evidence is decisive.
- **BENCH_REQUIRED:** physical evidence is needed; this label does not authorize a test now.
- **BLOCKED / IMPLEMENTATION HOLD:** unresolved implementation, safety or assembly conditions prevent release.
- **DEFERRED_PRODUCT_OPTIMIZATION:** a future product objective, excluded from P1 weight / packaging gates but not declared solved.
- **SUPERSEDED / HISTORICAL HOLD:** preserved evidence from a former mainline, not an active P1 subsystem.

Main-power-loss controlled close remains under study. **Total-energy-loss autonomous mechanical close is NOT CLOSED / NOT VALIDATED.** Larger P1 hardware or external power does not change that conclusion.

- [Current state](current-state.md)
- [System architecture](../architecture/system-overview.md)
- [Physical validation roadmap](physical-validation-roadmap.md)
- [Revision history](../development-log/revision-history.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
