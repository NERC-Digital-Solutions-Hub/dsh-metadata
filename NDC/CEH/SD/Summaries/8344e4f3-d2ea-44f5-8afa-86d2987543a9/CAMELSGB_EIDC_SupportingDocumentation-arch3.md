# CAMELS-GB: Catchment attributes and hydro-meteorological timeseries for 671 catchments across Great Britain

- Provides daily hydro-meteorological timeseries and a comprehensive set of catchment attributes for 671 GB catchments.
- Data period: 1 October 1970 to 30 September 2015.
- Open, community-oriented dataset designed to support environmental data analyses, modelling, and policy scrutiny.

## What is included

- Hydro-m meteorological timeseries
  - Variables: rainfall, potential evapotranspiration (PET), temperature, shortwave and longwave radiation, specific humidity, wind speed, and river discharge.
  - Temporal resolution: daily.
  - Data sources: CEH-GEAR (rainfall), CHESS-met (meteorology), CHESS-PE (PET), NRFA (river discharge).
  - PET implemented with Penman-Monteith; two PET estimates provided (PET and PETI) to account for interception.
  - 671 catchments; no missing data in meteorological series; flow series may contain NaN where data are missing.
  - File naming: CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930.txt (16436 rows, 11 columns).

- Catchment attributes (8 classes)
  - Topography: gauge_id, gauge_name, location coordinates, area, elevation statistics, drainage path slope.
  - Climatic indices: mean precipitation, mean PET, aridity, seasonality, snow fraction, high/low precipitation frequencies and durations, timing metrics.
  - Hydrologic signatures: mean discharge, runoff ratio, streamflow elasticity, flow-duration curve metrics, baseflow indices, timing metrics for high/low flow periods, low/high flow quantiles.
  - Land cover: percentages of deciduous/evergreen woodland, grass, shrubs, crops, urban, inland water, bare soil, and dominant land cover.
  - Soils: detailed soil properties (sand/silt/clay fractions, depth to roots, organic carbon, bulk density, available water content, hydraulic conductivity, porosity), including missing-data indicators and percentile values.
  - Hydrogeology: groundwater productivity categories, fracture/intergranular flow indicators.
  - Hydrometry: gauge type, data availability window, discharge uncertainty, stage-discharge related metrics.
  - Human influences: abstraction/discharge metrics, reservoir attributes (count, capacity, usage for hydroelectricity, reservoir network, and related metadata), data limitations noted (England-only data, time-variant coverage, potential misalignment with sub-catchments).
  - Data sources for attributes are described in the dataset documentation; several caveats apply (e.g., land cover snapshot from 2015, soil data heterogeneity, abstraction/discharge data coverage).

- Catchment boundaries
  - Shapefiles for CAMELS_GB_catchment_boundaries in British National Grid projection.
  - Boundaries derived from CEH IHDTM flow-direction grids; boundaries may introduce errors if catchment area definitions are imprecise.

## Data sources and context

- Context and motivation
  - Built to extend open data resources (CAMELS family) by providing a consistent GB-wide, large-sample dataset for hydrometeorological analyses and modelling.
  - Originates from integration efforts in the UK Environmental Virtual Observatory and the MaRIUS drought/water-scarcity programme.
  - Aims to improve data accessibility, reproducibility, and cross-catchment comparability through common data structures and open-source tools.

- Data provenance and reproducibility
  - Uses NRFA river flow data, CEH-GEAR rainfall, CHESS-met meteorology, CHESS-PE PET, CEH IHDTM for boundaries, UK soil and hydrogeology datasets, and Lands cover maps (LCM2015) with caveats about snapshot nature and classification uncertainties.
  - Open access philosophy; accompanying CAMELS-GB paper recommended for detailed methodology and usage guidance.

## Data construction and processing

- Deriving timeseries and attributes
  - Catchment timeseries computed by assigning 50 m grid cell values to catchment masks and averaging to produce catchment-mean values (weighted by grid cell area).
  - Clear guidance on handling missing data (e.g., flow NaNs; other meteorological fields complete).
  - Attribute files organized by class with gauge_id as the key linkage.

- Data formats and access
  - Timeseries: CSV files for each catchment with 16436 daily records and 11 data columns.
  - Attributes: eight text files (one per attribute class) listing attributes per catchment with gauge_id as the key.
  - Boundary data: ESRI shapefile (.shp) format.
  - Supplementary information on data sources and access provided in the documentation.

## Key caveats and considerations for monitoring and policy use

- Data completeness and coverage
  - Meteorological fields are complete; discharge data may have gaps ('NaN') depending on station history and data availability.
  - Abstraction and discharge attributes for human influences are England-only and may be NaN for catchments spanning England/Wales or England/Scotland; totals are mean values with caveats about time periods and reporting.

- Spatial and temporal resolution limitations
  - Land cover is a snapshot (LCM2015) and subject to classification uncertainties; may differ from NRFA land-use representations.
  - Soil properties exhibit high spatial heterogeneity; correlations with ground measurements may be weak due to pedotransfer function limitations and data origin.

- Boundary definitions and scale
  - Catchment boundaries are model-derived and may introduce errors in hydrometeorological attribution for poorly defined areas, especially for smaller catchments.

- Data governance and usability
  - Dataset is designed to be openly shareable with metadata, but certain data components (e.g., some abstraction datasets) come with licensing and scope caveats.
  - Recommends consulting the CAMELS-GB paper for deeper understanding of variable definitions, methods, and limitations.

## Guidance for use in monitoring and policy decision-making

- Use CAMELS-GB to:
  - Benchmark hydro-meteorological behaviour and catchment responses across GB.
  - Support model development and evaluation for drought risk, water scarcity, and policy scenario analysis.
  - Facilitate cross-catchment comparative studies with harmonized variables and transparent metadata.

- Best practices:
  - Read the CAMELS-GB paper for detailed methodology and dataset-specific notes.
  - Consider data quality flags, missing-data patterns, and the snapshot nature of certain attributes when interpreting results.
  - Leverage the accompanying boundary and attribute files to align with your monitoring framework’s governance and reproducibility requirements.

## Acknowledgements and references

- Funded by UK Natural Environment Research Council (NERC) through MaRIUS: NE/L010399/1.
- Related datasets and methodological references provided (e.g., CAMELS-CL for Chile, CAMELS-USA, CHESS datasets, NRFA, BGS hydrogeology, CEH GEAR, etc.).
- Authors acknowledge project contributors and data providers; users encouraged to cite the CAMELS-GB paper and dataset in analyses.