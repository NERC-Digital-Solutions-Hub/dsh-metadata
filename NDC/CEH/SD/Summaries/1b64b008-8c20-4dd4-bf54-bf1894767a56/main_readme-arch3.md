The dataset herein is the source code and inputs required to reproduce the 3D volumetric data describing the energy density of photons with a simulated environment and the heatmaps and journey lengths for ensembles of weighted random walkers experiencing the specific simulated environments.

## Overview
- Delivers the full chain to reproduce outputs used in the publication about streetlighting and darkness.
- Comprises three components plus a scripts directory to automate tasks.
- Requires an external LiDAR dataset; publication details are provided, with a contact for usage questions.

## Components of the Deposit
- Input data for the Monte Carlo Radiative Transfer (MCRT) code, including:
  - Configuration files
  - Spectra (.json5)
  - Photometric data for luminaires (.ldt)
  - Geometry (.obj)
- MCRT solver and library:
  - Aetherus 0.2.0 (Rust source code)
  - The MCRT code and dependencies (libnetcdf v4.6.0, libpng v1.5.13)
- Weighted random walking code:
  - grid_walker-0.1.0 (snapshot of code used for weighted random walks)
- Automation scripts:
  - A scripts directory containing tools to reproduce results
- External dataset (required for reproduction):
  - LiDAR data from Defra National LIDAR Programme 2020 1m
  - Tile: national_lidar_programme_dtm-2020-1-SX99sw
  - Files: DTM_SX9090_P_10601_20200322_20200322.tif and accompanying .tfw
  - Location and access details provided in the setup notes

## Reproduction Workflow
- Build and test the MCRT solver:
  - Requires Rust toolchain (Rust 1.68.1)
  - Libraries: libnetcdf 4.6.0, libpng 1.5.13
  - Steps: tar -zxvf aetherus-0.2.0.tar.gz, cd into Aetherus-0.2.0, cargo build
  - Run unit tests with cargo test
  - README at Aetherus-0.2.0/aetherus-0.2.0-README.md
- Prepare and run the weighted random walker code:
  - Requires Python 3.10.12
  - Setup virtual environment:
    - tar -zxvf grid_walker-0.1.0.tar.gz
    - cd grid_walker-0.1.0
    - python -m venv venv
    - source venv/bin/activate
    - pip install -r requirements.txt
  - Documentation: grid_walker-0.1.0/grid_walker-0.1.0-README.md
- Reproduce outputs:
  - Run MCRT scenarios:
    - Directory with scenarios: in/lights
    - Script: scripts/run_scenarios.sh
    - Command: ./scripts/run_scenarios.sh ./in/lights/ ./in/template.main.json5
  - Outputs are deposited into out/
  - Extract isoheight planes (0m, 4m, 10m) from voxel data:
    - Script: scripts/extract_scenario_isoheights.sh ./out/*/energy_density.nc
    - Note: sets up Python environment in scripts/venv
  - Compute random walks from isoheights:
    - Change to isoheight_planes
    - Run: ../grid_walker-0.1.0/scr/run_all.sh ../in/grid_walker.template.toml
  - Outputs of random walks are located in isoheight_planes/walk/

## Setup Details and Dependencies
- External LiDAR data:
  - Defra National LIDAR Programme 2020 1m
  - Tile: national_lidar_programme_dtm-2020-1-SX99sw
  - Access: provided URL and tile details; requires placement of DTM_SX9090_P_10601_20200322_20200322.tif and .tfw in dataset root
- MCRT setup:
  - Rust toolchain from rustup (recommended: Rust 1.68.1)
  - Libraries: libnetcdf v4.6.0, libpng v1.5.13
- Python setup:
  - Python 3.10.12
  - Virtual environment and dependencies managed via requirements.txt in grid_walker

## Publication and Contact
- Outputs used in the publication: Changing streetlighting schemes and the ecological availability of darkness (DOI to follow)
- For questions regarding usage: Sam Morrell (s.a.f.morrell@exeter.ac.uk)