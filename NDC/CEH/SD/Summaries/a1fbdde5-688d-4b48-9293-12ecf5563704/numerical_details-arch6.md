# Summary

- The document describes two CFD data collections related to flow around biofilm structures and bedforms, intended to support data exploration and analysis.

## Dataset 1: Biofilm-streamer flow in laminar regime (biofilm-streamer in a channel)

- Scope
  - 1240 total files across four Reynolds numbers (Re = 400, 500, 600, 700).
  - 310 files per Re, starting at 0.12 seconds with 0.12-second time steps.
  - Focus: how changing Reynolds number affects ambient flow hydrodynamics and the oscillation frequency of a single biofilm streamer.

- Modelled domain and setup
  - Channel geometry: length 25 cm, depth 4 cm.
  - Biofilm streamer tail: oscillating, 2.5 cm long, attached to a rigid cylindrical base (1 cm diameter); base center at 2 cm from inlet and 2 cm from top/bottom walls.
  - Flow regime: laminar; Re calculated as Re = Umean D / ν using inlet velocity, base diameter, and ν.
  - Multiphysics approach: two nonoverlapping domains – fluid (Ωf) and solid (Ωs, biofilm); Navier-Stokes solver for fluid, linear elastic solver for biofilm; coupled fluid-structure interaction (FSI).
  - Simulation duration: 30 s total; first 2 s for flow development, then structural solver runs; point P coordinates recorded at each time step.

- Simulation details
  - Umean (inlet velocity): 0.4–0.7 m/s (corresponding to Re = 400–700).
  - Fluid density ρf = 1000 kg/m3; biofilm density ρb = 1000 kg/m3.
  - Material properties: Es = 5000 (Young’s modulus), υs = 0.4; dynamic viscosity μ = 0.01 Pa·s.
  - Data organization: files include coordinates (X, Y, Z), concentration (Cn), velocity components (U, u, V, W) and related quantities.

- Data variables (typical content)
  - Spatial coordinates: X, Y, Z
  - Scalar/concentration: Cn
  - Velocities: U (downstream), u, V (cross-stream), W (vertical)
  - Additional flow/derived fields for analysis (as described in the data tables)

- Outputs and outputs usage
  - Designed to enable end users to self-serve with numeric fields and to understand how ambient flow influences biofilm oscillations.
  - Outputs can be used to compute oscillation frequency and compare across Re values.

- References
  - Full setup and methodology described in Sinha, S., Hardy, R.J., Blois, G., Best, J.L., and Sambrook Smith, G.H. (2017). The influence of bed permeability on the structure of turbulent flow over bedforms: a numerical investigation. Water Resources Research, 53, 3067-3086. DOI: https://doi.org/10.1002/2016WR 019662

## Dataset 2: Bed permeability effects on flow over bedforms (boundary layer and Brinkman layer)

- Scope
  - Novel CFD model coupling surface and subsurface flow (boundary layer and Brinkman layer) to assess bed permeability effects on flow over bedforms such as dunes.
  - Includes a sensitivity study on how permeability alters near-bed flow structures.

- Modelled domain and parameters
  - Channel dimensions: length 4.8 m, width 0.35 m, height 0.60 m.
  - Permeable bed (files ending with _porbed): uniform spheres (diameter 0.038 m) arranged in a rectangular pattern; six sphere layers yielding hbed ≈ 0.228 m (bed porosity ~50%).
  - Flow depth above bed: hw = 0.19 m; ratio hw/hbed ≈ 0.8.
  - Dune (bedform) geometry: wavelength k = 0.41 m, amplitude 0.056 m, leeside angle 27°; dunes span the channel width.
  - Inlet and flow conditions: free stream velocity Uo = 0.16 m/s; Reynolds number Re ≈ 3.0 × 10^4; Froude number Fr ≈ 0.12.
  - Boundaries: downstream fixed pressure; walls no-slip; free surface approximated as a rigid lid.
  - Data structure: simulations include two sets of files (porbed and non-porous variations) with a comprehensive set of velocity, pressure, and turbulence variables.

- Data variables in the files
  - Spatial coordinates: X, Y, Z
  - Material/flow fields: PRPS (material variable), VEL1-X, VEL1-Y, VEL1-Z (velocity components), P1 (pressure)
  - Velocity components: U1 (downstream), V1 (lateral), W1 (vertical)
  - Turbulence metrics: KE (turbulent kinetic energy), Ε (dissipation rate), EP (turbulent dissipation rate), EPKE (product of KE and dissipation)
  - Normalized/boundary related fields: XN (x-normalised by domain length), ZN (z-normalised by domain length), NKE (KE normalised by inlet velocity squared), UN, WN (downstream and vertical velocity components normalised by inlet velocity)

- Outputs and outputs usage
  - Data suitable for analyzing the impact of bed permeability on surface and subsurface flow structures, especially in the context of dune-topography interactions.
  - Variables enable evaluation of flow distribution, pressure, velocity fields, and turbulence characteristics under permeable vs. impermeable bed conditions.

- References
  - Open access publication detailing bed permeability effects on turbulent flow over bedforms: Sinha et al. (2017). The influence of bed permeability on the structure of turbulent flow over bedforms: a numerical investigation. Water Resources Research. DOI: https://doi.org/10.1002/2016WR 019662

- Overall purpose for Data Support perspective
  - The two datasets provide richly structured CFD outputs with clearly defined spatial-temporal fields, designed to enable broad data use, cross-comparison across parameter regimes (Reynolds numbers, bed permeability), and development of self-serve data products (e.g., velocity and pressure fields, turbulence metrics) for downstream analyses and visualization.