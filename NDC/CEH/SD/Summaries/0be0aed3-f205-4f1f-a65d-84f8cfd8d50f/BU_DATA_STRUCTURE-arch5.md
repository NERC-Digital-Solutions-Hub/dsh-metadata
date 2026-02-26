# Data access

- Overview
  - Origin: ECN Data Centre (data.ecn.ac.uk) on behalf of the UK Environmental Change Network.
  - Owners: The UK Environmental Change Network programme, funded by a consortium of UK government departments and agencies.
  - Purpose: Support understanding of environmental change; data usage acknowledged by researchers; request of one reprint for citations.
  - Access: Data available at the provided URL: https://doi.org/10.5285/0be0aed3-f205-4f1f-a65d-84f8cfd8d50f

- Governance and provenance
  - Protocols: ECN maintains standard operating procedures to ensure comparability of data across sites; accompanying PDFs explain data collection methods.
  - Metadata and standards: Clear definitions for site codes, transects, sampling dates, and measured variables; quality information linked to data downloads.

- Content and structure of the dataset
  - Data types: Counts of animal droppings used as indices of relative abundance
    - D = deer droppings
    - G = grouse droppings
    - R = rabbit droppings
    - S = sheep droppings
  - Sampling design:
    - Dropping counts recorded twice yearly (late March and late September).
    - Indices used due to inability to directly measure population sizes for deer and rabbit; same approach for Grouse at Moor House.
  - Data fields in downloads:
    - SITECODE: unique ECN site code
    - LCODE: location ID within site
    - SDATE: sampling date
    - PLOTID: transect section
    - FIELDNAME: variable measured
    - VALUE: measured value
  - Supporting documentation:
    - ECN_BU2.csv: survey information (SITECODE, LCODE, CLEARDATE, SDATE, PLOTID, SURVEY)
    - ECN_BU3.csv: transect information (SITECODE, FROM_DATE, TO_DATE, LCODE, PLOTID, LENGTH, HABDESC)
    - ECN_BU_qtext.csv: quality text accompanying site-manager quality codes
  - Quality codes and context:
    - Q1–Q8: quality code fields with codes and descriptions
    - Extensive quality code list (e.g., 100–999) covering data loss, sampling issues, environmental/field conditions, laboratory issues, non-standard sampling, and other disruptions
    - 999 indicates an unusual event; associated explanatory text is in ECN_BU_qtext.csv

- Site and site-specific information
  - Explanatory site codes and details: T01–T10 with site names and precise geographic coordinates (e.g., T04 Moor House - Upper Teesdale; T06 Rothamsted; T08 Wytham; etc.)
  - Additional information about ECN sites available via the provided CEH catalogue link

- Quality assurance and data management
  - Site managers assign quality codes to reflect factors that may affect data quality; the quality appendices provide guidance and examples.
  - Quality metadata may include text descriptions for circumstances not covered by standard codes (referenced via quality text file when 999 is used).

- Practical considerations for reuse
  - Ensure proper acknowledgment of ECN data sources in any publication.
  - Refer to accompanying documentation for context on how measurements were collected and what the quality codes signify.
  - Use site and transect identifiers to join data with the supporting ECN_BU2.csv and ECN_BU3.csv metadata for accurate interpretation.
  - Be aware that data are structured as indices (droppings counts) rather than direct population sizes; interpret results accordingly.