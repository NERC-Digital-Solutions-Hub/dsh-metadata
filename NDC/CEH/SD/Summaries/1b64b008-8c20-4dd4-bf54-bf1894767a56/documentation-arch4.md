# Documentation for model code to simulate animal behaviour in response to light

- This dataset and accompanying code enable reproduction of 3D volumetric energy density data for photons in a simulated environment, plus heatmaps and journey lengths for ensembles of weighted walkers (emulated animals) across specific simulated environments.
- Includes source code for the Monte Carlo Radiative Transfer (MCRT) solver (Aetherus 0.2.0) and a weighted random-walking model (grid_walker 0.1.0), plus inputs, configuration files, and scripts to reproduce results.
- Outputs consist of 3D energy-density fields and 2D heatmaps/journey-length metrics derived from 2D slices of the energy data.

## Collection/generation methods

- Light intensity distributions (LIDs): photometry for light sources provided by lamp manufacturers, captured with goniophotometer in IES or LDT formats.
- Geometry: terrain and building geometries generated via a digital twins pipeline; terrain.obj and buildings/*.obj created from 1m Defra LIDAR-based terrain and DSM/DTM data; terrain tile and building footprints sourced from national datasets.
- Spectral reflectances: USGS Spectral Library version 7 (converted to CSV/JSON); materials include dark-grey asphalt for roads and medium red brick for buildings.
- Emission spectra: sourced from the LICA-UCM spectral database and converted to JSON for MCRT input.

## Nature and units of recorded values

- Geometry units: metres (1 geometry unit = 1 m).
- Emission spectra and spectral reflectances: relative units.
- Photometric data: luminous intensities in candela.

## Quality control

- MCRT code includes unit tests to verify component behavior and edge/nominal cases; grid walker tests compared against analytical predictions.
- Meshes checked for watertightness and correct vertex normal orientation.

## Details of data structure

- Deposit comprises four components:
  - Input data for the MCRT code and supporting files: configuration files, spectra (.csv), spectral reflectances (JSON), photometric data (.ies/.ldt), and geometry (.obj).
  - The MCRT solver (Aetherus 0.2.0) and its library, provided as source and compiled binaries.
  - The grid_walker code (v0.1.0) used for weighted random walks.
  - A scripts directory to automate reproduction of results.
- Contents include world/configuration files, geometry and texture assets, LID/photometric data, building terrain OBJ files, and numerous supporting scripts and test configurations.

## Reproducibility and data governance implications

- End-to-end, versioned code and data enable auditability and reproducibility of findings, with explicit input sources, configurations, and test suites.
- Data provenance spans multiple external sources (lamp photometry, national lidar/OS datasets, USGS spectral library, LICA-UCM spectra), highlighting the importance of data licenses, access rules, and metadata standards for ongoing use and integration into broader data ecosystems.

## Relevance for Data Leaders

- Aligns with a systems-level view of data: combines photometric data, geometry, spectral properties, and simulation code to produce actionable model outputs.
- Supports user-oriented product iteration through reproducible pipelines and clear provenance, aiding co-ownership and collaboration across data teams and partners.
- Demonstrates robust data quality practices (unit tests, mesh validity) and comprehensive metadata/rationale for each data component (units, sources, formats).
- Highlights potential data access considerations (external data sources and formats) and the need for ongoing coordination and standards to maintain discoverability and usability across networks.