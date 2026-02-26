# Groundwater2030: Data structure for field survey files

- Purpose and structure
  - Four separate CSV tables are provided to capture groundwater field survey data.
  - Tables can be joined using a set of common, unique identifier fields. 
  - Groundwater2030_sanrisk.csv and Groundwater2030_waterquality.csv use Wellcode as the primary key; the owner and customer surveys use Well number as the key.

- Files and primary keys
  - Groundwater2030_sanrisk.csv
    - Description: Sanitary risk inspection of groundwater sources
    - Primary key: Wellcode (Well ID)
  - Groundwater2030_waterquality.csv
    - Description: Water quality test results for groundwater sources
    - Primary key: Wellcode (Well ID)
  - Groundwater2030_well_owner_survey.csv
    - Description: Questionnaire survey of well owners
    - Primary key: Well number (Well ID)
  - Groundwater2030_WellCustomerSurvey.csv
    - Description: Questionnaire survey of well customers
    - Primary key: Well number (Well ID)

- Unique identifiers and coding
  - Unique identifiers take the form: W1…n, S1…n, B1…n
    - Prefix meaning: W = well, S = spring, B = borehole
  - O code indicates wells in the baseline survey where water quality data could not be collected now.
  - If owner or customer questionnaires could not be linked to an individual well, they are labeled with None followed by a number (e.g., None1, None2). All questionnaires still include neighbourhood information.

- Data relationships and considerations
  - A groundwater source may have multiple customers (one-to-many relationship for WellCustomerSurvey).
  - Sanitary risk and water quality data are tied to wells/sources via Wellcode; owner surveys link via Well number.
  - For baseline wells (O-coded), be aware there may be missing water quality data.
  - When merging datasets, ensure consistent handling of the W/S/B prefixes and the None labels to preserve source-level integrity and neighbourhood context.