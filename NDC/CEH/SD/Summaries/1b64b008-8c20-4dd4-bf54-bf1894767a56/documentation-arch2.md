# Documentation for model code to simulate animal behaviour in response to light

## Overview
- Describes a dataset and codebase to reproduce 3D volumetric energy density of photons in a simulated environment, plus heatmaps and journey lengths for ensembles of weighted walkers representing animals.
- Includes Monte Carlo Radiative Transfer (MCRT) solver, weighted random-walk code, configuration inputs, and scripts to reproduce results.

## What is included
- Source code and binaries for the MCRT solver (mcrt/aetherus-0.2.0) and the weighted random walking Python code (grid_walker-0.1.0).
- Input data directory (in/) with configuration files, spectra, photometric data, and geometry.
- A scripts directory to automate reproduction of results.
- A snapshot of the relevant codebases used to generate outputs in the publication.

## Collection/generation methods

### 1.1 Light Intensity Distributions (LIDs)
- Photometry for light sources provided in IES or LDT formats.
- Photometry data sourced from lamp manufacturers’ websites, obtained with a goniophotometer.

### 1.2 Geometry
- Terrain and buildings geometry stored as Wavefront OBJ files (.obj).
- Terrain geometry created by triangulating study plot bounds and elevating vertices using Defra National LIDAR Programme 2020 1m data.
- Buildings geometry constructed from Ordnance Survey VectorMap Local footprints, extruded to match DSM/DTM height differences from LIDAR data.

### 1.3 Spectral Reflectances
- USGS Spectral Library (version 7) used; data converted to CSV for MCRT.
- Materials include dark-grey asphalt for roads and medium red brick for buildings.

### 1.4 Emission Spectra
- Emission spectra from the LICA-UCM spectral database, converted to JSON for MCRT input interpolation.

## Nature and Units of recorded values
- Geometry units: metres (1 unit = 1 m).
- Emission spectra and spectral reflectances: relative units.
- Photometric data: luminous intensities in candela.

## Quality control
- MCRT code provided with unit tests; tests cover edge and nominal cases, and comparisons to analytical results for the grid_walker.
- Meshes checked to be watertight; vertex normals oriented correctly.

## Details of data structure

### 1. Data components
- Input data for the Monte Carlo radiative transfer code, including:
  - Configuration files, spectra (.csv), spectral reflectances (JSON), photometric data (.ldt/.ies), and geometry (.obj).

### 2. Software components
- The MCRT solver (Aetherus) version 0.2.0, provided as source code and compiled binaries for Linux and macOS.
- The grid_walker code (v0.1.0) for weighted random walks.

### 3. Automation
- A directory of scripts (scripts) to automate reproduction of results.

## Additional details
- Example files and structure include: in/, objs/, lids/, mats/, lights/, spec/, refs/, Aetherus-0.2.0/, grid_walker-0.1.0/, and scripts.
- Environment and testing materials:
  - scripts/environment.yml
  - Tests and configuration templates under grid_walker-0.1.0/tests

## Reproducibility and use for environmental analysis
- Enables reproducible simulation of light-affected animal movement in a defined environment.
- Provides standardized inputs (geometry, photometry, spectra) and traceable software versions to support scrutiny and policy-relevant environmental health analyses.