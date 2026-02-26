# The dataset herein is the source code and inputs required to reproduce the 3D volumetric data describing the energy density of photons with a simulated environment and the heatmaps and journey lengths for ensembles of weighted random walkers experiencing the specific simulated environments. This documentation will a) explain the contents of this deposited dataset, and b) provide a walkthrough of the steps to reproduce the outputs used in the publication the accompanying publication.

- This deposit provides everything needed to reproduce the article’s outputs related to 3D photon energy density, heatmaps, and random-walker trajectories in simulated environments.
- The materials are organized into three components plus automation scripts, enabling end-to-end replication of results used in the publication.

## Dataset contents

- Input data for the Monte Carlo Radiative Transfer (MCRT) code:
  - Configuration files
  - Spectra (.json5)
  - Photometric data for luminaires (.ldt)
  - Geometry (.obj)
- The MCRT solver and library:
  - Aetherus (Rust) used to generate outputs (0.2.0) with source code (.rs)
- Grid walker code:
  - Grid_walker (v0.1.0) source code for weighted random walks
- Automation scripts:
  - Directory named scripts to automate reproduction tasks

- Publication reference:
  - Outputs used in the publication “Changing streetlighting schemes and the ecological availability of darkness” (DOI forthcoming)
- Contact for usage questions:
  - Sam Morrell, s.a.f.morrell@exeter.ac.uk

## Reproducing the outputs (high level workflow)

- External data prerequisites:
  - LiDAR data: Defra National LIDAR Programme 2020 1m
  - Tile: national_lidar_programme_dtm-2020-1-SX99sw
  - File: DTM_SX9090_P_10601_20200322_20200322.tif and accompanying .tfw
  - Source: https://environment.data.gov.uk/survey and related tile URL
  - Place the LiDAR TIFF and .tfw in the dataset root

- MCRT solver setup and build:
  - Prerequisites: Rust toolchain (Rust 1.68.1)
  - Libraries: libnetcdf (v4.6.0), libpng (v1.5.13)
  - Build steps:
    - tar -zxvf aetherus-0.2.0.tar.gz in mcrt directory
    - cd into Aetherus-0.2.0 and run cargo build
  - Outputs:
    - Binary at target/debug/mcrt
  - Testing:
    - cargo test
  - Documentation:
    - README at Aetherus-0.2.0/aetherus-0.2.0-README.md

- Weighted random walking code setup:
  - Python 3 (target: 3.10.12)
  - Virtual environment setup and dependencies:
    - tar -zxvf grid_walker-0.1.0.tar.gz
    - cd grid_walker-0.1.0
    - python -m venv venv
    - source venv/bin/activate
    - pip install -r requirements.txt
  - Code reference:
    - grid_walker-0.1.0/grid_walker-0.1.0-README.md

- Running and reproducing outputs:
  - Reproduce lighting scenarios:
    - Location: in/lights
    - Script: scripts/run_scenarios.sh
    - Command: ./scripts/run_scenarios.sh ./in/lights/ ./in/template.main.json5
  - Outputs deposition:
    - Generated into out/ directory
  - Isoheight plane extraction:
    - Script: ./scripts/extract_scenario_isoheights.sh ./out/*/energy_density.nc
    - Note: sets up Python environment in scripts/venv
  - Random walk generation:
    - Change to isoheight_planes
    - Run: ../grid_walker-0.1.0/scr/run_all.sh ../in/grid_walker.template.toml
    - Outputs located at isoheight_planes/walk/

- Data products and storage:
  - Energy density and heatmaps produced in the out/ directory
  - Random-walk results stored in isoheight_planes/walk/

## Setup and prerequisites (summary)

- External data access:
  - LiDAR data from Defra National LIDAR Programme 2020 1m
  - Require access to specified tile and DTM TIFF/.tfw files and place in dataset root

- MCRT solver (Aetherus) setup:
  - Rust toolchain (Rust 1.68.1)
  - Libraries: libnetcdf v4.6.0, libpng v1.5.13
  - Build and test with cargo

- Grid walker (weighted random walking) setup:
  - Python 3.10.12
  - Virtual environment and dependencies from requirements.txt

- Reproduction workflow:
  - Run MCRT simulations for all lighting scenarios
  - Extract isoheight planes from voxel data
  - Run random walks on isoheight planes
  - Locate and interpret outputs in out/ and isoheight_planes/walk/

## Data provenance and accessibility

- The dataset is intended to enable transparent replication of the reported analyses and results in the published article.
- All steps—from data inputs to code execution and output generation—are documented with exact file paths, versions, and commands to facilitate auditing and reuse.
- If access issues arise or questions about usage occur, contact the author provided above.

## Publication reference

- Publication: Changing streetlighting schemes and the ecological availability of darkness
- DOI: to follow