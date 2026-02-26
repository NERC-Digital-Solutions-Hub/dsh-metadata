# Survey of the terrestrial habitats and vegetation of Shetland, 1974

## Overview and dataset purpose
- A comprehensive survey of terrestrial habitats, vegetation and soils in the Shetland Isles (Shetland, Scotland), conducted in 1974.
- Aimed to assess variation in vegetation, provide a user guide to habitat types, and establish a structural basis for monitoring future change.
- Data were gathered to support an environmental assessment for oil exploration impacts and to monitor environmental change over time.
- Outputs include standardized, multi-taceted data suitable for analysis and self-service exploration (plants, soils, habitats, and related biota).

## Geographic and temporal scope
- Geographic coverage: Shetland Isles, Scotland.
- Time period: 1974; survey data managed and documented for long-term monitoring.
- Privacy/locations: precise plot locations withheld to protect landowner privacy; squares are representative samples of larger land classes.

## Data components and formats
- SHETLAND_SURVEY_PLOT_DATA.csv
  - Descriptions for plot-level data, plot habitat within 50 m, and field-recorded codes.
  - Includes STRATA, PLOT, CODE, DESCRIPTION, FIELD_SHEET, YR (year = 1974).
- SHETLAND_SURVEY_PLOT_INFO.csv
  - Slope, aspect and soil information for each plot.
  - Includes STRATA, SURVEY_STRATA_SUB, PLOT, SLOPE (degrees), ASPECT (degrees), LITTER_TOP/BOT, ORG_TOP/BOT, MIXED_TOP/BOT, LEACH_TOP/BOT, WEATHER_TOP/BOT, UNDER_TOP, SOIL_PH (pH).
- SHETLAND_SURVEY_GROUND_FLORA.csv
  - Species list for nested plots (vascular plants, bryophytes, lichens) with cover data.
  - Includes STRATA, PLOT, YR (1974), NEST, COVER, SP_CODE, SP_NAME, FIELD_SHEET.
- Appendix II provides a Full Species list (extensive, including vascular plants, bryophytes, lichens, and other flora).

## Sampling design and survey design
- Sampling approach: stratified sampling across the Shetland land area.
- Stratification: 16 strata identified from a 1 km^2 map-based study; each stratum contained 5 x 1 km^2 units selected randomly.
- Plot design: within each 1 km^2 unit, the area was subdivided into 16 sub-squares; a 200 m^2 plot was randomly selected from within each sub-square (omitting sub-squares landing in water).
- Total plots: 927 selected; 911 actually surveyed due to inaccessibility or cropping.
- Field methods: Bunce & Shaw (1973) standardized survey procedures; a field handbook detailed the methods.
- Vegetation data collection: nested quadrat approach (4 m^2, 25 m^2, 50 m^2, 100 m^2, and full 200 m^2) with species recorded by size class and percent cover.
- Soil data collection: soil described by horizon with standard categories; shallow center-pit and auger samples to classify horizons; top 10 cm collected for pH analysis.
- Habitat data collection: within-plot and within-50 m surrounding area habitat types recorded; slope and aspect measured; definitions provided in the field handbook.

## Data collection details and key variables
- Vegetation data: all vascular plants, bryophytes, and macro-lichens recorded per plot; species list complemented by additional surveys for bryophytes/lichens.
- Soil data: horizon depths and descriptive categories; pH analysis of topsoil (10 cm) sample.
- Habitat data: habitat categories inside the plot and in the surrounding 50 m; slope and aspect captured.
- Parameters and codes: standardized data fields and recording codes maintained for cross-plots comparison.
- Data management: field data were digitized into structured CSVs with explicit column descriptions (codes, descriptions, depths, pH, etc.).

## Outputs, data quality and usage
- Data products are designed to enable: data discovery, cross-plot comparison, and self-serve exploration of vegetation, soils, and habitats.
- Standardized methods (Bunce & Shaw, 1973) underpin data quality and comparability across plots and variables.
- The datasets support historical environmental baselines for monitoring change in habitat types and vegetation since 1974.
- Outputs are suitable for integration with related Shetland environmental datasets and for supporting long-term monitoring programs.

## Access, limitations and interpretation notes
- Location privacy: precise plot coordinates are withheld; Bunce & Bassett (2015) provide context and classification for land areas without revealing exact sites.
- Data scope: 911 plots surveyed; data cover vegetation (including ground flora), soils, and habitats, with nested plot structure and multiple derived variables.
- Related publications and datasets: References include Bunce & Shaw (1973), Bunce & Bassett (2015) on land classification, and the Shetland project monitoring reports (1975).
- Appendices and field documentation: Appendix I plot codes and Appendix II full species list provide reference schemata and taxonomic nomenclature used at the time; field methods are described in the Shetland Vegetation Survey handbook.

## Applications and related use cases
- Historical baseline for habitat monitoring and biodiversity assessments in Shetland.
- Data integration with other Shetland environmental datasets to assess changes since 1974.
- Informing environmental impact assessments related to oil exploration by providing context on past environmental conditions.
- Development of data products (dashboards, reports) enabling stakeholders to explore vegetation, habitat types, and soil properties interactively.