# Computational Fluid Dynamics flow simulations for a section of the South Saskatchewan River, Canada

## Overview
- This dataset contains results from three-dimensional CFD flow simulations (OpenFOAM) focused on the impact of dunes on depth-averaged and near-bed flow fields in a section of the South Saskatchewan River, Canada.
- Two CFD scenarios were run on the same model domain: one incorporating dune-scale morphology and one with dunes removed, enabling direct comparison of dune effects.
- The work supports understanding sediment transport and bedform dynamics in sandy braided river settings.

## Data files and contents
- Dune_results.csv: CFD results for the model domain with dunes included.
- Smooth_results.csv: CFD results for the model domain with dune-scale topography removed.
- Each file contains seven columns:
  - Column 1: x coordinate (m) – downstream
  - Column 2: y coordinate (m) – cross-stream
  - Column 3: water depth (m)
  - Column 4: depth-averaged velocity component in downstream (x) direction (m/s)
  - Column 5: near-bed velocity component in downstream (x) direction (m/s)
  - Column 6: depth-averaged velocity component in cross-stream (y) direction (m/s)
  - Column 7: near-bed velocity component in cross-stream (y) direction (m/s)

## DEM creation and dune removal
- A high-resolution digital elevation model (DEM) of the model domain was created from airborne imagery (0.06 m pixel size; ~1500 m flight height) using Structure-from-Motion photogrammetry (SfM) and a depth-brightness regression model.
- SfM generated emergent-area DEMs and for a gravel-dominated bank section; the depth-brightness model covered other areas.
- Dunes were removed from the dune-topography DEM by:
  - Visually identifying banks and bar fronts to create masks.
  - Applying a moving-average, weighted-mean filter (window 6 m x 1 m, downstream axis aligned with dune length) to remove dune features from bar tops while preserving banks and bar lee slopes.

## CFD modelling details
- Solver: OpenFOAM (3D Navier–Stokes with RNG k-ε turbulence closure).
- Free surface: modeled with a rigid-lid approximation.
- Mesh: two structured finite-volume meshes (one with dunes, one without) consisting of 4948 × 1172 × 20 cells (downstream × cross-stream × vertical).
- Horizontal resolution: approximately 8 cm; vertical resolution: 20 cells; planar surface at zero depth.
- Inlet conditions: measured flow velocities.
- Outlet: Neumann pressure condition.
- Numerical schemes: second-order central differencing for gradients; second-order bounded central differencing for divergence; second-order accurate unbounded deferred correction for surface-normal gradients.
- Convergence criteria: pressure tolerance 1e-8; velocity, k, epsilon tolerances 1e-10; solver tolerances 1e-10 (pressure) and 1e-12 (velocity).
- Simulation outputs: two datasets corresponding to the two mesh configurations (with and without dunes).

## Data provenance and references
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
- Context: "Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery" (Strick et al., 2019) – Earth Surface Processes and Landforms, doi:10.1002/esp.4558.

## Potential analyses and applications
- Quantify how dune presence alters depth-averaged and near-bed velocity fields in both downstream and cross-stream directions.
- Compare flow-field changes between dune-inclusive and dune-free scenarios to infer dune-driven modifications to shear stress and potential sediment transport pathways.
- Use high-resolution DEM-based setups to test sensitivity to bedform topography and to support predictive modelling of flow–bedform interactions in braided rivers.
- Leverage the paired datasets to develop or validate simplified models that estimate dune impacts on velocity fields at comparable scales.