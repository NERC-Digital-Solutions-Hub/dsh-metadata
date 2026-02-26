Outburst flood simulations of various dam failure scenarios from Tsho Rolpa glacial lake, Nepal, 2020: supporting document

## Overview
- Creates GLOF scenarios for Tsho Rolpa Lake using a simple dam breach model combined with a high-performance 2-D hydrodynamic model.
- Produces dam breach flow results for 12 GLOF scenarios and 2-D flood hydrodynamics results for the worst-case scenario.
- Location: downstream area of Tsho Rolpa Lake (27°30′–27°51′ N, 86°10′–86°29′ E); map projection: WGS 1984 Transverse Mercator.

## Data contents and scope
- Data files: 1 CSV file (Breach_flow_under_different_GLOF_scenarios) and 24 TIFF files (12 max water depth maps, 12 max water velocity maps for each scenario).
- CSV structure: 25 columns total; first column Time (s); next 12 columns = water depth for each scenario; final 12 columns = discharge for each scenario.
- TIFFs: 12 files for maximum depth (one per scenario) and 12 files for maximum velocity (one per scenario).

## Methods: collection and modeling
- Numerical modeling method: 2-D depth-averaged shallow water equations (SWEs) solved with a finite volume Godunov-type scheme featuring automatic shock-capturing.
- Governing equations include water depth, unit-width discharges, bed slope, and bed roughness (Manning coefficient).
- Computational approach: parallelized high-performance computing on GPUs using NVIDIA CUDA.

## Calibration and validation
- No validation performed; model emphasizes mass and momentum conservation with minimal parameters.
- Calibration steps are not described; reliance on prior successful applications rather than new validation.

## Analytical methods
- Maximum water depth and maximum flow velocity for each scenario are extracted from the time-series results of the hydrodynamic simulations.

## Nature and units of data
- Water depth: meters.
- Flow velocity: meters per second.

## Data quality and governance
- Quality control notes indicate no validation was conducted.
- Metadata details provided within the dataset description (e.g., file names, column meanings) but no external metadata governance described.

## Data structure details
- CSV file: 25 columns (Time; 12 depth columns; 12 discharge columns).
- TIFF files: 24 total (12 depth maps, 12 velocity maps corresponding to the 12 scenarios).
- Spatial context: downstream region of the lake; projection and coordinates specified.

## Geospatial and visualization context
- Downstream area coordinates and the projection are specified; Figure 1 illustrates maximum inundation depth and maximum flow velocity for the worst-case scenario.