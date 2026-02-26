# Summary

- The document describes two CFD data collections that explore flow behavior in different contexts and with different modeling approaches.
- The overarching aim is to provide data that can inform understanding of fluid-structure interactions and porous/Bed-permeability effects in laminar and transitional flow regimes.

## Dataset 1: Biofilm-streamer flow in laminar regime

- Scope
  - 1240 data files total, organized by Reynolds number (Re = 400, 500, 600, 700).
  - For each Re, 310 files representing the biofilm streamer oscillation.
  - Time series: starts at 0.12 s with increments of 0.12 s; total simulated time is 30 s.
- Physical setup
  - 2D-ish description in a channel: length 25 cm, depth 4 cm.
  - Biofilm streamer attached to a rigid cylindrical base (diameter 1 cm) with an oscillating tail (2.5 cm); base center located 2 cm from inlet and 2 cm from channel walls.
  - Inlet open-channel conditions with parabolic velocity profile; two seconds allocated for flow development before tissue/structure solver starts.
- Fluid-structure interaction (FSI)
  - Two non-overlapping domains: fluid Ωf and solid biofilm Ωs.
  - Fluid: Navier–Stokes solver provides pressure/velocity fields.
  - Solid: linear elastic solver provides spatial displacement of biofilms.
  - Coupled FSI details are described in the accompanying solver section (not reproduced here).
- Governing/operational parameters
  - Umean (inlet velocity): 0.4–0.7 m/s (mapped to Re values via D and ν).
  - D = biofilm base diameter parameter; ρf = ρb = 1000 kg/m³; μ = 0.01 kg/(m·s); Es = 5000; υs = 0.4.
  - Domain geometry described with Fig. 1 reference.
- Data variables in files
  - Spatial coordinates: X, Y, Z (m).
  - Cn: concentration (g/L).
  - U, V, W and their components: downstream, cross-stream, vertical velocities.
- Data access notes
  - Files ending with _dune and _porbed are accompanied by a related open-access publication detailing workflow and context: Sinha et al. (2017) on bedform flow structures and permeability (Water Resources Research).
- Relevance for data leadership
  - Demonstrates end-to-end data collection (geometry, material properties, time-resolved fields) across multiple Reynolds numbers.
  - Highlights data governance needs: consistent variable naming, unit usage, and metadata to support reuse and cross-study integration.
  - Useful for validating data discovery practices, reproducibility, and cross-team collaboration around CFD-based data products.

## Dataset 2: Bed permeability and surface–subsurface flow (boundary layer and Brinkman layer)

- Scope
  - CFD model simulating flow that couples boundary layer flow and a Brinkman layer to study bed permeability effects on bedform flow structure.
  - Open-access publication reference: Sinha, Hardy, Blois, Best, and Sambrook Smith (2017), Water Resources Research.
- Physical setup
  - Channel dimensions: length 4.8 m, width 0.35 m, height 0.60 m.
  - Permeable bed scenario (_porbed): uniform spheres (D = 0.038 m) packed in rectangular geometry, six sphere layers giving hbed ≈ 0.228 m and porosity ~50%.
  - Permeable bed region spans the full flume cross-section; dune scenario has a representative dune with k = 0.41 m, amplitude 0.056 m, leeside angle 27°, spanning channel width.
  - Flow conditions: Uo = 0.16 m/s, results in Re ≈ 3.0 × 10^4 and Fr ≈ 0.12.
  - Boundary conditions: fixed-pressure outlet with mass exchange, no-slip walls, rigid-lid approximation at the free surface.
- Data variables in files
  - Spatial coordinates: X, Y, Z (m).
  - PRPS: material state indicator (water/solid).
  - Velocity components: VEL1-X, VEL1-Y, VEL1-Z; downstream velocity U1; cross-stream V1; vertical W1.
  - Turbulent metrics: KE (turbulent kinetic energy), Ε (dissipation rate), EP (turbulent dissipation rate), EPKE (product of KE and dissipation rate), NKE (normalized KE), UN, WN, XN, ZN (normalised coordinates by domain length).
  - Additional columns indicate normalization and scaling (e.g., KN/NKE, velocities normalized by inlet velocity).
- Data access notes
  - Comprehensive variable set allows analysis of near-bed and over-bed flow structures, including surface and subsurface interactions.
- Relevance for data leadership
  - Exemplifies coupling of different physical layers (surface flow and Brinkman subsurface) in a single dataset, underscoring the importance of cross-domain data interoperability.
  - Emphasizes the need for detailed metadata to describe complex variable mappings, normalizations, and boundary conditions.
  - Provides a case study for evaluating data standardization, discoverability, and quality controls when integrating multi-physics CFD data across projects.

## Cross-cutting data governance and quality considerations for Data Leaders

- Data system view
  - Both datasets require careful documentation of domain geometry, material properties, boundary conditions, and solver configurations to enable reuse and replication.
  - Metadata should clearly map units, coordinate systems, and variable definitions (e.g., velocity components, geospatial coordinates, and normalization schemes).
- Data discovery and accessibility
  - Ensure consistent naming conventions and file tagging (e.g., _dune, _porbed) to facilitate searchability across CFD datasets.
  - Link data with the associated publications and solver manuals to provide context for model assumptions and limitations.
- Data quality and standards
  - Noted heterogeneity in variable naming and formatting (e.g., convergence of column headers like BLANK or blank columns) underscores need for standard data schemas when sharing CFD outputs.
  - Documentation of validation steps, time stepping, and flow development periods improves reliability and governance.
- Gaps and opportunities
  - Potential data gaps include explicit error estimates, mesh/solver settings, and convergence criteria to improve reproducibility.
  - Opportunities exist to create standardized data products (e.g., time-series of point P in biofilm study, bed-permeability flux metrics) that can be reused by policy-makers, engineers, and researchers.
- Actions for Data Leaders
  - Establish a shared metadata schema for CFD datasets covering geometry, materials, flow regimes, solver configurations, and boundary conditions.
  - Promote cross-project collaboration to build a community of practice around CFD data assets, reducing duplication and improving data quality.
  - Prioritize data discoverability, provenance, and versioning to support ongoing analysis, iteration, and dissemination.