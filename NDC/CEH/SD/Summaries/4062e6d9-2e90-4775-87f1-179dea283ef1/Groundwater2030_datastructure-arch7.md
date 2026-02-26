# Groundwater2030: Data structure for field survey files

## Overview
- The data are provided as four separate CSV tables that can be joined via common identifier fields.
- Identifiers are unique to each groundwater source and serve as primary keys for sanitary risk and water quality data; well IDs are used as a foreign key for other datasets.
- Tables:
  - Groundwater2030_sanrisk.csv (sanitary risk inspections) — Well ID field: Wellcode
  - Groundwater2030_waterquality.csv (water quality test results) — Well ID field: Wellcode
  - Groundwater2030_well_owner_survey.csv (well owner questionnaire) — Well ID field: Well number
  - Groundwater2030_WellCustomerSurvey.csv (well customer questionnaire) — Well ID field: Well number

## Datasets and Key Fields
- Groundwater2030_sanrisk.csv: Description = Sanitary risk inspection of groundwater sources; Well ID field = Wellcode
- Groundwater2030_waterquality.csv: Description = Water quality test results; Well ID field = Wellcode
- Groundwater2030_well_owner_survey.csv: Description = Questionnaire survey of well owners; Well ID field = Well number
- Groundwater2030_WellCustomerSurvey.csv: Description = Questionnaire survey of well customers; Well ID field = Well number

## Identifier scheme
- Unique identifiers take the form:
  - W1…n for wells
  - S1…n for springs
  - B1…n for boreholes
- Prefix indicates source type (W = well, S = spring, B = borehole)
- An additional code O indicates wells in the baseline survey for which water quality data could not be collected
- If owner or customer questionnaires could not be linked to an individual well, they are labelled None1, None2, etc. All questionnaires include neighbourhood information

## Linking across datasets
- The four tables are joinable on the respective Well ID fields (Wellcode or Well number).
- There may be one-to-many relationships: one groundwater source can have multiple customers.
- Some wells may appear in sanitary risk and/or water quality data but not have linked owner/customer questionnaire data.

## GIS usage and considerations
- Enables map-based visualization of sanitary risk and water quality by well/spring/borehole type.
- Useful to join with spatial data (locations) using the same identifiers to create geographic representations of risk and quality.
- Ensure consistent identifier matching across tables (Wellcode vs Well number) when integrating into GIS workflows.

## Data quality and limitations
- There may be missing water quality data for some wells (code O indicates baseline wells with no water quality data).
- Some owner/customer questionnaires cannot be linked to a specific well and are labeled None#, though neighbourhood information is retained.
- Data are distributed across multiple sources, which may require careful cleaning and standardization before GIS integration.