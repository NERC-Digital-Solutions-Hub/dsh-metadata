# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology.

- Overview
  - UK Environmental Change Network (ECN) dataset focused on Macrolepidoptera using standard light traps.
  - Data collected nightly across multiple sites (one moth trap per site) as part of Rothamsted Insect Survey methodology.
  - Purpose: enable understanding of environmental change effects on moth populations; data should be acknowledged and citations sent as reprints.

- Dataset ownership and sponsorship
  - Sponsored by a consortium of UK government departments and agencies (e.g., Defra, Environment Agency, Natural England, NERC councils, Scottish and Welsh authorities).
  - Site management and funding support site monitoring and network coordination.

- Data collection and scope
  - Protocol: standardized light-trap method for Macrolepidoptera; nightly recordings.
  - Period: data spanning e.g., 1992–2012 across sites; single moth trap per site (LCODE always 1).
  - Supplemental quality information accompanies the data to aid interpretation and usage.

- Data structure (Table 1)
  - SITECODE: site code (e.g., T01, T02, …)
  - LCODE: location code (1 for all sites in this dataset, as there is one trap per site)
  - SDATE: sampling date (dd-mmm-yyyy)
  - FIELDNAME: either a quality code (denoting data quality) or a species code
  - VALUE: if FIELDNAME is a quality code, contains the detailed quality code; if FIELDNAME is a species code, indicates the observed count of individuals

- Site information (Site codes and details)
  - T01 to T12 included (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Cairngorms)
  - Each site includes coordinates and date range entries (e.g., 02-Jan-1993 to 26-Dec-2012 for Drayton)
  - Additional site information available at the ECN catalogue link

- Taxonomic and coding framework
  - Table 3a: Quality codes (Q1–Q8) referenced in data fields
  - Table 3b: Species codes mapping to:
    - Latin names and common names for numerous moth taxa
    - Extensive numeric codes (e.g., 100 for Furcula bicuspis, Alder Kitten; 2178 for Plutella xylostella, Diamond back moth; etc.)
  - Table 4: Comprehensive quality code definitions (e.g., data loss, sampling issues, debris in sample, environmental disturbances)

- Quality, metadata, and usage notes
  - ECN site managers assign standardized quality codes to reflect data quality and sampling conditions
  - Codes cover data loss, incomplete samples, debris, weather impacts, and other disturbances
  - 999 code indicates an unusual event requiring accompanying qualitative text
  - Importance of using accompanying quality information (ECN_IM2.csv and ECN_IM_qtext.csv)

- Supplemental information
  - ECN_IM2.csv: indicates trap open period (number of days traps were set)
  - ECN_IM_qtext.csv: textual notes describing additional quality context for observations (absence explanations, inconsistencies)

- How to use and attribution
  - Acknowledge ECN data usage and provide a reprint of any publication citing the dataset
  - Recognize data collection methodology as Rothamsted Insect Survey standard protocol
  - Use quality codes and supplemental files to interpret presence/absence and counts accurately

- Key considerations for Data Leaders
  - System-level view: understand data flow from collection to metadata enrichment (quality codes, supplemental files)
  - Data discoverability: standardized site codes, coordinates, and date ranges across sites
  - Data quality and standardization: reliance on ECN quality codes; need to integrate supplemental quality information for robust analyses
  - Data access and interoperability: large, coded taxonomy dataset with extensive metadata; plan for cross-network reuse and integration
  - Collaboration and governance: dataset owned by ECN with broad government sponsorship; acknowledge and engage with data providers when utilizing findings

- Contact and provenance
  - Originator: ECN Data Centre, Centre for Ecology and Hydrology
  - Data governance and usage guidance provided by ECN and sponsoring UK government bodies
  - Additional site information and dataset context available via ECN catalogue link provided in the metadata