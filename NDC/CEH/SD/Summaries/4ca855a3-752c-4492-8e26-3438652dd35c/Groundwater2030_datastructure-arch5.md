# Groundwater2030: Data structure for field survey files

## Overview
- Four CSV tables: Groundwater2030_sanrisk.csv, Groundwater2030_waterquality.csv, Groundwater2030_well_owner_survey.csv, Groundwater2030_WellCustomerSurvey.csv.
- Tables can be joined via common identifier fields to form a cohesive dataset about groundwater sources.
- Unique groundwater sources are identified with prefixes: W (well), S (spring), B (borehole); O indicates wells in Baseline survey with no current water quality data.
- Multiple customers may be associated with a single groundwater source; all questionnaires include neighborhood information.

## Data structure and identifiers
- Groundwater sources are encoded with unique IDs using prefixes W, S, B.
- An additional O code marks wells from the baseline survey lacking current water quality data.
- Primary keys by dataset:
  - Groundwater2030_sanrisk.csv: Wellcode (Well ID) as primary key.
  - Groundwater2030_waterquality.csv: Wellcode (Well ID) as primary key.
  - Groundwater2030_well_owner_survey.csv: Well number as primary key.
  - Groundwater2030_WellCustomerSurvey.csv: Well number as primary key.
- Within the wellcode/well number field, IDs form forms like W1…n, S1…n, B1…n; and None1…n indicates unlinked owner/customer questionnaire records.

## Tables and primary keys
- Groundwater2030_sanrisk.csv
  - Purpose: Sanitary risk inspection data for groundwater sources.
  - Key: Wellcode.
- Groundwater2030_waterquality.csv
  - Purpose: Water quality test results for groundwater sources.
  - Key: Wellcode.
- Groundwater2030_well_owner_survey.csv
  - Purpose: Questionnaire survey of well owners.
  - Key: Well number.
- Groundwater2030_WellCustomerSurvey.csv
  - Purpose: Questionnaire survey of well customers.
  - Key: Well number.

## Identifiers, linkage, and data integrity
- Datasets are linked via Wellcode/Well number fields to form a joined view of sanitary risk, water quality, owner, and customer information.
- Ownership and customer records may have the same source but multiple entries per source; the data structure accommodates multiple customers per groundwater source.
- When owner/customer questionnaires cannot be linked to a specific well, entries labeled None1, None2, etc. are used, but neighborhood information is still included.

## Special codes and data linkage notes
- ID prefixes indicate source type: W (well), S (spring), B (borehole).
- O indicates wells in the baseline survey without available water quality data.
- Neighborhood information is included in all questionnaire data, supporting contextual analyses even when some links are missing.

## Data governance considerations for Data Stewards
- Ensure consistent application of prefixes and IDs across all tables to maintain reliable join key integrity.
- Manage and document cases where links are missing or labeled None…, and track any provenance or status (e.g., O-coded wells with no current water quality data).
- Validate that multiple customer records per source are correctly associated and that the linkage between owner and source remains clear.
- Establish update and versioning practices so that changes in one table (e.g., new water quality results or updated owner information) can be reflected across all linked datasets.
- Maintain metadata describing field definitions, data collection timelines, and any preprocessing/transformation steps applied to align the four tables for sharing and reuse.