# Inputs for wildfire simulations in Fire Dynamics Simulator (FDS) in forest environments

## Overview
- Dataset supporting wildfire modelling in FDS for forest environments.
- Includes five LAS point clouds for different fuel classes on a 40×40 m Pinus ponderosa plot, BDF bulk density files, and three FDS input files for separate simulations.
- Aims to enable researchers and practitioners to simulate fire behaviour and evaluate the impact of fuel configurations and treatments.

## Data components

- LAS Files
  - five .las files representing segmented fuel classes on the forest plot:
    - grass_crop.las
    - shrub_crop.las
    - wood_crop.las (tree stem)
    - leaf_crop.las (tree branch + leaves)
    - leaf_crop_high.las (tree branch + leaves after virtual treatment)
  - Captured with Riegl-VZ400i TLS in Sycan Marsh, Oregon (40×40 m plot).
  - LAS follows ASPRS specification for broad compatibility.

- BDF (Bulk Density Files)
  - For each LAS, a corresponding BDF file encodes bulk density values per voxel (10 cm voxel size).
  - BDFs are Fortran unformatted binaries, stored as 2D arrays to reduce file size.
  - Bulk density values mapped to vegetation types using generic values from McGrattan et al. (2013).

- FDS (Fire Dynamics Simulator) Input Files
  - simulation_1.fds: wildfire simulation configuration for the base scenario.
  - simulation_2.fds: wildfire simulation after applying the virtual pruning treatment.
  - simulation_3.fds: a very high-resolution wildfire simulation.

## Site and data collection details

- Site: Sycan Marsh preserve, Klamath Basin, Oregon, USA (over 8000 hectares; diverse wetlands and forest).
- Plot: 40×40 m Pinus ponderosa forest segment within the preserve.
- Data collection window: 2019-07-08 to 2019-07-12.
- Instrumentation: RIEGL-VZ400i TLS, 750 kHz sampling rate, vertical sampling density 0.21 degrees, height ≥1.5 m, max range ~2000 m.
- Data segmentation: four fuel classes (grass, leaves, shrub, wood) with an additional virtual leaf treatment; segmentation performed using custom deep learning algorithms (code available at https://github.com/3DFin).

## Processing and preparation

- Bulk density files created by a modified python script (based on FDS User Guide 17.2.2). Original 3D arrays were converted to 2D arrays to reduce size.
- Virtual treatment: pruning represented by removing all leaf points within 3 meters of the ground to reduce vertical fuel continuity.
- FDS inputs include parameters for environmental conditions, fuel properties, and ignition points for three scenarios.

## How to use the data

- Prerequisites: Install Fire Dynamics Simulator (FDS) from NIST.
- Steps to run a simulation (example using simulation_1.fds):
  - Open a terminal and navigate to the folder containing the FDS files.
  - Run: fds_local simulation_1.fds
  - After completion, view outputs (3D visualizations, logs) with Smokeview: smokeview simulation_1
  - Documentation and usage details are available in the FDS-SMV manuals.

## Additional notes

- The dataset provides cross-linked resources for data preparation and analysis, including a GitHub repository for the segmentation methods used to classify fuel classes.
- References: McGrattan et al. (2013) Fire Dynamics Simulator Users Guide (NIST SP 1019).