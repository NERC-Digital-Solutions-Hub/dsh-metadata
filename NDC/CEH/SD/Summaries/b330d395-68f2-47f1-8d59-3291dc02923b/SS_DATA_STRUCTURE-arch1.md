# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology
- UK Environmental Change Network (ECN) programme sponsored by a consortium of UK government departments and agencies
  - Member organisations include: Afri-Food and Biosciences Institute, BBSRC, Cyfoeth Naturiol Cymru - Natural Resources Wales, Defence Science & Technology Laboratory, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, Northern Ireland Environment Agency, Scottish Environment Protection Agency, Scottish Government, Scottish Natural Heritage

- Purpose and use
  - ECN aims to understand causes and consequences of environmental change
  - Data are used to inform research and practical decisions; please acknowledge data and send one reprint of any publication citing the data

- Protocol and data collection
  - Standard operating procedures to ensure comparability across sites (see accompanying ss.pdf)
  - Suction samplers measure soil solution chemistry; samples collected fortnightly
  - Replicate IDs (RID) track sampler changes; bulked samples indicated by RID 'XXS' (shallow) or 'XXD' (deep)
  - Quality control: standard QC solution analyzed with field samples; QC data available with the dataset; use accompanying quality information

- Data download and file structure
  - Core data fields: SITECODE, SDATE, RID, FIELDNAME, VALUE
  - Supporting documents:
    - ECN_SS2.csv: lab analysis information (SITECODE, RID, FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE)
    - ECN_SS_qtext.csv: quality-text for factors affecting data quality; includes SITE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, plus 999 code for unusual events (text in ECN_SS_qtext.csv)
    - ECN_QC1.csv: quality control solution data (SITECODE, SDATE, FIELDNAME, VALUE)
    - ECN_QC2.csv: additional lab analysis information (FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE)
  - Site codes and site metadata (see Site Codes)

- Site codes and locations
  - 12 ECN sites labeled T01–T12 with names and coordinates:
    - T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T08 Wytham; T09 Alice Holt; T10 Porton Down; T11 Y Wyddfa - Snowdon; T12 Cairngorms
  - Additional site information at: https://catalogue.ceh.ac.uk/id/813712d4-d162-4ede-aff8-cf1c337bdc27

- Explanatory information: variables (FIELDNAME)
  - Alkalinity (ALKY), Aluminium, Calcium, Chloride, Colour, Conductivity (CONDY), Dissolved Organic Carbon (DOC)
  - Iron, Magnesium, Ammonium (NH4N), Nitrate nitrogen (NO3N), pH, PHAQCS, PHAQCU, Phosphate phosphorus (PO4P)
  - Potassium, Sulphate (SO4S), Sodium, Total nitrogen (TOTALN), Total dissolved phosphorus (TOTALP)
  - Vacuum, Volume, and quality fields Q1–Q5 (quality codes)

- Quality codes (CODE meanings)
  - 100–104, 106, 108, 110, 111, 113: data issues or missing information (no information, no sample, partial loss, lab issues, etc.)
  - 122, 123, 124, 126, 137, 140, 160, 182: sampling or field issue notes (e.g., equipment or environmental conditions)
  - 200–223: adverse conditions or non-standard sampling dates/times
  - 501–507: laboratory-related issues (no sample, loss, contamination, insufficient sample, equipment failure, pre-filtered)
  - 999: unusual event (textual explanation provided in ECN_SS_qtext.csv)

- Usage notes and considerations
  - Use accompanying quality information when using data
  - Be aware of potential data access hurdles, scale mismatches, and data provenance requirements
  - Datasets may require integration across sites and formats; QC and metadata are essential for reliable analysis

- Acknowledgment and publication
  - Please acknowledge use of ECN data and send one reprint of any publication citing the data

- Access and further information
  - ECN site and variable details available through the provided URLs and the site catalogue
  - Data include measurement details (e.g., units for variables) and QC procedures to support reproducible analyses