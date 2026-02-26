# Supporting documentation

## Overview
- Dataset of modelled vegetation carbon output from the land surface model JULES, plus temperature and rainfall outputs.
- Outputs are monthly, at 1.5 km resolution.
- Four JULES simulations: two climate projections under a constant present-day CO2, and a CO2 pathway following the SRES A1B scenario.
- Includes both vegetation carbon and the associated climate variables (temperature and rainfall).

## Provenance and context
- Simulations driven by climatological data downscaled from a 25 km x 25 km grid to 1.5 km x 1.5 km from the HadRM3-PPE-UK ensemble.
- CO2 scenarios: constant present-day CO2 (386.5 ppm) and the A1B pathway.
- Global climate sensitivity values used: 3.5 K (standard configuration) and 7.1 K (ensemble member with higher sensitivity).
- JULES is a community-developed model led by the UK Met Office and Centre for Ecology and Hydrology; access requires registration on the JULES repository.

## Model configuration and data lineage
- Data produced with JULES version vn4.9.
- Model configuration available on the Rose suite u-ao645 under the branch transient_25km_drive (registration required).
- Reference frameworks and sources: Nakicenovic et al. 2000 (IPCC SRES A1B).

## Data structure and format
- File format: NetCDF (.nc).
- Each file contains: lat/lon grid, a time series of the monthly midpoints, and the dataset values.
- Directory structure: 35K and 71K directories (climatology used to run simulations), each containing Const_CO2 and CO2 subdirectories.
- Within each subdirectory: three .nc files containing the described objects; naming example: Temp_35K_Const_CO2.nc for temperature data for the 3.5K, constant CO2 simulation.

## Variables and content
- Variables included per file: temperature, rainfall, and vegetation carbon outputs produced by JULES.
- Associations between files and simulations are encoded in the file names (e.g., climate sensitivity, CO2 scenario).

## Access, usability, and governance
- Access to JULES and its data requires registration (data creators/sharers should be aware of access controls).
- Data is structured to facilitate discovery and reuse, with explicit naming and directory conventions to indicate climatology, CO2 scenario, and temperature/climate variables.
- Documentation provides model version, configuration branch, and scenario details to support provenance, reproducibility, and interoperability.

## Metadata and documentation guidance
- Essential metadata to capture for stewardship:
  - Model: JULES, version vn4.9
  - Configuration: Rose suite u-ao645, branch transient_25km_drive
  - Scenarios: Const_CO2 vs CO2 (A1B pathway)
  - Climate sensitivity values: 3.5 K and 7.1 K
  - Downscaling source: HadRM3-PPE-UK ensemble
  - Spatial/temporal resolution: 1.5 km, monthly
  - Variables included: vegetation carbon, temperature, rainfall
  - File structure and naming conventions (NetCDF, example filenames)
  - Access restrictions and registration requirements
  - References for provenance: Nakicenovic et al. 2000

## References
- Nakicenovic, N., Alcamo, J., Davis, G., (2000) 'IPCC Special Report on Emission Scenarios', Cambridge