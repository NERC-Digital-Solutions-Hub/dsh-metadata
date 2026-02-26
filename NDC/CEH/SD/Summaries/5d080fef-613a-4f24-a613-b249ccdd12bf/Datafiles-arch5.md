# Datafiles

## Overview
- Inventory of data files and the time periods for which data are available.
- Covers multiple sites and data types related to forest and grassland ecosystems.

## Datasets and Files
- Forest (semi-mature forest site)
  - Forest_Rainfall_raw.csv
  - Forest_Rainfall_processed.csv
  - Forest_micrometeorology.csv
  - Forest_Throughfall_automatic.csv
  - Forest_Throughfall_manual.csv
  - Forest_Stemflow_raw.csv
  - Forest_Stemflow_processed.csv
  - Forest_Sapflow_raw.csv
  - Forest_Sapflow_processed.csv
  - Forest_Soilmoisture_raw.csv
  - Forest_Soilmoisture_processed.csv
  - Forest_Overlandflow.csv
- ReforestedTF / Young forest site
  - ReforestedTF_Rainfall_raw.csv
  - ReforestedTF_Rainfall_processed.csv
  - ReforestedTF_micrometeorology.csv
  - ReforestedTF_Throughfall_automatic.csv
  - ReforestedTF_Throughfall_manual.csv
  - ReforestedTF_Stemflow_raw.csv
  - ReforestedTF_Stemflow_processed.csv
  - ReforestedTF_Sapflow_raw.csv
  - ReforestedTF_Sapflow_processed.csv
  - ReforestedTF_Soilmoisture_raw.csv
  - ReforestedTF_Soilmoisture_processed.csv
  - ReforestedTF_Overlandflow.csv
- Degradedland / Degraded grassland site
  - Degradedland_Rainfall_raw.csv
  - Degradedland_Rainfall_processed.csv
  - Degradedland_micrometeorology.csv
  - Degradedland_Soilmoisture_raw.csv
  - Degradedland_Soilmoisture_processed.csv
  - Degradedland_Overlandflow.csv
  - Degradedland_Soil_Heat_flux.csv

## Time Periods
- Most files include explicit time ranges, typically around October 2014 to September 2015, with variations such as:
  - 03-10-2014 to 30-09-2015
  - 01-10-2014 to 30-09-2015
  - 15-10-2014 to 01-10-2015
  - 16-02-2015 to 30-09-2015
  - 30-09-2015 to 02-10-2014 (and similar framing for young forest)
- Some entries have incomplete or truncated time period data due to formatting in the source listing.

## Data Quality and Governance Considerations (Data Steward Perspective)
- The dataset collection includes both raw and processed versions, indicating the need for clear documentation of data processing steps and provenance.
- Descriptions are present, but formatting inconsistencies and occasional incomplete time ranges suggest a need for standardized metadata and validation.
- Data types span rainfall, micrometeorology, throughfall, stemflow, sapflow, soil moisture, runoff/overland flow, and soil heat flux across multiple sites (semi-mature forest, young forest, degraded grassland).
- Cross-site naming conventions and units should be harmonized to support discoverability and interoperability.
- There may be embargoes or access controls implied by “updates” and varied time spans; ensure appropriate data sharing permissions and governance workflows.

## Actions for Data Stewards
- Validate and standardize metadata (units, data collection methods, variable names, time stamps).
- Catalogue all files in a data portal, linking raw and processed versions to their descriptions and time periods.
- Confirm complete time period coverage for each file and resolve any formatting inconsistencies.
- Communicate data standards to data creators and ensure timely delivery of updates.
- Plan for ongoing maintenance and updates, including monitoring for embargoes or access restrictions.