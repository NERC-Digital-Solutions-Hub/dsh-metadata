# ECN Data Centre Dataset Description

- Purpose and role for analysts: A standardised environmental monitoring dataset from the ECN network, designed to show environmental health and policy performance over time through comparable, quality-assured data products.

- Data provenance and providers:
  - Dataset originator: ECN Data Centre, Centre for Ecology and Hydrology (CEH)
  - Data providers: UK Environmental Change Network (ECN) programme funded by multiple UK government departments and agencies
  - Acknowledgement and citation: Users should acknowledge ECN data and send one reprint of any publication citing the data

- Protocols and quality assurance:
  - Standard operating procedures to ensure comparability across sites
  - Laboratories receive a quality control (QC) solution analysed with field samples
  - Quality information accompanies data; use QC information in analyses

- Data content and structure:
  - Core data download fields:
    - SITECODE: ECN site code
    - SDATE: Sampling date
    - FIELDNAME: Variable measured
    - VALUE: Measured value
  - Supporting documentation and data fields cover timing of sampling, lab analysis, and quality checks (ECN_PC2.csv; ECN_PC_qtext.csv; ECN_QC1.csv; ECN_QC2.csv)
  - Site codes (T01–T12) with site names and geographic coordinates
  - Variables measured (examples): ALKY (alkalinity), CALCIUM, CHLORIDE, COLOUR, CONDY (conductivity), DOC (dissolved organic carbon), IRON, MAGNESIUM, NH4N, NO3N, PH, PHAQCS, PHAQCU, PO4P, POTASSIUM, SODIUM, TOTALN, TOTALP, VOLUME, etc.

- Quality codes and unusual events:
  - Site managers assign quality codes from a standard list (e.g., 100–133, 180, 182, 187, 191, 200, 501–507, 999)
  - 999 indicates an unusual event; additional text available in ECN_PC_qtext.csv
  - A separate chemistry QC file (ECN_PC_chemistry-QC.csv) provides post-hoc screening of measurements against theoretical/conductivity expectations

- Explanatory information:
  - Site names and coordinates for T01–T12 (examples: Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms)
  - Variables and units (e.g., ALKY mg/L, CONDY microSiemens/cm, PH 1–14)

- Data quality and interpretation guidance:
  - Quality control data and supporting QC files should be used to assess data reliability
  - ECN_PC_chemistry-QC.csv provides checks on conductivity balance and ion balance; recommended to include only samples flagged as acceptable for temporal trend analyses

- Usage notes and data handling:
  - Bulk collectors for precipitation chemistry collected weekly
  - Laboratories process samples with QC solutions; use accompanying QC information
  - Ensure correct interpretation of quality codes and accompanying text
  - When computing temporal trends or fluxes, prefer data points with overall_OK = 1 in ECN_PC_chemistry-QC.csv and avoid samples flagged for potential contamination or inadequate measurements

- Data access and dissemination:
  - Data are stored and made available via ECN data portals; researchers are encouraged to store and share derived datasets following standard practice

- Practical considerations for analysts:
  - Understand data provenance, site-specific conditions, and timing to ensure comparability across sites
  - Leverage standardized fields (SITECODE, SDATE, FIELDNAME, VALUE) for cross-site analyses
  - Use the quality codes and QC summaries to filter data for robust trend analysis
  - Acknowledge data sources and submit publications to ECN as requested

- Challenges and opportunities:
  - Increasing the value of datasets by integrating ECN data with other environmental data sources
  - Enhancing access to underlying data for wider use and secondary analyses