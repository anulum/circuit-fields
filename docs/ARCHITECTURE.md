<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FIELDS — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Field study | 3D geometry, dielectric/metal stack, mesh refinement plan, boundary excitations, power-dissipation map and convergence criteria for `openEMS` or `Elmer` | Pinned design-view, technology-profile and assembly/chiplet-stack digests with mesh-convergence checks |
| Field result | Multi-port touchstone S-parameters (causality and passivity verified), parasitic coupling matrices, steady-state and transient 3D temperature maps and thermo-mechanical warpage/stress bounds | Deterministic solver provenance, mesh-refinement residual bounds and explicit surrogate-versus-solver tagging |

## Licence isolation and surrogate non-sign-off rule

- **Separate-process copyleft solvers.** `openEMS` (`GPL-3.0`) and `Elmer` (`GPL-2.0` / `LGPL-2.1`) are invoked strictly via command-line input decks and output files in isolated processes.
- **Surrogates never sign off.** Any neural-operator field estimate is marked as an exploratory surrogate that never qualifies sign-off and is rejected by sign-off consumers unless backed by a deterministic solver result.

## Planned record schemas

- `circuit_fields.field_study.v1`
- `circuit_fields.field_result.v1`

These are planned identifiers. None of them is registered or qualified here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
