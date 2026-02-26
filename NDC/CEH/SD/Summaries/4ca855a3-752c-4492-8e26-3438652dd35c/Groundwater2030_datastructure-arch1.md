# Groundwater2030: Data structure for field survey files

- The data are provided as four separate CSV tables that can be joined using common identifier fields.
- Identifiers are unique to each groundwater source that formed the basis of the fieldwork, and link fields serve as primary keys (sanitary risk and water quality) or foreign keys (well customer data).

## Data Tables and Keys

- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspection of groundwater sources.
  - Key: Wellcode (primary key)
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources.
  - Key: Wellcode (primary key)
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners.
  - Key: Well number (primary key)
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers.
  - Key: Well number (primary key)

## Identifier System

- Unique identifiers are prefixed to indicate source type:
  - W = well, S = spring, B = borehole; followed by a numeric sequence (e.g., W1…, S1…, B1…).
- An additional code O marks wells in the baseline survey for which water quality data could not be collected.
- If owner or customer questionnaires could not be linked to an individual well, an entry is labelled None1–Nonen. All questionnaires include neighbourhood information.

## Linking and Relationships

- Sanitary risk and water quality data are linked by the Wellcode field (primary keys in their respective tables).
- Owner surveys link via Well number (foreign key), and customer surveys likewise use Well number.
- There may be more than one customer for a single groundwater source (one-to-many relationship between a source and customers).

## Practical Guidance for Analysts

- To integrate datasets, join sanrisk and waterquality on Wellcode.
- Attach owner and customer questionnaire data using Well number, mindful that multiple customers may exist per source.
- Use the O code to identify baseline wells lacking current water quality data.
- Unlinked questionnaires labelled None1–Nonen still carry neighbourhood information, which can inform spatial or demographic analyses.
- Ensure consistent interpretation of identifiers across tables (W/S/B prefixes and numeric sequences) when aggregating by source or type.