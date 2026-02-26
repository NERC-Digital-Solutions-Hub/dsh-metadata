# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- The ECN data are provided by the UK Environmental Change Network program, funded by a consortium of UK government departments and agencies.
- Data providers include multiple government and public land/environment bodies.
- Users should acknowledge the data sources and send one reprint of any publication citing ECN data.

## Dataset scope and content
- Data are 15-minute summaries derived from 10-second samplings collected by a logger.
- Primary variables: STAGE (Stage Height, meters) and DISCHARGE (Discharge, cumecs).
- Quality indicators accompany measurements:
  - HYCODE_ST and HYCODE_DI (hydrologic status codes for stage and discharge)
  - WICODE_ST and WICODE_DI (WISKI data quality codes for stage and discharge)
- Site coverage includes multiple ECN sites with unique SITECODEs (e.g., T02 Glensaugh, T04 Moor House - Upper Teesdale, T07 Sourhope, T08 Wytham, T11 Snowdon) and associated geographic coordinates.

## Data structure and access
- Data download fields:
  - SITECODE (site code)
  - SDATE (date of data recording)
  - SHOUR (hour of data recording)
  - SMINS (minute of data recording)
  - FIELDNAME (variable measured)
  - VALUE (measured value)
- Supporting documentation:
  - ECN_WD_qtext.csv: site managers’ quality notes for data quality issues, linked by SITECODE and FIELDNAME; includes date ranges, duration type, ongoing status, and descriptions.
- Explanatory information:
  - Site codes with names and precise coordinates.
  - Variable definitions and units:
    - STAGE: Stage Height (m)
    - DISCHARGE: Discharge (cumecs)
    - HYCODE_ST/DI and WICODE_ST/DI: definitions and coding for data quality and reliability.

## Protocols and standards
- Standard operating procedures ensure data comparability across sites; WD.pdf describes data collection methods.
- Moor House data include Environment Agency loggers using WISKI format (Hydrolog format used prior to 2004); both contain quality information.
- Emphasis on metadata, quality codes, and accompanying documentation to support data usability and traceability.

## Usage, attribution, and dissemination
- Users are asked to acknowledge ECN data usage and to provide one reprint of publications citing the data.
- Usage notes emphasize the importance of using accompanying quality information when analyzing the data.

## Site and variable details
- Site codes and locations:
  - T02: Glensaugh (56° 54' 33.36" N, 2° 33' 12.14" W)
  - T04: Moor House - Upper Teesdale (54° 41' 42.15" N, 2° 23' 16.26" W)
  - T07: Sourhope (55° 29' 23.47" N, 2° 12' 43.32" W)
  - T08: Wytham (51° 46' 52.86" N, 1° 20' 9.81" W)
  - T11: Snowdon (53° 4' 28.38" N, 4° 2' 0.64" W)
- Variables and units:
  - STAGE: Stage Height (m)
  - DISCHARGE: Discharge (cumecs)
  - Quality codes: HYCODE_ST, HYCODE_DI; WICODE_ST, WICODE_DI with specified meanings (e.g., 0 = no problems; 3 = data suspect; 4 = data unchecked; 1/2 = good/estimated within rating)

## Governance and organizational context for Data Leaders
- Clear data provenance and attribution requirements support accountability and demonstration of data value.
- Metadata, site-specific quality notes, and standardized formats enable discoverability, comparability, and reuse across networks.
- Documentation and protocols facilitate ongoing data quality assessment and facilitate collaboration across sites and partners.
- The dataset exemplifies coordinating across multiple providers and maintaining cross-site data integrity through standardized procedures and quality metadata.