# ECN Butterfly Monitoring Dataset

- Origin and governance
  - Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk; ecn@ceh.ac.uk), Centre for Ecology and Hydrology
  - Dataset Owners: UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies
  - Acknowledgement: Users should acknowledge data usage and send one reprint of any publication citing ECN data

- Purpose and scope
  - Data derived from the national Butterfly Monitoring Scheme (BMS) to study butterfly populations and trends
  - Aimed at enabling comparisons across sites and over time to understand environmental change impacts

- Protocol and data collection
  - Standard operating procedures ensure comparability across sites (see accompanying ib.pdf)
  - Transect method: butterfly records on a transect divided into up to 15 sections
  - Survey schedule: weekly walks from 1 April to 29 September each year
  - Observation area: 5 m x 5 m x 5 m box in front of the observer
  - Recording unit: butterflies seen flying within or entering the box
  - Environmental conditions: temperature between 13–17°C if sunshine is at least 60%; recording allowed up to 17°C with conditions otherwise, subject to not raining; northern upland sites have a 15°C upper limit
  - Quality context: use accompanying quality information when using the data

- Data content and structure
  - Core dataset: ECN_IB2.csv
    - Key fields: SITECODE (site code), LCODE (location ID within site), SDATE (sampling date), SECTION (transect section ID), FIELDNAME (species code), VALUE (measured value), BROODED (brood information: S = single-brooded, D = double-brooded)
  - Supporting documentation: ECN_IB2.csv describes the survey details
  - Quality metadata: ECN_IB_qtext.csv
    - Fields: SITECODE, LCODE, FIELDNAME (species or blank for whole survey), FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION
  - Quality notes: site managers can attach text explaining circumstances affecting data quality; viewable in ECN_IB_qtext.csv
  - Metadata and codes
    - Site codes: T01–T12 with site names and precise coordinates (e.g., T01 Drayton; T12 Cairngorms)
    - Species codes: numeric codes mapped to Latin and common names (example codes shown include 10 = Black-veined white; 100 = Small white; 102 = Silver-studded blue; 106 = Common blue; 116 = Purple hairstreak; 119 = Essex skipper; 123 = Painted lady; etc. Full mapping provided in the dataset)

- Data access and documentation
  - Data files: ECN_IB2.csv and ECN_IB_qtext.csv contain core and quality information
  - Site details and species codes: provided as explanatory information accompanying the data
  - Additional information: Explanatory site and species codes are available to interpret data correctly

- Practical considerations for analysts
  - Data integration: unifying data across multiple sites and formats; ensure alignment of site codes, location IDs, and date formats
  - Data quality: rely on quality notes and metadata to assess data reliability; account for dates, conditions, and any ongoing quality issues
  - Local-scale analysis: data may be sparse at local scales; plan for scale-appropriate analyses
  - Data rights and reproducibility: track data sources, and share datasets with metadata where possible; acknowledge ECN data usage and provide reprints if applicable

- Related notes
  - The dataset is part of a broader ECN program funded by multiple UK agencies and research organizations
  - The protocol and usage notes emphasize standardized collection to support robust trend analysis and cross-site comparisons