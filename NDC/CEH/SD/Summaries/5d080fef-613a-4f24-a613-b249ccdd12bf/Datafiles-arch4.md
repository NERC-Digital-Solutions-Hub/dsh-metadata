# Datafiles

## Overview
- An inventory of data files describing datasets and their availability for multiple study sites.
- Includes raw and processed data, methodological descriptions, and metadata across forest and degraded landscapes.
- Time periods primarily span late 2014 to late 2015, with multiple variables and measurement types.

## Data assets and contents
- Datafiles.rft: overview of the different files and the time period for which data are available.
- Study Sites.rtf: information on the three study sites.
- Methods.rtf: brief descriptions of data collection methods and the contents of the different datafiles.
- Forest site (semi-mature forest):
  - Forest_Rainfall_raw.csv: raw rainfall data; 03-10-2014 to 30-09-2015.
  - Forest_Rainfall_processed.csv: 5-minute rainfall data; 01-10-2014 to 30-09-2015.
  - Forest_micrometeorology.csv: 10-minute weather data; 15-10-2014 to 30-09-2015.
  - Forest_Throughfall_automatic.csv: 5-minute throughfall data (gutters); 01-10-2014 to 30-09-2015.
  - Forest_Throughfall_manual.csv: throughfall data from manual gauges; 01-10-2014 to 30-09-2015.
  - Forest_Stemflow_raw.csv: raw stemflow data; 16-02-2015 to 30-09-2015.
  - Forest_Stemflow_processed.csv: processed stemflow data; 16-02-2015 to 30-09-2015.
  - Forest_Sapflow_raw.csv: temperature data used to estimate sap flux density; 01-10-2014 to 01-10-2015.
  - Forest_Sapflow_processed.csv: sap flux density and sap flow data; 01-10-2014 to 01-10-2015.
  - Forest_Soilmoisture_raw.csv: raw soil moisture data; 15-10-2014 to 01-10-2015.
  - Forest_Soilmoisture_processed.csv: processed soil moisture data; 15-10-2014 to 01-10-2015.
  - Forest_Overlandflow.csv: daily runoff data from bounded overland flow plots; 01-10-2014 to 30-09-2015 (partial text available).
- Young forest site (reforested/tree fallow):
  - ReforestedTF_Rainfall_raw.csv: raw rainfall data; 02-10-2014 to 28-09-2015.
  - ReforestedTF_Rainfall_processed.csv: 5-minute rainfall data; 01-10-2014 to 30-09-2015.
  - ReforestedTF_micrometeorology.csv: 10-minute weather data; 15-10-2014 to 30-09-2015.
  - ReforestedTF_Throughfall_automatic.csv: 5-minute throughfall data; 01-10-2014 to 30-09-2015.
  - ReforestedTF_Throughfall_manual.csv: throughfall data from manual gauges; 01-10-2014 to 30-09-2015.
  - ReforestedTF_Stemflow_raw.csv: raw stemflow data; 17-02-2015 to 30-09-2015.
  - ReforestedTF_Stemflow_processed.csv: processed stemflow data; 17-02-2015 to 30-09-2015.
  - ReforestedTF_Sapflow_raw.csv: sapflow-related temperature data; 01-10-2014 to 30-09-2015.
  - ReforestedTF_Sapflow_processed.csv: sap flux density and sap flow data; 01-10-2014 to 01-10-2015.
  - ReforestedTF_Soilmoisture_raw.csv: raw soil moisture data; 01-10-2014 to 10-10-2015.
  - ReforestedTF_Soilmoisture_processed.csv: processed soil moisture data; 01-10-2014 to 01-10-2015.
  - ReforestedTF_Overlandflow.csv: daily runoff data; 01-10-2014 to 30-09-2015.
- Degraded grassland site:
  - Degradedland_Rainfall_raw.csv: raw rainfall data; 02-10-2014 to 29-09-2015.
  - Degradedland_Rainfall_processed.csv: 5-minute rainfall data; 01-10-2014 to 30-09-2015.
  - Degradedland_micrometeorology.csv: 5-minute weather data; 01-10-2014 to 01-10-2015.
  - Degradedland_Soilmoisture_raw.csv: raw soil moisture data (two notes indicate multiple entries/ ranges; first unspecified, second 15-10-2014 to 01-10-2015).
  - Degradedland_Soilmoisture_processed.csv: processed soil moisture data (two entries indicate multiple ranges; first unspecified, second 15-10-2014 to 01-10-2015).
  - Degradedland_Overlandflow.csv: daily runoff data; 01-10-2014 to 30-09-2015.
  - Degradedland_Soil_Heat_flux.csv: soil heat flux data; 01-10-2014 to 30-09-2015.

## Data formats and structure
- File types represented: primarily CSV (.csv) and rich text (.rtf/.rft) files.
- Data scope includes raw and processed versions, as well as methodological context (Methods and Study Sites files).
- Measurements cover hydrology, meteorology, and soil-plant water relations across multiple sites and measurement schemes (automatic and manual).

## Data governance and reuse considerations for Data Leaders
- Comprehensive metadata support: descriptions accompany each datafile, aiding discoverability and understanding of contents and time ranges.
- Data lineage: clear separation of raw vs. processed data, plus method descriptions, supports traceability and reproducibility.
- Site coordination: multiple study sites (semi-mature forest, young forest, degraded grassland) with parallel measurement schemes, enabling cross-site comparisons but requiring careful harmonization of time periods and formats.
- Data gaps and clarity needs: some time period entries are incomplete or ambiguous (e.g., Forest_Overlandflow.csv, degraded soil-moisture entries with multiple ranges), indicating a need for precise metadata and data provenance to ensure correct interpretation.
- Potential for integration: structured inventory across rainfall, micrometeorology, throughfall, stemflow, sapflow, soil moisture, and overlandflow data provides a rich basis for holistic water balance and ecosystem functioning analyses.

## End note
- The document serves as a foundational data catalog for planning data access, quality checks, and cross-site data assimilation in data-driven projects.