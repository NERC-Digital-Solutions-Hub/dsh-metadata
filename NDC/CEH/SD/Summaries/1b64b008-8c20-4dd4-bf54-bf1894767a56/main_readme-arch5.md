# The dataset herein is the source code and inputs required to reproduce the 3D volumetric data describing the energy density of photons with a simulated environment and the heatmaps and journey lengths for ensembles of weighted random walkers experiencing the specific simulated environments. This documentation will a) explain the contents of this deposited dataset, and b) provide a walkthrough of the steps to reproduce the outputs used in the publication the accompanying publication.

## Overview
- This deposit documents three components and supporting resources used to reproduce outputs in the publication “Changing streetlighting schemes and the ecological availability of darkness.”
- Contact for usage questions: Sam Morrell (s.a.f.morrell@exeter.ac.uk).
- Publication DOI to follow.

## Dataset components
- Component 1: Input data for the Monte Carlo Radiative Transfer (MCRT) code
  - Configuration files, spectra (.json5), photometric data for luminaires (.ldt), and geometry (.obj).
- Component 2: MCRT solver and library
  - Aetherus (Rust) code used to generate outputs (version 0.2.0) with its supporting library; provided as Rust source (.rs).
- Component 3: Grid_walker code
  - Snapshot of the grid_walker code used to perform weighted random walks (version 0.1.0).
- Component 4: Automation scripts
  - Directory of scripts (scripts) to automate steps required to reproduce results.

## What the dataset reproduces
- Outputs used in the publication titled “Changing streetlighting schemes and the ecological availability of darkness.”
- Includes 3D volumetric energy-density data for photons, heatmaps, and journey lengths for ensembles of weighted random walkers under the simulated environments.

## Reproducibility workflow and setup

### Prerequisites and dependencies
- Monte Carlo Radiative Transfer (MCRT) solver
  - Rust compiler toolchain (Rust 1.68.1)
  - Libraries: libnetcdf (v4.6.0), libpng (v1.5.13)
- Weighted random walking code
  - Python 3 (Python 3.10.12)
  - Virtual environment setup (venv) and dependencies from requirements.txt
- Documentation files and readmes are provided in the code repositories:
  - Aetherus-0.2.0/aetherus-0.2.0-README.md
  - grid_walker-0.1.0/grid_walker-0.1.0-README.md

### Reproducing the outputs (high-level steps)
1. External data setup
   - Obtain LiDAR data from the Defra National LIDAR Programme 2020 1m (tile: national_lidar_programme_dtm-2020-1-SX99sw).
   - Download and place the DTM_SX9090_P_10601_20200322_20200322.tif and its accompanying .tfw in the dataset root.
   - Access to the LiDAR data is via provided URLs; include the tile in the root directory as specified.
2. Compile the MCRT solver
   - Install Rust toolchain (Rust 1.68.1).
   - Ensure libraries libnetcdf v4.6.0 and libpng v1.5.13 are available.
   - Decompress and build:
     - tar -zxvf aetherus-0.2.0.tar.gz
     - cd Aetherus-0.2.0
     - cargo build
   - The MCRT binary will be at target/debug/mcrt; unit tests can be run with cargo test.
3. Prepare the weighted random walking code
   - Install Python and create a virtual environment:
     - tar -zxvf grid_walker-0.1.0.tar.gz
     - cd grid_walker-0.1.0
     - python -m venv venv
     - source venv/bin/activate
     - pip install -r requirements.txt
   - See grid_walker-0.1.0/grid_walker-0.1.0-README.md for configuration options.
4. Reproduce outputs
   - Run all lighting scenarios:
     - scripts/run_scenarios.sh ./in/lights/ ./in/template.main.json5
     - Outputs will be deposited into out/
   - Extract 2D isoheight planes (0 m, 4 m, 10 m):
     - ./scripts/extract_scenario_isoheights.sh ./out/*/energy_density.nc
     - This sets up a Python environment in scripts/venv.
   - Generate random walks from isoheight planes:
     - cd isoheight_planes
     - ../grid_walker-0.1.0/scr/run_all.sh ../in/grid_walker.template.toml
     - Results will be in isoheight_planes/walk/
5. Documentation and validation
   - Consult the included READMEs for detailed configuration and validation notes:
     - Aetherus-0.2.0/aetherus-0.2.0-README.md
     - grid_walker-0.1.0/grid_walker-0.1.0-README.md

## Data governance, access, and provenance

- Provenance
  - The dataset bundles input data, executable code (Rust and Python), and scripts used to reproduce publication results.
  - Versions are specified: MCRT solver (Aetherus) v0.2.0, grid_walker v0.1.0, Python 3.10.12, and Rust 1.68.1.
- Access and licensing
  - Publication with DOI to follow; usage questions directed to Sam Morrell.
  - External data (Defra LiDAR) required via provided URLs; access terms are governed by the LiDAR data source.
- Metadata and documentation
  - Reproducibility is supported by included README files, unit tests, and explicit build/run commands.
  - Outputs are organized under out/ and the random-walk results under isoheight_planes/walk/.
- Data quality and governance considerations for stewardship
  - Clear versioning and source-code provenance support auditability.
  - Large, multi-component workflow with cross-language tooling and external data dependencies; requires careful environment management.
  - Documentation provides explicit setup, build, and execution steps to ensure consistent re-use.

## Summary for data stewardship

- Comprehensive reproducibility package including inputs, executables (source), and automation scripts to reproduce the publication outputs.
- Clear dependencies and environment requirements across Rust and Python components, with specific versioning.
- External data dependencies (Defra LiDAR) documented with retrieval URLs and tile/file naming; governance depends on LiDAR data terms.
- Structured workflow from data preparation to simulation to isoheight extraction to random-walk analysis, with outputs stored in dedicated directories.
- Contact and publication linkage provided to facilitate usage queries and alignment with the associated study.