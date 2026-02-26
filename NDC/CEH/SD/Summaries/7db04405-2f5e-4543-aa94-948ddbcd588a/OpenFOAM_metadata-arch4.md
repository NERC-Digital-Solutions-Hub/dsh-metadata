# Discovery metadata: Files: dune_results.csv smooth_results.csv

## Summary
- Presents two Computational Fluid Dynamics (CFD) simulations for a section of the South Saskatchewan River, Canada, to investigate the effect of dunes on depth-averaged and near-bed flow fields.
- Compares a high-resolution dune-inclusive mesh with a dune-removed (smoothed) mesh to assess how dune morphology influences flow.

## Data Description
- Files:
  - dune_results.csv (includes results with dunes)
  - smooth_results.csv (includes results with dunes removed)
- Each file contains seven columns:
  1) Model domain downstream (x) coordinate in meters
  2) Model domain cross-stream (y) coordinate in meters
  3) Modelled water depth in meters
  4) Depth-averaged velocity component in downstream (x) direction (m/s)
  5) Near-bed velocity component in downstream (x) direction (m/s)
  6) Depth-averaged velocity component in cross-stream (y) direction (m/s)
  7) Near-bed velocity component in cross-stream (y) direction (m/s)

## Data Provenance and Context
- Aim: quantify how bedforms (dunes) affect flow fields using two CFD meshes (with and without dunes).
- Model setup:
  - 3D Navier–Stokes equations solved with OpenFOAM using RNG k-epsilon turbulence closure.
  - Free surface represented by a rigid-lid approximation.
  - Inlet conditions defined from measured flow velocities; Neumann condition at outlet.
  - Two structured CFD meshes: 4948 x 1172 x 20 cells (downstream x cross-stream x vertical).
  - Horizontal resolution ~8 cm; vertical resolution 20 cells; planar water surface at 0 m depth.
- DEM and data generation:
  - DEM resolution: 0.06 m, built from aerial imagery using Structure-from-Motion (SfM) photogrammetry and depth-brightness modeling.
  - SfM applied in emergent areas and a gravel river-bed section; depth-brightness model used elsewhere.
  - Dunes removed from the topography via visual bank/bar outline masking and a moving-average filter (6 m x 1 m, longest axis downstream) to create a dune-removed topography.
- Data production: two CFD meshes created (one with dunes, one with dunes removed) and simulations executed to produce the two result files.

## Data Quality, Metadata, and Reuse
- Metadata includes authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
- Contextual metadata describes the modeling decisions, DEM construction, dune removal method, and numerical settings.
- Related publication for methodology and results: Strick, RJP et al. (2019) Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery. Earth Surface Processes and Landforms, doi:10.1002/esp.4558.
- Licensing and data access details are not specified in the provided metadata.

## Modeling Details and Technical Notes
- Software: OpenFOAM (Open Source CFD).
- Turbulence: RNG k-epsilon closure.
- Free surface: rigid-lid approximation.
- Numerical schemes: second-order spatial gradients; second-order bounded central differencing for divergence; unbounded second-order deferred corrected scheme for Laplacian surface normal gradients.
- Convergence criteria: pressure 1e-8, velocity/k/epsilon 1e-10; solver tolerances: pressure 1e-10, velocity 1e-12.
- Inlet/outlet conditions: measured velocities (inlet); Neumann pressure (outlet).

## Potential Uses and Alignment with Data Leader Aims
- Enables assessment of data products (flow fields) derived from a high-resolution, dune-inclusive DEM versus a dune-removed DEM.
- Supports evaluation of data system aspects important to data leaders:
  - Clear data structure (CSV files with defined 7-column schema) and explicit physical units.
  - Thorough provenance and method metadata (DEM construction, dune removal process, CFD settings).
  - Alignment with broader data workflows (co-ownership of data quality and applicability to policy or research questions about river dynamics).
- Useful for researchers and practitioners evaluating data discoverability, reproducibility, and reuse in riverine CFD studies.

## Gaps and Considerations for Data Leaders
- Licensing details are not provided; clarify data rights and reuse permissions.
- No explicit data quality metrics beyond convergence tolerances; consider adding validation or uncertainty assessments.
- Metadata is detailed on technical methods but could be augmented with data lineage and versioning information for future updates.
- Potential for integration with broader data ecosystems (e.g., linking to the Strick et al. publication, linking to repository DOIs, adding metadata on data stewardship roles).

## Related Publication
- Strick, RJP et al. (2019). Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery. Earth Surface Processes and Landforms. DOI: 10.1002/esp.4558.