# Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland

- Open Government Licence: data are available under this licence; must include the citation Khamis et al. (2024) and DOI with use.
- Source and purpose: model outputs of daily mean volumetric water content (theta) and topsoil temperature (tsoil) at 1km across the UK mainland for 1965–2018; generated with neural networks trained on COSMOS-UK observational data.

## Overview of the dataset

- Outputs: daily mean volumetric water content (theta) and topsoil temperature (tsoil) on a 1km British National Grid across the UK mainland.
- Training data: COSMOS-UK network of cosmic ray neutron sensors (site-scale soil moisture) and time-domain transmissometry (TDT) probes; site measurements complemented with gridded auxiliary data when needed.
- Modelling approach:
  - Soil moisture: non-autoregressive neural network with causal convolutions and causally-masked temporal self-attention.
  - Topsoil temperature: fully-connected neural network; its output feeds the soil moisture model.
- Optional inputs:
  - Soil Water Index (Copernicus SWI) at 1km daily resolution for moisture model.
  - MODIS 1km Land Surface Temperature for soil temperature inputs (Day/Night).

## Data inputs and features

- Driving meteorology: temperature, pressure, total precipitation, relative humidity, longwave and shortwave radiation, wind speed, sunlight-hours (and shortwave radiation from sunlight-hours average).
- Static/environmental inputs: soil type vector (sand, silt, clay, chalk, peat), soil organic carbon, bulk density, base flow index (BFIHOST), land cover, elevation.
- Additional inputs: Copernicus SWI (moisture model) and MODIS LST (temperature model) when available.
- Training inputs vs operational inputs: training uses in-situ data where available; operational uses gridded proxies (UKCEH CHESS meteorology, Countryside Survey soil maps, BFIHOST, etc.) for locations away from COSMOS-UK sites.

## File format, naming and contents

- File format: NetCDF.
- File naming: 648 files named SM_YYYYMM.nc; organized in yearly folders YYYY.
- Content: 32-bit floating point arrays; missing values encoded as NaN.
- Variables in each file:
  - crs: coordinate reference system
  - theta: mean volumetric water content [0,1]
  - tsoil: mean topsoil temperature (°C)
  - time: time (date)
  - x: Easting (OSGB36) in metres
  - y: Northing (OSGB36) in metres

## Spatial coverage and resolution

- Grid: OSGB 1936 / British National Grid.
- Resolution: 1 km x 1 km.
- Grid centroids: first pixel at (500 m, 500 m).
- Spatial extent: Northing [0, 1,057,000] m; Easting [0, 656,000] m.

## Temporal coverage and resolution

- Period: 01 January 1965 to 31 December 2018.
- Temporal resolution: daily model outputs.

## Generation, processing and quality control

- Model architecture:
  - Soil moisture model: non-autoregressive with causal self-attention and 1D causal convolutions along time.
  - Temperature model: fully-connected network; temperature inputs include current and previous day meteorology; day/night MODIS LST if available.
- Training/conditioning data:
  - Inputs drawn from COSMOS-UK site measurements for hydrometeorology, soil temperature, elevation, soil carbon and bulk density.
  - Gridded proxies used for variables not observed at sites (land cover, soil texture, elevation, etc.).
  - Land cover: UKCEH Land Cover Map 2015; soil texture: BGS 1 km soil parent material map; BFIHOST used for hydrology descriptor.
- Objective/loss functions:
  - Soil moisture: multi-component loss including negative log-likelihood, gradient MAE, time-shift invariance component, and initial-condition MAE; optimization with Adam.
  - Topsoil temperature: mean squared error between predicted and observed temperatures.
- Quality control:
  - Remove COSMOS-UK VWC values > 90%.
  - Tadham Moor site removed from training after inspection.

## Data licensing, citation and access notes

- Licence: Open Government Licence.
- Citation requirement: must cite Khamis et al. (2024) and the associated DOI.
- Additional information: dataset described with extensive methodological and reference details; supplementary sources and DOIs provided for input data, training references, and software.

## Data use and applicability for data leadership

- Purpose alignment: supports data-driven decision making about soil moisture and temperature dynamics at high spatial and temporal granularity.
- Reproducibility and governance: detailed description of inputs, model architecture, training regime, and QC enables assessment, replication, and potential integration with broader data systems.
- Accessibility and discoverability: NetCDF format with explicit file naming and metadata structure facilitates discoverability and programmatic access for analysis, monitoring, and scenario planning.