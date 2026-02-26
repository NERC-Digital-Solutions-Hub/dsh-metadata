# The dataset herein is the source code and inputs required to reproduce the 3D volumetric data describing the energy density of photons with a simulated environment and the heatmaps and journey lengths for ensembles of weighted random walkers experiencing the specific simulated environments. This documentation will a) explain the contents of this deposited dataset, and b) provide a walkthrough of the steps to reproduce the outputs used in the publication the accompanying publication.

## Overview
- Purpose: A reproducibility deposit for the publication “Changing streetlighting schemes and the ecological availability of darkness,” containing code, data inputs, and scripts to reproduce the reported outputs.
- Structure: Four main components (inputs for MCRT, solver and library, grid_walker code, and automation scripts).
- Publication linkage: Outputs were used in the publication; a DOI will follow.
- Contact: Sam Morrell (s.a.f.morrell@exeter.ac.uk).

## Dataset contents (three main components)
- Input data for Monte Carlo Radiative Transfer (MCRT) code
  - Configuration files
  - Spectra (.json5)
  - Photometric data for luminaires (.ldt)
  - Geometry data (.obj)
- MCRT solver and library
  - Aetherus library and MCRT code used (0.2.0) provided as Rust source (.rs)
- Grid walker code
  - Snapshot of grid_walker source (v0.1.0) used to perform weighted random walks
- Automation scripts
  - Directory named scripts to automate reproduction steps

## Reproducing the outputs (workflow)
- External datasets
  - LiDAR data from Defra National LIDAR Programme 2020 (1m)
  - Tile: national_lidar_programme_dtm-2020-1-SX99sw
  - File: DTM_SX9090_P_10601_20200322_20200322.tif with accompanying .tfw
  - Place both files in the dataset root
- MCRT solver setup
  - Requires Rust toolchain (Rustup), tested with Rust 1.68.1
  - Libraries: libnetcdf v4.6.0, libpng v1.5.13
  - Build steps:
    - tar -zxvf aetherus-0.2.0.tar.gz
    - cd Aetherus-0.2.0
    - cargo build
  - Outputs located at target/debug/mcrt
  - Tests: cargo test
  - README: Aetherus-0.2.0/aetherus-0.2.0-README.md
- Weighted random walking code setup
  - Python 3.10.12
  - Setup virtual environment and dependencies:
    - tar -zxvf grid_walker-0.1.0.tar.gz
    - cd grid_walker-0.1.0
    - python -m venv venv
    - source venv/bin/activate
    - pip install -r requirements.txt
  - Documentation: grid_walker-0.1.0/grid_walker-0.1.0-README.md
- Reproducing outputs
  - Run MCRT simulations for all lighting scenarios
    - Location: in/lights
    - Command: ./scripts/run_scenarios.sh ./in/lights/ ./in/template.main.json5
  - Outputs generated to: out/
  - Extract 2D isoheight planes from voxel data at heights 0m, 4m, 10m
    - Command: ./scripts/extract_scenario_isoheights.sh ./out/*/energy_density.nc
    - Note: sets up Python environment in scripts/venv
  - Generate random walks from inputs
    - Navigate to isoheight_planes
    - Command: ../grid_walker-0.1.0/scr/run_all.sh ../in/grid_walker.template.toml
  - Outputs of random walks
    - Location: isoheight_planes/walk/

## Data management and outputs
- Data formats involved
  - Configuration and input data: .json5, .ldt, .obj
  - Energy density outputs: energy_density.nc (netCDF)
  - Isoheight plane data and walk results stored under isoheight_planes and out
- Reproducibility artifacts
  - Versioned code for MCRT (0.2.0) and grid_walker (0.1.0)
  - Scripts to automate scenario runs and post-processing
  - External LiDAR dataset required to reproduce scene geometry

## Access and contact
- For questions about usage of this resource, contact Sam Morrell at s.a.f.morrell@exeter.ac.uk