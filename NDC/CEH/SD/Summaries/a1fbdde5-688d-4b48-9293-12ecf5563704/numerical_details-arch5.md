# The data in these files simulates flow around a biofilm-streamer in the laminar flow regime

## Overview
- Two CFD data-grounded studies are described, with a focus on data generation, structure, and metadata for reuse.
- Dataset 1: 1240 files simulating flow around a biofilm-streamer in laminar regime across four Reynolds numbers (400–700), with 310 files per Re, starting at 0.12 s and incrementing by 0.12 s up to 30 s.
- Dataset 2: CFD study on bed permeability effects on flow over bedforms (boundary layer and Brinkman layer), used for a numerical sensitivity experiment in a river-channel context.

## Dataset 1 — Biofilm-streamer in laminar flow
- Objective and scope
  - Investigate how varying Reynolds number affects ambient flow hydrodynamics and the oscillation frequency of a single biofilm streamer.
- Modelled domain and setup
  - Geometry: channel length 25 cm, depth 4 cm; biofilm tail length 2.5 cm fixed to a rigid cylindrical base (1 cm diameter); base center located 2 cm from inlet and 2 cm from top/bottom walls.
  - Flow regime: laminar; Re numbers 400, 500, 600, 700 (calculated as Re = U mean D / ν).
  - Time expansion: simulations run for 30 s total; first 2 s allowed for flow development; data extraction for the remaining duration (point P tracked every time step).
  - Coupled solver: two nonoverlapping domains (fluid: Navier–Stokes; solid: linear elastic biofilm); fluid–structure interaction (FSI) solver described separately.
  - Inlet conditions: parabolic velocity profile with maximum velocity at the channel centerline; Umean values corresponding to Re range (0.4–0.7 m/s, per Table-1).
  - Physical properties: ρf = ρb = 1000 kg/m³; Es = 5000 (units context provided); υs = 0.4; µ = 10^-2 Pa·s.
- Data organization and content
  - Data files: 1240 total, organized as four Re-numbered groups (FinalCase1b1…310 for Re 400, FinalCase2b1…310 for Re 500, etc.).
  - Variant support: some files include _dune and _porbed naming for numerical experiment details.
  - Variables within files: X, Y, Z (spatial coordinates); Cn (concentration in g/L); U, V, W (velocity components downstream, cross-stream, vertical).
- Data provenance and references
  - Related open-access publication: Sinha et al. (2017) Water Resources Research; DOI provided in the document.
- Data governance considerations
  - Documentation needed: coordinate system, units, variable definitions, and treatment of concentration Cn.
  - Interoperability considerations: two-domain FSI model with potential _dune and _porbed variants; ensure consistent metadata across methods.
  - Access and reuse: large dataset; include dataset-level metadata, a data dictionary, and clear licensing/citation guidance.

## Dataset 2 — Bed permeability and flow over bedforms (CFD model)
- Objective and scope
  - Numerical sensitivity study to assess how bed permeability influences flow over bedforms (e.g., dunes) using a model that couples surface and subsurface flow.
- Modelled domain and parameters
  - Channel: 4.8 m length, 0.35 m width, 0.60 m height.
  - Bed treatment: permeable bed covering the entire flume with uniform spheres (Ø 0.038 m) in a rectangular arrangement; six layers yield a permeable depth hbed = 0.228 m; bed porosity ≈ 50%.
  - Flow conditions: flow depth hw = 0.19 m; Uo = 0.16 m/s; resulting freestream Reynolds number Re ≈ 3.0 × 10^4; Froude number Fr ≈ 0.12.
  - Dune geometry: wavelength k = 0.41 m, amplitude 0.056 m, leeside angle 27°, dune extends across channel width.
  - Boundary conditions: downstream end uses fixed-pressure outlet; walls are non-slip; free surface treated with a rigid-lid approximation.
- Data variables in files
  - Spatial coordinates: X, Y, Z.
  - Core variables: PRPS (material variable for water/solid), VEL1-X/Y/Z (velocity components in x/y/z), P1 (pressure), U1, V1, W1 (downstream/lateral/vertical velocity components), KE (turbulent kinetic energy) and Ε (dissipation rate), EP (turbulent dissipation rate), EPKE (product of KE and EP), XN/Z N (dimensionless spatial normalizations), NKE (normalized KE), UN/WN (velocity normalizations).
  - Additional columns and normalizations indicate a detailed turbulence and flow-field dataset intended for subsurface–surface coupling analysis.
- Data provenance and references
  - Cited open-access publication: Sinha et al. (2017) Water Resources Research; provides full methodological context for bed permeability effects on flow over bedforms.
- Data governance considerations
  - Metadata requirements: clear definitions for PRPS, velocity components, turbulent quantities, and all normalizations; specify units and scale (dimensional vs. nondimensional).
  - Interoperability concerns: multiple variables and potential variant naming (_dune, _porbed); harmonize data dictionaries and provide a unified metadata schema.
  - Accessibility and reuse: substantial data volume with rich turbulence metrics; require indexing by variant (dune vs. porbed), bed configuration, and flow regime; include licensing and a dataset usage guide.

## Data governance implications for Data Stewards
- Metadata and documentation
  - Create comprehensive metadata for each dataset, including: dataset title, description, geometry, solver settings, material properties, units, coordinate conventions, time steps, and variant identifiers (_dune, _porbed).
  - Develop a data dictionary that defines every variable (including Cn, PRPS, KE, Ε, EP, EPKE, NKE, UN, WN, etc.) and their units.
- Standardization and interoperability
  - Align naming conventions and units across both datasets; clearly document dimensional vs. nondimensional quantities (normalizations like XN, ZN, NKE).
  - Ensure consistent documentation for two-domain FSI and for bed-permeability variants to minimize misinterpretation during reuse.
- Provenance, quality, and versioning
  - Record solver versions, mesh details, convergence criteria, and any post-processing steps; assign persistent identifiers (DOIs or UUIDs) for each dataset and sub-sets (per Reynolds number, per variant).
  - Establish data quality notes and limitations (e.g., rigid-lid approximation for free surface, development period before sampling).
- Access, licensing, and reuse
  - Provide clear licensing, citation instructions, and reproduction guidance; specify any restrictions on redistribution or commercial use.
  - Offer access strategies for large files (e.g., chunking, streaming, or a data access API) and include example or sample files for testing.
- Discovery and maintainability
  - Index datasets by key attributes: Reynolds numbers (for Dataset 1), bed permeability variant (Dataset 2), dune/porbed designation, simulation time, and variable sets.
  - Plan for updates or future expansions (new Reynolds numbers, alternative bed configurations) with version control and changelogs.

## Practical recommendations for data custodians
- Implement a formal metadata schema covering dataset scope, geometry, physics, solver settings, units, and variable definitions.
- Use persistent identifiers for datasets and subsets; provide a data access plan, licensing terms, and clear citation guidance.
- Provide a data dictionary, sample files, and validation scripts to facilitate re-use and reproducibility.
- Harmonize formats and naming across both datasets to reduce interoperability barriers and improve discoverability.