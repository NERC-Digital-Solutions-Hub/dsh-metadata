# Catchment attributes and hydro-meteorological timeseries for 671 catchments across Great Britain (CAMELS-GB)

- Purpose: provide a freely available, standardized dataset of daily hydro-meteorological timeseries and catchment attributes to support environmental data analysis and modelling across Great Britain.
- Coverage: 671 catchments across Great Britain (NRFA SLA network); Northern Ireland excluded due to data limitations.
- Temporal span: daily data from 1 October 1970 to 30 September 2015.

## Data components

- Hydro-meteorological timeseries
  - Daily catchment-averaged series for: flow, rainfall, potential evapotranspiration (PET), temperature, shortwave radiation, longwave radiation, specific humidity, wind speed.
  - Rainfall: CEH-GEAR (1 km gridded rainfall estimates).
  - MET variables: CHESS-met (met data) and CHESS-PE (PET with two estimates: PET and PETI, the latter including interception on rainfall days).
  - Flow: observed discharge from the UK National River Flow Archive (NRFA); no missing data in met-related series, but flow series may contain NaN values.
  - File format: CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930.csv; 16436 rows per file, 11 columns; date in column 1; missing in flow denoted as NaN.
- Catchment attributes
  - Eight attribute files covering: topography, climate, hydrology, land cover, soils, hydrogeology, hydrometry, and human influences.
  - Each file starts with gauge_id (NRFA station ID) and contains multiple attributes with definitions, units, and data sources (Tables 2–9 in the document).
  - Land cover: attributes derived from Land Cover Map 2015 (LCM2015) at 1 km resolution; notes on snapshot nature and classification uncertainties.
  - Soils: 48 attributes from European Soil Database and bedrock depth products; caveats about spatial heterogeneity and pedotransfer function uncertainties.
  - Hydrogeology: 9 attributes based on BGS maps; suitable for regional comparisons but not sub-catchment fine-scale interpretation.
  - Hydrometry: 19 attributes describing gauging stations, data periods, discharge uncertainty, and channel characteristics.
  - Human influences: 21 attributes including abstractions, discharges, reservoir data, and their caveats (England-only data, time-period variation, potential misalignment with catchment boundaries, and returns to storage).
- Catchment boundaries
  - Boundaries derived from CEH Integrated Hydrological Digital Terrain Model (IHDTM) flow grids; catchment boundaries provided as CAMELS_GB_catchment_boundaries shapefile (British National Grid projection).
  - Note: potential boundary definition errors if catchment area is poorly defined.
- Data sources and accessibility
  - Key sources: NRFA (flow, boundaries, gauge metadata), CEH-GEAR (areal rainfall), CHESS-met, CHESS-PE, European Soil Database, BGS hydrogeology maps, CEH IHDTM, UK reservoir inventory, Environment Agency abstractions/discharges.
  - Additional documentation and a CAMELS-GB paper describe methodology and use cases; dataset is intended for broad community use.
- Documentation and files
  - Timeseries: per-catchment CSV with standardized naming and complete meteorological data; flow may have gaps.
  - Attributes: eight text files (one per attribute class) with gauge_id and detailed attribute columns.
  - Boundaries: a shapefile with catchment polygons.

## Data derivation and processing

- Timeseries calculation
  - For each catchment, 50 m grid cells within the catchment mask are matched to corresponding dataset grid cells; values are averaged to produce catchment-averaged timeseries.
  - This weighting accounts for varying catchment sizes and grid resolutions.
- Attribute derivation
  - Attributes are compiled from the respective source datasets (land cover, soils, hydrogeology, etc.) with explicit caveats on data limitations and temporal or spatial mismatches.
- Completeness and quality
  - Meteorological time series are reported as complete (no missing data); flow data may contain NaN values where observations are unavailable or flagged.

## Data quality, caveats and limitations

- Catchment boundaries
  - Potential errors if the boundary is not well-defined for a given gauging station.
- Land cover and soils
  - LC2015 is a snapshot; uncertainty due to satellite imagery and classification; soils data exhibit high spatial heterogeneity and pedotransfer function uncertainties may affect interpretations.
- Abstractions and discharges (human influences)
  - England-only data; some catchments have NaN values or partial coverage; abstractions may not map cleanly to catchments due to boundary definitions or groundwater contributions to neighboring catchments.
  - Data cover different time periods; abstraction returns and discharges may not reflect all withdrawals or returns (only treated wastewater included; other returns are not accounted for).
- Hydrological attributes
  - Discharge uncertainty estimates depend on methods used; may not apply uniformly across all stations or time periods.
- General guidance
  - Users are encouraged to read the CAMELS-GB paper for detailed methodology and to consider data limitations when making cross-catchment or temporal comparisons.

## Access, usage and guidance

- Purpose and usage
  - Freely available dataset intended for environmental data analyses and modelling, enabling reproducible, large-sample studies.
- Recommended reading
  - CAMELS-GB paper (Coxon et al.) for in-depth descriptions of data, derivations, and uncertainty considerations.
- Contact
  - For questions on data derivation or usage: gemma.coxon@bristol.ac.uk

## Context and acknowledgements

- Background
  - CAMELS-GB extends the CAMELS framework to Great Britain, building on prior CAMELS datasets in the US and Chile, with aims of open-source, comparable, and reproducible hydrometeorological data across large catchment samples.
- Funding and collaboration
  - Funded by the NERC UK Droughts and Water Scarcity programme (MaRIUS: Managing the Risks, Impacts and Uncertainties of droughts and water Scarcity).
  - Acknowledgements to data providers (NRFA, CEH, BGS, Environment Agency, etc.) and contributors to related open datasets.

- Related materials
  - CAMELS family papers and data descriptions for other regions (e.g., CAMELS-US, CAMELS-CL) to facilitate cross-region comparisons and synthesis.