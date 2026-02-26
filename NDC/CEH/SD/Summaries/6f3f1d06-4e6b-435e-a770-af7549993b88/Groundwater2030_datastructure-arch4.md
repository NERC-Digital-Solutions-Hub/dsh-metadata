# Groundwater2030: Data structure for field survey files

- Overview
  - Data provided as four separate CSV tables that can be joined using common identifier fields unique to each groundwater source.
  - For sanitary risk and water quality datasets, the identifier fields form primary keys. For the well customer field, Well IDs are held as a foreign key.

- Tables and key fields
  - Groundwater2030_sanrisk.csv (Description: Sanitary risk inspection of groundwater sources)
    - Well ID field: Wellcode
  - Groundwater2030_waterquality.csv (Description: Water quality test results)
    - Well ID field: Wellcode
  - Groundwater2030_well_owner_survey.csv (Description: Questionnaire survey of well owners)
    - Well ID field: Well number
  - Groundwater2030_WellCustomerSurvey.csv (Description: Questionnaire survey of well customers)
    - Well ID field: Well number

- Identifier formats and semantics
  - Unique identifiers take the form W1…n (well), S1…n (spring), B1…n (borehole).
  - An additional code O indicates wells in the baseline survey where water quality data could not be collected.

- Linking and data relationships
  - There may be more than one customer per groundwater source.
  - If owner or customer questionnaires could not be linked to an individual well, they are labeled None followed by a number (None1, None2, ...). All questionnaires include neighbourhood information.

- Data governance and usage considerations for data leaders
  - Maintain consistent prefix semantics (W/S/B) and O coding across datasets.
  - Ensure metadata clearly describes the primary/foreign key relationships and linking rules.
  - Address data gaps (O-coded wells) and potential multiple customers per source in analyses.
  - Preserve provenance and enable cross-table analyses by groundwater source through robust identifiers.