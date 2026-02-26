# The dataset herein is the source code and inputs required to reproduce the 3D volumetric data describing the energy density of photons with a simulated environment and the heatmaps and journey lengths for ensembles of weighted random walkers experiencing the specific simulated environments. This documentation will a) explain the contents of this deposited dataset, and b) provide a walkthrough of the steps to reproduce the outputs used in the publication the accompanying publication.

- Overview
  - Purpose: Deposited dataset to reproduce 3D photon energy density, heatmaps, and weighted random-walker trajectories in a simulated environment; accompanies a publication on streetlighting and ecological darkness.
  - Publication association: Outputs used in “Changing streetlighting schemes and the ecological availability of darkness.” DOI to follow.
  - Contact: Sam Morrell (s.a.f.morrell@exeter.ac.uk)

- Dataset components
  - Monte Carlo Radiative Transfer (MCRT) inputs: configuration files, spectra (.json5), luminaire photometric data (.ldt), and geometry (.obj).
  - MCRT solver and library: Aetherus (Rust) used to generate outputs (version 0.2.0; source code provided as Rust files).
  - Grid-walker code: snapshot of grid_walker (v0.1.0) for weighted random walks.
  - Reproducibility scripts: a scripts directory with automation to reproduce results described in the article.

- External data and prerequisites
  - LiDAR data: Defra National LIDAR Programme 2020 1m dataset required for reproduction; tile: “national_lidar_programme_dtm-2020-1-SX99sw”.
  - Data access: LiDAR tile and TIFF/TFW files available via specified URLs; place DTM_SX9090_P_10601_20200322_20200322.tif and its .tfw in the dataset root.

- Software setup and dependencies
  - MCRT solver (Rust)
    - Rust toolchain: rustup, using Rust 1.68.1.
    - Libraries: libnetcdf (v4.6.0), libpng (v1.5.13).
    - Build steps: untar aetherus-0.2.0.tar.gz in the mcrt directory, enter Aetherus-0.2.0, run cargo build; produced binary at target/debug/mcrt.
    - Tests: run cargo test; README at Aetherus-0.2.0/aetherus-0.2.0-README.md.
  - Weighted Random Walking code (Python)
    - Python: 3.10.12.
    - Virtual environment: create venv, activate, install dependencies from requirements.txt.
    - Documentation: grid_walker-0.1.0/grid_walker-0.1.0-README.md.

- Reproducing the outputs
  - Generate MCRT outputs
    - Scenarios: located in in/lights; execute scripts/run_scenarios.sh with arguments to process all scenarios: ./scripts/run_scenarios.sh ./in/lights/ ./in/template.main.json5.
    - Outputs: produced in out/ directory.
  - Extract isoheight planes
    - Extract 2D isoheight planes from voxel energy density data (0 m, 4 m, 10 m): run ./scripts/extract_scenario_isoheights.sh ./out/*/energy_density.nc.
    - Environment setup: Python environment prepared under scripts/venv.
  - Run weighted random walks
    - Change to isoheight_planes directory, then run: ../grid_walker-0.1.0/scr/run_all.sh ../in/grid_walker.template.toml.
    - Outputs: random-walk results stored in isoheight_planes/walk/.

- Outputs and data products
  - energy_density.nc: 3D volumetric energy density data for photons in the simulated environment.
  - isoheight_planes/walk/: directory containing results of weighted random walks corresponding to the isoheight planes.

- Notes and best practices
  - Reproducibility hinges on obtaining the external LiDAR dataset and matching software versions (Rust 1.68.1, Python 3.10.x) and specific library versions.
  - The workflow is multi-component, requiring successful completion of MCRT simulations before generating random-walk outputs.
  - The dataset includes scripts to automate steps and preserves configuration details to enable replication of the article’s outputs.