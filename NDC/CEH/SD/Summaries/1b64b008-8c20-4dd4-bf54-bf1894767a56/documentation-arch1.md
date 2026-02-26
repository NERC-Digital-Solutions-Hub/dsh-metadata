# Documentation for model code to simulate animal behaviour in response to light

- Overview
  - A dataset and accompanying code to reproduce 3D volumetric data describing photon energy density in a simulated environment, plus heatmaps and journey lengths for ensembles of weighted walkers (emulating animal behavior) in specific simulated environments.
  - Includes source code for snapshots of Monte Carlo Radiative Transfer (MCRT) code (Aetherus 0.2.0) and the weighted random-walking code (grid_walker 0.1.0), plus inputs, configuration files, and scripts to reproduce results.
  - Output flow: MCRT generates 3D energy density; grid_walker processes 2D planes from this data to produce heatmaps and journey lengths for walker ensembles.

- Collection/generation methods
  - 1.1 Light Intensity Distributions (LIDs)
    - Photometry for light sources provided in IES or LDT formats, sourced from lamp manufacturers who used goniophotometry.
  - 1.2 Geometry
    - Terrain geometry in OBJ format generated via a digital twins pipeline.
    - Terrain heights from Defra National LiDAR Programme 2020 at 1 m resolution.
    - Building geometry built from Ordnance Survey VectorMap Local data; ground plane extruded by height differences between LiDAR-derived DSM and DSM pixels.
  - 1.3 Spectral Reflectances
    - Based on USGS Spectral Library v7; materials include dark-grey asphalt for roads and medium red brick for buildings.
  - 1.4 Emission Spectra
    - Taken from the LICA-UCM spectral database and converted to JSON for integration with the MCRT inputs.

- 2 Nature and Units of recorded values
  - Geometry: units are metres (1 geometry unit = 1 m).
  - Emission spectra and spectral reflectances: provided in relative units.
  - Photometric data (luminous intensities): provided in candela.

- 3 Quality control
  - MCRT and grid_walker code packages include unit tests to verify individual components and alignment with analytical expectations.
  - Mesh integrity checks: watertight meshes and correctly oriented vertex normals.

- 4 Details of data structure
  - The deposit includes:
    - Input data for the MCRT solver, including configuration files, spectra (.csv), spectral reflectances (JSON), photometric data (.ldt/.ies), and geometry (.obj).
    - The MCRT solver (Aetherus 0.2.0) and supporting library, provided as source (.tar.gz) and as compiled Linux/macOS binaries.
    - A snapshot of the grid_walker code (v0.1.0) used for weighted random walks.
    - A scripts directory to automate reproduction tasks.
  - Complete file structure highlights:
    - in/grid_walker.template.toml, in/surfs.json5, in/template.main.json5, in/world.json5, in/lids/*, in/objs/terrain.obj, in/objs/buildings/*.obj, in/spec/*.json, in/mats/*.json5, in/lights/*.json5, and a wide set of Aetherus and grid_walker subdirectories with code and tests.
    - Tools and scripts for running scenarios, environment setup, and data processing are included (e.g., Python scripts, shell scripts, and configuration templates).
  - The dataset emphasizes reproducibility by providing code, configurations, and data to reproduce the published results.