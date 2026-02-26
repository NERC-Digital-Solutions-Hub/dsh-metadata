# Data access

- Data are available at the linked DOI: https://doi.org/10.5285/0be0aed3-f205-4f1f-a65d-84f8cfd8d50f
- Dataset originator: ECN Data Centre (Centre for Ecology and Hydrology) with contact ecn@ceh.ac.uk
- Dataset owners: UK Environmental Change Network (ECN) programme, sponsored by multiple UK government departments and agencies
  - Agencies include: AFBI, BBSRC, NRW, DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, SEPA, Scottish Government, SNH
- Usage acknowledgement: Please acknowledge data use and send one reprint of any publication citing ECN data

- Access protocol and comparability:
  - ECN has standard operating procedures to ensure site data are comparable
  - A companion PDF explains data collection methods

- Usage notes and interpretation:
  - Dropping counts are recorded on transects twice a year (late March and late September)
  - Relative abundance is estimated via an index method (not direct population size) for deer and rabbits
  - Moor House uses the same method for grouse
  - Include accompanying quality information when using the data

- Data download structure:
  - Core fields: SITECODE (site code), LCODE (location within site), SDATE (sampling date), PLOTID (transect section), FIELDNAME (variable), VALUE (measured value)
  - Additional quality fields: Q1–Q8 (quality codes as integers)

- Supporting documentation files:
  - ECN_BU2.csv: survey information (SITECODE, LCODE, CLEARDATE, SDATE, PLOTID, SURVEY)
  - ECN_BU3.csv: transect information (SITECODE, FROM_DATE, TO_DATE, LCODE, PLOTID, LENGTH, HABDESC)
  - ECN_BU_qtext.csv: qualitative context provided by site managers for quality issues (SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION)
  - Quality codes are described in the accompanying list

- Site codes (Explanatory Information): 10 ECN sites (T01–T10) with site names and coordinates
  - T01 Drayton
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down

- Variables and measurement details (FIELDNAME):
  - D: count of deer droppings (units: count)
  - G: count of grouse droppings (units: count)
  - R: count of rabbit droppings (units: count)
  - S: count of sheep droppings (units: count)
  - Q1–Q8: quality code fields (integers) indicating data quality factors

- Quality codes (selected examples):
  - 100–199: data quality issues and non-availability (e.g., data lost, no sample, partial loss)
  - 200–299: sampling/recording adverse conditions (e.g., weather, lighting)
  - 501–513: laboratory or measurement-related issues
  - 999: unusual event; view accompanying text for details

- Practical guidance for data use:
  - Review ECN_BU2/ECN_BU3 for survey and transect context
  - Check ECN_BU_qtext for any quality-text notes (particularly if Q codes include 999)
  - Use quality information to assess data suitability for analyses and comparability across sites

- Citation and reuse:
  - Acknowledge ECN data usage and, if applicable, share a reprint of publications citing the dataset