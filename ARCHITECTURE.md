<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FIELDS — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of Circuit Fields is implemented yet. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended data flow

1. **Mesh and boundary generation** build 3D electromagnetic and thermal problem definitions from die, package and stack geometries.
2. **Separate-process deterministic solving** runs `openEMS` and `Elmer` across two mesh densities to bound discretisation error and check S-parameter passivity/causality.
3. **Coupled export** delivers verified coupling and hotspot maps to analogue, photonic, physical, assembly and acceptance sign-off.

## Ownership

**This project owns** the planned Circuit Fields records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| circuit SPICE simulation | Circuit Analog |
| optical FDTD waveguide solving | Circuit Photonics |
| die layout and package/PCB design | Circuit Physical and Circuit Assembly |
| tapeout sign-off | Circuit Acceptance |

## Interpretation

- **Discretisation.** Solver results hold within their verified mesh-convergence and boundary-condition assumptions.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, domain rules and schema identifiers.
