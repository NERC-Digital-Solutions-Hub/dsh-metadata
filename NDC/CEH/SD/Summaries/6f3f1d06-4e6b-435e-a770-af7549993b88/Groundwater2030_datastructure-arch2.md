# Groundwater2030: Data structure for field survey files

- Purpose: Define a standard, joinable data structure for groundwater field survey data, enabling consistent environmental monitoring and analysis over time.

## Datasets and primary keys

- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspection data for groundwater sources
  - Primary key: Wellcode (Well ID field)
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources
  - Primary key: Wellcode (Well ID field)
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners
  - Key field: Well number (Well ID field)
  - Notes: May be linked to wells via foreign key; if not linked to an individual well, labelled None1–Nonen; neighbourhood information is included
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers
  - Key field: Well number (Well ID field)
  - Notes: May be linked to wells via foreign key; if not linked to an individual well, labelled None1–Nonen; neighbourhood information is included

## Identifiers and how tables relate

- Unique identifiers are tied to groundwater sources; used to join tables
- Prefix conventions:
  - W indicates a well
  - S indicates a spring
  - B indicates a borehole
  - O indicates baseline wells with no current water quality data
- Linking fields:
  - Sanrisk.csv and waterquality.csv use Wellcode as the primary key
  - Well_owner_survey.csv and WellCustomerSurvey.csv use Well number as the key; both link back to wells via these identifiers
- There can be more than one customer for a single groundwater source

## Notable conventions and edge cases

- Multiple customers may be associated with a single groundwater source
- Some owner/customer questionnaires may not link to a specific well; these are labeled None1, None2, etc., but still include neighbourhood information
- Baseline wells (prefix O) may lack associated water quality data

## Practical implications for monitoring and analysis

- Enables standardised aggregation and comparison across sanitary risk, water quality, and social context (owner/customer perspectives)
- Supports production of integrated outputs (reports, maps, charts) by linking datasets through consistent identifiers
- Facilitates data quality assurance, cleaning, and transformation by providing clear primary/foreign key relationships

## Data accessibility and reuse considerations

- Datasets are designed to be stored and uploaded to appropriate data portals, promoting access to underlying data for broader use and secondary analyses
- Structured linkage across datasets supports reuse in policy performance assessments and environmental health monitoring over time