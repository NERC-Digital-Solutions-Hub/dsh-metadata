# UK Environmental Change Network (http://www.ecn.ac.uk) Ground Predators (IG)

- Purpose and scope
  - Monitoring the abundance of ground predators (Carabidae) using pitfall traps to understand environmental change impacts.
  - Data collected fortnightly from May to October; part of the UK Environmental Change Network (ECN) ground predator protocol.
  - Data are structured to support assessment of environmental health, assist policy scrutiny, and inform future decisions.

- Provenance and governance
  - Dataset Originator: ECN Data Centre.
  - Dataset Owners: The UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies (list includes Defra, Natural England, Environment Agency, NERC, Scottish Government, Welsh Government, Northern Ireland Environment Agency, among others).
  - Usage and acknowledgement: ECN asks users to acknowledge data use and to send one reprint of any publication citing ECN data.
  - Metadata and data sharing: Accompanying quality information should be used; data sharing and metadata provisioning are emphasized as essential, with governance processes in place to ensure standards and up-to-date storage.

- Protocol and data collection
  - Protocol purpose: Monitor abundance of ground predators (Carabidae) via pitfall traps.
  - Data collection: Fortnightly sampling from May–October.
  - Reference: Protocol available at ECN measurements page.

- Data structure and content
  - Core data domains (in Oracle database):
    - D1IG_xxx: Site data tables (one per site; 12 sites total). Key fields include SITECODE, LCODE, etc.
    - D2IG_xxx: Trapping date information (when traps were set out).
    - D3IG_xxx: Habitat information (site-specific habitat descriptions).
  - Metadata and data structure notes: Core metadata tables are described separately in the metadata documentation.

- Site codes and site details
  - T01 to T12 represent 12 ECN ground predator sites, with:
    - Site names (e.g., Drayton, Glensaugh, Hillsborough, Moor House – Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa - Snowdon, Cairngorms)
    - Precise location coordinates (latitude/longitude) for each site
    - Date range of data available in the dataset (ranging from early 1990s to around 2012 for different sites)

- Field definitions and data coding
  - Fieldname (Q1–Q8): Each field holds either a species code or a quality code (integer). Quality codes are used to annotate data quality factors for each field.
  - Quality framework: ECN standard quality codes used to flag data quality issues, with an optional accompanying quality text for unusual events (code 999).
  - Species and taxonomic coding: A comprehensive coding system maps genus and species (and higher taxa) to numeric codes (e.g., Cicindela, Cicindela campestris, various genera and species across ground beetle taxa). The dataset includes extensive taxonomic codings covering multiple genera and species, enabling detailed biodiversity analysis.
  - Quality codes list: Examples include 100 (No information available), 101 (No sample/reading taken), 104 (Sample frozen), 999 (Unusual event) among a broader set of codes capturing sampling and processing conditions, environmental interferences, and lab-related issues.

- Data quality and metadata considerations
  - Metadata: Core metadata tables and accompanying metadata documentation govern data interpretation, with emphasis on site metadata (locations, date ranges) and trap deployment details.
  - Data transformation and governance: Data may require transformation for usability; provenance, validation, cleaning, and reporting are part of the data processing workflow to ensure transparency and quality.

- Usage notes and access requirements
  - Acknowledgement: Users are requested to acknowledge ECN data usage.
  - Publication sharing: A reprint of any publication citing ECN data should be provided to ECN.
  - Data sharing and quality information: Outputs should accompany quality information and adhere to data governance standards to ensure datasets meet required standards and remain up-to-date.