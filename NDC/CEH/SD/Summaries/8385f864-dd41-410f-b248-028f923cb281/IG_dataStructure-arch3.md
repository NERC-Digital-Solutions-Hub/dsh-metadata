# ECN Ground Beetles Dataset Documentation

- Purpose and scope
  - Designed to monitor the abundance of ground predators (Carabidae) using pitfall traps.
  - Data are collected fortnightly from May to October.
  - Protocol emphasizes the use of accompanying quality information to ensure appropriate data use.

- Dataset origin and ownership
  - Originator: ECN Data Centre (Centre for Ecology and Hydrology) - dataset hosting and dissemination.
  - Owners: The UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies.
  - Sponsoring organisations include: AFI, BBSRC, NRW, DSTL, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, and SNH.
  - Data use acknowledgement: ECN requests acknowledgment of data use and one reprint of any publication citing ECN data.

- Protocol and data collection
  - Standard operating procedures to ensure cross-site data comparability.
  - Sampling method: pitfall traps used to monitor ground beetles (Carabidae).
  - Sampling cadence: fortnightly visits during May–October.
  - Use of quality information (metadata) to accompany data usage.

- Data structure and fields (main dataset download)
  - Key fields in the ECN data download:
    - SITECODE: Unique ECN site code.
    - LCODE: Location ID (unique within site).
    - SDATE: Sampling date.
    - TRAP: Trap number.
    - FIELDNAME: Variable measured (e.g., quality codes, species/genera information).
    - VALUE: Value of the measured variable.
    - TYPE: Additional species-level information for Pterostichus madidus (e.g., gender, leg color morphs; codes M/F/R/B for sex and morphs).
  - Purpose of FIELDNAME values includes quality codes and taxonomic descriptors (e.g., species or genus labels across many taxa).

- Supporting documentation and data supplements
  - ECN_IG2.csv: Trap deployment/t timing information.
    - Fields: SITECODE, LCODE, FROMDATE (trap set-out), SDATE (trap collection).
  - ECN_IG3.csv: Habitat information.
    - Fields: SITECODE, LCODE, HABDESC (habitat description).
  - ECN_ig_qtext.csv: Quality text for data quality issues.
    - Includes FIELDNAME, quality codes, and TEXT explanations for non-standard or unusual circumstances (linked to quality code 999 in data).
  - Explanatory information and site codes
    - Site codes (e.g., T01–T12) with site names and precise coordinates.
    - Provides context for site locations and allows spatial interpretation of data.
  - Explanatory information: Field names
    - FIELDNAME mappings include quality codes (Q1–Q8 and related ranks for species) and extensive taxon-specific descriptors (e.g., 6453 100 = Cicindela, etc., covering numerous genera and species across Carabidae and related taxa).
  - Explanatory information: Quality codes
    - A comprehensive list of quality codes (e.g., 100 = No information available, 101 = No sample taken, 999 = Unusual event) with descriptions to support data quality assessment and filtering.

- Site codes and locations
  - 12 ECN sites with names and coordinates (e.g., Drayton, Glensaugh, Hillsborough, Moor House – Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms).
  - Each site has a unique SITECODE and LCODE, enabling site-level tracking and cross-site comparisons.

- Taxa and field-name details
  - The dataset includes a detailed, extensive mapping of field names to taxonomic groups, including genus and species-level entries for numerous ground beetle taxa.
  - The FIELDNAME entries align with taxonomic codes (e.g., 6453 2714 = Pterostichus madidus; 6453 2713 = Pterostichus macer; etc.), enabling species- and genus-level analysis across a broad beetle assemblage.

- Data governance, accessibility, and challenges
  - Data governance focus areas include data quality assurance, metadata completeness, data cleaning, transformation, and clear presentation of findings (reports, charts, dashboards).
  - Common challenges for monitoring frameworks highlighted in the aims:
    - Access to data and data availability, including timely access.
    - Data silos within and between organizations hindering integration.
    - Barriers to publicly sharing underlying datasets.
    - Keeping metadata up to date and ensuring datasets meet standards.
    - Metadata inadequacy and data format needing transformation to be usable.
    - Communicating complex results clearly.
    - Establishing and maintaining data governance processes for storage, sharing, and up-to-date datasets.

- Usage considerations for monitoring frameworks
  - Emphasizes the importance of standardized protocols for cross-site comparability.
  - Highlights the need for accompanying metadata (quality, habitat, deployment timing) to enable robust use in policy evaluation and decision-making.
  - Demonstrates how a large, government-supported monitoring program can structure data flow from collection (field) to dissemination (downloadable datasets and supporting docs) and to governance (quality codes, site metadata, and acknowledgments).

- Practical takeaways for policy and management
  - When designing environmental health monitoring, ensure:
    - Clear protocols and standardization across sites.
    - Comprehensive metadata and quality codes to assess data reliability.
    - Public data-sharing policies balanced with site-specific concerns.
    - Mechanisms to capture habitat and deployment context to support interpretation.
    - Governance structures for data storage, curation, and accessibility.
  - Facilitate stakeholder and expert engagement to define useful measures and avoid data duplication.
  - Plan for data gaps and data gaps remediation through targeted data collection and transparent data quality reporting.