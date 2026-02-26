# Computational Fluid Dynamics flow simulations for a section of the South Saskatchewan River, Canada

- Overview
  - A dataset of CFD flow simulation results for a section of the South Saskatchewan River, Canada.
  - Includes two simulations to assess the effect of dunes on flow fields: one with dune-inclusive high-resolution morphology and one with dunes removed from the model domain.

- Data Content
  - Files: dune_results.csv and smooth_results.csv.
  - Each file contains seven columns:
    - Column 1: Model domain downstream (x) coordinate (m)
    - Column 2: Model domain cross-stream (y) coordinate (m)
    - Column 3: Model domain water depth (m)
    - Column 4: Depth-averaged velocity component in downstream (x) direction (m/s)
    - Column 5: Near-bed velocity component in downstream (x) direction (m/s)
    - Column 6: Depth-averaged velocity component in cross-stream (y) direction (m/s)
    - Column 7: Near-bed velocity component in cross-stream (y) direction (m/s)

- Data Collection and Processing
  - DEM creation from aerial imagery with 0.06 m pixel resolution (approx. 1500 m flight height) using structure-from-motion photogrammetry (SfM) and a depth-brightness model.
  - DEM construction combined SfM results and depth-brightness estimates; dune outlines identified to preserve banks/bar fronts while removing dunes from bar tops.
  - Dune removal performed with a moving-average, weighted-mean filter (6 m x 1 m, longest axis downstream).
  - Two CFD meshes generated with identical layout: 4948 x 1172 x 20 cells (downstream x cross-stream x vertical); horizontal resolution ~8 cm; vertical 20 cells; planar free surface (rigid-lid).

- Modeling Details
  - Solver: OpenFOAM, solving three-dimensional Navier–Stokes equations with RNG k-ε turbulence model.
  - Free surface: represented by rigid-lid approximation.
  - Inlet conditions: measured flow velocities.
  - Outlet condition: Neumann pressure.
  - Numerical schemes: second-order central differencing for gradients; second-order bounded central differencing for divergence; second-order unbounded deferred corrected scheme for surface normal gradients.
  - Convergence and tolerances: pressure 1×10^-8; velocity, k, ε 1×10^-10 (iterations); solver tolerances: pressure 1×10^-10; velocity 1×10^-12.

- Outputs and Usage
  - Provides comparative results to quantify how dunes modify depth-averaged and near-bed flow.
  - Useful for data exploration, self-service analysis, and informing further data products (e.g., dashboards, charts, or reports) related to bedform dynamics and flow fields.
  - Related publication: Strick, RJP et al. 2019 (Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery).

- Related Publication
  - Strick, RJP et al. 2019. DOI: 10.1002/esp.4558.

- Context and Access
  - Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
  - Data are results from CFD simulations designed to investigate the impact of dunes on river flow within a specific study area.
  - Data suitable for re-use in comparative studies of dune morphology effects on hydrodynamics or for validating simplified models of dune–flow interactions.