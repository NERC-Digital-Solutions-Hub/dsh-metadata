# Groundwater2030: Data structure for field survey files

- Four separate CSV tables are provided: Groundwater2030_sanrisk.csv, Groundwater2030_waterquality.csv, Groundwater2030_well_owner_survey.csv, and Groundwater2030_WellCustomerSurvey.csv.
- Each table can be joined using common identifier fields, which are unique to each groundwater source that formed the basis of the fieldwork.
- The Sanitary risk and Water quality datasets use Wellcode as the primary key; the WellOwner and WellCustomer surveys use Well number as the primary key (foreign keys to the same sources).

## Tables and key fields

- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspection of groundwater sources.
  - Well ID field: Wellcode.
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources.
  - Well ID field: Wellcode.
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners.
  - Well ID field: Well number.
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers.
  - Well ID field: Well number.

## Identifier conventions and linking

- Unique identifiers take the form: W1…n (well), S1…n (spring), B1…n (borehole). The prefix indicates source type (W = well, S = spring, B = borehole).
- An additional code O indicates wells in the baseline survey for which water quality data could not be collected now.
- There may be more than one customer for each groundwater source.
- If owner or customer questionnaires could not be linked with an individual well, they are labelled None1-n. All questionnaires include neighbourhood information.

## Data quality, standardisation, and use

- The designed structure supports standardised analysis across sanitary risk, water quality, and stakeholder (owner/customer) perceptions.
- Enables cross-table QA, cleaning, and transformation to produce outputs (e.g., maps, charts) for environmental monitoring and policy assessment.
- Data should be stored and uploaded to appropriate portals to ensure accessibility for downstream analyses and broader data reuse.