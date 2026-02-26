# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- The ECN (Environmental Change Network) data centre provides environmental data collected across multiple sites in the UK, with data providers including major government departments and agencies.
- Purpose: support research on environmental change; data use should be acknowledged, and users are asked to send one reprint of any publication citing ECN data.

## Data provenance and protocol
- The ECN operates with standard operating procedures to ensure data comparability across sites.
- Users should refer to the accompanying pc.pdf for details on data collection methods.

## Data structure and content
- Data download fields:
  - SITECODE: Unique code for each ECN site
  - SDATE: Sampling date
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Site codes and locations (examples):
  - T01–T12 with site names (e.g., Drayton, Glensaugh, Hillsborough, etc.) and precise coordinates.
- Variables being measured (FIELDNAME) include:
  - Alkalinity (ALKY), Aluminium, Calcium, Chloride, Colour, Conductivity (CONDY), Dissolved Organic Carbon (DOC), Iron, Magnesium, Ammonium (NH4N), Nitrate-N (NO3N), pH, pH measurements (PHAQCS, PHAQCU), Phosphate (PO4P), Potassium, Sulphate (SO4S), Sodium, Total Nitrogen/Phosphorus, Volume of sample, and quality fields Q1–Q6.
- Units are provided alongside many variables (e.g., mg/L, µS/cm, pH, ml).

## Quality assurance and quality control
- Quality control procedures:
  - Use of a standard quality control solution sent to labs; QC data accompany the dataset.
  - Quality information must be used when analyzing data.
- Quality codes:
  - A standard list of codes (100–999) indicates various issues (e.g., 100 = no information available, 501–507 = laboratory/analysis issues, 999 = unusual event).
  - If 999 is used, accompanying quality text describes the unusual event (ECN_PC_qtext.csv).
- Post-hoc and chemistry QC:
  - ECN_PC_chemistry-QC.csv provides post-hoc screening results, including checks on conductivity versus theoretical conductivity, ion balance, and phosphate contamination indicators.
  - COND_RATIO_OK, ION_DIFF_OK, PO4_OK, and OVERALL_CHECK_OK columns indicate data quality suitability for temporal analyses and calculations of concentrations/fluxes.

## Supporting documentation
- ECN_PC2.csv: Lab analysis details (SITECODE, FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE).
- ECN_PC_qtext.csv: Qualitative notes for quality events (SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION).
- ECN_QC1.csv and ECN_QC2.csv: Additional quality control data for QC samples and lab analyses (structure mirrors data fields with sampling and analysis timestamps).
- ECN_PC_chemistry-QC.csv: Post-hoc chemistry QC results and interpretation guidance.

## Site and variable details
- Site Codes (example mappings):
  - T01: Drayton
  - T02: Glensaugh
  - T03: Hillsborough
  - T04: Moor House - Upper Teesdale
  - T05: North Wyke
  - T06: Rothamsted
  - T07: Sourhope
  - T08: Wytham
  - T09: Alice Holt
  - T10: Porton Down
  - T11: Snowdon (Y Wyddfa)
  - T12: Cairngorms
- Variables and their descriptions include alkalinity, major ions (Ca, Mg, Na, K, Cl, SO4, NO3, NH4, PO4), dissolved organic carbon, conductivity, pH, colour absorbance, temperature-like quality indicators, and sample volume.

## Data usage guidance
- Follow ECN’s data acknowledgement and citation requirements; share reprints where possible.
- Combine ECN data with other data sources only after ensuring compatibility via the provided protocols.
- Leverage the accompanying quality documentation to filter data (e.g., use OVERALL_CHECK_OK = 1 for robust trends analyses).

## Key considerations and challenges
- Data can be patchy and stored in multiple formats; rely on standard ECN quality codes and QC documentation to assess usability.
- Data interpretation requires attention to quality flags, unusual events (code 999), and laboratory-specific notes.
- For robust temporal analyses, prioritize data points flagged as OK in the post-hoc chemistry QC (COND_RATIO_OK, ION_DIFF_OK, PO4_OK, OVERALL_CHECK_OK).