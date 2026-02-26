# Datafiles

## Overview
- A data file catalog listing datasets across multiple study sites with descriptions and time ranges.
- Includes raw and processed datasets, plus metadata files describing sites and data collection methods.

## Datasets by site and type

- Semi-mature forest site
  - Forest_Rainfall_raw.csv: raw rainfall data
  - Forest_Rainfall_processed.csv: 5-minute rainfall data
  - Forest_micrometeorology.csv: 10-minute weather data
  - Forest_Throughfall_automatic.csv: 5-minute throughfall data (gutters)
  - Forest_Throughfall_manual.csv: throughfall data from manual gauges
  - Forest_Stemflow_raw.csv: raw stemflow data
  - Forest_Stemflow_processed.csv: processed stemflow data
  - Forest_Sapflow_raw.csv: temperature data for sap flux density
  - Forest_Sapflow_processed.csv: sap flux density and sap flow data
  - Forest_Soilmoisture_raw.csv: raw soil moisture data
  - Forest_Soilmoisture_processed.csv: processed soil moisture data
  - Forest_Overlandflow.csv: daily runoff data
- Reforested (young forest) site
  - ReforestedTF_Rainfall_raw.csv: raw rainfall data
  - ReforestedTF_Rainfall_processed.csv: 5-minute rainfall data
  - ReforestedTF_micrometeorology.csv: 10-minute weather data
  - ReforestedTF_Throughfall_automatic.csv: 5-minute throughfall data (gutters)
  - ReforestedTF_Throughfall_manual.csv: throughfall data from manual gauges
  - ReforestedTF_Stemflow_raw.csv: raw stemflow data
  - ReforestedTF_Stemflow_processed.csv: processed stemflow data
  - ReforestedTF_Sapflow_raw.csv: temperature data for sap flux density
  - ReforestedTF_Sapflow_processed.csv: sap flux density and sap flow data
  - ReforestedTF_Soilmoisture_raw.csv: raw soil moisture data
  - ReforestedTF_Soilmoisture_processed.csv: processed soil moisture data
  - ReforestedTF_Overlandflow.csv: daily runoff data
- Degraded grassland site
  - Degradedland_Rainfall_raw.csv: raw rainfall data
  - Degradedland_Rainfall_processed.csv: 5-minute rainfall data
  - Degradedland_micrometeorology.csv: 5-minute weather data
  - Degradedland_Soilmoisture_raw.csv: raw soil moisture data
  - Degradedland_Soilmoisture_processed.csv: processed soil moisture data
  - Degradedland_Overlandflow.csv: daily runoff data
  - Degradedland_Soil_Heat_flux.csv: soil heat flux data

## Data collection metadata

- Datafiles.rft: overview of the different files and the time period for which data are available.
- Study Sites.rtf: information on the three study sites.
- Methods.rtf: brief description of the methods used to collect the data and the contents of the different datafiles.

## Time periods and data granularity

- Many datasets cover 2014-10-01 to 2015-09-30 (approximate annual window), with some datasets having slightly different ranges (e.g., stemflow and specific measurements).
- Data granularity varies:
  - 5-minute and 10-minute measurements for rainfall, micrometeorology, and throughfall
  - Daily runoff data for overlandflow
  - Temperature-based sapflow estimates (sap flux density and sap flow)
  - Separate raw and processed versions to support data cleaning and transformation

## How this supports data use

- Enables cross-site analysis of hydrological processes (rainfall, throughfall, stemflow, sapflow, soil moisture, overlandflow, heat flux).
- Supports building self-serve data products (dashboards, reports, pivot tables) by combining multiple datasets.
- Provides metadata and methods to validate and reproduce analyses across semi-mature, young forest, and degraded grassland sites.

## Considerations and next steps for Data Support

- Verify any blank or ambiguous Time period fields in the catalog; consult the accompanying RTF metadata for exact ranges.
- Review Methods.rtf and Study Sites.rtf to understand site contexts and data collection protocols before integration.
- Plan data harmonization (units, timestamps, intervals) when combining raw and processed datasets across sites.
- Develop data products and dashboards that compare cross-site hydrological variables and temporal patterns.