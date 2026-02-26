# Groundwater2030: Data structure for field survey files

- Overview
  - Four separate CSV tables are provided for groundwater field survey data.
  - Tables can be joined using common identifier fields; identifiers are unique to each groundwater source.
  - Primary keys: Groundwater2030_sanrisk.csv and Groundwater2030_waterquality.csv use Wellcode as the key; Groundwater2030_well_owner_survey.csv and Groundwater2030_WellCustomerSurvey.csv use Well number as the key.
  - The structure supports linking sanitary risk, water quality, well owner surveys, and well customer surveys for each groundwater source.

- Tables and key fields
  - Groundwater2030_sanrisk.csv
    - Description: Sanitary risk inspection data for groundwater sources.
    - Well ID field: Wellcode (primary key).
  - Groundwater2030_waterquality.csv
    - Description: Water quality test results for groundwater sources.
    - Well ID field: Wellcode (primary key).
  - Groundwater2030_well_owner_survey.csv
    - Description: Questionnaire survey of well owners.
    - Well ID field: Well number (primary key).
  - Groundwater2030_WellCustomerSurvey.csv
    - Description: Questionnaire survey of well customers.
    - Well ID field: Well number (primary key).

- Key conventions and linkage
  - Unique identifiers take the form: W1…n (well), S1…n (spring), B1…n (borehole).
  - The prefix (W/S/B) indicates source type; an additional code O marks wells in the baseline survey where water quality data could not be collected.
  - There may be more than one customer for a single groundwater source.
  - If owner or customer questionnaires could not be linked to an individual well, they are labeled None1, None2, etc. All questionnaires include neighbourhood information.

- Data quality and governance implications
  - Clear cross-table linkage relies on consistent use of the Wellcode/Well number identifiers.
  - O-codes signal incomplete data coverage (baseline wells without current water quality data), important for gap analysis.
  - Handling of None-linked questionnaires and varying source types (W/S/B) requires careful metadata management to maintain traceability and data provenance.

- Practical considerations for monitoring frameworks
  - Enables integrated monitoring across sanitary risk, water quality, and stakeholder surveys for each groundwater source.
  - Supports identification of data gaps (e.g., baseline wells lacking water quality data) and data provenance issues (ownership and customer linkage).
  - Facilitates dataset joining while preserving the distinction between well-based and other source types and accommodating multiple customers per source.