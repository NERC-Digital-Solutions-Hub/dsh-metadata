# Groundwater2030: Data structure for field survey files

## Overview
- Describes the four CSV tables, how they interrelate, and the identifiers used to join them.
- Aims to enable a complete view of sanitary risk, water quality, and survey responses for groundwater sources.

## Data files and structure
- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspection data for groundwater sources.
  - Primary key: Wellcode.
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources.
  - Primary key: Wellcode.
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners.
  - Primary key: Well number.
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers.
  - Primary key: Well number.

## Identifiers and keys
- Unique source identifiers use prefixes: W (well), S (spring), B (borehole); forms W1..n, S1..n, B1..n.
- An additional code O on wells indicates baseline wells with no current water quality data available.
- In owner/customer questionnaires, unlinked wells may be labeled None1, None2, etc. All questionnaires include neighborhood information.

## Linking across datasets
- Sanrisk.csv and Waterquality.csv use Wellcode as primary keys.
- Owner survey and Customer survey use Well number as primary keys (treated as foreign keys to the same wells/sources).
- Tables can be joined on the common identifiers to form a consolidated dataset across risk, quality, and stakeholder perspectives.

## Data quality and gaps
- Potential gaps include:
  - Wells with only baseline data (O) and no water quality data.
  - Questionnaires that cannot be linked to a specific well (None).
  - Possibility of multiple customers per groundwater source.

## Data governance considerations for Data Leaders
- Document and manage the identifier scheme, join keys, and linkage rules in metadata.
- Monitor data quality, provenance, and consistency when integrating datasets.
- Establish handling procedures for missing or unlinked records (O and None cases) and document their impact.
- Ensure clear metadata around neighborhood information collected in surveys to support discoverability and contextual analysis.