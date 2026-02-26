# Groundwater2030: Data structure for field survey files

## Overview
- Four separate CSV tables capture sanitary risk, water quality, well owner surveys, and well customer surveys.
- Tables can be joined using common, groundwater-source-specific identifiers, enabling integrated GIS analyses.

## Tables and Key Fields
- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspection of groundwater sources.
  - Key: Wellcode (primary key for this dataset).
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources.
  - Key: Wellcode (primary key for this dataset).
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners.
  - Key: Well number (used to link to groundwater sources; may have multiple records per source).
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers.
  - Key: Well number (used to link to groundwater sources; may have multiple records per source).

## Identifier Conventions
- Unique identifiers take forms: W1…n (well), S1…n (spring), B1…n (borehole).
- Prefix indicates source type: W = well, S = spring, B = borehole.
- O indicates wells in the baseline survey for which water quality data could not be collected now.

## Linkage and Data Relationships
- The sanrisk and waterquality datasets use their respective Wellcode fields as primary keys.
- The owner and customer survey datasets use Well number as the linking field (foreign key) to the groundwater sources.
- There may be more than one customer per groundwater source.

## Data Quality and Completeness
- Some owner/customer questionnaire records may not be linked to a specific well and are labeled as None1, None2, etc., but still include neighborhood information.
- Water quality data may be missing for certain wells (code O in identifiers).

## GIS and Mapping Implications
- Enables creation of map-based layers for sanitary risk, water quality, and survey insights.
- Use the W/S/B prefixes to categorize features (well, spring, borehole) and the neighborhood data from questionnaires to enrich spatial analyses.
- Plan handling of missing data (O) and unlinked questionnaires when building integrated datasets.