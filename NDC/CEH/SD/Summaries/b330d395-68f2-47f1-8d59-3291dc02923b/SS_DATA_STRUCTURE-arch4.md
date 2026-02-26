# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- The UK Environmental Change Network (ECN) programme collects environmental data through site monitoring and network coordination.
- Dataset Owners are a consortium of UK government departments and agencies supporting ECN, including Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NI Environment Agency, Scottish Environment Protection Agency, Scottish Government, and Scottish Natural Heritage.
- Acknowledgement of data use is requested, and be sure to send one reprint of any publication citing ECN data.

## Data governance and structure
- ECN applies standard operating procedures to ensure data comparability across sites; accompanying ss.pdf explains data collection.
- Data are structured for download with core fields:
  - SITECODE (site code), SDATE (sampling date), RID (replicate ID), FIELDNAME (variable measured), VALUE (measured value).
- Supporting documentation provides lab analysis details and data quality context:
  - ECN_SS2.csv: lab analysis metadata (lab ID, dates, etc.).
  - ECN_SS_qtext.csv: site manager quality text describing data issues; linked by quality code 999 when applicable.
  - ECN_QC1.csv and ECN_QC2.csv: quality control data for instruments and analyses.

## Protocol and sampling details
- Suction samplers measure soil solution chemistry; sampling occurs fortnightly.
- If a sampler is replaced, a new RID is issued.
- If insufficient sample collected on a day, samples can be bulked with RID codes XXS (shallow) or XXD (deep).
- A standard QC solution is analysed with field samples; QC data accompany the dataset and should be used as part of data quality assessment.

## Data structure and download formats
- Main dataset fields for download:
  - SITECODE, SDATE, RID, FIELDNAME, VALUE.
- Supporting documentation fields (ECN_SS2.csv) include:
  - SITECODE, RID, FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE.
- Quality context fields (ECN_SS_qtext.csv) include:
  - SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING.
- Quality codes list (ECN quality codes) and explanations are included, with 999 used for unusual events and textual explanations when needed.

## Explanatory information: variables and units
- FIELDNAME entries cover key water chemistry and related properties, including:
  - ALKY (Alkalinity, mg/L), ALUMINIUM (mg/L), CALCIUM (mg/L), CHLORIDE (mg/L), COLOUR (absorbance at 436 nm, nM), CONDY (conductivity, microSiemens/cm), DOC (dissolved organic carbon, mg/L), IRON (mg/L), MAGNESIUM (mg/L), NH4N (ammonium, mg/L), NO3N (nitrate nitrogen, mg/L), PH (pH scale), PHAQCS/PH AQCU (Aquacheck pH readings), PO4P (phosphorus, mg/L), POTASSIUM (mg/L), SO4S (sulphate, mg/L), SODIUM (mg/L), TOTALN (mg/L), TOTALP (mg/L), VACUUM (residual vacuum, bar), VOLUME (ml).
- Units are specified alongside each variable; quality codes Q1–Q5 accompany measurements to indicate data quality factors.

## Quality codes
- Standard ECN quality codes cover data issues from data loss to field or laboratory problems, e.g.:
  - 100–115, 122, 123, 124, 126, 137, 140, 160, 182, 200–223, 501–507, 508–509, 511, 999.
- 999 indicates an unusual event with accompanying quality text.
- Descriptions cover issues like no information, lost samples, partial loss, equipment failures, contaminants, non-standard sampling, and laboratory problems.

## Sites and access
- ECN site codes T01–T12 correspond to 12 sites with named locations:
  - T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House - Upper Teesdale, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Snowdon (Y Wyddfa), T12 Cairngorms.
- Each site has geographic coordinates provided in the documentation.
- Further information about ECN sites is available at the ECN catalogue link: https://catalogue.ceh.ac.uk/id/813712d4-d162-4ede-aff8-cf1c337bdc27.

## Usage, attribution, and contact
- Acknowledge ECN data use and provide one reprint of any publication citing ECN data.
- Data are accompanied by extensive metadata and documentation to support data quality assessment and integration into broader analyses.
- For questions or access details, refer to the ECN Data Centre contact (ecn@ceh.ac.uk) and the data portal at the provided URL.