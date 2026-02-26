# Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland, NERC EDS Environmental Information Data Centre

## Overview
- Dataset provides model outputs of daily mean volumetric water content (theta) and topsoil temperature (tsoil) at 1 km across the UK mainland for 1965–2018.
- Generated using neural network models trained on COSMOS-UK site observations (cosmological neutron sensors for soil moisture) and time-domain reflectometry data.
- Soil moisture model uses a non-autoregressive architecture with causal convolutions and temporally masked self-attention; topsoil temperature uses a fully-connected neural network. Output of the temperature model feeds the moisture model.
- Inputs include daily meteorology, soil properties, land cover, soil carbon, bulk density, elevation, and optional satellite inputs (Copernicus Soil Water Index for moisture; MODIS LST for temperature).

## Data content and structure
- File format: NetCDF (32-bit floating point arrays; missing values as NaN).
- 648 files named SM_YYYYMM.nc, organized in yearly subfolders YYYY.
- Variables per file include:
  - crs: Coordinate reference system
  - theta: Mean volumetric water content [0,1]
  - tsoil: Mean topsoil temperature [°C]
  - time: Time (Date)
  - x: Easting (OSGB36 grid, metres)
  - y: Northing (OSGB36 grid, metres)
- Grid structure:
  - OSGB 1936 / British National Grid
  - Grid centroids at 1 km resolution (first pixel at 500 m, 500 m)
  - Spatial extent: Northing 0 to 1,057,000 m; Easting 0 to 656,000 m

## Spatial and temporal coverage
- Spatial resolution: 1 km × 1 km
- Temporal coverage: 01 January 1965 to 31 December 2018
- Outputs are aligned to 1 km grid cells, described at grid-centroid locations

## Data acquisition and processing
- Soil moisture inputs:
  - Driving meteorology: temperature, pressure, precipitation, humidity, longwave/shortwave radiation, wind, sunlight hours
  - Soil type vector (sand, silt, clay, chalk, peat), soil organic carbon, bulk density
  - Base Flow Index from hydrology of soil types (BFIHOST)
  - Land cover vector; optional Copernicus Soil Water Index
  - Training data drawn from COSMOS-UK site measurements and gridded products where needed
- Topsoil temperature inputs:
  - Driving meteorology (current and previous day), soil type vector, soil carbon, bulk density, land cover, elevation
  - Optional MODIS Land Surface Temperature (Day/Night)
  - Operational inputs use gridded meteorology and soil maps when in-situ data are not available
- Training and model design meet objectives to replicate observed soil moisture and temperature dynamics, combining site-scale measurements with broader grid-scale inputs

## Quality control and validation
- Training data QC:
  - Removed COSMOS-UK VWC values > 90%
  - Tadham Moor COSMOS-UK site removed after data inspection
- Model optimization:
  - Soil moisture: four-part loss function (negative log-likelihood with predictive distribution, gradient MAE, time-shift invariance term, loss to initial condition)
  - Optimized with Adam
  - Soil temperature: mean squared error
- In operational use, where in-situ data are unavailable, gridded inputs are used to maintain coverage

## Licensing, citation, and access
- Licensing: Open Government Licence
- Citation requirement: Must include the citation:
  Khamis, D.; Smith, R.; Fry, M.; Evans, J. (2024). Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland, NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/5100e84a-6af9-419b-b4b64a5df13b1aec
- Further information: https://doi.org/10.5285/5100e84a-6af9-419b-b4b64a5df13b1aec

## Governance and stewardship considerations (Data Steward perspective)
- Metadata and discovery:
  - Ensure complete metadata in catalogues (variables, units, spatial/temporal extents, file structure)
  - Link to the licensing and citation requirements within data portals and internal catalogs
- Standards and interoperability:
  - Maintain consistent NetCDF conventions, variable naming, and coordinate reference system (OSGB36)
  - Document input data sources, preprocessing steps, and model architecture for reproducibility
- Data quality and provenance:
  - Track training data composition (COSMOS-UK coverage) and preprocessing decisions (outlier removal)
  - Record any changes to input datasets used in operational versus training phases
- Access, sharing, and updates:
  - Ensure open access under the Open Government Licence while clearly stating any embargoes or limitations
  - Provide versioning and update pathways if reprocessing or model retraining occurs
- Usage and attribution:
  - Communicate required citation prominently in downstream data usage and publications
- Integration with other datasets:
  - Maintain compatibility with CHESS meteorology, Countryside Survey soil maps, and MODIS inputs to support reproducibility and cross-dataset analyses

## References
- Stanley et al. (2023). Daily and sub-daily hydrometeorological and soil data (2013–2022) [COSMOS-UK]. NERC EDS Environmental Information Data Centre.
- Bauer-Marschallinger et al. (2018). Soil Moisture from Fusion of Scatterometer and SAR: Remote Sensing.
- Rowland et al. (2017). Land Cover Map 2015 (1 km).
- British Geological Survey (2014). UK Soil Parent Material Map, 1 km.
- Griffin et al. (2019). Revising BFIHOST for flood frequency estimates.
- Wan et al. (2015). MODIS LST (MOD11A1).
- Henrys et al. (2012). Countryside Survey soil carbon and bulk density datasets.
- Morris & Flavin (1990). Digital terrain model for hydrology.
- Robinson et al. (2023). CHESS-met meteorology dataset.