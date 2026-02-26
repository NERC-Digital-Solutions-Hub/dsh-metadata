# Groundwater2030: Data structure for field survey files

## What the data are
- Four separate CSV tables that can be joined using common identifier fields.
- Identifiers are unique to each groundwater source that formed the basis of the fieldwork.
- For the sanitary risk and water quality datasets, these fields form primary keys.
- For the well customer field, Well IDs are held as a foreign key.

## Tables and key fields
- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspection of groundwater sources
  - Well ID field: Wellcode
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources
  - Well ID field: Wellcode
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners
  - Well ID field: Well number
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers
  - Well ID field: Well number

## Identifier scheme and linking
- Unique identifiers take the form W1…n, S1…n, B1…n:
  - W = well, S = spring, B = borehole
- An additional code O indicates wells in the baseline survey for which water quality data could not be collected.
- Where owner or customer questionnaires could not be linked to an individual well, they are labeled None1, None2, etc.
- All questionnaires include neighbourhood information even when links to specific wells are missing.

## Practical implications for data management
- You can merge datasets via the common Wellcode/Well number fields to create a unified view per groundwater source.
- Be mindful of:
  - Multiple customers per groundwater source
  - Wells with baseline status (O) and missing water quality data
  - Potential unlinked owner/customer questionnaires (None codes)
- Ensure consistent metadata and proper documentation of identifiers to maintain data discoverability and usability across analyses.