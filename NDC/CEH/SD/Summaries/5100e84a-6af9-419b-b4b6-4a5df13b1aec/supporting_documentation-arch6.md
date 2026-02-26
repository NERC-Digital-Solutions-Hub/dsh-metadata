# Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland

## Overview
- Dataset of model outputs for daily mean volumetric water content (theta) and topsoil temperature (tsoil) on a 1km grid across the UK mainland.
- Temporal coverage: 01 January 1965 to 31 December 2018.
- Generated with neural network models trained on COSMOS-UK observational data (cosmic ray neutron sensors at ~50 sites).
- Soil moisture model: non-autoregressive network with causal convolutions and causally-masked temporal self-attention.
- Topsoil temperature model: fully-connected neural network; its output feeds into the soil moisture model.
- Key inputs for soil moisture: daily meteorology (temp, pressure, precipitation, RH, longwave/shortwave radiation, wind, solar hours), soil type vector (sand, silt, clay, chalk, peat), soil organic carbon, bulk density, base flow index (BFIHOST), land cover, soil temperature, elevation; optional Copernicus Soil Water Index 1km product.
- Key inputs for soil temperature: current and previous day meteorology, soil type vector, soil organic carbon, bulk density, land cover, elevation; optional MODIS Land Surface Temperature (Day/Night).

## Data content and variables
- Outputs: theta (mean volumetric water content, 0–1) and tsoil (topsoil temperature in degrees C).
- Spatial resolution: 1km x 1km on the OSGB 1936 / British National Grid.
- File format: NetCDF (.nc) with 32-bit floating point data; missing values are NaN.
- Core variables per file:
  - crs (coordinate reference system)
  - theta (mean volumetric water content)
  - tsoil (mean topsoil temperature)
  - time (date)
  - x (Easting in metres, OSGB grid)
  - y (Northing in metres, OSGB grid)

## Spatial and temporal coverage
- Spatial coverage: UK mainland on OSGB 1936 grid; grid-box centroids at 1km resolution (first pixel at 500m,500m).
- Spatial extent: Northing [0, 1,057,000]; Easting [0, 656,000] metres.
- Temporal coverage: 1965-01-01 to 2018-12-31.
- Temporal resolution: daily outputs.

## File structure and access
- Files: 648 NetCDF files named SM_YYYYMM.nc, covering each month of a given year.
- Organization: yearly subfolders labeled by year (YYYY).
- Contents per file: 32-bit floating point arrays; uses NaN for missing data.
- Access guidance: outputs are model-based products designed for exploration and secondary analysis; optional satellite inputs available to enhance model inputs during training or operational use.

## Data acquisition and processing (generation/transformation)
- Soil moisture map architecture: non-autoregressive model using a blend of causal self-attention and 1D causal convolutions over time; trained to replicate COSMOS-UK site observations (neutron probes) and time-domain transmissometry.
- Inputs parameterizing key hydrological processes:
  - Interception/throughfall (precipitation, land cover)
  - Runoff/infiltration (soil type, elevation)
  - Evapotranspiration (radiation, humidity, temperatures, wind, land cover)
  - Drainage (soil carbon content, soil type, bulk density)
  - Optional input: Copernicus Soil Water Index (2 cm)
- Training data handling:
  - In-situ COSMOS-UK measurements where available; otherwise gridded products used.
  - Land cover from UKCEH Land Cover Map 2015; soil texture vector from BGS soil maps (sand, silt, clay, chalk, peat); BFIHOST used for hydrological context.
  - Gridded driving meteorology from CHESS; soil carbon and bulk density from Countryside Survey maps; elevation from a 50 m DEM aggregated to 1 km; MODIS LST used when available.
- Loss function components for soil moisture:
  - Negative log-likelihood of observed VWC given predicted mean and uncertainty
  - MAE of the time gradient between predicted and true VWC
  - Time-shift invariance term via a second forward pass with forward-shifted initial conditions
  - Regularization to keep predictions close to initial conditions
  - Optimized with Adam
- Soil temperature model:
  - Loss as mean squared error between predicted and observed daily temperatures
- Quality control during training:
  - COSMOS-UK data with VWC > 90% removed
  - Tadham Moor site removed after inspection

## Quality and caveats
- Training relies on patchy or variable-quality in-situ data; gridded inputs are used to supplement where site data are unavailable.
- Outputs are model-derived and dependent on input data quality, including optional satellite products.
- Explicit quality control steps described for training data; users should consider uncertainties associated with model-based estimates, especially in data-sparse regions or periods.

## Practical usage and opportunities for Data Support
- Data Support use cases:
  - Combine with local meteorology, land cover, and soil data to explore soil moisture dynamics and temperature trends at 1km scale.
  - Build self-serve dashboards or dashboards with time-series exploration for planning in agriculture, water resources, or land management.
  - cross-validate with other hydrological datasets or incorporate into regional risk assessments (e.g., drought, irrigation planning).
- Potential data products:
  - Time-series analyses of soil moisture and temperature by region or land cover type.
  - Integration with other environmental layers (soil texture, carbon, elevation) for enhanced decision support.
- Usage considerations:
  - Be mindful of model-based nature and the training data's spatial-temporal coverage.
  - Consider using optional input variables (e.g., Copernicus SWI, MODIS LST) where relevant to refine interpretation or complement other datasets.

## References
- Stanley et al. (2023) COSMOS-UK observational data
- Bauer-Marschallinger et al. (2018) Soil moisture fusion
- Rowland et al. (2017) Land Cover Map 2015
- British Geological Survey (2014) UK Soil Parent Material Map
- Griffin et al. (2019) BFIHOST
- Wan et al. (2015) MODIS Land Surface Temperature
- Henrys et al. (2012) Countryside Survey soil maps
- Morris & Flavin (1990) Digital terrain model
- Robinson et al. (2023) CHESS meteorology dataset
- Adam Kingma & Ba (2017) Adam optimizer