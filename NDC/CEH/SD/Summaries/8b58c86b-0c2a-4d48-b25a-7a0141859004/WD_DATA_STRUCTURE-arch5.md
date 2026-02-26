# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk)

## Overview
- The dataset is provided by the UK Environmental Change Network (ECN) through its Data Centre, with sponsorship from multiple UK government departments and agencies.
- Data providers include the ECN partner organisations listed; acknowledgement of data use is requested, and authors are asked to send a reprint of any publication citing the data.

## Protocol and Standards
- ECN maintains standard operating procedures to ensure data comparability across sites.
- A accompanying document (WD.pdf) explains how data are collected to support consistent usage and interpretation.

## Usage Notes and Data Quality
- Data consist of 15-minute summaries derived from 10-second logger samplings.
- Users should rely on accompanying quality information when using the data.
- Moor House – Upper Teesdale data use an Environment Agency logger; current formats include WISKI (Hydrolog format previously used). Quality codes are provided for both stage and discharge data.

## Data Download and Structure
- Core download fields: SITECODE (site), SDATE (date), SHOUR (hour), SMINS (minute), FIELDNAME (variable), VALUE (measured value).
- Quality context is available via the ECN_WD_qtext.csv file, which site managers can attach to explain data quality issues.

## Supporting Documentation and Site Information
- ECN_WD_qtext.csv: supports quality notes with fields for site, variable, date ranges, and ongoing status.
- Site codes and locations:
  - T02 Glensaugh
  - T04 Moor House – Upper Teesdale
  - T07 Sourhope
  - T08 Wytham
  - T11 Y Wyddfa – Snowdon
- Coordinates are provided for each site; further site information is available at the ECN site catalogue.

## Variables and Coding
- STAGE: Stage Height (meters)
- DISCHARGE: Discharge (cubic meters per second)
- HYCODE_ST/HYCODE_DI: Hydrolog codes indicating data status (e.g., 0 = no problems, 3 = data suspect, 4 = data unchecked)
- WICODE_ST/WICODE_DI: WISKI quality codes (e.g., 1 = good within rating, 2 = estimated within rating)

## Governance and Stewardship Considerations
- Upload datasets to relevant portals and catalogue data holdings.
- Respect data sharing limitations and establish update mechanisms.
- Document work performed on datasets to maintain provenance and reuse clarity.

## Challenges for Data Stewards
- Incomplete picture of user needs and priorities.
- Timely receipt of data from producers and ensuring metadata completeness.
- Managing data across many systems and formats, including non-interoperable or legacy formats.
- Handling large datasets and, where applicable, outdated databases requiring bespoke solutions.