# Groundwater2030: Data structure for field survey files

- Four CSV data tables are provided:
  - Groundwater2030_sanrisk.csv: Sanitary risk inspection of groundwater sources. Primary key: Wellcode.
  - Groundwater2030_waterquality.csv: Water quality test results for groundwater sources. Primary key: Wellcode.
  - Groundwater2030_well_owner_survey.csv: Questionnaire survey of well owners. Uses Wellcode as the linking field.
  - Groundwater2030_WellCustomerSurvey.csv: Questionnaire survey of well customers. Uses Wellcode as the linking field.

- Linking and identifiers:
  - All tables share common identifier fields that allow joining the datasets.
  - Unique identifiers for groundwater sources are form W1…n (well), S1…n (spring), B1…n (borehole).
  - An O code indicates wells from the baseline survey for which water quality data could not be collected now.
  - Within the wellcode / well number field:
    - W, S, B prefixes denote source type (well, spring, borehole).
    - Some wells may have multiple associated customers.

- Customer and owner linkage:
  - It is possible that more than one customer is linked to a single groundwater source.
  - When owner or customer questionnaires could not be linked to an individual well, they are labeled with 'None' followed by a number (e.g., None1, None2).
  - All questionnaires include neighbourhood information, even when direct linkage to a specific well is not possible.

- Data governance and structure implications for monitoring frameworks:
  - The structure supports clear data integration across sanitary risk, water quality, and stakeholder surveys via consistent identifiers.
  - Primary and foreign key design facilitates traceability and reproducibility of monitoring analyses.
  - Presence of baseline and missing data indicators (O, NoneX) requires explicit handling in reporting and data quality checks.
  - Metadata and data provenance considerations are essential to verify dataset usefulness and compatibility for governance, sharing, and up-to-date maintenance.