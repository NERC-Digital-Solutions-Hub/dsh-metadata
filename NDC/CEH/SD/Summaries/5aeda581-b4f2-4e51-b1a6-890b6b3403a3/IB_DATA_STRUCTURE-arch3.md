# ECN Butterfly Monitoring Dataset

## Overview
- Provides butterfly monitoring data collected under the UK Environmental Change Network (ECN) Programme.
- Data are gathered across multiple ECN sites and are intended to support understanding environmental change impacts on butterfly populations.
- Data are governed and shared under ECN protocols, with expectations for attribution and data sharing.

## Originators and Owners
- Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk; ecn@ceh.ac.uk), Centre for Ecology and Hydrology.
- Dataset Owners: Network sponsored by a consortium of UK government departments and agencies including Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, DEFRA, Environment Agency, Natural England, NERC, Scottish Government, and others.
- ECN requests acknowledgment of data use and requests one reprint of any publication citing the data.

## Protocol and Data Collection
- ECN maintains standard operating procedures to ensure cross-site data comparability; refer to accompanying ib.pdf for collection details.
- Butterfly Monitoring Notes:
  - Transect divided into up to 15 sections; transects walked weekly.
  - Observation window: 1 April to 29 September each year.
  - Observers record butterflies within an imaginary 5m x 5m x 5m box in front of the observer.
  - Temperature constraints: 13–17°C with at least 60% sunshine; recording possible above 17°C under suitable conditions; northern upland sites capped at 15°C.
  - Use accompanying quality information when using the data.

## Data Structure and Fields
- Data Download Fields (ECN_IB2.csv):
  - SITECODE: Unique code for each ECN site.
  - LCODE: Location ID (unique within site).
  - SDATE: Sampling date.
  - SECTION: Transect section ID.
  - FIELDNAME: Species code.
  - VALUE: Measured variable value.
  - BROODED: Number of broods (S=single-brooded, D=double-brooded).
- Supporting Documentation (ECN_IB2.csv):
  - Adds site-level and sampling metadata (SITECODE, LCODE, SDATE, etc.).
- Supporting Documentation (ECN_IB_qtext.csv):
  - Quality text notes from site managers explaining circumstances affecting data quality.
  - Fields include SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.

## Site and Species Metadata
- Site Codes (Explanatory Information):
  - T01 to T12 with site names and precise geographic coordinates (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms).
- Species Codes (Explanatory Information):
  - Numeric codes map to Latin and common names for butterfly species (e.g., 10 = Black-veined white; 100 = Small white; 106 = Common blue; 29 = Small heath; 90 = Swallowtail; 54 = Brimstone; etc.).
  - The mapping covers a broad range of UK butterfly species with both scientific and common names.

## Usage, Attribution, and Publication Sharing
- Data usage should acknowledge ECN data origin.
- ECN requests a reprint of any publication citing ECN data.
- Data sharing considerations are explicitly addressed; underlying data should be shared where appropriate, but may be subject to governance and metadata barriers.

## Data Quality, Metadata, and Governance
- Data quality depends on site-reported quality notes and standardized procedures to ensure comparability.
- Metadata gaps can hinder verification and reuse; ECN provides structured metadata fields and quality information to facilitate assessment.
- Governance includes adherence to standard operating procedures, data cleaning, transformation, analysis, and clear presentation in outputs (reports, charts, dashboards), with data governance processes for storage, sharing, and updates.

## Relevance for Monitoring Framework Authors
- Demonstrates a structured approach to designing environmental health monitoring data, including:
  - Clear provenance and governance (originators, owners, and usage expectations).
  - Standardized protocols for cross-site comparability.
  - Defined data schema with precise field meanings and data types.
  - Rich metadata and quality annotations to support data quality assessment.
  - Transparent site and species metadata to facilitate cross-study integration.
  - Incentives and requirements for data sharing and publication attribution.

## Notable Considerations and Barriers Highlighted
- Potential barriers common to monitoring frameworks:
  - Data gaps and data quality issues at certain sites.
  - Access delays or restrictions to datasets.
  - Organizational silos hindering data sharing.
  - Requirement to publicly share datasets and accompanying metadata.
  - Maintaining up-to-date datasets and comprehensive metadata.
  - Transforming data formats for interoperability.
  - Communicating complex findings clearly to stakeholders.
  - Establishing and maintaining robust data governance and data management standards.