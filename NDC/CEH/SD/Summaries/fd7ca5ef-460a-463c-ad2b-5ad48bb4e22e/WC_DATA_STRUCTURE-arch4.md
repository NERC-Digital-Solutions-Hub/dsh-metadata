# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- Source and stewardship: ECN Data Centre coordinates data from the UK Environmental Change Network, funded by a consortium of government departments and agencies.
- Partners/providers: Includes Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, Scottish agencies, and others.
- Usage and attribution: Acknowledgement of data use is requested; researchers should send one reprint of any publication citing ECN data.

## Data Collection and Protocol
- Standardization: ECN uses standard operating procedures to ensure data comparability across sites; supporting protocol details are provided (wc.pdf).
- Sampling: Dip samples collected weekly to measure stream water chemistry.
- Quality control: Laboratories receive a standard quality control solution; QC data accompany the dataset and should be used as part of data quality assessment.
- Data quality information: Quality information and associated QC documentation must be consulted when using the data.

## Data Structure and Access
- Core data fields: SITECODE (site code), LCODE (location ID within site), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measured value).
- Supporting documentation files:
  - ECN_WC2.csv: Lab analysis details (SITECODE, LCODE, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE).
  - ECN_WC_qtext.csv: Site manager quality codes and explanatory text (with 999 for unusual events); fields include SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
  - ECN_QC1.csv: QC solution field data (SITECODE, SDATE, FIELDNAME, VALUE).
  - ECN_QC2.csv: Additional lab QC data (SITECODE, FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE).
- Site codes and locations: Explanatory Information provides mappings (e.g., T02 Glensaugh; T04 Moor House; T05 North Wyke; plus coordinates for each site).
- Variables measured: FIELDNAME includes a wide range of water chemistry and related metrics (e.g., ALKY, ALUMINIUM, CALCIUM, CHLORIDE, COLOUR, CONDY, DOC, IRON, MAGNESIUM, NH4N, NO3N, PH, PHAQCS, PHAQCU, PO4P, POTASSIUM, SODIUM, STAGE, TOTALN, TOTALP, etc.) with corresponding units.

## Quality and Metadata
- Quality codes: A comprehensive list of quality codes (e.g., 100–129, 169, 170, 182, 191, 200, 501–511, 999) with descriptions for data loss, sampling issues, laboratory issues, weather-related effects, and unusual events.
- Quality text: When codes indicate unusual events, accompanying text explains circumstances (via ECN_WC_qtext.csv).

## Usage, Standards, and Governance
- Data comparability: Protocols ensure cross-site comparability; users should refer to accompanying documentation for collection methods.
- Metadata and discoverability: Detailed field definitions, site mappings, and QC documentation support data discovery and appropriate reuse.
- Data updates and stewardship: Ongoing data collection across ECN sites; documentation provides structure for updating datasets and evaluating data suitability.

## Practical Implications for Data Leaders
- Holistic data system view: The dataset exemplifies a multi-site, standardized environmental data system requiring governance around data formats, metadata, and quality controls.
- User needs and co-ownership: Rich metadata and QC information support diverse user needs (policy colleagues, researchers) with potential for co-ownership of data products through clear provenance and quality context.
- Data availability and access: Data are organized with explicit structure (site, location, date, variable, value) and comprehensive supporting docs to aid discovery and reuse; however, users must navigate multiple accompanying files (ECN_WC2.csv, ECN_WC_qtext.csv, ECN_QC1.csv, ECN_QC2.csv).
- Barriers and challenges: While not explicit in the notes, typical data leadership considerations (in line with the archetype) include managing data access barriers, ensuring granularity and coverage across sites, and integrating quality codes into data workflows.
- Attribution and impact tracking: The requirement to acknowledge data use and provide reprints enables impact tracking and value demonstration for funders and stakeholders.