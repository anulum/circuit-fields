<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FIELDS — repository foundation
-->

# Decision: isolate 3D electromagnetic and electro-thermal multiphysics solvers in Circuit Fields

## Context

High-speed links, RF inductors, thermo-optic phase shifters and 3D chiplet stacks depend on full-wave electromagnetic and 3D thermal physics that 2.5D RC extractors cannot model, using heavy copyleft solvers.

## Decision

**What Circuit Fields owns:**
- field study;
- field result;

**What it imports:** only Circuit Core and Circuit Technology.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| circuit SPICE simulation | Circuit Analog |
| optical FDTD waveguide solving | Circuit Photonics |
| die layout and package/PCB design | Circuit Physical and Circuit Assembly |
| tapeout sign-off | Circuit Acceptance |

## Consequences

**What can be qualified now:** repository governance and validation tooling, before domain code exists.

**What it cannot qualify:** unimplemented schemas, solvers, hardware or sign-off verdicts.

**Architectural consequences:**
- Circuit Fields encapsulates `openEMS` and `Elmer` behind separate-process boundaries and supplies verified S-parameter and thermal records across domains;
- neural surrogates can accelerate exploration without ever entering sign-off.
