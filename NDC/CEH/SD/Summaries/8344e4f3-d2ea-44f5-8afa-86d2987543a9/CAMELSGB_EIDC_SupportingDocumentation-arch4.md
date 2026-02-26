# Catchment attributes and hydro-meteorological timeseries for 671 catchments across Great Britain (CAMELS-GB)

## Summary
- A freely available dataset of hydro-meteorological timeseries and catchment attributes for 671 catchments across Great Britain.
- Daily timeseries ( Oct 1, 1970 to Sep 30, 2015 ) including flow, rainfall, potential evapotranspiration, temperature, and various meteorological variables, plus a comprehensive set of catchment attributes.
- Attributes cover topography, climate, hydrology, land cover, soils, hydrogeology, hydrometry, and human influences.
- Data are compiled from the UK National River Flow Archive (NRFA) and enhanced with meteorological datasets (CEHGEAR, CHESS-met, CHESS-PE).
- Aims to support wide-ranging environmental data and modeling analyses with consistent, comparable data across a large sample of GB catchments.
- Documentation and a related CAMELS-GB paper are recommended reading for proper use and context.

## Context and purpose
- Built from NRFA data and additional open datasets as part of the CAMELS family, following the CAMELS blueprint used in the USA, Chile, and other countries.
- Motivated by the MaRIUS drought and water scarcity projects and the UK Environmental Virtual Observatory to improve data integration, openness, and reproducibility.
- Designed to enable cross-catchment comparisons and model testing with standardized variable names and data structures.

## Data scope and catchments
- 671 GB catchments selected from the NRFA SLA network, excluding Northern Ireland (and two gauges without suitable catchments).
- Catchments span diverse climatic and hydrologic regimes and are representative of the broader gauging network.
- Catchment boundaries derived from CEH IHDTM flow direction grids; boundaries may introduce errors where delineation is poor.

## Hydro-meteorological timeseries (3.3)
- Variables included: discharge, rainfall, potential evapotranspiration (PET) with two estimates (PET and PETI, the latter including interception), temperature, humidity, wind speed, shortwave and longwave radiation.
- Daily data sources: rainfall from CEH-GEAR; meteorology from CHESS-met; PET from CHESS-PE; PETI applies interception corrections.
- Time period: 1 Oct 1970 to 30 Sep 2015; meteorological data are complete (no missing values); discharge data may include missing values (NaN).
- Files: 671 CSV time-series files named CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930, each with 16436 rows plus header and 11 data columns.
- Time series are catchment-averaged, derived by weighting grid-cell values within each catchment boundary.

## Catchment attributes (3.4)
- Eight attribute files corresponding to eight classes:
  - Topographic attributes
  - Climatic attributes
  - Hydrologic attributes
  - Land cover attributes
  - Soil attributes
  - Hydrogeology attributes
  - Hydrometry attributes
  - Human influence attributes
- Each file lists gauge_id (NRFA gauge ID) as the first column, followed by multiple attributes with detailed descriptions, units, and data sources.
- Key attribute themes:
  - Location, area, and drainage/topography (elevation, slope, area)
  - Climate indices (mean precipitation, PET, aridity, seasonal patterns, snow fraction, high/low precipitation frequencies and durations)
  - Hydrologic signatures (mean discharge, runoff ratio, baseflow indicators, flow elasticity, slope of flow duration curves, baseflow indices, characteristic timing metrics)
  - Land cover composition and dominant land-cover class
  - Soil properties (sand/silt/clay fractions, organic content, bulk density, water content, porosity, depth to bedrock)
  - Hydrogeology (productivity of groundwater units, fracture vs. intergranular flow indicators)
  - Hydrometry (gauge type, data availability window, discharge uncertainty indicators)
  - Human influences (water abstractions and discharges, reservoir attributes, ratios by sector, reservoir counts and capacities)
- Notable caveats:
  - Land cover is a snapshot (LCM 2015) and may differ from NRFA-derived classifications.
  - Soil attributes carry high spatial heterogeneity and pedotransfer function uncertainties.
  - Abstraction and discharge data are England-only and may be incomplete or time-limited; some effects may cross catchment boundaries.
  - Discharge uncertainty estimates depend on the method used and may not apply uniformly across all time series.
- Attribute data are designed to enable large-sample comparative analyses and model diagnostics.

## Deriving catchment attributes and timeseries (3.5)
- Attributes and timeseries are computed by assigning 50 m grid cell values to catchment mask cells and averaging (weighted by cell area) to produce catchment-level values.

## Data files and formats (4)
- 4.1 Hydro-meteorological timeseries
  - File naming: CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930
  - Contents: daily, catchment-averaged timeseries; 11 data columns; date in YYYY-MM-DD; missing values only in discharge (NaN) for some series.
- 4.2 Catchment attributes
  - Eight text files named CAMELS_GB_<attribute_class>_attributes.txt (e.g., topographic, climatic, hydrologic, landcover, soil, hydrogeology, hydrometry, humaninfluence)
  - Each file: first column is gauge_id; subsequent columns are attributes with defined names, units, data sources.
  Tables 2-9 provide detailed header definitions for each attribute class.
- 4.2 Catchment boundary data
  - Shapefile CAMELS_GB_catchment_boundaries on the British National Grid projection.

## Data sources and accessibility (5)
- Primary data source: UK National River Flow Archive (NRFA) for daily discharge and gauge information.
- Supporting meteorology and terrain datasets:
  - CEH-GEAR for gridded daily rainfall
  - CHESS-met for meteorology
  - CHESS-PE for potential evapotranspiration
  - CEH IHDTM for catchment boundaries
- Additional sources for land cover (LCM2015), European soil data, British Geological Survey hydrogeology maps, reservoir and abstraction data (England-focused), and environment agency datasets.
- Accessibility notes: dataset is freely available; users are encouraged to consult the CAMELS-GB paper for full methodology and context.

## Guidance notes (6)
- The CAMELS-GB dataset is designed for broad use in environmental data analyses and modelling.
- A CAMELS-GB paper with more detailed methodology is recommended prior to use.
- For questions on data derivation or usage, contact the corresponding author listed in the document.

## Acknowledgements (7)
- Funded by NERC UK Droughts and Water Scarcity Programme (MaRIUS; NE/L010399/1).
- Acknowledgement of contributors and data providers, including institutional sources and individuals.

## References
- Key sources cited include CAMELS-related datasets (CAMELS-US, CAMELS-CL), MaRIUS, CEH-GEAR, CHESS datasets, NRFA products, BGS hydrogeology maps, and related hydrology literature.