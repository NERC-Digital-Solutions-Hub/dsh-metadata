# ECN Water Chemistry Dataset Documentation

## Overview
- Dataset originator: ECN Data Centre (Centre for Ecology and Hydrology), with ECN data documenting environmental change.
- Data providers: UK government departments and agencies contributing to ECN via site monitoring or network coordination (e.g., Defra, Natural England, Scottish Government, Welsh Government, Environment Agency, NERC, etc.).
- Purpose: support understanding of environmental change, scrutinise and evaluate policy, and inform future monitoring decisions; emphasises usefulness of measures through stakeholder engagement and cross-organisational learning.
- Data governance emphasis: data sharing, metadata quality, and transparent data management are central; datasets are intended to be quality assured, cleaned, transformed, and presented clearly, often via reports, charts, or dashboards.

## Data provenance and governance
- Users are asked to acknowledge data use and to send one reprint of publications citing ECN data.
- Protocols: ECN operates standard operating procedures to ensure data comparability across sites (refer to wc.pdf for data collection explanations).
- Data sharing and metadata: essential but can pose barriers; coordination with data originators helps overcome metadata gaps and access issues.
- Governance: emphasis on data quality assurance, openness, and appropriate data storage, sharing, and updates.

## Data structure and access
- Data download schema includes:
  - SITECODE: unique ECN site code
  - LCODE: location ID within site
  - SDATE: sampling/data recording date
  - FIELDNAME: variable measured
  - VALUE: measured value
- Supporting documentation:
  - ECN_WC2.csv: lab analysis metadata (sampling date, lab ID, pH measurement times, etc.)
  - ECN_WC_qtext.csv: site manager quality notes corresponding to quality codes
  - ECN_QC1.csv and ECN_QC2.csv: quality control data for lab analyses
- Site and location information (Explanatory Information: Site Codes) includes several ECN sites (e.g., Glensaugh, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Snowdon, Cairngorms) with their coordinates.
- Variables being measured (FIELDNAME) cover a wide range of water chemistry and related measures (alkalinity, major ions, conductivity, dissolved organic carbon, nutrients, pH, flag indicators such as Aquacheck pH readings, dissolved total nitrogen/phosphorus, etc.) with corresponding units.
- Quality codes (Explanatory Information: Quality Codes): a comprehensive list of codes describing data quality issues or unusual events (e.g., data loss, sample issues, lab issues, weather impacts, unusual events) including a catch-all 999 for unusual events requiring accompanying text.

## Sampling, quality control, and metadata
- Usage notes:
  - Dip water samples are collected weekly to measure stream water chemistry.
  - A standard quality control solution is analyzed with field samples to assure lab accuracy; QC data accompany the main dataset.
  - Quality information must be consulted when using the data.
- Quality codes provide context for data quality and potential issues (from field sampling conditions to laboratory processing and unusual events).

## Site, variables, and data interpretation
- Site codes map to specific ECN sites with precise geographic coordinates, enabling spatial analyses of environmental changes.
- Variables span key water chemistry indicators relevant to monitoring environmental health, ecosystem status, and potential policy impacts.
- Data interpretation benefits from:
  - Access to accompanying metadata and quality codes to assess data reliability
  - Understanding of sampling cadence (weekly dip samples) and lab QC procedures
  - Awareness of potential data gaps or quality concerns indicated by site-specific quality text

## Using the dataset for monitoring frameworks
- Useful for:
  - Evaluating policy impact on environmental health indicators
  - Informing future monitoring design through understanding data completeness, timeliness, and standardisation needs
  - Communicating complex findings via clear data presentation (charts, dashboards) with transparency about data quality
- Considerations and barriers:
  - Data may be incomplete or heterogenous across sites; standardisation and metadata completeness are ongoing concerns
  - Public sharing requirements and data governance processes can influence data reuse
  - Transforming and validating dataset formats may require effort to ensure usability across monitoring frameworks

## Endnotes and attribution
- Acknowledgement of ECN data use and reference to accompanying documentation are encouraged to support recognition of data value for environmental change research.