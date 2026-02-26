# Groundwater2030: Data structure for field survey files

## Overview
- The data are provided as four separate CSV tables that can be joined via common identifier fields.
- Identifiers are unique to each groundwater source and serve as primary keys for sanitary risk and water quality datasets; well-related surveys use Well IDs as keys.
- Tables:
  - Groundwater2030_sanrisk.csv (Sanitary risk inspection) – Wellcode as primary key
  - Groundwater2030_waterquality.csv (Water quality test results) – Wellcode as primary key
  - Groundwater2030_well_owner_survey.csv (Well owner questionnaire) – Well number as primary key
  - Groundwater2030_WellCustomerSurvey.csv (Well customer questionnaire) – Well number as primary key

## Datasets and Primary Keys
- Groundwater2030_sanrisk.csv — Description: Sanitary risk inspection of groundwater sources; Primary key: Wellcode
- Groundwater2030_waterquality.csv — Description: Water quality test results; Primary key: Wellcode
- Groundwater2030_well_owner_survey.csv — Description: Questionnaire survey of well owners; Primary key: Well number
- Groundwater2030_WellCustomerSurvey.csv — Description: Questionnaire survey of well customers; Primary key: Well number

## Identifier conventions
- Unique identifiers use prefixes to indicate source type:
  - W… = well
  - S… = spring
  - B… = borehole
- Additional code O indicates wells in the baseline survey for which water quality data could not be collected.

## Linking and relationships
- There may be more than one customer for each groundwater source.
- If owner or customer questionnaires could not be linked to an individual well, they are labeled as None1, None2, etc.
- All questionnaires still include neighbourhood information, facilitating spatial context.

## GIS implications and how to use
- Join strategy:
  - Use Wellcode as the join key for sanitary risk and water quality tables.
  - Use Well number for owner and customer survey tables; ensure consistent formatting when merging with the central groundwater source dataset.
- Create an integrated dataset for mapping by:
  - Merging sanrisk and waterquality on Wellcode.
  - Linking owner and customer surveys via Well number, while handling potential None links.
- Prepare for spatial analysis by ensuring neighbourhood and location attributes are retained, and address any missing links or O-prefixed codes.

## Data quality and preprocessing considerations
- Expect missing water quality data for some baseline wells (O codes).
- Ensure consistency of identifiers across tables to avoid mismatches.
- Clean and harmonize varying formats of Wellcode/Well number during joins.

## Usage tips for effective visualization
- Represent wells, springs, and boreholes distinctly using the W/S/B prefixes.
- Map sanitary risk and water quality indicators as layered attributes or choropleth visuals.
- Indicate sources with multiple customers using aggregated or linked customer surveys to show stakeholder reach.