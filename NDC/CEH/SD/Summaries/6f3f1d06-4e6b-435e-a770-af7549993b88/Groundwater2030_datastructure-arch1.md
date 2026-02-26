# Groundwater2030: Data structure for field survey files

## Overview
- The data are provided as four separate CSV tables intended to be joined via common identifier fields.
- Tables cover sanitary risk (sanrisk), water quality, well owner surveys, and well customer surveys.

## Tables and primary keys
- Groundwater2030_sanrisk.csv: Sanitary risk inspection data; primary key is Wellcode.
- Groundwater2030_waterquality.csv: Water quality test results; primary key is Wellcode.
- Groundwater2030_well_owner_survey.csv: Questionnaire survey of well owners; primary key is Well number.
- Groundwater2030_WellCustomerSurvey.csv: Questionnaire survey of well customers; primary key is Well number.

## Identifier conventions
- Unique identifiers in the Wellcode/Well number fields follow forms:
  - W1…n for wells
  - S1…n for springs
  - B1…n for boreholes
  - O indicates baseline wells for which water quality data could not be collected now.

## Linking across tables
- For sanitry risk and water quality, Wellcode serves as the primary key.
- For owner and customer surveys, the key field is described as Well number.

## Special notes on data linkage
- A groundwater source may have more than one customer.
- When owner/customer questionnaires cannot be linked to an individual well, they are labeled None followed by a number (e.g., None1, None2). All questionnaire records include neighbourhood information.

## Practical considerations for analysts
- Plan joins across four tables using the appropriate primary key fields (Wellcode or Well number) and account for multiple customers per source.
- Be aware of O-prefixed entries representing baseline wells lacking current water quality data.
- Expect potential records that cannot be linked to a specific well and handle None-linked cases in analyses requiring site-level alignment.