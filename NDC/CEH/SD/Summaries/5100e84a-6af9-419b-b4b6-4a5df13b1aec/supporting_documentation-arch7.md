# Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland

- Purpose and content
  - A data product providing model outputs of daily mean volumetric water content (theta) and topsoil temperature (tsoil) at 1 km resolution across the UK mainland.
  - Time period: 01 January 1965 – 31 December 2018.
  - Generated with neural networks trained on COSMOS-UK site observations (neutron sensors and time-domain transmissometry).
  - Outputs are stored as NetCDF files and are designed for GIS use and map-based analysis.

- Spatial and temporal specifics
  - Spatial framework: OSGB 1936 / British National Grid (grid-box centroids; first pixel at 500 m, 500 m).
  - Spatial resolution: 1 km x 1 km.
  - Spatial extent: grid coordinates from 0 to 1,057,000 m Northing and 0 to 656,000 m Easting.
  - Temporal resolution: daily outputs.
  - File structure: 648 NetCDF files named SM_YYYYMM.nc, organized in yearly subfolders YYYY.

- File details
  - Data format: 32-bit floating point arrays; missing values represented as NaN.
  - Key variables inside files:
    - crs: Coordinate reference system.
    - theta: Mean volumetric water content (fractional, 0–1).
    - tsoil: Mean topsoil temperature (degrees Celsius).
    - time: Time (date).
    - x: Easting (metres, OSGB grid).
    - y: Northing (metres, OSGB grid).

- Model and inputs (generation/processing)
  - Soil moisture model
    - Non-autoregressive neural network using causal convolutions and causally-masked temporal self-attention.
    - Main inputs: daily meteorology (temperature, pressure, precipitation, humidity, longwave/shortwave radiation, wind, sunlight hours), soil type vector (sand/silt/clay/chalk/peat), soil organic carbon, bulk density, base flow index (BFIHOST), land cover, soil temperature, elevation.
    - Optional input: daily 1 km Soil Water Index (Copernicus) satellite product.
    - Output used as input to the moisture model.
  - Topsoil temperature model
    - Fully-connected neural network.
    - Inputs: current and previous day meteorology (temp, precipitation, longwave/shortwave radiation, sunlight hours), soil type vector, soil organic carbon, bulk density, land cover, elevation.
    - Optional input: MODIS 1 km Land Surface Temperature (LST) day/night values.
  - Training data and inputs
    - Training uses in-situ COSMOS-UK measurements where available; gridded data substitute at locations away from COSMOS sites.
    - Land cover: UKCEH Land Cover Map 2015; soil texture vector from BGS soil parent material map (sand/silt/clay/chalk/peat).
    - Base flow index: BFIHOST (gridded at 1 km).
    - Gridded meteorology: CHESS dataset for locations away from COSMOS sites.
    - Soil carbon and bulk density: Countryside Survey 1 km maps.
    - Elevation: UKCEH 50 m DEM averaged to 1 km.
    - Spatial alignment relies on 1 km grid with a ground-truthing approach combining COSMOS data and gridded proxies.
  - Loss function and optimization
    - Soil moisture loss components:
      - Negative log likelihood of observed VWC under predicted distribution.
      - Mean absolute error of the time gradient of predicted vs observed VWC.
      - Time-shift invariance term (second forward pass with shifted start time).
      - Initial-condition adherence term (MAE at t0 vs initial condition).
    - Optimizer: Adam.
    - Soil temperature loss: mean squared error between predicted and observed daily temperatures.

- Data quality and QC
  - COSMOS-UK training data cleaned by removing VWC values > 90%.
  - Tadham Moor site removed after data quality review.

- Data use and attribution
  - Licence: Open Government Licence (data and citation requirements apply).
  - Citation requirement: Khamis, D.; Smith, R.; Fry, M.; Evans, J. (2024). Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland, NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/5100e84a-6af9-419b-b4b64a5df13b1aec
  - Additional information: https://doi.org/10.5285/5100e84a-6af9-419b-b4b64a5df13b1aec

- References and data sources
  - COSMOS-UK daily and sub-daily hydrometeorological and soil data (2013–2022).
  - Data sources for inputs and auxiliary layers (MODIS, CHESS, Land Cover 2015, soil maps, DEM, and related literature) as listed in the document.