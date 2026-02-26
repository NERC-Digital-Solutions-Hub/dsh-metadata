# Groundwater2030: Data structure for field survey files

## Overview
- The dataset consists of four separate CSV tables that can be joined using common identifier fields.
- Identifiers are unique to each groundwater source and form primary keys for sanitary risk and water quality data.
- For the well customer dataset, Well IDs are held as a foreign key.

## Data files
- Groundwater2030_sanrisk.csv: Sanitary risk inspection data; primary key field = Wellcode.
- Groundwater2030_waterquality.csv: Water quality test results; primary key field = Wellcode.
- Groundwater2030_well_owner_survey.csv: Questionnaire survey of well owners; primary key field = Well number.
- Groundwater2030_WellCustomerSurvey.csv: Questionnaire survey of well customers; primary key field = Well number.

## Identifiers and coding schemes
- Unique identifiers take the form W1…n, S1…n, B1…n:
  - W = well, S = spring, B = borehole.
  - O prefix indicates wells in the baseline survey for which water quality data could not be collected.
- If owner or customer questionnaires could not be linked to an individual well, they are labelled None1–n, but still include neighbourhood information.

## Linking and relationships
- There may be more than one customer per groundwater source.
- Well IDs in the owner survey and customer survey datasets link to the corresponding source identifiers in the other tables.
- Aggregation and analysis can be performed by joining on these identifiers to create integrated views (e.g., linking sanitary risk, water quality, and survey responses).

## Practical guidance for data support
- Use the common identifiers to join the four tables and create consolidated records per groundwater source.
- Account for multiple customers per source and for None-linked questionnaire entries.
- Handle O-prefixed wells as missing water quality data in the baseline set.
- Maintain awareness of the prefix (W/S/B) to correctly categorize source types during analysis.
- Ensure neighbourhood information from owner/customer surveys is preserved when integrating with sanitary risk and water quality data.