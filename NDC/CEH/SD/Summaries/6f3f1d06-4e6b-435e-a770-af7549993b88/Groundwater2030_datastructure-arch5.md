# Groundwater2030: Data structure for field survey files

- The dataset is provided as four separate CSV tables that can be joined using common identifier fields.
- Four tables:
  - Groundwater2030_sanrisk.csv: Sanitary risk inspection data; primary key is Wellcode.
  - Groundwater2030_waterquality.csv: Water quality test results; primary key is Wellcode.
  - Groundwater2030_well_owner_survey.csv: Questionnaire survey of well owners; primary key is Well number.
  - Groundwater2030_WellCustomerSurvey.csv: Questionnaire survey of well customers; primary key is Well number.
- Each table uses identifiers unique to each groundwater source; Wellcode (for sanrisk and waterquality) and Well number (for owner and customer surveys) are the linking fields across tables.

## Identifier scheme and codes

- Unique identifiers take the form:
  - W1…n for wells
  - S1…n for springs
  - B1…n for boreholes
- Prefix indicates source type: W = well, S = spring, B = borehole.
- An additional code O indicates wells from the baseline survey for which water quality data could not be collected later.
- Where owner or customer questionnaires could not be linked to an individual well, entries are labelled None1, None2, etc., though neighbourhood information is still included.

## Linking and data integrity

- The sanrisk and waterquality tables share the Wellcode field as the key; these form the primary keys for their respective datasets.
- The well_owner_survey and WellCustomerSurvey tables use Well number as the key; these act as primary keys for their datasets and can be linked to other tables via the same underlying well identifiers.
- All four tables can be joined through the shared groundwater source identifiers, enabling integrated analyses across sanitary risk, water quality, and user perspectives (owners and customers).

## Notable data features and caveats

- There may be more than one customer associated with a single groundwater source.
- Some wells in the baseline survey (code O) do not have corresponding water quality data.
- If a questionnaire could not be linked to a specific well, it is still associated with neighbourhood information, preserving geographic context.

## Data governance implications for Data Stewards

- Metadata should document the identifier schemes, the meaning of W/S/B prefixes, and the O baseline code, as well as the None labeling for unlinked questionnaires.
- Ensure consistent handling of join keys and clear guidance on how to link across the four CSVs.
- Maintain clear versioning and update procedures to keep all four tables synchronized when new data are added or existing data are revised.
- Provide documentation on data availability and any limitations (e.g., baseline wells lacking water quality data, unlinked questionnaires) to support discoverability and appropriate reuse.