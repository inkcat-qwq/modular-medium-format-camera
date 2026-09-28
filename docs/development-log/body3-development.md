# BODY3 Development

> **Record:** Sanitized structural architecture history  
> **Current direction:** BODY3 / P1; real structural validation required  
> **Updated:** 2026-09-28

BODY3 replaces BODY2 as the body direction for a 645-class camera with a body-mounted focal-plane shutter. It retains the D3 shoulder finder, fixed rear datum and modular rear adapter, while reorganizing load-bearing and service responsibilities around the shutter.

| Milestone | Historical result | Scope of evidence |
| --- | --- | --- |
| BODY3_SHUTTER_ARCH01 | CANDIDATE; architecture review could continue | New structural / shutter-bay relationship with a rear datum independent of the shutter. Not a real shutter or back-compatibility result. |
| BODY3_STRUCTPACK01 | HOLD | Structural packaging candidate; real DM22 removal prevented a complete service-sequence conclusion. |
| BODY3_FRAME01 | CANDIDATE; digital frame direction retained | Digital load-path and selected geometry checks. Actual joints, strength and manufacturing process remained open. |
| CAMERA_GEN1_CONCEPT01 | CONCEPT / HOLD | BODY3, H2, shared iris and a single Optical Insert brought into one whole-camera concept; native delivery was incomplete at that stage. |
| CAMERA_GEN1_COMPACT01 | CANDIDATE; native delivery recovered, product portability HOLD | Native model recovery and selected integration checks; functional and physical gates remained open. |
| CAMERA_P1_BASELINE01 | CURRENT P1 DIRECTION | Inherited host supports function-first development. No final lightweight variant or manufacturing configuration is selected by that inheritance. |

## What is retained

The rear datum belongs to the fixed body structure and must remain stable during ordinary shutter service. The shutter is not the precision structural link between the front and the rear. The modular rear adapter and D3 retain distinct responsibilities.

Separate positioning, seating and clamping remains a guiding principle. Existing concept host geometry supplies a development reference, not proof of real DM22 seating, locking or imaging registration.

## How P1 changes packaging and service gates

P1 accepts documented size, weight, actuator and electronics exceptions in support of function. Complete-cassette service was a product intent; P1 may use staged tool-assisted maintenance. This change does not make an obstructed assembly route valid, excuse hard interference or permit loss of the fixed rear datum.

The latest IMPL02 shutter still has assembly and bearing-maintenance blockers. Its final installed state must not be confused with a demonstrated installation sequence. Earlier body-level service checks do not automatically cover the later populated shutter mechanism.

## What remains unverified

Full frame strength, real joints and process feasibility, assembly / service repeatability, actual rear-back registration and synchronization, D3 physical observation and complete optical / shutter performance require evidence. CAD continuity, native file reopening and selected collision checks do not close those requirements.

Source basis: BODY3_SHUTTER_ARCH01 architecture gate, BODY3_STRUCTPACK01 structural gate, BODY3_FRAME01 gate preserved in the P1 inputs, COMPACT01 integration / portability reports, P1 baseline and IMPL02 gate. Only high-level conclusions are public.

- [P1 transition](p1-functional-prototype-transition.md)
- [Shutter development](shutter-architecture-development.md)
- [Historical BODY2 integration](body2-rev05-architecture-integration.md)
- [Current system](../architecture/system-overview.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
