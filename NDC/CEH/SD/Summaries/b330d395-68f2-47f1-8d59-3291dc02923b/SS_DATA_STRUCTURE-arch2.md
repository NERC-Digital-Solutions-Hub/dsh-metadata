# Dataset Originator

- The ECN Data Centre at the Centre for Ecology and Hydrology is the originator of the dataset.
- Data are part of the UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies.

## Overview

- Dataset records soil solution chemistry from ECN monitoring sites, with standardised procedures to enable cross-site comparability.
- ECN seeks acknowledgment of data use and a reprint of publications citing the dataset.

## Provenance and Sponsoring

- Dataset Owners: UK Environmental Change Network (ECN) programme.
- Sponsoring organisations include: Agri-Food and Biosciences Institute, BBSRC, Cyfoeth Naturiol Cymru - Natural Resources Wales, DSTL, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, Northern Ireland Environment Agency, SEPA, Scottish Government, Scottish Natural Heritage.
- Acknowledgement and citation: users should acknowledge data use and send one reprint to ECN.

## Data Collection Protocol

- Standard operating procedures ensure data comparability across sites; see accompanying ss.pdf for collection explanation.
- Monitoring method: suction samplers measure soil solution chemistry, samples collected fortnightly.
- Replication handling: replacement of suction samplers is indicated by a new RID (replicate ID).
- Bulk sampling: if insufficient samples are collected, daily samples may be bulked; RID values XXS (shallow) and XXD (deep) indicate bulked samples.
- Quality assurance: a standard QC solution is sent to laboratories and analyzed with field samples; QC data available with dataset; use accompanying quality information for data usage.

## Data Structure and Access

- Primary data fields in download:
  - SITECODE: unique ECN site code
  - SDATE: sampling date
  - RID: replicate ID
  - FIELDNAME: measured variable
  - VALUE: measured value
- Supporting documentation files:
  - ECN_SS2.csv: lab analysis information (e.g., SITECODE, RID, FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE)
  - ECN_SS_qtext.csv: quality text descriptions (SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING)
  - ECN_QC1.csv: QC standard solution results (SITECODE, SDATE, FIELDNAME, VALUE)
  - ECN_QC2.csv: additional lab analysis information (SITECODE, FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE)
- Site metadata and coordinates are provided for each ECN site (T01–T12) with site names and geographic coordinates.
- Additional information about ECN sites is available via the ECN site catalogue.

## Variables and Units

- Explanatory variable names include: ALKY (Alkalinity, mg/L), ALUMINIUM (mg/L), CALCIUM (mg/L), CHLORIDE (mg/L), COLOUR (absorbance at 436 nm, nM), CONDY (conductivity, microSiemens/cm), DOC (dissolved organic carbon, mg/L), IRON (mg/L), MAGNESIUM (mg/L), NH4N (ammonium, mg/L), NO3N (nitrate nitrogen, mg/L), PH (pH), PHAQCS and PHAQCU (Aquacheck pH readings, pH scale 1–14), PO4P (phosphate phosphorus, mg/L), POTASSIUM (mg/L), SO4S (sulphate, mg/L), SODIUM (mg/L), TOTALN (mg/L), TOTALP (mg/L), VACUUM (residual vacuum, bar), VOLUME (sample volume, mL).
- Quality fields Q1–Q5 (quality codes) accompany measurements.

## Quality Codes

- 100: No information available - data lost
- 101–111, 113, 115, 122, 123, 124, 126, 137, 140, 160, 182: various in-field issues (e.g., no sample, snow, debris, flooding, equipment issues)
- 200–223: adverse conditions affecting sampling/recording; non-standard sampling date/time
- 501–508, 511: laboratory-related issues (no sample, lost sample, contamination, etc.)
- 999: Unusual event – see quality text for details

## Site Details

- 12 ECN sites (T01–T12) with names and precise coordinates:
  - Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon (Y Wyddfa), Cairngorms
- Site-specific geographical data available through the ECN site catalogue link.

## Usage Guidance for Analysts

- Use standardized field names and the accompanying quality information to interpret data.
- Consider QC data and quality codes when assessing data reliability.
- When combining ECN data with other datasets, leverage the standardized protocols to enhance cross-dataset comparability.
- Properly acknowledge ECN data usage and share publications as requested.