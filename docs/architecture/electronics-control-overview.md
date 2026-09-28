# Electronics and Control Architecture Overview

> **Current phase:** P1 Functional Prototype Development  
> **Status:** Implementation required; historical software models retained  
> **Hardware validation:** Not yet completed  
> **Updated:** 2026-09-28

P1 electronics must support BODY3, K3 / ACT-E, H2, the moving universal iris, one reference Optical Insert, D3 assistance and DM22 synchronization. SYS_ELEC01, SYS_POWER01, SYS_IO01, SYS_UI01 and SYS_ICD01 remain useful development history. Their old BODY2 / FM-C / Copal assumptions and load budgets do not define the current hardware.

## Responsibilities

| Domain | Intended responsibility | Evidence still required |
| --- | --- | --- |
| Body supervision | Coordinate preparation, calibration validity, user input, exposure transaction and faults | Real controller, timing, fault handling and interconnects |
| Shutter local control | ACT-E trajectories, direct curtain-bar position, independent endpoint checks and closing states | Drive / sensor hardware, actual motion, safe stopping and closing |
| H2 / q | Measure actual non-rotating cage position | Sensor integration, zero / direction, repeatability and calibration |
| Iris / Optical Insert | Aperture status and reference-lens identity / calibration responsibilities | Actual iris, connections and real optical profile |
| Ranging | Independent subject-distance estimate with validity and freshness | Device, target selection, environmental behavior and calibrated pairing |
| Finder assistance | Electronic frameline and three small NEAR / OK / FAR focus cues | Physical optical path, visibility and invalid-data behavior |
| Body UI | Detailed information, preparation, faults and unknown outcomes | Physical controls / display and human-factors evidence |
| DM22 boundary | Externally supported preparation / synchronization only | Real external electrical interface and observed capture behavior |

The focus comparison uses **subject distance + actual lens q + lens calibration**. Manual focusing remains the intended operation. Unknown, stale or mismatched calibration data must not become an OK cue. The optical scene remains in D3; detailed settings remain on the body display. A full HUD is not the current architecture.

## Power and closing are separate evidence gates

Normal power, shutter transient loads and safety reserve have different responsibilities. P1 may use external development power and larger boards / actuators, but actual load, isolation, regeneration, thermal behavior and fault response must still be established. Historical low-power Copal assumptions cannot be transferred to ACT-E.

**Main-power-loss controlled close:** architecture under study, relying on independently available safety energy, control and closing-state evidence. Energy calculations alone do not qualify reserve hardware or a safe power path.

**Total-energy-loss autonomous mechanical close:** **NOT CLOSED / NOT VALIDATED**. The passive mechanism remains a candidate with incomplete release / capture and unmeasured dynamic behavior. Neither a manual cover nor an external emergency supply proves autonomous closing after all usable energy is lost.

P1-01_SHUTTER_IMPL02 remains **IMPLEMENTATION HOLD — NOT READY FOR CONTROLLED BENCH PLANNING**. No circuit, pinout, reserve specification, safety-mechanism geometry or hardware wiring guide is released here.

## Exposure and digital-back boundary

The target sequence is optical viewing, range-assisted manual focus, iris setting, preparation, a fresh release request, exposure, controlled close, actual DM22 storage confirmation and light-safe reset. This is a validation objective, not a completed capture record.

DM22 retains independent power, processing and storage. Body control is not assumed to read RAW files or have an automatic write-complete signal. Shutter closed, synchronization observed and image saved are different facts; storage confirmation may require user observation on the back. Fault or ambiguous outcome must not cause an automatic retry.

## Interfaces and calibration

Positioning and load-bearing remain mechanical responsibilities; contacts and software identity do not establish optical registration. P1 requires traceable pairing of the body, adapter / back and real reference lens, with q and range data validity kept explicit. Unknown geometry or signals remain TBD rather than being interpreted as zero or success.

MCUs, PCBs, buses, harnesses, connectors, the integrated battery system and the real DM22 synchronization interface are not frozen. Local component candidates in IMPL02 do not constitute a released system BOM. Protection, hardware timing, ESD / EMC, connector durability, thermal behavior and control ergonomics remain physical evidence needs.

Source basis: CAMERA_P1_BASELINE01 requirements / system baseline and P1-01_SHUTTER_IMPL02 safety-power / sensing reviews. The P1 system baseline takes precedence over conflicting historical SYS interface assumptions.

- [System architecture](system-overview.md)
- [Subsystem status](../overview/subsystem-status.md)
- [Evidence roadmap](../overview/physical-validation-roadmap.md)
- [Shutter development](../development-log/shutter-architecture-development.md)
- [SYS historical milestones](../development-log/revision-history.md#electronics-and-system-integration)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
