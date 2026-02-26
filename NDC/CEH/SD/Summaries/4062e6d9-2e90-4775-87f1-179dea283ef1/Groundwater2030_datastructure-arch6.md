# Groundwater2030: Data structure for field survey files

## Overview
- Four separate CSV tables form the groundwater field survey dataset.
- Tables can be joined via common identifier fields unique to each groundwater source.
- Identifiers serve as primary keys for some datasets and foreign keys for others.
- Prefix codes (W, S, B) indicate source type: Well, Spring, Borehole. An O suffix marks wells from the baseline survey with no current water quality data.
- When possible, questionnaires are linked to wells; when not linkable, records are labeled None1-n but still include neighbourhood information.

## Files and what they contain
- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspections of groundwater sources.
  - Key field: Wellcode (Well ID).
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources.
  - Key field: Wellcode (Well ID).
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners.
  - Key field: Well number (Wellcode-like identifier).
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers.
  - Key field: Well number (Wellcode-like identifier).

## Identifiers and keys
- Unique IDs by source type:
  - W1…n = Wells
  - S1…n = Springs
  - B1…n = Boreholes
- O suffix on a Well ID indicates a baseline-survey well with no current water quality data.
- Linking fields:
  - Sanrisk and WaterQuality datasets use Wellcode as the primary key.
  - Owner and Customer surveys use Well number as the key (foreign key to the corresponding well source).
- Note: It is possible for a single groundwater source to have multiple associated customers.

## Linking rules and special codes
- Where owner or customer questionnaires cannot be linked to a specific well, the value is recorded as None1, None2, etc., but neighbourhood information remains available.
- All questionnaire records include neighbourhood data to support spatial or locality-based analyses.

## Data quality and integration considerations
- Potential challenges:
  - Multiple customers per groundwater source requiring careful aggregation.
  - Data may be patchy across the four tables and across formats/systems.
  - Cross-table joins depend on correct and consistent use of Wellcode/Well number keys.
- Practical implications for data support:
  - Validate and harmonize identifiers across datasets before joining.
  - Handle O-coded wells separately when analyzing water quality vs. baseline data.
  - When presenting outputs, clearly indicate unlinked questionnaires (None) and the neighbourhood context.
  - Develop self-serve dashboards that allow filtering by source type (W/S/B), neighbourhood, and data availability (sanitary risk, water quality, owner, and customer responses). 

## Usage guidance for data products
- Use the identifiers to create integrated views linking sanitary risk, water quality, and survey responses at the source level.
- Provide provenance notes and clarify any records with missing water quality data (O-coded) or unlinked questionnaires (None).
- Ensure consistent labeling and mapping between Wellcode and Well number fields when combining datasets.