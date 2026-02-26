# UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012

- Originator: ECN Data Centre (CN Data Centre at Centre for Ecology and Hydrology)
- Data providers: UK Environmental Change Network programme and sponsoring government departments/agencies (multiple UK bodies listed)
- Purpose and use: Data provided to understand environmental change; users should acknowledge dataset and send one reprint of any publication citing the data

- Scope and coverage
  - Dataset title: UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012
  - Sites: 12 ECN sites (T01–T12) across the UK with site-specific coordinates and date ranges
  - Time coverage: 1992–2012 (dates vary by site; some sites end 2012, others earlier)
  - Parameters: Soil solution chemistry measurements (alkalinity, major cations/anions, conductivity, colour absorbance, dissolved organic carbon, pH, total nitrogen/phosphorus, etc.)
  - Variables and units are specified in Fieldnames (e.g., ALKY mg/L, CALCIUM mg/L, pH, CONDY microSiemens/cm, VOLUME ml, etc.)

- Data structure and metadata
  - Core data fields: SITECODE, SDATE, RID, FIELDNAME, VALUE
  - Additional data structure: Varies for analytical details (SITECODE, RID, FROMDATE, FROMHOUR, FROMMINUTE, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE)
  - Site codes: 12 sites with names, geographic coordinates, and dataset date ranges (e.g., T01 Drayton, T08 Wytham, T12 Cairngorms)
  - Fieldnames: List of measured variables (ALKY, ALUMINIUM, CALCIUM, CHLORIDE, COLOUR, CONDY, DOC, IRON, MAGNESIUM, NH4N, NO3N, PH, PHAQCS, PHAQCU, PO4P, POTASSIUM, SO4S, SODIUM, TOTALN, TOTALP, VACUUM, VOLUME, Q1–Q5)
  - Units: Each fieldname has corresponding units (e.g., mg/L, µS/cm, pH, ml, bar)
  - Quality codes: Standard ECN quality codes (100–201, 222, 501–509, 511, 999) with defined meanings; 999 used for unusual events with accompanying text
  - Supporting/ancillary documentation: "ECN soil solution chemistry data: 1992-2012" with DOI; ECN_SS2.csv contains additional analytical information; accompanying quality information should be used when using data

- Data collection protocol and quality assurance
  - Sampling method: Suction samplers measure soil solution chemistry; samples collected fortnightly
  - Replicates: RID identifies replicates; new RID used when suction samplers are replaced
  - Bulk sampling: If insufficient sample from samplers, daily samples can be bulked with RID values XXS (shallow) or XXD (deep)
  - Quality control: Standard QC solution analyzed alongside field samples; QC data available with dataset and must be used
  - Documented procedures: SoilSolutionChemistryProtocol.pdf accompanying the dataset
  - Data processing: Datasets are cleaned, quality assured, and transformed before sharing; metadata includes data availability and limitations

- Data governance, access, and use
  - Publication and reuse: Acknowledge ECN data usage; provide one reprint of any publication citing the data
  - Data updating: Procedures exist to update datasets and manage data sharing limitations
  - Accessibility: Data are uploaded to relevant portals and catalogued; accompanying metadata and quality information enable discoverability and re-use
  - Documentation: Supporting documentation and QA information (ECN_SS2.csv and quality codes) accompany the data to facilitate proper interpretation

- Practical considerations for Data Stewards
  - Ensure alignment between data creators/sharers and user needs by maintaining clear metadata and documentation
  - Enforce standards for data accuracy, metadata completeness, consistent units, and reproducible quality codes
  - Manage data provenance, including RID changes, bulk sampling indicators, and QC data linkage
  - Monitor data availability, embargoes, and any potential data gaps or non-standard sampling events
  - Coordinate with multiple systems and formats across sites; preserve interoperability and provide guidance for dataset updates
  - Maintain and communicate the meaning of quality codes to support reliable data interpretation and traceability

- Key notes and limitations
  - Quality information may be extensive; review accompanying quality text for unusual events (code 999)
  - Some sites have shorter date ranges or interruptions in sampling; consult site-specific date ranges when using data
  - Large, multi-site dataset with varied sampling details requires careful handling of RID and fieldname/unit consistency
  - Additional analytical details are provided in ECN_SS2.csv; ensure integration with primary data for analyses

- Contact and acknowledgement
  - Data users should acknowledge ECN data and consider sending a reprint of publications citing the data
  - Data provenance and contributor details are documented to support appropriate stewardship and credit allocation