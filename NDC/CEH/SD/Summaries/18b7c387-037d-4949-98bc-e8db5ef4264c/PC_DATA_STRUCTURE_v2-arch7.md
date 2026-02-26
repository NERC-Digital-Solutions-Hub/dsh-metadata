# ECN Data Centre Dataset

- Source and purpose
  - Dataset originate from ECN Data Centre (Centre for Ecology and Hydrology) with data providers including a consortium of UK government departments and agencies.
  - Purpose: provide precipitation chemistry data suitable for GIS-based visualization and analysis to support understanding environmental change.

- GIS relevance and audience
  - Designed for map-based data visualisations to help policy colleagues, clients, and the public explore spatial and temporal patterns.
  - Audience-oriented workflow emphasizes locating site positions, comparing site data, and presenting spatial features clearly.

- Data coverage and site information
  - 12 ECN sites (Site Codes T01–T12) with named locations and geographic coordinates.
  - Site list includes Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon (Y Wyddfa), Cairngorms.
  - Location coordinates are provided for each site, enabling accurate GIS mapping and spatial joins.

- Data model and fields
  - Core data download fields:
    - SITECODE: site identifier
    - SDATE: sampling date
    - FIELDNAME: variable measured (e.g., ALKY, CALCIUM, NO3N, PH, etc.)
    - VALUE: measured value
  - Supporting documentation fields expand temporal and lab metadata:
    - FROMDATE/FROMHOUR/FROMMINS: deployment time of bulk collectors
    - SHOUR/SMINS: sampling time
    - LAB_NID: laboratory performing analyses
    - PHDATE/PHHOUR/PHMINS; FILTDATE; COMPDATE: analysis-related timestamps
    - VOLUME: sample volume
    - Q1–Q6: quality codes at measurement level
  - Fieldnames include a wide range of chemical constituents and related measurements:
    - Alkalinity (ALKY/ALKY mg/L)
    - Major ions and nutrients (e.g., CALCIUM, CHLORIDE, CONDUCTIVITY, DOC, IRON, MAGNESIUM, NH4N, NO3N, PH, PO4P, POTASSIUM, SODIUM, TOTALN, TOTALP)
    - Physical property (COLOUR, VOLUME), and multiple pH assessments (PH, PHAQCS, PHAQCU)
  - Units are specified alongside field definitions (e.g., mg/L, µS/cm, pH, ml).

- Quality assurance and quality control
  - Protocols ensure data comparability across sites; accompanying PC.pdf explains collection methods.
  - Routine quality control: standard QC solution analyzed alongside field samples.
  - Quality codes allow site managers to flag data quality issues using a predefined list (e.g., 100–133, 180, 182, 187, 191, 200, 222, 223, 501–507, 508–511) plus 999 for unusual events.
  - Additional QC documentation:
    - ECN_PC_qtext.csv provides text notes for quality events (associated with code 999).
    - ECN_CCU chemistry QC (ECN_PC_chemistry-QC.csv) compares measured conductivity against theoretical conductivity and assesses ion balance (cations/anions) with multiple flags:
      - COND_RATIO_OK, ION_DIFF_OK, PO4_OK, OVERALL_CHECK_OK
      - Criteria for acceptable ranges and guidance on including data in temporal analyses.

- Data provenance and usage notes
  - Data usage requests acknowledgement: users should acknowledge ECN datasets and send a reprint of any publication citing the data.
  - Data packaging includes both primary measurements (ECN_PC2.csv) and extensive supporting documentation (ECN_PC_qtext.csv, ECN_QC1.csv, ECN_QC2.csv, etc.).
  - The dataset emphasizes the need to consult accompanying quality information when analyzing or visualizing data.

- How to use in GIS/map-based workflows
  - Join ECN data to the site location table using SITECODE to map sampling locations and summarize measurements by site and date.
  - Create time-series visualizations per site for selected FIELDNAMEs (e.g., NO3N, NH4N, PH, ELECTROLYTES).
  - Apply quality filters using quality indicators (e.g., Q1–Q6, QUALITY_TEXT for 999 events, OVERALL_CHECK_OK) to ensure spatial analyses rely on reliable data.
  - Use supporting documentation to interpret timestamps (FROMDATE, SHOUR, etc.) and to understand sampling volume and laboratory processing, ensuring accurate spatial-temporal alignment.
  - Consider potential data gaps due to quality flags or non-standard sampling days when interpreting maps and trends.

- Practical considerations and caveats
  - Data are distributed across multiple files and supporting documents; ensure integration with the core dataset (SITECODE, SDATE, FIELDNAME, VALUE) via proper joins.
  - Data availability and accuracy may be affected by quality flags; apply filters based on the ECN QC criteria for robust spatial analyses.
  - Data for very low-concentration ions may be sensitive to measurement uncertainty; consult QC guidance before deriving mean concentrations or flux estimates.

- Access and contact
  - Originator contact: ECN Data Centre (http://data.ecn.ac.uk, ecn@ceh.ac.uk).
  - Acknowledgement and reprint requirements help quantify dataset usage and value for environmental-change research.