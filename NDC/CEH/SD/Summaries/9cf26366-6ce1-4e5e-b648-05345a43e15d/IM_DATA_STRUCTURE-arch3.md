# ECN Macrolepidoptera Dataset

## Overview
- Originator: ECN Data Centre (http://data.ecn.ac.uk), Centre for Ecology and Hydrology.
- Dataset Owners: UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies including AFBI, BBSRC, NRW, DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, and Scottish Natural Heritage.
- Purpose: Collect and provide environmental change data to understand causes and consequences of environmental change; support monitoring, analysis, and policy evaluation.
- Protocol and scope: Standard light-trap protocol for Macrolepidoptera; Rothamsted Insect Survey methodology; data recorded nightly.
- Data use and dissemination: Acknowledgement requested for data use; request for one reprint of any publication citing the data; data are intended to be quality assured and openly shared where appropriate within governance constraints.
- Notes on data quality and metadata: Accompanied by supplemental quality information; metadata and quality controls are integral to data usability.

## Data provenance, structure, and coverage
- Data origin: Macrolepidoptera observations collected via standardized light-trap protocol.
- Data structure: Core fields include SITECODE, LCODE, SDATE, FIELDNAME, VALUE.
  - SITECODE: Site identifier.
  - LCODE: Location/trap code (per site, typically '1' as there is one moth trap per site in this dataset).
  - SDATE: Sampling date (dd-mmm-yyyy).
  - FIELDNAME / VALUE: If FIELDNAME is a quality code, VALUE contains the detailed quality code; if FIELDNAME is a species code, VALUE indicates the count of observed individuals.
- Site coverage and metadata: Ten sites listed with site names, coordinates, and observation date ranges.
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T12 Cairngorms
  - Date ranges span from early 1990s to 2012, with site-specific windows (e.g., Drayton 1993–2012, Rothamsted 1992–2012, Cairngorms 2001–2012).
- Additional site information: Central ECN site catalog link provided for further information.

## Taxonomy, codes, and quality controls
- Quality codes (Table 3a): Quality code indicators (Q1–Q8) mapped to descriptive quality codes (detailed in Table 4).
- Species codes (Table 3b): Extensive mapping of numeric species codes to Latin names and common names of macro-moths (examples include 100 Alder Kitten, 1001 Rush Veneer, 31 Painted Lady, 31–various mappings, up to hundreds of codes with extensive aliasing and macro/micro groupings).
- Supplemental quality information: Two accompanying files
  - ECN_IM2.csv: Periods over which moth traps were open (e.g., PERIOD = 1 for daily trap emptying; other values indicate multi-day openings).
  - ECN_IM_qtext.csv: Text descriptions of quality events that explain absences or data inconsistencies.
- Quality codes (Table 4): Comprehensive ECN quality codes (501–primitive lab codes, 999 for unusual events) covering data collection, sample handling, laboratory processing, and environmental conditions (e.g., instrument issues, condensation, flooding, rainfall, grazing, sampling disturbances, etc.).
- Data governance implication: Data quality and provenance are codified; site managers assign codes to indicate data quality and context, enabling transparent assessment of data reliability.

## Access, attribution, and data governance
- Usage acknowledgement: ECN requests acknowledgement of data use to gauge dataset impact and demonstrate value for environmental-change research.
- Publication requirement: Request to send one reprint of any publication citing the ECN data.
- Data sharing and governance: Emphasis on sharing underlying data where appropriate, with governance processes to ensure standards, storage, and up-to-date maintenance; transformation and metadata enrichment may be necessary to ensure usability.
- Supplemental metadata considerations: Quality metadata and supplemental files (ECN_IM2.csv and ECN_IM_qtext.csv) accompany the primary dataset to enhance interpretability and data quality appraisal.

## Practical considerations for monitoring and policy evaluation
- Monitoring aims alignment: Data collected to inform policy scrutiny, evaluate environmental health measures, and guide future decisions.
- Data quality and access challenges (as identified by archetype perspective):
  - Potential data gaps and variable data quality standards across sites.
  - Access barriers due to data sharing constraints and metadata completeness.
  - Silos between organisations could hinder cross-site data synthesis.
  - Need for robust metadata to verify data suitability and comparability.
  - Data transformation requirements due to varied data formats and coding schemes.
  - Communicating complex, species-rich findings clearly to stakeholders.
- Data handling and reporting workflow:
  - Data are quality assured, cleaned, transformed, analyzed, and reported via reports, charts, or dashboards.
  - Outputs are disseminated with stakeholder consultations and appropriate data governance for sharing underlying data.
  - Supplementary information (trap periods and quality notes) is essential for accurate interpretation and temporal analysis.

## Endnotes and external references
- ECN site information and wider context available at the ECN data catalog and related owner/partner organisations’ portals.
- Supplemental materials: ECN_IM2.csv and ECN_IM_qtext.csv provide trap-period data and qualitative explanations of unusual or contextual data, respectively.