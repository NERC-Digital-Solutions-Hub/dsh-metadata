# Groundwater2030: Data structure for field survey files

- Purpose and scope
  - Four separate .csv tables designed to be joined via common identifier fields.
  - Data describe groundwater sources used in fieldwork, enabling sanitary risk assessment, water quality evaluation, and owner/customer surveys.
  - Identifiers are unique to each groundwater source and serve as primary keys (for some tables) or foreign keys (linkage across tables).

- Tables and key fields
  - Groundwater2030_sanrisk.csv
    - Description: Sanitary risk inspection of groundwater sources.
    - Primary key: Wellcode (Well ID field)
  - Groundwater2030_waterquality.csv
    - Description: Water quality test results for groundwater sources.
    - Primary key: Wellcode (Well ID field)
  - Groundwater2030_well_owner_survey.csv
    - Description: Questionnaire survey of well owners.
    - Primary key: Well number
  - Groundwater2030_WellCustomerSurvey.csv
    - Description: Questionnaire survey of well customers.
    - Primary key: Well number

- Identifiers and how they are used
  - Wellcode: used as the primary key for sanitary risk and water quality data.
  - Well number: used as the primary key for owner and customer surveys.
  - Unique codes include prefixes W, S, B (Well, Spring, Borehole) with an O code indicating wells from the baseline survey for which current water quality data could not be collected.
  - There may be multiple customers for a single groundwater source, necessitating a one-to-many relationship between wells and customer records.

- Linking and data structure considerations
  - Within the wellcode/well number fields, identifiers are designed to join the related data across tables.
  - When owner or customer questionnaires cannot be linked to a specific well, they are labeled as None followed by a numeric suffix (None1–NoneN), though neighbourhood information remains included for all questionnaires.

- Data quality, governance and potential challenges
  - The structure supports data verification across multiple datasets but relies on consistent identifier use.
  - Potential challenges align with broader monitoring concerns: data gaps (especially for water quality data via O baseline cases), linking difficulties across tables, and ensuring metadata completeness for effective use and auditability.
  - Public sharing of dataset references and provenance is implicit in the need for clear IDs and neighbourhood context to facilitate data governance and reuse.

- Practical implications for monitoring frameworks
  - Enables integrated assessment of sanitary risk, water quality, and stakeholder perspectives (owners and customers).
  - Supports tracking of data completeness (e.g., baseline wells with missing water quality data) and the impact of data linkage on interpretation.
  - Provides a clear schema for data curation, quality assurance, and reporting through combined analyses of the four datasets.