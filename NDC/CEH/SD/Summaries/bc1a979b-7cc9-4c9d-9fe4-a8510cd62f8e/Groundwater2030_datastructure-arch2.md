# Groundwater2030: Data structure for field survey files

## Overview
- Data provided as four separate CSV tables intended to be joined via common identifier fields.
- Identifiers are unique to each groundwater source (well, spring, borehole) that underpinned fieldwork.
- Sanitary risk and water quality datasets use Wellcode as the primary key; owner and customer surveys use Well number as the linking field.
- Designed to support consistent environmental monitoring by enabling cross-table analyses across risk, quality, and stakeholder survey data.

## Data Tables and Keys
- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspection of groundwater sources
  - Well ID field: Wellcode
  - Primary key: Wellcode
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources
  - Well ID field: Wellcode
  - Primary key: Wellcode
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners
  - Well ID field: Well number
  - Relationship: Owner responses linked via Well number (foreign key)
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers
  - Well ID field: Well number
  - Relationship: Customer responses linked via Well number (foreign key)

## Identifiers and Linking
- Unique identifiers for sources follow prefixes:
  - W = well, S = spring, B = borehole
  - Formats: W1…n, S1…n, B1…n
- O prefix indicates baseline wells for which water quality data could not be collected now.
- If owner or customer questionnaires cannot be linked to an individual well, they are labeled None1, None2, etc., but still include neighbourhood information.

## Data Quality and Notes
- The sanrisk and waterquality tables use Wellcode as the primary key; owner and customer surveys use Well number as a foreign key to join with the source records.
- There may be multiple customers per groundwater source, implying one-to-many relationships in customer data.
- Neighbourhood information is included in questionnaire records, supporting spatial analyses even when direct linkage to a well is missing.

## Practical Usage for Monitoring Analysts
- Use consistent identifiers to combine risk, quality, and survey data for comprehensive environmental health assessments.
- Validate cross-table linkages (Wellcode vs. Well number) and handle any None-linked questionnaires.
- Leverage the prefix system (W/S/B) to categorize sources in analyses and visualizations.
- Incorporate neighbourhood information to contextualize survey responses and field measurements.
- Be mindful of O-designated baseline wells lacking current water quality data during trend analyses.