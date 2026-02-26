# UK Environmental Change Network (http://www.ecn.ac.uk) Atmospheric Chemistry: Nitrogen Dioxide (AN) Dataset

## Overview
- NO2 concentration data collected by the UK Environmental Change Network (ECN) using passive diffusion tubes.
- Data intended to support monitoring of environmental change and assessment of policy performance over time.
- Dataset originated by the ECN Data Centre; owned and funded by a consortium of UK government departments and agencies.
- Time coverage varies by site (approximately 1993–2012) across 12 ECN sites.

## Data Collection Protocol
- Passive diffusion tubes deployed for two-week periods to measure NO2.
- Blanks are collected and not exposed on arrival; blanks analyzed alongside experimental tubes for QA.
- Quality information is essential and accompanies the dataset for proper use.
- Data and measurements are to be quality assured, cleaned, and transformed before analysis.

## Data Structure and Metadata
- Data stored in an Oracle database, with 12 site-specific tables:
  - D1AN_xxx: dataset identifiers and sample-related metadata.
  - D2AN_xxx: sample collection details (deployment and sampling timing).
- Core fields include:
  - SITECODE, SDATE, TUBEID, FIELDNAME, VALUE (for D1AN_xxx).
  - Deployment date/time (DEPDATE, DEPHOUR, DEPMIN), Sampling date/time, etc. (for D2AN_xxx).
- Field names and measurement types include:
  - WEIGHTNO2 (weight of NO2 on the mesh), NO2 (NO2 concentration in micrograms/m3), NO2PPB (NO2 concentration in ppb), TDIFF (exposure duration in minutes), and Q1–Q8 quality codes.
- Metadata documentation and accompanying quality information are required for proper data use.

## Site Coverage and Time Range
- Site codes and names:
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Y Wyddfa - Snowdon
  - T12 Cairngorms
- Each site has a specified geographic location and a dataset date range (e.g., T01: 20-Jan-1993 to 26-Dec-2012; T12: 10-Nov-1999 to 12-Dec-2012).

## Field Names, Measurements, and Quality Flags
- Primary measurements and related fields:
  - WEIGHTNO2: Weight of NO2 on the diffusion mesh (micrograms).
  - NO2: NO2 concentration (micrograms/m3).
  - NO2PPB: NO2 concentration (ppb).
  - TDIFF: Exposure time (minutes).
  - Q1–Q8: Quality codes (integer) indicating data quality aspects.
- Quality codes follow a standard ECN list with codes such as:
  - 100–105, 106–188, 189–235, 501–513, 999 (unusual event).
  - Codes cover data loss, no sample/reading, sample contamination or loss, environmental interferences (e.g., snow, leaves, insects), equipment issues, sampling in unusual conditions, laboratory issues, and other anomalies.
- 999 indicates an unusual event; a descriptive text explains the circumstances in the accompanying quality information.

## Quality Assurance and Data Quality Codes
- ECN site managers assign quality codes from a standard list to indicate factors affecting data quality.
- Multiple codes can be applied per sample; additional explanatory text is provided when codes do not cover the event.
- Detailed quality descriptions and any non-standard notes are accessible via the dataset’s quality information.

## Usage, Citation, and Data Access
- Users are asked to acknowledge the use of ECN data to help demonstrate dataset value.
- Please send one reprint of any publication citing the ECN data.
- Protocol reference and accompanying quality metadata should be consulted for proper data interpretation.
- Data are stored and accessible through ECN data portals and databases.

## Practical Implications for Analysts Monitoring the Environment
- Provides a standardised, multi-site NO2 monitoring dataset suitable for trend analysis and policy assessment.
- Enables cross-site comparisons and integration with other ECN environmental data, given consistent structure and quality flags.
- Requires applying the ECN quality codes and referencing the accompanying quality information for accurate interpretation.
- Facilitates verification against established data sources, data cleaning, and transformation prior to analysis.
- Supports long-term environmental health evaluations by leveraging site-specific temporal ranges and metadata.