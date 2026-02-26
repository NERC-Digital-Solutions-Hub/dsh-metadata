# Catchment attributes and hydro-meteorological timeseries for 671 catchments across Great Britain (CAMELS-GB)

- Provides catchment-scale hydro-meteorological timeseries and a comprehensive set of catchment attributes for 671 catchments across Great Britain.
- Integrates river flow data from the UK National River Flow Archive with new meteorological timeseries and landscape attributes.

## What is included

- Hydro-meteorological timeseries (daily, 1 Oct 1970 to 30 Sep 2015) for each catchment
  - Variables: rainfall, potential evapotranspiration (PET), temperature, shortwave radiation, longwave radiation, humidity, wind speed
  - Additional meteorological inputs: derived PET estimates (two versions: PET and PETI)
  - Discharge data (flow) from NRFA; no missing data in meteorological series, but some gaps (NaN) in flow
  - Data files: CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930.txt (16436 rows, 11 columns per file)
- Catchment boundaries
  - Derived boundaries for 671 catchments using CEH IHDTM flow-direction grids
  - Shapefile: CAMELS_GB_catchment_boundaries (British National Grid)
- Catchment attributes (8 classes, for 671 catchments)
  - Topographic attributes (location, area, elevations, drainage path slope)
  - Climatic indices (mean precipitation, PET, aridity, seasonality, snow fraction, high/low precipitation frequency and timing)
  - Hydrologic signatures (mean discharge, runoff ratio, rainfall–discharge elasticity, slope of flow duration curve, baseflow indices, baseflow estimates, high/low flow quantiles and their characteristics)
  - Land cover attributes (percent cover of deciduous/evergreen woodland, grass, shrubs, crops, urban, inland water, bare soil; dominant land cover)
  - Soils (sand, silt, clay, organic content, bulk density, available water content, hydraulic properties, depth to bedrock, and related percentiles and missing-data indicators)
  - Hydrogeology (productivity-weighted fractions for high/moderate/low productivity, fracture vs intergranular flow, etc.)
  - Hydrometry (gauge type, data availability window, discharge uncertainty metrics, bankfull and structure-full flow, etc.)
  - Human influences (benchmark catchment status, mean abstractions for surface/groundwater, discharges, reservoir attributes, and related caveats)
- Data provenance and harmonisation
  - Data sources include NRFA, CEHGEAR, CHESS-met, CHESS-PE, CEH IHDTM, BGS hydrogeology maps, UK reservoir inventories, and UK Land Cover Map 2015
  - Open data practices aligned with CAMELS datasets (USA, Chile, etc.) to enhance comparability and reproducibility

## Data structure and access

- Time frame and coverage
  - Daily data from 1 October 1970 to 30 September 2015
  - 671 GB catchments; Northern Ireland excluded due to inconsistent meteorological datasets
- File naming and formats
  - Timeseries: CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930.txt
  - Catchment attributes: CAMELS_GB_<attribute_class>_attributes.txt
  - Boundary data: CAMELS_GB_catchment_boundaries.shp (ESRI shapefile)
- Data quality notes
  - Meteorological datasets are complete (no missing values)
  - Flow data contain NaN entries in places; treat as missing
  - Land cover is based on 2015 snapshot (LCM2015) and carries inherent classification uncertainties
  - Soil attributes rely on European Soil Database and pedotransfer relationships; spatial heterogeneity and pedotransfer uncertainties are acknowledged
  - Abstraction and discharge data are England-centric with caveats about temporal coverage and attribution to specific catchments
- Documentation and guidance
  - Users are advised to read the CAMELS-GB paper for detailed attribute descriptions and methodological notes
  - Acknowledgement and contact information provided for data questions

## How to use (Data Support perspective)

- Data integration and product creation
  - Combine hydro-meteorological timeseries with catchment attributes to build self-serve analytical tools (dashboards, position-specific dashboards, or pivot-like analyses)
  - Cross-catchment analyses enabled by consistent naming, units, and open formats across time series and attributes
- Quality assurance and preprocessing
  - Verify catchment boundaries align with target gauges; account for boundary-related potential errors in time series extraction
  - When comparing hydrologic signatures, consider varying length and NaN prevalence in discharge data
  - Use climatic and hydrologic signatures to identify catchments with unique behaviors or data quality concerns
- Potential analyses and data products
  - Hydrological regime classification using hydrologic signatures
  - Trend and anomaly analyses in hydrometeorological variables
  - Regional heatmaps of aridity, seasonality, and high/low flow characteristics
  - Data-driven drought and flood risk assessments leveraging PETPETI contrasts and discharge sensitivities
- Best practices and caveats
  - Land cover and soil attributes come with uncertainties; interpret correlations with caution
  - Abstraction and reservoir data are not uniformly complete across all catchments; use mean totals as indicative indicators rather than exact measures
  - Read the CAMELS-GB paper for deeper methodological context before applying analyses

## Guidance and support

- The dataset is designed as freely available to support environmental data and modelling analyses
- For usage questions or data derivation details, contact gemma.coxon@bristol.ac.uk
- The CAMELS-GB paper is recommended reading to complement dataset usage and interpretation