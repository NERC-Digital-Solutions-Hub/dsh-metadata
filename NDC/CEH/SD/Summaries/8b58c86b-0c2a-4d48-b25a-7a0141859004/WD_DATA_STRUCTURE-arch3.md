# ECN Data Centre Dataset Description

- Purpose and use for monitoring frameworks
  - Provides environmental hydrology data for understanding environmental change: 15-minute summaries of hydrological measurements across multiple ECN sites.
  - Key measures include Stage Height (STAGE, meters) and Discharge (DISCHARGE, cubic meters per second).
  - Aims to support scrutiny and evaluation of policy, with standardised data to enable comparable analyses across sites.
  - Data quality and metadata accompany the dataset to aid interpretation and clear presentation of findings (reports, charts, dashboards).

- Data provenance and scope
  - Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Data Providers: UK government departments and agencies supporting ECN through funding and coordination (e.g., Defra, Environment Agency, Natural England, natural resources agencies, research councils, and devolved administrations).
  - Protocols: Standard Operating Procedures to ensure cross-site comparability; accompanying WD.pdf explains data collection methods.
  - Usage notes:
    - Data are 15-minute summaries from 10-second samplings collected by loggers.
    - Users should apply accompanying quality information when analysing the data.
    - Moor House - Upper Teesdale site uses an Environment Agency logger with WISKI format (Hydrolog format used prior to 2004); both carry quality codes.
  - Data download schema:
    - SITECODE (site identifier), SDATE (date), SHOUR (hour), SMINS (minute), FIELDNAME (variable), VALUE (measured value).
  - Supporting documentation:
    - ECN_WD_qtext.csv captures site-specific quality notes; fields include SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
  - Explanatory information: Site codes and locations
    - T02 Glensaugh
    - T04 Moor House - Upper Teesdale
    - T07 Sourhope
    - T08 Wytham
    - T11 Snowdon (Y Wyddfa)
    - Each site includes precise coordinates.
  - Variables explained:
    - STAGE: Stage Height (m)
    - DISCHARGE: Discharge (cumecs)
    - HYCODE_ST/DI: Hydrolog codes for stage and discharge (data quality flags such as 0 = no problems, 3 = data suspect, 4 = data unchecked)
    - WICODE_ST/DI: WISKI quality codes for stage and discharge (e.g., 1 = good, within rating; 2 = estimated, within rating)

- Data access, documentation, and governance
  - Data use acknowledgment: ECN requests acknowledgment of data usage and one reprint of any publication citing ECN data.
  - Data sharing: Data are intended to be shared with appropriate quality context; metadata and quality notes are provided to facilitate reuse.
  - Governance: Data quality indicators and explicit metadata support transparent verification and reuse; standardised formats and documentation help maintain data standards across the network.

- Relevance to monitoring framework challenges
  - Addresses data gaps and standards through multi-agency collaboration, SOPs, and metadata to enable reliable cross-site monitoring.
  - Mitigates access and interoperability barriers with defined data fields, quality indicators, and supporting QC documentation.
  - Supports clear communication of findings via standardized variables, site metadata, and quality codes, while acknowledging that data sharing and evolving metadata can still present barriers.