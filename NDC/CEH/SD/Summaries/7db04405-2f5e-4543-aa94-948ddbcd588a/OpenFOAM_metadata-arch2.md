# Computational Fluid Dynamics flow simulations for a section of the South Saskatchewan River, Canada

## Overview
- Investigates the impact of bedforms (dunes) on depth-averaged and near-bed flow fields in a section of the South Saskatchewan River.
- Compares two CFD simulations: one with dune morphology included and one with dunes removed.

## Data and files
- Datasets: dune_results.csv and smooth_results.csv
- Each dataset contains seven columns:
  - Model domain downstream (x) coordinate (m)
  - Model domain cross-stream (y) coordinate (m)
  - Model domain water depth (m)
  - Depth-averaged downstream velocity (u, m/s)
  - Near-bed downstream velocity (u at near-bed, m/s)
  - Depth-averaged cross-stream velocity (v, m/s)
  - Near-bed cross-stream velocity (v at near-bed, m/s)

## Data provenance and authors
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth
- Context: Results from Computational Fluid Dynamics flow simulations for a section of the South Saskatchewan River, Canada.
- Publication context: Related work by Strick et al. (2019) on bedform dynamics and bedload sediment flux; doi:10.1002/esp.4558.

## Modelling approach and setup
- CFD tool: OpenFOAM solving three-dimensional Navier-Stokes equations with RNG k-epsilon turbulence closure.
- Surface representation: Free surface modeled using a rigid-lid approximation.
- Inlet conditions: Measured flow velocities; outlet: Neumann pressure condition.
- Numerical schemes: Second-order central differencing for gradients; second-order bounded central differencing for divergence; second-order unbounded deferred corrected scheme for Laplacian surface normals.
- Convergence criteria: Pressure tolerance 1x10^-8; velocity, k, and epsilon tolerances 1x10^-10; solver tolerances 1x10^-10 for pressure and 1x10^-12 for velocity.

## Geometry, DEM creation, and dune removal
- DEM generation: 0.06 m pixel-resolution DEM from aerial imagery (~1500 m height) using Structure-from-Motion photogrammetry (Pix4D) and depth-brightness regression; SfM for emergent areas and a gravel-dominated bank region; depth-brightness model for other areas.
- Dune removal: Banks and bar outlines masked in ARCMAP; dunes removed from bar tops using a moving-average, weighted-mean filter (window 6 m x 1 m, downstream-oriented).
- Mesh details: Two structured finite-volume meshes, each 4948 x 1172 x 20 cells (downstream x cross-stream x vertical); horizontal resolution ~8 cm; vertical resolution 20 cells; planar surface at 0 m depth.

## Outputs
- Two simulation results are provided:
  - Dune_results.csv: with dunes present
  - Smooth_results.csv: with dunes removed
- Purpose: quantify how dunes alter depth-averaged and near-bed flow fields across the study section.

## Reproducibility, standards, and data management
- Clear documentation of data sources, processing steps, and modelling choices.
- Results stored as standard CSV files with explicit units and coordinate references.
- Datasets aligned with associated publication for traceability and reuse.
- Data management approach supports storage and sharing via appropriate environmental data portals.

## Relevance to environmental monitoring
- Demonstrates a reproducible approach to assess how bedforms influence flow structure and potential sediment transport in braided river systems.
- Provides a baseline to compare how morphological changes (dunes) affect velocity fields and depth, informing habitat and hydrodynamic assessments.

## Accessibility and integration
- Data and results are organized for integration with broader monitoring datasets and publications.
- Designed to enable others to access underlying data and reproduce analyses, supporting transparent environmental monitoring and policy evaluation.