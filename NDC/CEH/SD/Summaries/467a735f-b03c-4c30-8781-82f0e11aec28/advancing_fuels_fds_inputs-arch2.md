# Summary

## Overview
- A dataset of inputs for wildfire simulations in Fire Dynamics Simulator (FDS) focused on a 40 x 40 m Pinus ponderosa forest plot in Sycan Marsh, Oregon, USA.
- Contains five segmented LAS point clouds representing different fuel classes, each with an associated Bulk Density File (BDF), plus three FDS input files for separate simulations.
- Purpose: support modelling and understanding fire behaviour in forest ecosystems.

## Data Formats and Components
- LAS (point clouds): five files representing fuel classes; acquired with a Riegl-VZ400i TLS in ASPRS LAS format.
  - grass_crop.las, shrub_crop.las, wood_crop.las, leaf_crop.las, leaf_crop_high.las (leaf class after virtual pruning)
- BDF (Bulk Density Files): Fortran unformatted binary files encoding bulk density values on a 10 cm voxel grid; each BDF corresponds to a LAS file and uses a voxelized 10 cm grid with density values in g/cm³.
- FDS (Fire Dynamics Simulator) input files: three text-based input files defining simulation configurations.
  - simulation_1.fds: baseline wildfire simulation
  - simulation_2.fds: simulation after applying virtual pruning
  - simulation_3.fds: very high-resolution simulation
- Virtual treatment: pruning to remove leaf points within 3 meters of the ground to reduce vertical fuel continuity.

## Site and Data Collection
- Site: Sycan Marsh Preserve, Klamath Basin, Oregon; extensive wetland with surrounding forest; study area within the preserve.
- Plot: 40 x 40 meters, Pinus ponderosa.
- Acquisition window: 2019-07-08 to 2019-07-12.
- Equipment: RIEGL-VZ400i terrestrial laser scanner (TLS) with 750 kHz sampling rate; vertical sampling density 0.21 degrees; mounted on a tripod at least 1.5 m high; max range 2000 m; near-infrared 1050 nm.

## Data Processing and Methods
- Point cloud segmentation: four primary fuel classes (grass, shrub, wood/tree stem, leaves) with an additional leaf class split after virtual treatment; segmentation performed using custom Deep Learning algorithms (code available at https://github.com/3DFin).
- Bulk Density Files creation: adapted Python script based on FDS User Guide (McGrattan et al., 2013); voxelized into 10 cm voxels; density values assigned per fuel type; BDF stored as a 2D array for efficiency.
- References for bulk density methodology: McGrattan et al. (2013) Fire Dynamics Simulator Users Guide.

## How to Use the Data
- Prerequisites: Install Fire Dynamics Simulator (FDS) from NIST.
- Steps:
  - Open a terminal and navigate to the directory containing the desired simulation_*.fds file.
  - Run the simulation with: fds_local simulation_1.fds (or corresponding file for other scenarios).
  - After completion, outputs such as 3D visualizations and data logs are generated.
  - View results with Smokeview: smokeview simulation_1.
- Documentation and guidance are aligned with FDS-SMV manuals and NIST resources linked in the dataset.

## Site Description
- Sycan Marsh Preserve: a significant wetland area (>8000 hectares) within the Klamath Basin, Oregon, featuring diverse landscapes that include marshes and forested areas, contributing to ecosystem variability.

## Notes on Reproducibility and Access
- Data integrate LAS, BDF, and FDS inputs to enable reproducible fire-impacts analyses.
- Deep Learning-based segmentation and a public code repository support reuse and extension of the methodologies.

## References
- McGrattan, K., McDermott, R., Weinschenk, C., and Forney, G. (2013). Fire Dynamics Simulator Users Guide, Sixth Edition, NIST SP. 
- Additional methodological context available via FDS-SMV documentation and related NIST resources.