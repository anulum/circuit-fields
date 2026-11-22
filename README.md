<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FIELDS — repository foundation
-->

# Circuit Fields

Circuit Fields is being built as the conditional specialist repository for 3D full-wave electromagnetic extraction (`openEMS`) and finite-element electro-thermal and thermo-mechanical analysis (`Elmer`) across on-chip passives, high-speed interconnects, carrier boards and 3D chiplet stacks — operating completely deterministically without requiring AI. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed electromagnetic solver adapter, finite-element thermal runner, S-parameter validator or qualified record schema.

Circuit Fields is part of the **SC Neuromorphic Computing Systems** group (SC-NEUROMORPHIC-COMPUTING-SYSTEMS). The [group and project map](https://github.com/anulum/sc-neurocore/blob/main/docs/ecosystem.md) shows the whole programme and where this repository sits in it.

**What does not exist yet:**
- an electromagnetic or finite-element thermal solver adapter;
- a registered runtime record schema;
- a qualified touchstone S-parameter or 3D thermal impedance model.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Field study | 3D geometry, dielectric/metal stack, mesh refinement plan, boundary excitations, power-dissipation map and convergence criteria for `openEMS` or `Elmer` |
| Field result | Multi-port touchstone S-parameters (causality and passivity verified), parasitic coupling matrices, steady-state and transient 3D temperature maps and thermo-mechanical warpage/stress bounds |

**Static imports:** only Circuit Core and Circuit Technology.

**Records read without importing domain code:**

| Source | Records consumed |
|---|---|
| Circuit Core and Circuit Technology | entity references, design views, operation profiles, system budgets and technology profiles |
| Circuit Assembly | assembly views and chiplet/3D stack geometries |
| Circuit Flow and Circuit Learning | design-step learning records and grader bundle specifications |

**Capability registration and handoffs:** Registers under the specialist tool-profile manifest with Circuit Core and supplies S-parameter, crosstalk and 3D thermal models to Circuit Analog, Circuit Photonics, Circuit Physical, Circuit Assembly and Circuit Acceptance.

**Explicit non-claims and operating boundaries:**
- Every electromagnetic and thermal study completes deterministically without machine learning.
- Neural operator surrogates (`neuraloperator`, `physicsnemo` Fourier neural operators) are exploratory screening proposals only and never substitute for deterministic `openEMS` and `Elmer` sign-off.
- `openEMS` (`GPL-3.0`) and `Elmer` (`GPL-2.0` with `LGPL-2.1` libraries) execute strictly as separate processes over file boundaries.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future domain artefact will carry the platform's common provenance envelope, its source and environment digests, its confidentiality compartment and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or sign-off verdict.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
