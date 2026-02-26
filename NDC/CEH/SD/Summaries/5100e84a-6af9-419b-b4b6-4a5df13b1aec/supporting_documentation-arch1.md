# Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland

## Overview
- Dataset of model outputs for daily mean volumetric water content (theta) and topsoil temperature (tsoil) at 1km across the UK mainland, covering 1965–2018.
- Generated with neural network models trained on COSMOS-UK observational data (cosmos-uk site sensors provide site-scale soil moisture measurements).
- Soil moisture model is non-autoregressive with causal convolutions and causally-masked temporal self-attention; topsoil temperature model is a fully-connected neural network.
- Inputs include daily meteorology, soil properties, land cover, elevation, soil organic carbon, bulk density, and hydrology-related indices; optional satellite products are supported.
- Outputs can be used to study soil moisture dynamics, climate-vegetation interactions, and hydrological processes at fine spatial and daily temporal scales.

## Data Details
- Variables: theta (mean volumetric water content; fractional [0,1]), tsoil (mean topsoil temperature; °C); time; x (Easting; OSGB36), y (Northing; OSGB36); crs.
- File format: NetCDF (32-bit floating point arrays); missing values denoted as NaN.
- Time unit: Time is stored as dates; daily resolution.

## Spatial Coverage and Resolution
- Spatial framework: OSGB 1936 / British National Grid.
- Grid representation: grid-box centroids at 1km resolution (first pixel at 500m, 500m).
- Spatial extent: [0, 1057000] metres Northing, [0, 656000] metres Easting.
- Spatial resolution: 1km x 1km.

## Temporal Coverage and Resolution
- Time period: 01 January 1965 to 31 December 2018.
- Temporal resolution: daily outputs.

## File Information
- Number of files: 648 NetCDF files named SM_YYYYMM.nc (YYYY = year, MM = month).
- Organization: files are stored in yearly subfolders named YYYY.
- File contents: 32-bit floating point arrays; missing values are NaN. Variable descriptions correspond to crs, theta, time, tsoil, x, y.

## Data Acquisition and Processing
- Model architecture:
  - Soil moisture (theta): non-autoregressive neural network with causal convolutions and causally masked temporal self-attention.
  - Topsoil temperature (tsoil): fully-connected neural network.
- Input data and features:
  - Driving meteorology: temperature, pressure, total precipitation, relative humidity, longwave radiation, shortwave radiation, wind speed, sunlight-hours average shortwave radiation.
  - Soil type vector: normalized ratios for sand, silt, clay, chalk, peat.
  - Soil organic carbon and bulk density; land cover; elevation; base flow index from hydrology of soil types (BFIHOST).
  - Optional: Copernicus Soil Water Index (SWI) 1km product for moisture model; MODIS Land Surface Temperature (LST) for tsoil model.
  - For operational use away from COSMOS-UK sites, gridded products replace in-situ inputs (meteorology from CHESS, soil maps for carbon/bulk density, elevation from DEM).
- Training data and targets:
  - Training uses COSMOS-UK site measurements (hydrometeorology, soil temperature, soil carbon, bulk density, elevation).
  - Where in-situ data are unavailable, gridded proxies are used.
- Output integration:
  - tsoil is used as an input to the soil moisture model.
- Loss function components for theta:
  - Negative log-likelihood of true VWC under predicted normal distribution (mean and uncertainty).
  - Mean absolute error of the time gradient between predicted and true VWC.
  - Time-shift invariance term via a second forward pass with forward-shifted initial conditions.
  - Regularization term enforcing adherence to initial conditions.
  - Optimized with Adam optimizer.
- Loss function for tsoil:
  - Mean squared error between predicted and observed daily tsoil.

## Quality Control
- Training data filtering: COSMOS-UK VWC values >90% excluded; Tadham Moor site removed after visual data inspection.
- No additional QC details beyond the training-time filtering noted in the methods.

## Licensing and Access
- Open Government Licence; data available under the stated terms.
- Citation required: Khamis, D.; Smith, R.; Fry, M.; Evans, J. (2024). Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland, NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/5100e84a-6af9-419b-b4b64a5df13b1aec

## References
- Stanley et al. (2023, COSMOS-UK network).
- Bauer-Marschallinger et al. (2018) on SWI data integration.
- Rowland et al. (2017) Land Cover Map 2015.
- British Geological Survey (2014) UK Soil Parent Material Map.
- Griffin et al. (2019) BFIHOST.
- Wan et al. (2015) MODIS LST data.
- Henrys et al. (2012) Countryside Survey soil maps.
- Morris & Flavin (1990) digital terrain model for hydrology.
- Robinson et al. (2023) CHESS-met meteorology dataset.
- Kingma & Ba (2017) Adam optimizer.

## Analyst Considerations
- Potential uses:
  - Correlating soil moisture and topsoil temperature with meteorological drivers, land cover, and soil properties at 1km scale.
  - Developing regional hydrological or climate impact analyses, or validating soil moisture models against observed data.
  - Temporal trend analyses across 1965–2018 at fine resolution.
- Caveats:
  - Outputs are model-based and depend on training data density (COSMOS-UK site coverage) and gridded proxies where in-situ data are missing.
  - Data span ends in 2018; may require updating for recent decades.
  - Spatial and temporal extrapolation beyond training inputs should be treated with caution.