# Data access

## Overview
- The UK Environmental Change Network (ECN) data focus on monitoring environmental change, using standardized data collection to enable comparability across sites.
- The primary dataset documents counts of animal droppings (deer, grouse, rabbit, sheep) recorded as indices of relative abundance, with transects surveyed twice yearly.

## Access & provenance
- Data are available at: https://doi.org/10.5285/0be0aed3-f205-4f1f-a65d-84f8cfd8d50f
- Dataset originator: ECN Data Centre (data.ecn.ac.uk; ecn@ceh.ac.uk)
- Dataset owners: UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies (list includes DEFRA, Natural England, Environment Agency, NERC, and others)
- Acknowledgement and citation: Users should acknowledge the data and send one reprint of any publication citing the data

## Protocol and quality
- ECN maintains standard operating procedures (SOPs) to ensure data comparability across sites; a PDF accompanies this document detailing data collection methods.
- Usage notes emphasize reliance on accompanying quality information when using the data.
- Dropping counts are recorded twice a year (late March and late September); droppings are used as an index rather than direct population counts.
- Moor House uses the same method for estimating relative abundance of grouse.

## Data structure and contents
- Core data fields for the main download:
  - SITECODE: unique ECN Site code
  - LCODE: location ID (unique within site)
  - SDATE: sampling date
  - PLOTID: transect section
  - FIELDNAME: variable measured (e.g., counts by species)
  - VALUE: measured value (count)
- Supporting documentation files:
  - ECN_BU2.csv: survey information (SITECODE, LCODE, CLEARDATE, SDATE, PLOTID, SURVEY)
  - ECN_BU3.csv: transect information (SITECODE, FROM_DATE, TO_DATE, LCODE, PLOTID, LENGTH, HABDESC)
  - ECN_BU_qtext.csv: site manager quality text (SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION)
- Quality codes (ECN_BU_qtext.csv defines meanings for codes used in data downloads):
  - A broad range of codes (e.g., 100–999) indicating issues such as no information, partial loss, environmental interferences, laboratory issues, non-standard sampling, and more
  - 999 indicates an unusual event; associated text in ECN_BU_qtext.csv explains specifics
- Data fields:
  - FIELDNAME values include D (deer droppings), G (grouse droppings), R (rabbit droppings), S (sheep droppings), and quality fields Q1–Q8 (quality codes)

## Site codes and variables
- Explanatory site codes (example sites and coordinates):
  - T01 Drayton
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
- Each site has a named location and geographic coordinates; additional site information is available via the ECN site catalogue

## How to use
- Use the standardized fields (SITECODE, LCODE, SDATE, PLOTID, FIELDNAME, VALUE) to compile comparable time-series of relative abundance indices.
- Consult ECN_BU2.csv and ECN_BU3.csv for survey and transect context; use ECN_BU_qtext.csv to interpret quality codes.
- Apply quality codes and notes to assess data reliability for any analysis or reporting.

## Notes on data use
- Data users are encouraged to fully leverage the accompanying quality information to interpret results.
- When publishing, acknowledge ECN data usage and consider providing a reprint to ECN.