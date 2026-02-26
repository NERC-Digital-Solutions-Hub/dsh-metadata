# Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland

## Overview
- Daily model outputs of volumetric water content (theta) and topsoil temperature (tsoil) at 1 km resolution across the UK mainland.
- Time period: 01 January 1965 to 31 December 2018.
- Generated with neural networks trained on COSMOS-UK observational data (cosmic ray neutron sensors and time domain transmissometry probes).

## Data products and variables
- Primary variables:
  - theta: mean volumetric water content (fractional, 0-1)
  - tsoil: mean topsoil temperature (degrees Celsius)
- Spatial grid: OSGB36 / British National Grid, 1 km x 1 km grid, grid-centroid references
- Temporal resolution: daily
- Coordinate variables: crs, x (Eastings), y (Northings), time (date)
- Data format: NetCDF (.nc), 32-bit floating point; missing values are NaN
- Optional satellite inputs used in some runs:
  - Copernicus Soil Water Index (SWI) input for soil moisture model
  - MODIS Land Surface Temperature inputs for soil temperature model

## File format and naming
- 648 NetCDF files named SM_YYYYMM.nc
- Directory structure organized by year (YYYY)
- Contents described by standard metadata in each file (variables listed in accompanying documentation)

## Spatial and temporal coverage
- Spatial coverage: UK mainland on OSGB 1936 / British National Grid, grid-box centroids (500 m, 500 m) within extents [0, 1057000] m Northing and [0, 656000] m Easting
- Spatial resolution: 1 km x 1 km
- Temporal coverage: 1965-01-01 to 2018-12-31
- Temporal resolution: daily

## Data acquisition and processing (modeling approach)
- Soil moisture (theta) model:
  - Neural network with non-autoregressive architecture using causal convolutions and causally-masked temporal self-attention
  - Trained on COSMOS-UK site data (neutron probes and TDT probes) and gridded data where site data are unavailable
  - Inputs include: meteorology (temp, pressure, precipitation, humidity, radiation, wind, daylight), soil type vector, soil organic carbon, bulk density, base flow index (BFIHOST), land cover, soil temperature, elevation
  - Optional input: daily 2 cm Copernicus SWI
  - Training inputs: site measurements (hydrometeorology, soil temperature, elevation, soil carbon and bulk density); gridded products for variables not measured at COSMOS-UK sites
  - Land cover and soil texture derived from external maps; BFIHOST used at 1 km resolution
  - In operational use, gridded driving meteorology and soil properties replace in-situ inputs where necessary
- Topsoil temperature (tsoil) model:
  - Fully-connected neural network
  - Inputs: current and previous day meteorology (temperature, precipitation, longwave/shortwave radiation, daylight)
  - Optional input: MODIS Day/Night Land Surface Temperature
  - Output of tsoil model used as input to soil moisture model
- Training and loss:
  - Loss for theta combines four components (negative log-likelihood, gradient MAE, time-shift invariance term, and initial-condition adherence)
  - Optimized with Adam
  - Topsoil temperature model trained with mean squared error
- Data provenance:
  - COSMOS-UK observational data underpin training (site-level measurements)
  - Gridded ancillary data sourced from CHESS meteorology, Countryside Survey soil maps, BGS soil materials, Land Cover Map 2015, and other referenced datasets

## Quality control and data governance
- Quality control:
  - Remove COSMOS-UK VWC values > 90%
  - Tadham Moor site excluded after visual inspection
- Data governance and sharing:
  - Data available under Open Government Licence
  - Clear citation required for data use
  - Underlying data and outputs are intended to be openly shared and reusable within governance and monitoring contexts

## Access, licensing, and reuse
- Licensing: Open Government Licence (data use allowed with attribution)
- Citation requirement: Khamis, D.; Smith, R.; Fry, M.; Evans, J. (2024). Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland, NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/5100e84a-6af9-419b-b4b64a5df13b1aec
- Additional information and dataset details available via the provided DOI links
- Intended for integration into monitoring frameworks and decision-support for environmental health and land-surface processes

## References
- Stanley et al. (2023). COSMOS-UK observational data (dataset). NERC EDS EIDC. https://doi.org/10.5285/5060cc27-0b5b-471b-86eb-71f96da0c80f
- Bauer-Marschallinger et al. (2018). Soil moisture fusion methods. Remote Sensing, 1019, 1030. DOI: 10.3390/rs10071030
- Rowland et al. (2017). Land Cover Map 2015 (1km). NERC EIDC. https://doi.org/10.5285/7115bc48-3ab0-475d-84ae-fd3126c20984
- British Geological Survey (2014). UK Soil Parent Material Map, 1km
- Henrys et al. (2012). Countryside Survey soil maps (topsoil carbon, bulk density)
- Wan et al. (2015). MODIS LST data (MOD11A1)
- Morris & Flavin (1990). A digital terrain model for hydrology
- Robinson et al. (2023). CHESS-met meteorology dataset for Great Britain
- Kingma & Ba (2017). Adam optimizer