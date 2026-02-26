# Dataset Originator

- Overview
  - ECN Data Centre (Centre for Ecology and Hydrology) manages environmental change data.
  - ECN program funded by a consortium of UK government departments and agencies; data are from site monitoring and network coordination activities.
  - Partners include Agri-Food & Biosciences Institute, BBSRC, Cyfoeth Naturiol Cymru, Defence Science & Technology Laboratory, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, and Scottish Natural Heritage.
  - Users are asked to acknowledge data use and to send one reprint of any publication citing ECN data.

- Data Providers
  - Ministries and agencies listed above contribute to site monitoring or network coordination.
  - Acknowledgment and reprint request mentioned.

- Protocols and Data Quality
  - Standard operating procedures ensure data comparability across sites (details in accompanying wc.pdf).
  - Weekly dip sampling for stream water chemistry; quality control solution used at laboratories analyzed alongside field samples.
  - Quality information accompanies the data; use quality data when analyzing.

- Usage Notes
  - Dip samples measure stream water chemistry; sampling is weekly.
  - Quality control data accompany datasets; use these to assess data quality.
  - Quality codes and accompanying texts explain data issues or unusual events.

- Data Download Structure
  - Core download fields: SITECODE (site code), LCODE (location ID within site), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measured value).
  - Supporting documentation for lab analyses is provided in ECN_WC2.csv (lab details and sampling times).

- Supporting Documentation
  - ECN_WC2.csv: Lab analysis information; includes SITECODE, SDATE, FIELDNAME, VALUE.
  - ECN_WC_qtext.csv: Site managers’ quality codes and associated explanatory text for quality issues.
  - ECN_QC1.csv: Quality control solution data (lab analysis field name and value).
  - ECN_QC2.csv: Additional QA/QC lab analysis information (bulk deployment, sampling times, lab, pH measurements, filtration dates).
  - Explanatory material about site codes and variable names.

- Site Codes and Variables
  - Explanatory Site Codes: Examples include T02 Glensaugh; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T08 Wytham; T11 Snowdon; T12 Cairngorms; coordinates provided for many sites.
  - Variables being measured (FIELDNAME) include:
    - ALKY (Alkalinity), ALUMINIUM, CALCIUM, CHLORIDE, COLOUR, CONDY (Conductivity), DOC (Dissolved Organic Carbon),
      IRON, MAGNESIUM, NH4N (Ammonium), NO3N (Nitrate nitrogen), PH (pH), PHAQCS, PHAQCU (pH measures by Aquacheck),
      PO4P (Phosphate phosphorus), POTASSIUM, SO4S (Sulfate), SODIUM, STAGE (Water level), TOTALN, TOTALP, plus quality fields Q1–Q6.
  - Units are provided alongside most variables (e.g., mg/L, µS/cm, pH, mm).

- Quality Codes
  - Range of codes indicating data quality or issues, including:
    - 100 No information available; 101 No sample/reading; 102 Sample lost; 103 Partial loss; 105–119 various environmental or sampling issues (weather, debris, etc.); 126/127 River/lake status; 169–229 various events affecting sampling.
    - 501–511 Laboratory-related issues (no sample, contamination, insufficient sample, equipment failure, etc.).
    - 999 Unusual event (see accompanying quality text).
  - These codes help explain data gaps or quality implications.

- Explanatory Information
  - Site Codes and variable definitions linked to further information:
    - Site catalog and site coordinates available at the provided ECN catalogue link.
    - Variable descriptions and units detailed for accurate interpretation.

- Attribution and Usage Guidance
  - Acknowledge ECN data usage in publications; report back with a reprint if possible.
  - Review accompanying quality information to properly interpret data quality and any caveats for analysis.
  - The data are intended to be comparable across sites via standardized procedures; consult wc.pdf for data collection methods.