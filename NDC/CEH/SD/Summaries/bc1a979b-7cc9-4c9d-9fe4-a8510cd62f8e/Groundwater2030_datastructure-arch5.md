# Groundwater2030: Data structure for field survey files

## Overview
- The data are provided as four separate CSV tables that can be joined using common identifier fields.
- Identifiers are unique to each groundwater source and form primary keys for sanitary risk and water quality data, with Well IDs serving as foreign keys in the well owner survey.

## Datasets and key fields
- Groundwater2030_sanrisk.csv
  - Description: Sanitary risk inspection of groundwater sources
  - Well ID field: Wellcode
- Groundwater2030_waterquality.csv
  - Description: Water quality test results for groundwater sources
  - Well ID field: Wellcode
- Groundwater2030_well_owner_survey.csv
  - Description: Questionnaire survey of well owners
  - Well ID field: Well number
- Groundwater2030_WellCustomerSurvey.csv
  - Description: Questionnaire survey of well customers
  - Well ID field: Well number

## Identifier conventions
- Unique identifiers take the form W1….n, S1….n, B1…..n:
  - W = well, S = spring, B = borehole
- An O code indicates wells in the baseline survey for which water quality data could not be collected now.
- If owner or customer questionnaires cannot be linked to an individual well, they are labelled None followed by a number (None1, None2, …).
- All questionnaires still include neighbourhood information.

## Relationships and data integration
- There may be more than one customer per groundwater source.
- The Wellcode/Well number fields serve as the primary keys in their respective tables and enable joins across datasets.
- Linkages between sanitary risk, water quality, and survey data are achieved through these identifiers.

## Data management and stewardship considerations
- Ensure consistent use of W/S/B prefixes, O codes, and None-linked entries across all tables.
- Maintain referential integrity when joining datasets (primary vs. foreign keys).
- Document data transformations, cleaning, and any dataset-level changes.
- Be aware of data availability limitations and potential gaps where water quality data are missing (O codes).
- Plan for updates and versioning; facilitate uploading to portals and cataloging as data holdings.

## Potential challenges for data stewards
- Managing multiple systems/formats and ensuring interoperability.
- Handling large datasets and ensuring timely access and transfer.
- Achieving and documenting comprehensive metadata, including linkage rules and data provenance.
- Accommodating scenarios where some questionnaires cannot be linked to wells while preserving neighbourhood information.