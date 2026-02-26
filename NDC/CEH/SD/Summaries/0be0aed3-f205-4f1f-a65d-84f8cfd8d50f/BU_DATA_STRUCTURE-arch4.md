# Data access

- Overview
  - Dataset focuses on transect-based droppings counts (deer, grouse, rabbit, sheep) used as indices of relative abundance; not direct population sizes.
  - Data collected across multiple ECN sites, with accompanying quality information to support proper use.

- Dataset origin and ownership
  - Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - ECN programme owners/sponsors: a consortium of UK government departments and agencies (e.g., DEFRA, Natural England, SEPA,wrn Welsh Government, etc.) funding site monitoring or network coordination.
  - Usage acknowledgement: users should acknowledge data and send one reprint of any publication citing the data.

- Access and governance
  - Data are available at the provided DOI URL.
  - ECN provides standard operating procedures to ensure data comparability across sites; see accompanying PDF for collection methodology.

- Usage notes and limitations
  - Dropping counts are recorded biannually (late March and late September).
  - Population size cannot be directly measured for certain species; indices are used to estimate relative abundance.
  - Moor House methodology also applied to grouse relative abundance.
  - Use accompanying quality information when using the data.

- Data structure and primary download fields
  - Core data fields: SITECODE (site), LCODE (location within site), SDATE (sampling date), PLOTID (transect section), FIELDNAME (variable measured), VALUE (measured value).
  - Example: unique code per ECN site, transect details, and measured variable values.

- Supporting documentation files
  - ECN_BU2.csv: survey information with SITECODE, LCODE, CLEARDATE, SDATE, PLOTID, SURVEY.
  - ECN_BU3.csv: transect details with SITECODE, FROM_DATE, TO_DATE, LCODE, PLOTID, LENGTH, HABDESC.
  - ECN_BU_qtext.csv: quality text for site managers’ quality codes, with SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.

- Site and variable metadata
  - Explanatory site codes (e.g., T01–Drayton, T04–Moor House, etc.) with site names and geographic coordinates.
  - Explanatory variables (FIELDNAME):
    - D = count of deer droppings
    - G = count of grouse droppings
    - R = count of rabbit droppings
    - S = count of sheep droppings
    - Q1–Q8 = quality codes associated with data points
  - Quality codes (Q1–Q8 context): reference a comprehensive, standardized list of codes indicating data quality issues or conditions (e.g., 100 = no information available, 201 = biting insects affected sampling, 501–513 = laboratory/measurement uncertainties or errors, 999 = unusual event).

- Quality and data integrity
  - Quality codes are included in the data download and can be supplemented by accompanying text in ECN_BU_qtext.csv for unusual or ongoing issues.
  - The dataset emphasizes the use of quality metadata to assess suitability and reliability for analyses.

- Additional resources
  - ECN site information and broader ECN catalog reference: link provided for further site metadata and context.
  - Related documentation and governance information available via ECN resource pages.