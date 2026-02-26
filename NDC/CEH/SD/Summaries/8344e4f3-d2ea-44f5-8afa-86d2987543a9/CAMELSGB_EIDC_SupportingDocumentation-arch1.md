# Catchment attributes and hydro-meteorological timeseries for 671 catchments across Great Britain (CAMELS-GB)

- Overview
  - Freely available dataset of daily hydro-meteorological timeseries and catchment attributes for 671 catchments across Great Britain.
  - Integrates river flow data from the UK National River Flow Archive with new meteorological timeseries and a comprehensive set of catchment attributes.
  - Time period: 1 October 1970 to 30 September 2015.
  - Includes rainfall, potential evapotranspiration (PET), temperature, radiation, humidity, wind, and discharge, plus extensive catchment descriptors.

- Context and motivation
  - Builds on UK Environmental Virtual Observatory and MaRIUS projects to unify national datasets for improved hydrological understanding, model simulations, and predictions.
  - Aims to enable large-sample hydrological analyses with consistent variables, open-source tools, and reproducible methodologies.
  - CAMELS-GB complements existing CAMELS datasets (USA, Chile, etc.) with GB-specific attributes and uncertainty characterisation.

- Data scope: catchments and boundaries
  - 671 catchments selected from the UK NRFA SLA network; excludes Northern Ireland and two gauges lacking suitable boundaries.
  - Catchment boundaries derived from CEH IHDTM flow direction grids; boundaries may introduce errors if poorly defined.
  - Shapefiles of catchment boundaries provided in British National Grid projection.

- Hydro-meteorological timeseries (3.3)
  - Daily data (1970-10-01 to 2015-09-30) for each catchment:
    - Discharge (flow), precipitation, PET, temperature, shortwave radiation, longwave radiation, specific humidity, wind speed.
  - Data sources:
    - Precipitation: CEH-GEAR (1 km gridded rainfall estimates).
    - Met timeseries: CHESS-met (1961–2015) and CHESS-PE for PET (1961–2015).
    - PET calculations use Penman-Monteith; two PET estimates:
      - PET: well-watered grass, transpiration only.
      - PETI: intercept interception correction on rainfall days.
  - Data characteristics:
    - No missing data in meteorological timeseries.
    - Flow timeseries may include missing values (NaN).
    - Timeseries files are named CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930 (16436 rows, 11 columns).

- Catchment attributes (eight attribute files; Tables 2–9)
  - Categories:
    - Topography (location, area, elevations, drainage path slope, etc.).
    - Climatic indices (mean precipitation/PET, aridity, seasonality, snow fraction, high/low precipitation metrics, timing).
    - Hydrologic signatures (mean discharge, runoff ratio, flow-ecology sensitivities, baseflow, flow duration curve metrics, low/high flow statistics).
    - Land cover (percentages of deciduous/evergreen woodlands, grass, shrubs, crops, urban, inwater, bare soil; dominant land cover).
    - Soils (sand/silt/clay percentages, depth to roots, organic carbon, bulk density, available water, porosity, depth to bedrock proxies; data include missing-value indicators).
    - Hydrogeology (productivity categories, fracture/intergranular flow, no groundwater).
    - Hydrometry (gage type, data periods, discharge uncertainty, bankfull and structure-full flow, etc.).
    - Human influences (benchmark status, surface water abstractions, groundwater abstractions, discharges, abstractions by sector, reservoir attributes, etc.).
  - Notes and caveats:
    - Land cover uses 2015 UK Land Cover Map ( LC Map 2015 ); differences vs NRFA attributes and uncertainties from satellite imagery.
    - Soils rely on European Soil Database and pedotransfer functions; high spatial heterogeneity and function choice uncertainties.
    - Hydrogeology attributes derived from BGS maps; suitable for regional comparisons but not sub-catchment scale detail.
    - Human-influence data (abstractions/discharges) cover England only; many catchments have NaN or partial data; timing varies by dataset; abstractions may not map directly to catchment-scale discharge.
    - Some water returns to storages and complex interactions may not be fully captured.
  - Data file format:
    - Eight text files: CAMELS_GB_topographic_attributes, CAMELS_GB_climatic_attributes, CAMELS_GB_hydrologic_attributes, CAMELS_GB_landcover_attributes, CAMELS_GB_soil_attributes, CAMELS_GB_hydrogeology_attributes, CAMELS_GB_hydrometry_attributes, CAMELS_GB_humaninfluence_attributes.
    - Each file uses gauge_id as the first column, followed by corresponding attributes.

- Derivation of catchment attributes and timeseries
  - Each 50 m grid cell within a catchment mask is assigned the value of the corresponding dataset grid cell (based on the lower-left corner alignment) and the mean is computed to obtain a catchment-averaged value.
  - This weighted averaging accounts for varying grid cell sizes, important for small catchments in heterogeneous regions.

- Data files and accessibility
  - Timeseries data: CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930.csv
    - Date (yyyy-mm-dd) in column 1; 10 additional data columns described in Table 1.
    - Missing data in flow timeseries indicated as NaN; other timeseries are complete.
  - Catchment attributes: CAMELS_GB_*_attributes.txt (8 files), with gauge_id as column 1 and subsequent attribute columns per Tables 2–9.
  - Catchment boundaries: CAMELS_GB_catchment_boundaries.shp (ESRI shapefile) on the British National Grid projection.
  - Data sources overview (without DOIs) and access details provided; NRFA API, CEHGEAR, CHESS-met, CHESS-PE; bibliography and data provenance described.

- Guidance for use
  - Read the CAMELS-GB paper for detailed methodology, data processing steps, and caveats before using the dataset.
  - Consider the length and completeness of the flow timeseries when calculating hydrologic signatures; account for NaNs and the 1 October 1970–30 September 2015 window.
  - Use PET and PETI thoughtfully depending on interception correction needs in PET-related analyses.
  - Be mindful of boundary definition uncertainties and the snapshot nature of land cover data when interpreting relationships across catchments.
  - Data provenance and metadata are provided to enable reproducibility and traceability of analyses.

- Data sources and acknowledgements
  - UK National River Flow Archive (NRFA) for discharge data.
  - CEH Gridded Estimates of Areal Rainfall (CEHGEAR) for precipitation.
  - CHESS-met and CHESS-PE for meteorology and PET.
  - Integrated Hydrological Digital Terrain Model (IHDTM) for catchment boundaries.
  - UK Land Cover Map 2015 (LCM2015) for land cover attributes.
  - European Soil Database and Pedotransfer functions for soil attributes.
  - British Geological Survey (BGS) hydrogeology maps for hydrogeology attributes.
  - Environment Agency data for abstractions and discharges; reservoir inventories.
  - MaRIUS project and UK Environmental Virtual Observatory as foundational contexts.

- Access and contact
  - Dataset intended for broad use; contact gemma.coxon@bristol.ac.uk for questions about data derivation or usage.
  - CAMELS-GB paper and Earth System Science Data publication recommended for detailed description and validation.
  - Acknowledgement of MaRIUS program and contributing researchers.