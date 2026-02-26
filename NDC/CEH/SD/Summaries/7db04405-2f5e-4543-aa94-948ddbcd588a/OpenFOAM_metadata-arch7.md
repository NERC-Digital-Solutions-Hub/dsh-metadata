# Discovery metadata:

- Overview: This dataset contains the results of Computational Fluid Dynamics (CFD) flow simulations for a section of the South Saskatchewan River, Canada, focusing on the impact of dunes on depth-averaged and near-bed flow fields. Two CFD result files are provided, each in CSV format with seven columns of data.
- Data files: dune_results.csv and smooth_results.csv
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth
- Context: The CFD simulations compare high-resolution dune-inclusive morphology with a dune-removal morphology to assess how bedforms influence flow characteristics.

## Data files and structure

- Each file contains seven columns:
  - Column 1: Model domain downstream (x) coordinate (m)
  - Column 2: Model domain cross-stream (y) coordinate (m)
  - Column 3: Model domain water depth (m)
  - Column 4: Depth-averaged velocity component in downstream (x) direction (m/s)
  - Column 5: Near-bed velocity component in downstream (x) direction (m/s)
  - Column 6: Depth-averaged velocity component in cross-stream (y) direction (m/s)
  - Column 7: Near-bed velocity component in cross-stream (y) direction (m/s)

## Data sources and creation

- Digital elevation model (DEM) construction:
  - Source: Specially commissioned aerial imagery
  - Resolution: 0.06 m pixel size
  - Acquisition: ~1500 m altitude, fixed-wing aircraft with UltraCamXp sensor
  - DEM generation: A combination of Structure-from-Motion (SfM) photogrammetry ( Pix4D) and a depth-brightness regression model
  - Coverage: Emergent areas and a gravel-dominated bank section
  - DEM merging: SfM-derived DEMs merged with depth-brightness model outputs to produce a single DEM for CFD meshing
- Dune removal process (to create the “smooth” morphology):
  - Banks and bar fronts identified visually in ARCMAP; raster masks created to isolate bar surfaces
  - Dunes removed from bar tops using a moving-average, weighted-mean filter
  - Filter window: 6 m x 1 m, longest axis in the downstream (dune-length) direction
  - Banks and bar lee slopes preserved; dune topography removed only from bars
- CFD mesh generation:
  - Meshes: Two structured finite-volume meshes (one dune-inclusive, one dune-removed)
  - Dimensions: 4948 x 1172 x 20 cells (downstream x cross-stream x vertical)
  - Horizontal resolution: ~8 cm
  - Vertical resolution: 20 cells; planar water surface at 0 m depth
- CFD modelling details:
  - Solver: OpenFOAM
  - Governing equations: Three-dimensional Navier–Stokes
  - Turbulence model: RNG k-ε
  - Free surface: Rigid-lid approximation
  - Inlet conditions: Measured flow velocities
  - Outlet: Neumann pressure condition
  - Numerical schemes: Second-order central differencing (gradients), second-order bounded central differencing (divergence), and an unbounded second-order deferred correction for Laplacian surface normal gradients
  - Convergence criteria: 1×10^-8 for pressure; 1×10^-10 for velocity, k, and ε
  - Solver tolerances: 1×10^-10 for pressure; 1×10^-12 for velocity

## Data provenance and related research

- Publication: Strick, RJP et al. (2019). Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery. Earth Surface Processes and Landforms, doi:10.1002/esp.4558.

## Potential GIS usage and considerations

- Map-like data products: The two CSVs enable spatial mapping of depth and velocity fields across the study reach, with direct comparison between dune-inclusive and dune-removed scenarios.
- Integration opportunities: Combine with the 0.06 m DEM-derived terrain layers and bank/bar morphology for advanced visualizations of flow alteration due to bedforms.
- Considerations:
  - Ensure coordinate reference system alignment between CFD outputs and GIS layers.
  - Interpret depth- and velocity-related data in the context of the dune presence/absence scenario.
  - Use the DEM and mask-derived dune removal workflow to reproduce or extend analyses in similar braided river environments.