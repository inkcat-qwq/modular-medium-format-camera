# Current Project State

> **Current phase:** P1 Functional Prototype Development  
> **System status:** Functional prototype development; complete physical camera not verified  
> **Updated:** 2026-09-28

The active mainline is **P1 FUNCTIONAL PROTOTYPE**. The objective is the first camera that can complete the real shooting chain. The phase has changed from architecture / simulation toward implementation; this is not a claim that a working prototype already exists.

## Current configuration

| Active subsystem | Current direction |
| --- | --- |
| BODY3 | 645-class maximum optical architecture; fixed rear datum, modular rear adapter, D3 shoulder finder and body-mounted shutter. |
| P1-01 Shutter | K3 flexible dual-curtain + ACT-E direct closed-loop electric drive. IMPL02 is the latest applicable shutter state. |
| FOCUS-H2 | Large-diameter manual focusing with a non-rotating moving optical cage and direct actual q measurement. |
| Universal Iris | Shared aperture in the moving optical cage, moving with focus; actual mechanism still required. |
| Optical Insert | Lensboard-like replaceable optical carrier; one reference lens initially; real lens data and locking remain open. |
| D3 | Retained direct optical scene path; physical optical validation required. |
| Frameline / focus cues | Electronic frameline and three small NEAR / OK / FAR cue lights as functional requirements; no full HUD. |
| Electronic Ranging | Independent subject-distance measurement, compared with actual q and lens calibration for manual focus guidance. |
| DM22 interface | P1 back; true mounting, registration, locking and synchronization remain unverified. |
| Electronics / Power / UI | Body supervision, shutter control, power and safe-power responsibilities, range / q / iris / display integration; real hardware required. |

## Latest shutter gate

**P1-01_SHUTTER_IMPL02: IMPLEMENTATION HOLD — NOT READY FOR CONTROLLED BENCH PLANNING.**

The right-side drive arrangement is the retained P1 implementation candidate. Optical / coded direct bar sensing replaces the earlier packaging candidate, but the custom sensing arrangement is not qualified hardware. Installed-state improvements do not demonstrate a complete assembly or maintenance route.

Remaining blockers include hard interferences, incomplete assembly / bearing service, incomplete mechanical release and capture, and unverified power / reserve / sensing hardware. Main-power-loss controlled close is an architecture under study. Total-energy-loss autonomous mechanical close is **NOT CLOSED / NOT VALIDATED**. Modelled closing motion does not establish safe real closing.

## System blockers

- **Shutter / power:** drive and packaging implementation; controlled closing; main and safety power; complete assembly and maintenance paths.
- **H2 / q:** actual motion mechanism, support / retention, repeatability and direct q sensing integration.
- **Iris / Optical Insert:** actual aperture mechanism; datums, locking and reinstall repeatability; real reference-lens geometry and aperture compatibility.
- **DM22:** measured mounting datum, registration, locking, removal, synchronization and actual image-storage confirmation.
- **D3 / range / UI:** consistent physical finder configuration, electronic frameline and cue visibility, ranging behavior and calibration.
- **Electronics / body:** real hardware, fault behavior and interconnects; structural joints, service and datum preservation.

No complete prototype, working shutter, validated lens / iris, full DM22 compatibility, manufacturing readiness or production readiness is claimed.

## Function first; portability deferred

P1 prioritizes function, adjustability, repeatability, safety and serviceability. It may be heavier or thicker, use larger actuators and PCBs, external debug power, and ordinary aluminum, steel and standard parts. These allowances do not waive functional or safety gates.

COMPACT01 recovered native CAD delivery while its product portability gate remained open. CAMERA_P1_BASELINE01 reclassified weight and packaging optimization as **DEFERRED PRODUCT OPTIMIZATION / POST-P1 LIGHTWEIGHT PRODUCT REDESIGN**. This is a deferral, not proof that portability is solved. Possible magnesium, CFRP or hybrid structures remain future intent; no GEN1-L CAD is established.

## What changed from the old public state

BODY2 is historical. FM2 / FM-C and the old Copal-in-each-lens architecture are **SUPERSEDED / HISTORICAL HOLD**. H2, the moving universal iris and Optical Insert define the current front direction. VF13 fixed-brightline work and SYS software studies remain historical evidence, not proof of the current electronic framing or hardware implementation.

## Next gate and source scope

Continue P1-01 shutter implementation until its function, safety, assembly and measurement gaps can support a separately reviewed next step. The [roadmap](physical-validation-roadmap.md) then proceeds through P1-02 H2, P1-03 iris / insert, P1-04 DM22, P1-05 electronics / power / range / UI, P1-06 integration and P1-07 controlled bench / prototype release planning. It is not a calendar schedule or current bench authorization.

This snapshot uses CAMERA_P1_BASELINE01 for the system strategy, COMPACT01 for inherited host / product-study evidence and P1-01_SHUTTER_IMPL02 for current shutter details. Earlier gates remain history where superseded. Unknown physical facts remain TBD; they are not filled with nominal values.

- [System architecture](../architecture/system-overview.md)
- [Subsystem status and evidence levels](subsystem-status.md)
- [P1 transition](../development-log/p1-functional-prototype-transition.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
