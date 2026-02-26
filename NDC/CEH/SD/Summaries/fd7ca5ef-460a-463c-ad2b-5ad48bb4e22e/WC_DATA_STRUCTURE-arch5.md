# Dataset Originator

- Overview
  - ECN Data Centre hosts environmental datasets; ECN is sponsored by a consortium of UK government departments and agencies funding site monitoring and network coordination.
  - Data providers include multiple UK bodies (e.g., Defra, Natural England, NERC, SEPA, etc.).
  - Users are asked to acknowledge the data use and to send one reprint of any publication citing ECN data.

- Protocol and Standardization
  - ECN operates standard operating procedures to ensure data comparability across sites.
  - A accompanying wc.pdf explains data collection methods and protocols.

- Usage Notes
  - Dip samples for stream water chemistry are collected weekly.
  - A standard quality control (QC) solution is analyzed alongside field samples to monitor lab performance; QC data are available with the dataset.
  - Always use the accompanying quality information when using the data.

- Data Download and Supporting Documentation
  - Core download fields include SITECODE (site code), LCODE (location ID within site), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measured value).
  - Supporting Documentation files:
    - ECN_WC2.csv: lab analysis information.
    - ECN_WC_qtext.csv: site manager quality text notes for events affecting data quality.
    - ECN_QC1.csv: QC solution field data (lab analyses in QC checks).
    - ECN_QC2.csv: additional lab analysis metadata for QC.
  - Explanatory information provided for sites, variables, and quality codes.

- Explanatory Information
  - Site Codes: Examples include T02 Glensaugh, T04 Moor House - Upper Teesdale, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T11 Snowdon, T12 Cairngorms, with precise geographic coordinates.
  - Variable Being Measured (FIELDNAME): Includes alkalinity (ALKY), aluminium, calcium, chloride, colour, conductivity (CONDY), dissolved organic carbon (DOC), iron, magnesium, ammonium (NH4N), nitrate-nitrogen (NO3N), pH (PH), various pH measurement methods (PHAQCS, PHAQCU), phosphate phosphorus (PO4P), potassium, sulphate (SO4S), sodium, water stage (STAGE), total nitrogen (TOTALN), total phosphorus (TOTALP), and associated quality codes (Q1–Q6, plus Q-values).
  - Quality Codes: Comprehensive list of codes indicating data quality issues (e.g., 100 No information available, 101 No sample taken, 105 Snow in funnel, 169 High river flow, 501 Laboratory: No sample, 506 Equipment failure, 999 Unusual event with accompanying text). Multiple codes can be applied per record, and 999 is used when an unusual event requires textual explanation.

- Governance, Usage and Documentation
  - Acknowledgement and publication traceability are encouraged to demonstrate data value for environmental-change research.
  - Data updates and sharing follow ECN's protocols to maintain consistency and comparability across datasets and sites.
  - Documentation of work performed on datasets may be encouraged to accompany releases.

- Challenges for Data Stewards
  - Aligning diverse user needs with standardized datasets.
  - Timely ingestion of data from multiple sites and systems.
  - Achieving consistent metadata and ensuring interoperability across formats.
  - Handling large data volumes and updating legacy databases while preserving data provenance.