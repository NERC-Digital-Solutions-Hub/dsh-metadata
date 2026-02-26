# ECN Butterfly Monitoring Dataset

- Overview
  - Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (http://data.ecn.ac.uk)
  - Dataset Owners: UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies (e.g., DEFRA, Natural England, NERC, Scottish Government, Welsh Government, etc.)
  - Purpose: Long-term data collection to understand environmental change; standard protocols to enable comparability across sites; data intended for research and policy-relevant analysis.
  - Acknowledgement: Users must acknowledge data use and provide a reprint of any publication citing ECN data.

- Data governance and standards
  - Protocol and comparability: ECN maintains standard operating procedures to ensure data are comparable across sites; ib.pdf explains data collection.
  - Quality and metadata: Data usage relies on accompanying quality information; site managers can attach text about conditions affecting data quality (ECN_IB_qtext.csv).
  - Metadata structure: Data are organized with site, location, sampling date/time, weather, and species information to support traceability and reuse.
  - Data access and provenance: Data are maintained by ECN with defined site coordinates and documented methodologies; site and species codes enable consistent referencing.

- Data structure and content
  - Main dataset fields (Data Download): SITECODE (ECN Site code), LCODE (Location ID within site), SDATE (Date of data recording), SECTION (Transect section), FIELDNAME (Species code), VALUE (Measured value), BROODED (Number of broods; S = single-brooded, D = double-brooded).
  - Methodology (Usage Notes): Butterfly monitoring follows the national Butterfly Monitoring Scheme; transect walked weekly from 1 April to 29 September; observer records butterflies within a 5m x 5m x 5m box; recording conditions depend on temperature and sunshine; standardized quality information should be used.
  - Supporting documentation (ECN_IB2.csv): Additional survey information including SITECODE, LCODE, SDATE, SHOUR, SMINS, RECORDER, RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK.
  - Quality metadata (ECN_IB_qtext.csv): Textual notes describing data quality issues; fields include SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
  - Site codes (Explanatory Information: Site Codes): 12 ECN sites (T01–T12) with site names and precise coordinates (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms); links to broader ECN site catalog.
  - Species codes (Explanatory information: Species codes): Comprehensive mapping of numeric codes to Latin and common butterfly names (e.g., 10 = Black-veined white, 100 = Small white, 102 = Silver-studded blue, etc.); includes numerous codes and a placeholder XX for “No butterflies present.”

- Data quality, standards, and reuse
  - Quality information: Users are advised to consult accompanying quality notes to assess data suitability for analysis.
  - Data freshness and updates: Data are collected over multiple sites with standardized transects and periodic updates; site-level quality notes may change over time (as indicated in ECN_IB_qtext.csv).

- Site and species codes for governance and integration
  - Site codes link each data record to a physical ECN site and location, enabling geo-spatial integration and cross-site analyses.
  - Species codes enable consistent cross-site species-level analyses and replication of studies across the ECN network.

- Practical considerations for Data Leaders
  - Whole-system view: Data are designed to support cross-site comparisons and long-term environmental monitoring, aligning with a broad data strategy.
  - User needs and co-ownership: Documentation and quality notes help ensure data meet the needs of policy colleagues and researchers; clear attribution supports collaboration and network-wide data reuse.
  - Discoverability and standards: Standardized codes, documented protocols, and supporting CSVs enhance discoverability, interoperability, and data quality assessment.
  - Data access barriers: While data are accessible via ECN channels, potential barriers can include site-specific constraints and the need to consult quality metadata for rigorous analyses.

- Contact and provenance
  - Primary contact: ECN Data Centre (ECN@ceh.ac.uk)
  - Explanatory resources: Protocol document (ib.pdf) and the accompanying CSV files for data structure and quality metadata
  - Further information: ECN site catalog and related resources available through the ECN and CEH catalog portals

- Summary of key components
  - Main dataset: ECN butterfly observations with site, location, date, transect section, species code, observed value, and brood information.
  - Supporting datasets: ECN_IB2.csv (sampling details and environmental context), ECN_IB_qtext.csv (quality notes).
  - Lookup tables: Site codes (T01–T12) with coordinates; species codes mapping to Latin and common names.