# Summary

- The document comprises two open CFD data studies, each detailing domain setups, simulation parameters, and data variables used to analyze flow around biofilm-streamers and bed-permeability effects on dune-scale bedforms, with attention to reproducibility and data accessibility.

## Biofilm-streamer in laminar flow (Reynolds numbers 400–700)

- Objective
  - Investigate how ambient flow characteristics and the oscillation frequency of a single biofilm streamer depend on Reynolds number in laminar flow.
- Data scope
  - 1240 data files in total, across four Reynolds numbers (400, 500, 600, 700).
  - For each Re, 310 sequential time-step files starting at 0.12 seconds, with 0.12-second intervals.
  - Simulations cover 30 seconds of physical time.
- Geometry and physical setup
  - Channel: length 25 cm, depth 4 cm.
  - Biofilm streamer: oscillating tail length 2.5 cm attached to a rigid cylindrical base (1 cm diameter); base center located 2 cm from inlet and 2 cm from top/bottom walls.
  - Fluid-structure interaction (FSI): two non-overlapping domains—fluid Ωf (Navier-Stokes) and solid Ωs (linear elastic biofilm). Flow develops for the first 2 seconds before the structural solver starts.
- Simulation details
  - Parabolic inlet flow with maximum velocity along the centerline.
  - Total simulated time: 30 seconds; coordinates at a point P are saved at every time step.
  - Parameters (per Table-1):
    - Inlet mean velocity Umean: 0.4–0.7 m/s (corresponding to Re 400–700).
    - Fluid density ρf = 1000 kg/m3; biofilm density ρb = 1000 kg/m3.
    - Biofilm Young’s modulus Es = 5000 (units: kg/(m·s2)); Poisson’s ratio υs = 0.4.
    - Dynamic viscosity μ = 0.01 kg/(m·s).
- Data and variables
  - Spatial coordinates: X, Y, Z (m).
  - Scalar/concentration: Cn (g/L).
  - Velocity components: U (downstream), V (cross-stream), W (vertical).
- Data access and references
  - Data are intended to support a CFD model of boundary-layer flow coupled to the Brinkman-like biofilm domain; related to an open-access publication by Sinha et al. (2017) on bed permeability and flow structure.
  - Some files are labeled to indicate specific solver configurations (e.g., _dune, _porbed).

## Bed permeability and dunes over bed forms (permeable bed and dune flow)

- Objective
  - Assess how bed permeability influences flow over bed forms (e.g., dunes) using a CFD model that treats both boundary-layer and Brinkman-type subsurface flow within a unified scheme.
- Domain and geometry
  - Channel: length 4.8 m, width 0.35 m, height 0.60 m.
  - Permeable bed scenario (_porbed): six layers of uniform spheres (diameter D = 0.038 m) packed in a rectangular arrangement, yielding a bed thickness hbed = 0.228 m and porosity ~50%.
  - Bedforms: a dune spanning the channel width, with wavelength k = 0.41 m, amplitude 0.056 m, leeside angle 27 degrees.
  - Flow conditions: flow depth hw = 0.19 m; ratio hw/hbed = 0.8.
- Boundary conditions and flow regime
  - Freestream inlet velocity Uo = 0.16 m/s; resulting freestream Reynolds number Re ≈ 3.0 × 10^4 and Froude number Fr ≈ 0.12.
  - Outlet: fixed-pressure boundary; mass flux allowed in/out.
  - Walls: no-slip; free surface modeled with a rigid-lid approximation.
- Data and variables
  - Spatial coordinates: X, Y, Z (m).
  - Material/physical fields: PRPS (material variable for water/solid), P1 (pressure, Pa), U1/X, V1/Y, W1/Z (velocity components), KE (turbulent kinetic energy), Ε (dissipation rate), EP (turbulent dissipation rate), EPKE (product of KE and dissipation), XN/ZN (normalized coordinates), NKE (KE normalized by inlet velocity squared), UN/WN (velocities normalized by inlet velocity).
  - Additional normalized and diagnostic variables track flow and turbulence structure.
- Data access and references
  - Detailed numerical setup and results are linked to the open-access publication by Sinha et al. (2017) in Water Resources Research, focusing on bed permeability and flow over bedforms.
- Data specifics
  - File content includes both boundary-layer and Brinkman-layer variables (e.g., velocity components, pressure, turbulent quantities) to enable analysis of interactions between surface and subsurface flow under permeable-bed conditions.