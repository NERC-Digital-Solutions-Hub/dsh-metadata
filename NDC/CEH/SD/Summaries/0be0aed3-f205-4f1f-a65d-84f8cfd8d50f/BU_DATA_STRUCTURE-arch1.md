# Data access

- Overview
  - ECN Data Centre hosts the UK Environmental Change Network (ECN) dataset, funded by UK government departments/agencies and used to understand environmental change.
  - Dataset owners/partners include several UK government and research bodies.
  - Users should acknowledge the data and send one reprint of any publication citing the data.

- Access and governance
  - Data available at a DOI link: https://doi.org/10.5285/0be0aed3-f205-4f1f-a65d-84f8cfd8d50f
  - ECN provides standard operating procedures to ensure cross-site comparability; accompanying PDF explains data collection methods.

- Data content and measurement approach
  - Primary measurements are dropping counts on transects used as indices of relative abundance:
    - D = count of deer droppings
    - G = count of grouse droppings
    - R = count of rabbit droppings
    - S = count of sheep droppings
  - Dropping counts are collected twice a year (late March and late September).
  - For Moor House, the same methodology is used for Grouse.
  - Data are accompanied by quality information to support proper use.

- Data structure and download format
  - Core data fields in downloads:
    - SITECODE: unique ECN site code
    - LCODE: location ID (unique within site)
    - SDATE: sampling date
    - PLOTID: transect section
    - FIELDNAME: variable measured
    - VALUE: measured value
  - Supporting documentation:
    - ECN_BU2.csv: survey information (SITECODE, LCODE, CLEARDATE, SDATE, PLOTID, SURVEY)
    - ECN_BU3.csv: transect details (SITECODE, FROM_DATE, TO_DATE, LCODE, PLOTID, LENGTH, HABDESC)
    - ECN_BU_qtext.csv: quality text for site managers (SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION)

- Site codes and geographic metadata
  - Site codes (T01–T10) with site names and precise coordinates:
    - T01 Drayton; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T08 Wytham; T09 Alice Holt; T10 Porton Down
  - Explanatory information available at the ECN site catalogue link.

- Variables and quality codes
  - Field names (FIELDNAME) include:
    - D: deer droppings (count)
    - G: grouse droppings (count)
    - R: rabbit droppings (count)
    - S: sheep droppings (count)
  - Quality code fields (Q1–Q8): integer quality indicators associated with data readings
  - Quality codes (selected examples):
    - 100–139, 140–199, 200–205, 501–513, 999: range of codes describing issues such as no information, sampling problems, equipment issues, environmental factors, laboratory issues, and unusual events
  - Unusual events are flagged with code 999 in the main data and can be explored via ECN_BU_qtext.csv for descriptive text.

- Important usage notes for analysts
  - The data represent relative abundance indices, not exact population sizes.
  - Use the accompanying quality codes and text to assess data reliability and context for each measurement.
  - The dataset emphasizes cross-site comparability through standardized protocols and documented site/transect metadata.