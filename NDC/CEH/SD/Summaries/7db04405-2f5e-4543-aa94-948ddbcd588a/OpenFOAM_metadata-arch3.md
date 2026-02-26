# CFD results for dunes in the South Saskatchewan River

## Overview
- Dataset comprises results from Computational Fluid Dynamics (CFD) flow simulations for a section of the South Saskatchewan River, Canada.
- Two CSV files are provided: dune_results.csv (with dunes) and smooth_results.csv (dunes removed).
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
- Objective: investigate the effect of bedforms (dunes) on depth-averaged and near-bed flow fields.

## Data structure and content
- Each file contains seven columns:
  - Column 1: Model domain downstream (x) coordinate (m)
  - Column 2: Model domain cross-stream (y) coordinate (m)
  - Column 3: Model domain water depth (m)
  - Column 4: Depth-averaged downstream velocity (u, m/s)
  - Column 5: Near-bed downstream velocity (u, m/s)
  - Column 6: Depth-averaged cross-stream velocity (v, m/s)
  - Column 7: Near-bed cross-stream velocity (v, m/s)

## Methodology and data generation
- DEM and mesh development:
  - High-resolution digital elevation model (DEM) built from aerial imagery with 0.06 m pixel resolution.
  - DEM created from Structure-from-Motion (SfM) photogrammetry and a water-depth–brightness regression model.
  - SfM applied in emergent areas and along a gravel-rich bank; depth-brightness model used elsewhere.
  - Banks and bar fronts identified visually; masks produced to separate bar surfaces for filtering.
  - Dune removal performed on bar tops using a moving-average, weighted-mean filter (window 6 m × 1 m, downstream axis aligned with dune length).
  - Result: two DEMs for CFD meshes—one with dunes, one with dunes removed.
- CFD setup:
  - Solver: OpenFOAM (3D Navier–Stokes with RNG k–epsilon turbulence closure).
  - Surface: rigid-lid approximation.
  - Mesh: two structured finite-volume meshes (4948 × 1172 × 20 cells in downstream × cross-stream × vertical).
  - Horizontal resolution: ~8 cm; vertical: 20 cells; planar water surface at 0 m depth.
  - Inlet: measured flow velocities; outlet: Neumann pressure condition.
  - Numerical schemes: second-order for gradients and bounded central differencing for divergence; second-order deferred corrected for Laplacian surface normals.
  - Convergence criteria: pressure tolerance 1×10^-8; velocity, k, epsilon tolerances 1×10^-10.
  - Outputs: dune_results.csv (with dunes) and smooth_results.csv (dunes removed).

## Context and publication
- Related publication: Strick, RJP et al. 2019. Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery (Earth Surface Processes and Landforms). DOI: 10.1002/esp.4558.
- The dataset supports evaluating how bedforms influence flow fields, contributing to understanding bedform dynamics and sediment transport in braided river systems.

## Data provenance and accessibility
- Data were produced by a team of researchers and shared as two CSV files with detailed metadata describing geometry, flow fields, and near-bed versus depth-averaged velocities.
- The documentation outlines the data generation workflow, from high-resolution DEM construction to dune-removal processing and CFD modeling, facilitating reproducibility.

## Relevance to monitoring frameworks
- Demonstrates a structured approach to generating environmental performance indicators from process-based modeling (CFD) to assess geomorphic features (dunes) and their impact on river hydrodynamics.
- Highlights the importance of:
  - Comprehensive metadata (data provenance, processing steps, and model parameters).
  - Versioning and comparing alternative scenarios (with vs. without dunes) to isolate effects.
  - Open sharing of underlying data and results to support scrutiny and policy-informed decisions.
  - Clear documentation of data quality and convergence criteria to ensure confidence in findings.

## Challenges and considerations for monitoring
- High data resolution and complex preprocessing (DEM creation, dune removal) introduce potential sources of error and require careful documentation.
- The need to balance data sharing with quality assurance, metadata completeness, and reproducibility.
- Ensuring accessibility of model inputs, parameters, and processing steps to enable reuse in monitoring frameworks.