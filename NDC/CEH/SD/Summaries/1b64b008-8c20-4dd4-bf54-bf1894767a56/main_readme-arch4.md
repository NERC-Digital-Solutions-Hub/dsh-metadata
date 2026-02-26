# The dataset herein is the source code and inputs required to reproduce the 3D volumetric data describing the energy density of photons with a simulated environment and the heatmaps and journey lengths for ensembles of weighted random walkers experiencing the specific simulated environments. This documentation will a) explain the contents of this deposited dataset, and b) provide a walkthrough of the steps to reproduce the outputs used in the publication the accompanying publication.

## Overview
- A deposit of materials to reproduce the outputs of the publication “Changing streetlighting schemes and the ecological availability of darkness.”
- Contains source code, configuration data, and scripts to run Monte Carlo radiative transfer simulations and weighted random walks within a specified simulated environment.
- Aimed at enabling end-to-end reproducibility, including data inputs, software builds, and execution steps.

## What is Included
- The input data for the Monte Carlo Radiative Transfer (MCRT) code, including:
  - Configuration files
  - Spectra (.json5)
  - Photometric data for luminaires (.ldt)
  - Geometry (.obj)
- The MCRT solver and library:
  - Aetherus (0.2.0) Rust source code (as .rs)
- The grid_walker code (v0.1.0) used for weighted random walks:
  - Snapshot of its source code
- A scripts directory containing automation tools to reproduce results

## External Dataset Requirements
- LiDAR data from the Defra National LIDAR Programme 2020 1m
  - Tile: national_lidar_programme_dtm-2020-1-SX99sw
  - File name: DTM_SX9090_P_10601_20200322_20200322.tif
  - Associated .tfw metadata file
- These files must be placed in the root directory of the dataset to reproduce results

## Setup and Dependencies

### External Datasets
- Ensure LiDAR data is available and accessible as specified, including the DTM TIFF and world file (.tfw)

### Monte Carlo Radiative Transfer Solver (MCRT)
- Prerequisites:
  - Rust toolchain (Rust 1.68.1)
  - libnetcdf v4.6.0
  - libpng v1.5.13
- Build steps:
  - tar -zxvf aetherus-0.2.0.tar.gz inside the mcrt directory
  - cd Aetherus-0.2.0
  - cargo build
  - The MCRT binary is located at target/debug/mcrt
- Testing:
  - Run cargo test
- Reference/README:
  - Aetherus-0.2.0/aetherus-0.2.0-README.md

### Weighted Random Walking Code
- Prerequisites:
  - Python 3.10.12
- Setup:
  - tar -zxvf grid_walker-0.1.0.tar.gz
  - cd grid_walker-0.1.0
  - python -m venv venv
  - source venv/bin/activate
  - pip install -r requirements.txt
- Documentation:
  - grid_walker-0.1.0/grid_walker-0.1.0-README.md

## Reproducing the Outputs

### Run MCRT Scenarios
- Lighting scenarios are in in/lights
- Run all scenarios:
  - ./scripts/run_scenarios.sh ./in/lights/ ./in/template.main.json5
- Outputs are deposited into the out/ directory

### Extract Isoheight Planes
- After simulations, extract 2D planes from voxel data at isoheights 0m, 4m, and 10m:
  - ./scripts/extract_scenario_isoheights.sh ./out/*/energy_density.nc
- Python environment setup for this step is prepared in:
  - scripts/venv

### Generate Random Walks
- Change to isoheight_planes and run:
  - ../grid_walker-0.1.0/scr/run_all.sh ../in/grid_walker.template.toml
- Resulting random-walk data is available in:
  - isoheight_planes/walk/

## Outputs and Accessibility
- Primary outputs used in the associated publication are produced in:
  - out/ (MCRT results and related data)
  - isoheight_planes/walk/ (random-walk results)
- The workflow provides traceability from input data to final results, via versioned code and configuration files

## Contact and Publication
- For questions regarding usage, contact Sam Morrell at:
  - s.a.f.morrell@exeter.ac.uk
- Publication reference:
  - “Changing streetlighting schemes and the ecological availability of darkness” (DOI to follow)

## Data Governance and Reproducibility Considerations
- The deposit emphasizes end-to-end reproducibility with explicit versioning (Aetherus 0.2.0, grid_walker 0.1.0) and environment setup (Rust 1.68.1, Python 3.10.12).
- External data access relies on the specified LiDAR tile and its metadata; access permissions and licensing should be considered for downstream use.
- Clear sequencing of steps (build → configure → run → extract → walk) supports governance of the data workflow and potential cross-institution collaboration.