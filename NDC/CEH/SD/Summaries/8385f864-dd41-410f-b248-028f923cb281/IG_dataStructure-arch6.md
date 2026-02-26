# ECN Ground Beetles Dataset (Carabidae) Protocol and Data Download

- Origin and purpose
  - ECN Data Centre (Centre for Ecology and Hydrology) is the dataset originator.
  - The UK Environmental Change Network (ECN) sponsors dataset ownership and governance.
  - Purpose: monitor abundance of ground predators (Carabidae) using pitfall traps across ECN sites; data support environmental change research and policy relevance.

- Dataset scope and site information
  - Multi-site UK dataset with site codes T01–T12 (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms).
  - Each site has a unique SITECODE and location (latitude/longitude provided in explanatory data).
  - Additional site information available via ECN site catalogue link.

- Data collection protocol
  - Standard operating procedures to ensure data comparability across sites.
  - Monitoring method: pitfall traps to assess ground beetle (Carabidae) abundance.
  - Sampling frequency: fortnightly from May to October.
  - Use accompanying quality information when using data.

- Data download structure and fields
  - Core data fields for each observation:
    - SITECODE: Unique ECN site code.
    - LCODE: Location ID (unique within site).
    - SDATE: Sampling date.
    - TRAP: Trap number.
    - FIELDNAME: Variable measured (e.g., quality codes Q1–Q8, taxa).
    - VALUE: Measured value (numeric or coded, depending on FIELDNAME).
    - TYPE: Additional information for specific taxa (e.g., Pterostichus madidus sex and leg colour morphs).
  - Taxa representation
    - A comprehensive taxon field mapping (e.g., 6453 2714 = Pterostichus madidus; multiple genus/species codes following the ECN taxonomic scheme).
    - Includes unidentified (UU) and “no ground beetles present” (XX) indicators.
  - Quality and metadata fields
    - QUALITY codes are embedded as FIELDNAMEs (e.g., Q1–Q8) with descriptive VALUEs defined in the Quality Codes list.
    - Explanatory metadata for quality assessment (including 999 for unusual events and accompanying text where applicable).

- Supporting documentation and quality notes
  - ECN_IG2.csv: Trap deployment dates (FROMDATE, SDATE) and site/location codes.
  - ECN_IG3.csv: Habitat information per site/location (HABDESC).
  - ECN_IG_qtext.csv: Textual quality explanations associated with quality codes; '999' indicates an unusual event; linked to ECN_ig_qtext.csv in the data download.
  - Quality codes
    - A detailed list (100, 101, 102, ..., 999) describing data quality, sample handling, environmental conditions, laboratory issues, and unusual events.
    - 999 used for unusual events with accompanying descriptive text.

- Data usage, rights, and attribution
  - ECN requests acknowledgement of data use to demonstrate dataset value in research on environmental change.
  - Request that you send one reprint of any publication citing the dataset.
  - Data users should refer to accompanying documentation for data collection and quality context.

- Access and additional information
  - Site-level and site coordinate information available via ECN site catalogue (link provided in the document).
  - The dataset includes explanatory information about variable naming (FIELDNAME), site codes, and quality codes to support data discovery and integration.
  - Encouraged data usage patterns: combine core data with habitat and quality metadata to produce dashboards, reports, or self-service analyses; document data quality considerations in outputs.

- Contact
  - For dataset questions: ECN Data Centre (ecdn@ceh.ac.uk or the listed contact on the ECN data portal).

- Practical notes for data support and analytics
  - Expect patchy data across sites and time due to field conditions and quality events; use the ECN_qtext and quality codes to assess data reliability.
  - When building end-user products (dashboards, pivot tables), join by SITECODE, LCODE, and SDATE; be aware of FIELDNAME semantics (e.g., quality codes vs. taxa).
  - Use Supporting Documentation to enrich datasets with trap timing and habitat context for robust analyses of beetle assemblages and environmental drivers.