# Documentation for model code to simulate animal behaviour in response to light

## Overview
- Dataset to reproduce 3D volumetric data of photon energy density in a simulated environment, plus heatmaps and journey lengths for ensembles of weighted walkers.
- Includes source code for the Monte Carlo Radiative Transfer (MCRT) solver and the weighted random walking code, along with inputs and configuration files required to run simulations.
- Outputs: 3D energy density fields from MCRT and 2D-plane derived heatmaps/journey metrics from the weighted walker simulations.

## Collection and generation methods
- MCRT solver: mcrt/aetherus-0.2.0 (tar.gz) and supporting library (Aetherus) with associated configuration files (JSON/JSON5).
- Weighted random walking: grid_walker-0.1.0 (tar.gz) and its scripts.
- Inputs located in in/: 
  - Light intensity distributions (LIDs) from lamp manufacturers in IES/LDT formats.
  - Geometry: terrain.obj and multiple building OBJ files generated via a digital twins pipeline, using Defra LiDAR 2020 1m data for terrain and DSM/DTM references.
  - Spectral reflectances: USGS Spectral Library v7 (converted to CSV/JSON as appropriate).
  - Emission spectra: from LICA-UCM spectral database (converted to JSON for inputs).
- Metadata and configuration: JSON/JSON5 files for MCRT and related scripts. Large geometry data (e.g., terrain.obj) is included as part of the deposit.

## Nature, units, and data formats
- Geometry units: metres (1 unit = 1 m).
- Emission spectra and spectral reflectances: provided in relative units.
- Photometric data: luminous intensities in candela (cd).
- Data formats: a mix of OBJ (geometry), CSV/JSON/JSON5 (spectral data, configurations), IES/LDT (LIDs), and tarballs for executable code and libraries; includes compiled binaries for MCRT on multiple platforms.

## Quality control and reproducibility
- MCRT code includes unit tests to verify components in isolation; edge cases and analytical predictions are used for cross-checks (especially for grid_walker).
- Meshes checked to be watertight with correct vertex normal orientation.
- Versioned software provided:
  - MCRT solver: Aetherus 0.2.0 (source code and binaries).
  - Grid walker: grid_walker 0.1.0 (source code).
- Scripts and configurations to reproduce results are included (scripts directory, environment.yml, and run scripts).

## Data structure and file layout
- Deposit consists of four components:
  - Input data and configuration for the MCRT run (spectra, spectral reflectances, photometric data, geometry).
  - The MCRT solver (Aetherus 0.2.0) and supporting library, with source code and platform binaries.
  - The grid_walker code (v0.1.0) used for weighted random walks.
  - A scripts directory to automate reproduction tasks.
- Notable contents include:
  - in/ with world/configuration and input files
  - in/objs/ terrain.obj, buildings/*.obj, sky.*.obj/mtl
  - in/lids/, in/refs/, in/mats/, in/lights/ with multiple related files
  - Aetherus-0.2.0/ (full code, tests, and tooling)
  - grid_walker-0.1.0/ (code and tests)
  - scripts/ (environment.yml, run scripts, and Python utilities)
  - Extensive listing of individual files and paths to support discovery and reproducibility

## Reproducibility and usage support
- The dataset provides a complete snapshot to reproduce published results, including:
  - Configuration and input files for the MCRT run
  - The exact software versions used to generate outputs
  - A separate grid_walker implementation and its inputs
  - Automation scripts and environment definitions to execute end-to-end workflows

## Data governance and stewardship considerations
- Provenance and source data:
  - Photometry and spectral data sourced from lamp manufacturer measurements and established spectral libraries; LiDAR-derived geometry from national datasets.
  - Clear attribution of data sources is embedded in the metadata and file descriptions, enabling traceability of inputs.
- Metadata and discoverability:
  - Rich description of data components, formats, and the relationship between MCRT outputs and downstream heatmaps/journey metrics.
  - Extensive file layout and versioned software enhance discoverability and reproducibility.
- Licensing and reuse:
  - The document does not specify licensing or usage rights for the data or code; assess and document licenses, attribution requirements, and redistribution terms before reuse.
- Data volume and formats:
  - Large geometry files (e.g., terrain.obj) and multiple binary tarballs may impact transfer and storage planning; ensure governance records note file sizes, formats, and storage implications.
- Update and maintenance:
  - While the materials are versioned, there is no explicit update policy or embargo details provided; establish a governance plan for future updates, dependency management, and compatibility between MCRT and grid_walker components.

## Summary for data stewardship
- The document provides a well-structured, provenance-rich dataset designed to reproduce complex photonics- and movement-simulation results, with clearly separated components for inputs, simulation code, and post-processing code.
- Governance priority areas include clarifying licenses, ensuring ongoing access to large asset files, and maintaining version alignment across MCRT, grid_walker, and scripts to support long-term discovery, reuse, and updates.