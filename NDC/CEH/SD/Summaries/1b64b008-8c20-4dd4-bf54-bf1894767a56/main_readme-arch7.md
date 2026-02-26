# Changing streetlighting schemes and the ecological availability of darkness

- Overview
  - A dataset deposit intended to reproduce 3D volumetric energy density of photons in simulated environments, plus heatmaps and journey lengths for ensembles of weighted random walkers. It accompanies a publication on streetlighting and ecological darkness.
  - The repository contains input data, source code, and automation scripts to reproduce the publication outputs.

- What is included
  - Input data for the Monte Carlo Radiative Transfer (MCRT) code
    - Configuration files
    - Spectra (.json5)
    - Photometric data for luminaires (.ldt)
    - Geometry (.obj)
  - Monte Carlo Radiative Transfer solver and library
    - Aetherus (Rust) framework used to generate outputs (0.2.0), provided as Rust source (.rs)
  - Grid walker code
    - Weighted random walking code (grid_walker) snapshot (v0.1.0)
  - Automation scripts
    - A directory named scripts to reproduce results
  - Documentation references for the code and tests
    - README files for MCRT and grid_walker included in their respective directories

- External data required
  - LiDAR data from Defra National LIDAR Programme 2020 (1m)
  - Study tile: national_lidar_programme_dtm-2020-1-SX99sw
  - Data file: DTM_SX9090_P_10601_20200322_20200322.tif plus its .tfw georeference file
  - These files must be placed in the dataset root for reproduction

- Setup and requirements
  - Monte Carlo Radiative Transfer (MCRT) solver
    - Rust toolchain (Rust 1.68.1)
    - Libraries: libnetcdf (v4.6.0), libpng (v1.5.13)
    - Build steps: extract mcrt, enter Aetherus-0.2.0, run cargo build
    - Build outputs: target/debug/mcrt
    - Tests: cargo test; README at Aetherus-0.2.0/aetherus-0.2.0-README.md
  - Weighted Random Walking Code
    - Python 3.10.12
    - Virtual environment setup: tar zxvf grid_walker-0.1.0.tar.gz, python -m venv venv, source venv/bin/activate, pip install -r requirements.txt
    - Documentation: grid_walker-0.1.0/grid_walker-0.1.0-README.md

- Reproducing the outputs (workflow)
  - Run all MCRT lighting scenarios
    - Use scripts/run_scenarios.sh with input lights and a template configuration
    - Example: ./scripts/run_scenarios.sh ./in/lights/ ./in/template.main.json5
  - Output management
    - Outputs deposited into the out/ directory
  - Extract 2D isoheight planes from voxel data
    - Use Python script: ./scripts/extract_scenario_isoheights.sh ./out/*/energy_density.nc
    - This step sets up a Python environment at scripts/venv
  - Generate random walks from isoheight planes
    - Change to isoheight_planes directory
    - Run: ../grid_walker-0.1.0/scr/run_all.sh ../in/grid_walker.template.toml
    - Resulting walk data located in isoheight_planes/walk/

- Outputs and data formats
  - 3D volumetric data: energy density of photons in simulated environments
  - Heatmaps and journey lengths for ensembles of weighted random walkers
  - 2D isoheight planes extracted from voxel data at heights 0 m, 4 m, and 10 m
  - Energy density data stored in energy_density.nc (NetCDF)
  - Reproducible outputs organized under out/ and isoheight_planes/walk/

- File and directory structure (key paths)
  - in/lights/ and in/template.main.json5
  - out/ (simulation results)
  - isoheight_planes/ (2D plane data)
  - isoheight_planes/walk/ (random walk results)
  - scripts/ (automation and environment setup)
  - scripts/venv (Python virtual environment)

- Contact
  - Sam Morrell, s.a.f.morrell@exeter.ac.uk

- GIS relevance and notes
  - Enables reproducible generation of 3D energy density, heatmaps, and path-length metrics that can be mapped and analyzed in GIS workflows.
  - Integrates LiDAR-derived topography with photometric data to produce geospatial outputs suitable for policy analysis, urban planning, and ecological darkness studies.
  - The workflow combines high-resolution external geospatial data (LiDAR) with photometric modeling and random-walk analyses, supporting map-based visualisations and spatial decision-making.