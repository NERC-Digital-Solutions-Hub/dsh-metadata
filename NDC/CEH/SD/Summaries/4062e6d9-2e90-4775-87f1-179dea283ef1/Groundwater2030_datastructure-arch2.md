# Groundwater2030: Data structure for field survey files

- Overview
  - The dataset consists of four separate CSV tables designed to be joined via common identifier fields.
  - Identifiers are unique to each groundwater source and form primary keys for sanitation risk and water quality data; well IDs in owner and customer surveys act as foreign keys.
  - Tables support linking sanitary risk, water quality, and survey data for comprehensive groundwater monitoring analysis.

- Tables and keys
  - Groundwater2030_sanrisk.csv
    - Description: Sanitary risk inspection of groundwater sources.
    - Well ID field: Wellcode.
  - Groundwater2030_waterquality.csv
    - Description: Water quality test results for groundwater sources.
    - Well ID field: Wellcode.
  - Groundwater2030_well_owner_survey.csv
    - Description: Questionnaire survey of well owners.
    - Well ID field: Well number.
  - Groundwater2030_WellCustomerSurvey.csv
    - Description: Questionnaire survey of well customers.
    - Well ID field: Well number.

- Identifier scheme
  - Unique identifiers follow the form W1…n (well), S1…n (spring), B1…n (borehole).
  - An additional code O marks wells in the baseline survey for which current water quality data could not be collected.

- Linking and data richness
  - More than one customer may be associated with a single groundwater source.
  - If an owner or customer questionnaire cannot be linked to a specific well, it is labeled None1, None2, etc.
  - All questionnaires include neighbourhood information.

- Practical implications for monitoring and analysis
  - The structured keys enable integrated analyses across sanitary risk, water quality, and survey data.
  - Analysts should handle O codes (missing current water quality), and multiple customers per source during joins and analyses.
  - Data governance and accessibility considerations are supported by having explicit primary/foreign keys and neighbourhood/context information.