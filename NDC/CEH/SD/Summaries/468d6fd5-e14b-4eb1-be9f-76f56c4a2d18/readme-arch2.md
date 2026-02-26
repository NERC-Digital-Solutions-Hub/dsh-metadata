# CWatM-Ebro-1km

- Overview
  - A dataset containing input data and settings to run the Community Water Model (CWatM) for the Ebro River basin in Spain.
  - Includes: elevation, flow direction, river routing, lakes/reservoirs, soils, groundwater, land cover, crop coefficients, population and GDP, and water demands (irrigation, livestock, industry, domestic).
  - Developed by Dr David Haro Monteagudo (University of Aberdeen) with Dr Andrea Momblanch Benavent (Cranfield University) and IIASA technical assistance.

- Format and structure
  - File formats: netCDF (.nc), text (.txt), TIFF (.tif), CSV (.csv).
  - Directory structure (highlights):
    - init: warm-up initialization file to stabilize storages.
    - input_netcdf: earth surface input maps (including a catchment mask).
    - groundwater: GLHYMPS-based groundwater inputs.
    - landcover: forest, grassland, irrPaddy, irrNonPaddy (each with crop coefficients, interception, root depth, etc.).
    - landsurface: topo and demand-related data.
    - routing: river routing and lake/reservoir routing inputs.
    - kinematic: channel properties.
    - lakesreservoirs: lake/reservoir attributes and geometry.
    - soil: 19 soil-property files.
    - settings: model settings, initialization files, and reservoir transfer/downstream specs.
    - meteo: meteorological inputs (EMO-5 core; alternatives listed).
  - Spatial and temporal coverage:
    - Region: Ebro River basin, Spain.
    - Resolution: 1 x 1 km.
    - Temporal: daily data from 01/01/1990 to 31/12/2012.

- Model and calibration
  - Model: CWatM (distributed hydrological model for global/regional water resources assessment).
  - Calibration: against Tortosa gauge using an evolutionary computation framework; intended for evaluating water supply/demand and environmental needs.
  - Computational setup: run on Windows 10 (64-bit) with high-end hardware.
  - Modifiability: cwatm_setting.csv allows parameter and input file alterations; EMO-5 is the default dataset, with additional precipitation datasets available for analysis.
  - Running guidance: instructions are provided in the CWatM user manual.

- Data provenance and sources
  - Elevation and land cover: Copernicus; flow direction: EU-Hydro; river routing: EUDEM; lakes/reservoirs: HydroLakes.
  - Soil properties: Dai et al. (2019); groundwater: GLHYMPS.
  - Crop coefficients: MIRCA2000.
  - Water demand drivers: various literature (e.g., Klein Goldewijk et al. 2017; Wriedt et al. 2009; Steinfeld et al. 2006; Gleick et al. 2009; Pastor et al. 2014).
  - Population and GDP: HYDE/SSP-based projections (Jones & O’Neill; Riahi et al.).
  - Meteorology: EMO-5 dataset; alternative precipitation datasets include SPREAD, CHELSA-W5E5, CRU TS3.10, MSWEP.
  - All datasets are projected/cropped to the study area and resampled to 1 km2 before running.

- Data processing and quality
  - Data processing: all inputs reprojected, cropped, and resampled to 1x1 km2 grid prior to model runs.
  - Quality control: no additional quality control beyond relying on published sources.

- Outputs and usage for monitoring
  - The dataset supports consistent, standardised assessment of the hydrological cycle, water balance, and environmental needs within the Ebro basin.
  - Useful for monitoring environmental health and policy performance over time, with transparent data provenance and reproducible configurations.

- Miscellaneous and references
  - Related publications: CWatM foundational papers (e.g., Burek et al. 2020; Guillaumot et al. 2022).
  - Input/output references and data source citations provided (MSWEP, CHELSA, MIRCA2000, HYDE, etc).
  - Additional articles in preparation are noted for future updates.