<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FIELDS — repository foundation
-->

# Data and authority boundaries

## Present tooling

**Execution inputs.** The maintained checkout and the selected development environment are what the repository controls inspect.

**Received inputs.** Descriptors, dependency receipts and generated inventories cannot nominate an acceptance policy or an executable.

**Bounded checks.** Controls inspect bounded local paths and emit fixed diagnostics.

Foundation qualification is in progress.

## Future domain inputs

**Supplied data, with no authority.** The following inputs are treated strictly as supplied data:
- 3D stackups, GDSII/package geometries and material tensors;
- block power-density maps and port definitions.

They grant no authority to:
- substitute a neural surrogate for deterministic solver sign-off;
- link `GPL`/`LGPL` solver libraries in-process;
- waive S-parameter passivity or mesh-convergence failures.

**Comments and embedded text are data.** Descriptions, netlist comments and datasheets arriving inside supplied inputs are data, never instructions to an operator or an agent.

**Public-repository data boundary.** Hosted CI for this public repository runs on public material only. Confidential foundry-NDA, customer, export-controlled or secret-bearing material never enters this repository, its CI or its issues.

## Threats and the rules that answer them

| Threat | Architectural rule |
| --- | --- |
| Neural operator surrogates masking RF crosstalk, non-passive S-parameters or 3D chiplet thermal hotspots | Surrogates are restricted to rapid design screening; sign-off requires deterministic two-mesh `openEMS` and `Elmer` solutions with S-parameter passivity and causality verification |
| Copyleft multiphysics solver linkage | `openEMS` and `Elmer` run strictly as separate child processes over file boundaries |

## Residuals named, not removed

- **Boundary conditions.** Thermal hotspot predictions depend on the ambient convection and heatsink boundary conditions declared in the study.

**Not claimed:** no isolation, physical, statistical, safety or durability guarantee is claimed by this foundation.
