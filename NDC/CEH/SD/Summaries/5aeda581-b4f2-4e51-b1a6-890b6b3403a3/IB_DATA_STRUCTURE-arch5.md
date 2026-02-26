# ECN Butterfly Monitoring Dataset

## Overview
- The dataset is part of the UK Environmental Change Network (ECN) and is managed by the ECN Data Centre at the Centre for Ecology and Hydrology.
- Dataset owners are a consortium of UK government departments/agencies funding soil monitoring and network coordination.
- Purpose: support research into environmental change by providing standardized, comparable butterfly monitoring data across multiple sites, with metadata and quality information.
- Key components:
  - Primary data file structure (ECN_IB2.csv) with site, location, date, transect section, species code, and measurement value.
  - Supporting documentation (ECN_IB2.csv metadata, ECN_IB_qtext.csv for quality notes).
  - Site codes (T01–T12) with names and precise coordinates.
  - Species code mappings (numerical codes to Latin and common names), including a code for no butterflies present.
- Data usage and acknowledgment: ECN requests acknowledgment of data use and one reprint of any publication citing the data.

## Protocol and Data Governance
- ECN provides standard operating procedures (protocols) to ensure data comparability across sites (refer to accompanying ib.pdf).
- Site managers and data creators are involved in data collection, quality assessment, and metadata annotation.
- Data sharing and updates are governed by established procedures; data are uploaded to relevant portals and catalogued.
- Publication and attribution: users should acknowledge ECN data use and share a reprint with ECN.

## Data Structure and Metadata

- ECN_IB2.csv (primary data)
  - SITECODE: Unique ECN site code
  - LCODE: Location ID within site
  - SDATE: Date of data recording
  - SECTION: Transect section ID (up to 15 sections)
  - FIELDNAME: Species code (see species codes)
  - VALUE: Measured value (butterfly count/presence)
  - BROODED: Breeding status (S = single-brooded, D = double-brooded)

- ECN_IB_qtext.csv (quality context)
  - SITECODE, LCODE: Site and location identifiers
  - FIELDNAME: Species affected (blank if whole survey)
  - FROM_DATE, TO_DATE: Time window for the quality issue
  - DATETYPE: Length of time the issue applies (D for day, R for range)
  - CONTINUING: Is issue ongoing? (Y/N)
  - DESCRIPTION: Text description of data quality issue

- Supporting documentation fields
  - ECN site managers can attach site-specific quality text to explain circumstances affecting data quality.

- Explanatory information: Site Codes
  - T01–T12 with site names (e.g., Drayton, Glensaugh, Hillsborough, etc.) and precise coordinates.

- Explanatory information: Species codes
  - Numeric codes map to Latin and common names for numerous butterfly species (e.g., 2 = Aglais urticae / Small tortoiseshell; 10 = Aporia crataegi / Black-veined white; 40 = Danaus plexippus / Monarch; 90 = Papilio machaon / Swallowtail; XX = no butterflies present). A comprehensive mapping covers many species.

## Data Quality and Usage Guidance
- Use of accompanying quality information (ECN_IB_qtext.csv) is recommended to interpret potential data quality issues.
- Protocols ensure comparability across sites, with standardized sampling (weekly transects April 1 to September 29; 5m x 5m observation box; temperature/sunlight conditions guidance).
- Quality notes allow site managers to document circumstances that may affect data, such as weather, observer, or site-specific events.

## Availability, Access, and Updates
- Data are organized for download via structured fields (SITECODE, LCODE, SDATE, SECTION, FIELDNAME, VALUE, BROODED, etc.).
- Supporting documentation files (ECN_IB2.csv, ECN_IB_qtext.csv) accompany the dataset to aid interpretation and quality assessment.
- ECN uploads datasets to relevant portals; updates are managed through the established data governance processes.

## Practical Considerations for Data Stewards
- Engage with data creators to ensure timely data submission and adherence to metadata standards (site codes, species codes, date formats).
- Maintain interoperability across systems and formats by adhering to ECN’s standard procedures and documentation.
- Track data usage and impact via acknowledgments and reprints to demonstrate dataset value.

## Challenges (as relevant to Data Stewards)
- Incomplete understanding of user needs and priorities.
- Timeliness of data from creators.
- Ensuring metadata completeness and standardization across many sites.
- Handling large, potentially non-interoperable datasets from diverse systems.
- Managing updates and quality issues across multiple sites and years.

## Contact and Further Information
- Dataset originator: ECN Data Centre, Centre for Ecology and Hydrology (website and contact in dataset)
- Acknowledgment and data-use inquiries should be directed to ECN with a request to receive a reprint of any publication citing the data.