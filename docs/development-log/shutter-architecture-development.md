# Shutter Architecture Development

> **Current prototype direction:** K3 + ACT-E  
> **Latest milestone:** P1-01_SHUTTER_IMPL02  
> **Current gate:** IMPLEMENTATION HOLD — NOT READY FOR CONTROLLED BENCH PLANNING  
> **Updated:** 2026-09-28

The shutter moved from the historical Copal-in-each-lens front architecture to a body-mounted focal-plane architecture. K3 is the retained flexible dual-curtain direction; ACT-E provides direct closed-loop electric actuation. No physically working shutter is claimed.

## Milestone sequence

| Milestone | Decision / result | Evidence boundary |
| --- | --- | --- |
| SHUTTER01_KIN01 | K3 primary research candidate; kinematic HOLD | Compared curtain topologies; retained digital kinematic evidence, not a working mechanism. |
| SHUTTER02_DRIVE01 | K3 retained; mechanical closure HOLD | Drive, energy, braking, capture, reset and connection gaps remained. |
| SHUTTER03_ACTUATION01 | ACT-E next mainline; implementation / safe-closure HOLD | ACT-S became reference only; ACT-H was not selected. Conditional actuation models did not qualify hardware. |
| SHUTTER04_IMPL01 | Implementation / safe-closure HOLD | Realistic actuator scale and inertia exposed unresolved drive, support, power and service problems. Earlier miniature-actuator assumptions were superseded. |
| P1-01_SHUTTER_IMPL01 | Function-first implementation HOLD | Slower prototype operating studies and component candidates; placement, sensing, assembly and safety conflicts remained. |
| P1-01_SHUTTER_IMPL02 | CURRENT P1 DIRECTION / IMPLEMENTATION HOLD | Right-side drive and optical / coded direct bar reference candidates; remaining hard interferences, assembly / bearing service and safe closing not closed. |

## Why ACT-E replaced ACT-S

The actuation review favored controlled electric trajectories to simplify the normal brake / high-speed capture / reset-clutch chain. The spring-based mechanical route had not closed that chain. ACT-E still requires credible actuator dynamics, transmission, sensing, static holding, power and fault management. Its selection is an architecture decision, not a completed implementation.

Passive bias considered for emergency closing is separate from the normal exposure drive. It does not restore ACT-S as an active alternative mainline.

## Latest IMPL02 interpretation

| Topic | Public status |
| --- | --- |
| Primary prototype direction | K3 flexible dual-curtain + ACT-E direct closed-loop electric drive |
| Motor placement | Right-side drive arrangement retained as P1 candidate; installed-state D3 improvement does not demonstrate full assembly |
| Direct bar sensing | Optical / coded direct bar reference candidate; custom implementation, accuracy, light isolation and integration require evidence |
| Main-power-loss controlled close | Architecture under study; reserve, drive and isolation behavior unverified |
| Total-energy-loss autonomous mechanical close | NOT CLOSED / NOT VALIDATED |
| Assembly / maintenance | Complete installation and bearing service remain unresolved; known hard interferences retained |
| Release gate | IMPLEMENTATION HOLD / NOT READY FOR CONTROLLED BENCH PLANNING |

Independent endpoint evidence must complement direct bar sensing. Motor angle alone is not a substitute for actual bar position. Source simulations include failure cases and do not establish a safe closing probability or guarantee. Normal operation, loss of main power and loss of all usable energy require distinct evidence.

## Next evidence

The next step is to resolve the concrete implementation, interference, assembly, service and safety gaps sufficiently to support a separately reviewed validation plan. Real component behavior, friction / damping / release / capture behavior, power and reserve limits, opacity and sensing must replace modelling assumptions.

No public speed claim, complete actuator-load table, reserve sizing, drive dimensions or safety-mechanism geometry is included. These studies do not authorize procurement, manufacture or connection to a real back.

Source basis: original SHUTTER01–03 gate records referenced by the supplied packages, SHUTTER04 implementation gate, P1-01 IMPL01 gate, and IMPL02 gate / motor placement / sensor / Level 1 / Level 2 / assembly / service reviews. Newer applicable implementation conclusions supersede earlier candidates without erasing their failure evidence.

- [P1 transition](p1-functional-prototype-transition.md)
- [BODY3 development](body3-development.md)
- [Electronics and power responsibilities](../architecture/electronics-control-overview.md)
- [Current state](../overview/current-state.md)
- [Public Release Policy](../../PUBLIC_RELEASE_POLICY.md)
