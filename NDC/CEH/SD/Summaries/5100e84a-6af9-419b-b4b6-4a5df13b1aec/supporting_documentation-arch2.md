# Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland

- Licensing and citation: Data are available under the Open Government Licence. Users must include the citation: Khamis, D.; Smith, R.; Fry, M.; Evans, J. (2024). Modelled daily soil moisture and soil temperature at 1km resolution across the UK mainland, NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/5100e84a-6af9-419b-b4b64a5df13b1aec

- Purpose and scope
  - Provides model outputs of daily mean volumetric water content (theta) and topsoil temperature (tsoil) at 1km across the UK mainland.
  - Coverage: 01 January 1965 to 31 December 2018.
  - Outputs generated with neural network models trained on COSMOS-UK observational data (cosmic ray neutron sensors and TDT probes).

- Key outputs
  - theta: daily mean volumetric water content (fractional, 0–1).
  - tsoil: daily mean topsoil temperature (degrees Celsius).

- Models and inputs
  - Soil moisture model: non-autoregressive neural network using causal convolutions and causally-masked temporal self-attention.
  - Topsoil temperature model: fully-connected neural network; its output informs the soil moisture model.
  - Primary inputs for soil moisture: daily meteorology (temperature, pressure, precipitation, humidity, longwave/shortwave radiation, wind, daylight), soil type vector (sand, silt, clay, chalk, peat), soil organic carbon, bulk density, BFIHOST, land cover, soil temperature, elevation; optional: Copernicus Soil Water Index 1km product.
  - Primary inputs for soil temperature: current and previous day meteorology, soil type vector, soil organic carbon, bulk density, land cover, elevation; optional: MODIS Day/Night Land Surface Temperature.

- Training and data sources
  - Training on COSMOS-UK site measurements (neutron sensors and TDT probes) to ground-truth moisture dynamics.
  - Where COSMOS-UK data are unavailable, gridded products are used (e.g., CHESS meteorology, Countryside Survey soil maps, UKCEH elevation).
  - Land cover from Land Cover Map 2015; soil texture from UK soil parent material map; BFIHOST from hydrology of soil types.

- File format and contents
  - File format: NetCDF.
  - Naming: 648 files named SM_YYYYMM.nc, organized in yearly folders YYYY.
  - Data type: 32-bit floating point; missing values as NaN.
  - Core variables per file: crs, theta, time, tsoil, x (Easting, OSGB36), y (Northing, OSGB36).

- Spatial and temporal coverage
  - Spatial coverage: OSGB 1936 / British National Grid; grid-centroid sampling at 1km resolution (first pixel at 500m,500m).
  - Spatial extent: x in [0, 656000] metres Easting; y in [0, 1057000] metres Northing.
  - Spatial resolution: 1 km × 1 km.
  - Temporal coverage: 1965-01-01 to 2018-12-31.
  - Temporal resolution: daily.

- Data acquisition and processing details
  - Neural architecture combines causal self-attention and 1D causal convolutions for soil moisture mapping.
  - Inputs selected to capture interception, runoff/infiltration, ET, drainage, and soil properties; Copernicus Soil Water Index used to enhance inputs.
  - Training used in-situ measurements at COSMOS-UK sites; where unavailable, gridded data supply inputs for training and operational use.
  - Loss functions for soil moisture include components for likelihood, gradient alignment, time-shift invariance, and initialization adherence; optimizer: Adam.
  - Soil temperature model uses mean squared error loss; inputs and processing mirror the moisture model where applicable.

- Quality control
  - Removed COSMOS-UK VWC values > 90%.
  - Tadham Moor COSMOS-UK site excluded after data inspection.

- References
  - Key references detailing COSMOS-UK data, inputs, and modeling approaches are provided (data source papers, land cover and soil products, and methodological papers).