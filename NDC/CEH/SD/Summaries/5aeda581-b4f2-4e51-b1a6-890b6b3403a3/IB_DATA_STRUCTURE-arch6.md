# Dataset Originator

## Overview
- Source: ECN Data Centre, Centre for Ecology and Hydrology (dataset originator). 
- Owners: UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies.
- Purpose: Environmental change research data provision; acknowledgement requested for uses and a reprint of publications citing the data.

## Governance and Attribution
- Dataset governance: ECN recommends acknowledgement of data use; request for one reprint of any publication citing the data.
- Data access: Data are provided with accompanying documentation to ensure understanding of collection methods and data quality.

## Protocol and Data Quality
- Standardisation: ECN uses standard operating procedures to ensure site-to-site comparability (see accompanying ib.pdf for collection methodology).
- Quality assurance: Data quality information is attached in supporting documentation (ECN_IB_qtext.csv); site managers can add notes explaining data quality issues or circumstances affecting data.
- Scope of methodology: Butterfly Monitoring Scheme implemented across sites; transects divided into up to 15 sections; weekly transect walks from 1 April to 29 September.

## Data Collection and Usage Notes
- Transect method: Butterflies recorded within a 5m x 5m x 5m imaginary box along transect; sightings are recorded when butterflies fly within or pass through the box.
- Conditions: Recording temperature guidelines (13–17°C with certain sunshine requirements; higher temperatures allowed if not raining; northern upland sites capped at 15°C); transect pace should be even.
- Data handling: Use accompanying quality information when using the data.

## Data Files and Structure
- Main data file fields (ECN_IB.csv):
  - SITECODE: Unique ECN site code
  - LCODE: Location ID (unique within site)
  - SDATE: Date of data recording
  - SECTION: Transect section ID
  - FIELDNAME: Species code
  - VALUE: Measured value
  - BROODED: Brood information (S = single-brooded, D = double-brooded)
- Supporting documentation (ECN_IB2.csv):
  - SITECODE, LCODE, SDATE, SHOUR, SMINS, RECORDER, RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK
- Quality notes (ECN_IB_qtext.csv):
  - SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION
  - Allows site managers to attach context that may affect data quality.
- Site codes (Explanatory Information: Site Codes):
  - T01–T12 with site names (e.g., Drayton, Glensaugh, Hillsborough, etc.) and precise coordinates.
- Species codes (Explanatory Information: Species codes):
  - Numeric codes mapped to Latin and common names (e.g., 10 = Black-veined white, 100 = Small white, 102 = Silver-studded blue, etc.; XX = No butterflies present).
  - The list provides a comprehensive mapping for all recorded species.

## Access and Further Information
- ECN site catalogue: https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27
- Additional details: Full species and site code mappings included in the accompanying documentation.

## How Data Support Professionals Can Help
- Data integration: Combine ECN butterfly data with other environmental datasets using SITECODE, SDATE, and SECTION to align spatial-temporal contexts.
- Data quality management: Leverage ECN_IB_qtext.csv quality notes to annotate or filter records with quality concerns.
- End-user self-service: Prepare dashboards or pivot tables using main fields (SITE, date, section, species code, counts) and provide guidance on interpreting brood status (BROODED).
- Data documentation: Ensure attribution in reports/publications; include references to ECN data and the accompanying protocol (ib.pdf) and quality notes.
- Data re-use and impact tracking: Acknowledge use and, where possible, request reprints to demonstrate data impact.