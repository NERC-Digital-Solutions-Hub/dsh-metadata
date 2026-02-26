# Discovery metadata: Files: dune_results.csv smooth_results.csv

- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth
- Data scope: Results from Computational Fluid Dynamics (CFD) flow simulations for a section of the South Saskatchewan River, Canada
- Data files:
  - dune_results.csv
  - smooth_results.csv
  - Each file contains seven columns of data (see below)

## Data structure and variables

- Columns (per file):
  - Column 1: Model domain downstream (x) coordinate, meters
  - Column 2: Model domain cross-stream (y) coordinate, meters
  - Column 3: Model domain water depth, meters
  - Column 4: Depth-averaged velocity component in downstream (x) direction, meters per second
  - Column 5: Near-bed velocity component in downstream (x) direction, meters per second
  - Column 6: Depth-averaged velocity component in cross-stream (y) direction, meters per second
  - Column 7: Near-bed velocity component in cross-stream (y) direction, meters per second

## Context and aim

- Purpose: Investigate the effect of dunes on depth-averaged and near-bed flow fields
- Approach: Two CFD meshes were used
  - One with high-resolution DEM including dunes
  - One with dune-scale morphology removed
- Geospatial context: South Saskatchewan River, Canada
- Publication link: Strick, RJP et al. 2019, Earth Surface Processes and Landforms (doi:10.1002/esp.4558)

## Data creation and provenance

- Digital elevation model (DEM) construction:
  - Source imagery: aerial photography at 0.06 m pixel resolution from ~1500 m height
  - Techniques:
    - Structure-from-Motion (SfM) photogrammetry (via Pix4D) for emergent areas and a gravel-dominated river bank section
    - Depth-brightness model used to estimate water depth from image brightness in other areas
  - DEM merging to form a single model domain for CFD meshing
- Dune removal process:
  - Banks and bar fronts outlined in ARCMAP; masks created to preserve banks/bar lee slopes
  - Dune removal on bar tops using a moving-average, weighted-mean filter (window 6 m x 1 m, downstream axis)
- CFD modelling:
  - Software: OpenFOAM
  - Governing equations: three-dimensional Navier–Stokes with RNG k-ε turbulence model
  - Free surface: represented with rigid-lid approximation
  - Inlet: measured flow velocities
  - Outlet: Neumann pressure condition
  - Numerical schemes: second-order central differences (gradients), bounded central differences (divergence), unbounded second-order deferred corrected for surface-normal gradients
  - Convergence criteria: pressure tolerance 1e-8; velocity, k, ε tolerances 1e-10
  - Solver tolerances: pressure 1e-10; velocity 1e-12

## Mesh and numerical details

- CFD mesh characteristics:
  - Two structured, finite-volume meshes
  - Dimensions: 4948 x 1172 x 20 cells (downstream x cross-stream x vertical)
  - Horizontal resolution: ~8 cm
  - Vertical resolution: 20 cells; planar water surface at 0 m depth
- Simulation runs:
  - Dune_results.csv: results with dunes present (high-resolution DEM)
  - Smooth_results.csv: results with dunes removed from the topography

## Data quality, limitations, and considerations

- Limitations and caveats:
  - Free-surface dynamics approximated with rigid-lid approximation
  - Inlet conditions based on measured velocities; outlet with Neumann pressure
  - DEM and dune-removal procedures introduce preprocessing steps that affect flow fields
  - Dataset reflects two specific model setups (with and without dunes) for a single river section
- Documentation and reproducibility:
  - Comprehensive description of data creation, preprocessing, and modelling steps included
  - Clear definitions of each variable and unit conventions
  - Related publication provides methodological context and validation

## Access, licensing, and reuse

- Data accessibility: Discovery metadata indicates availability of two .csv result files
- Related materials:
  - Publication: Strick, RJP et al. 2019
  - DOI: 10.1002/esp.4558
- Suggested reuse considerations:
  - Use alongside publication for interpretation and reproducibility
  - Cite both the dataset and the Strick et al. (2019) paper
  - Acknowledge preprocessing steps (DEM creation methods, dune-removal filter) when reusing results

## Governance and stewardship notes for Data Stewards

- Provenance and traceability:
  - Clear authorship and data lineage from DEM construction to CFD results
  - Linkage to publication facilitates reproducibility and provenance tracking
- Metadata completeness:
  - Detailed variable definitions, units, and methodological context are provided
  - Ensure continued accessibility of both files and the associated metadata
- Data quality management:
  - Document modelling assumptions (rigid-lid, RNG k-ε, solver tolerances)
  - Maintain records of dune-removal technique and mask creation to support future updates or reprocessing
- Preservation planning:
  - Store both dune and smooth datasets together with their identical structure for comparability
  - Preserve links to DEM construction methods and source imagery metadata
- User guidance:
  - Provide clear description of how to interpret YAML/CSV fields and how the two scenarios differ
  - Include notes on limitations when applying results to other river reaches or conditions