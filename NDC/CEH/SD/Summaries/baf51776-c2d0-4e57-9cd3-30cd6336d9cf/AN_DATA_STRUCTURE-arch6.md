# Dataset Originator

## Overview
- Originator: ECN Data Centre (Centre for Ecology and Hydrology) 
- Dataset associated with the UK Environmental Change Network (ECN) programme
- Dataset Owners/Sponsors: A consortium of UK government departments and agencies (including Defra, Natural England, Natural Resources Wales, Northern Ireland Environment Agency, Scottish Government, Scottish Environment Protection Agency, among others)
- Acknowledgement and publication: ECN requests acknowledgement of data use and a copy of one reprint of any publication citing ECN data

## Purpose and Scope
- Designed to support understanding environmental change by providing standardized, comparable NO2 diffusion-tube data across multiple ECN sites
- Facilitates data discovery, integration, and reuse for research and policy support

## Dataset Ownership and Sponsorship
- Sponsored by a broad group of government departments and agencies
- Data use should credit ECN and its funders; request for a reprint helps demonstrate dataset value

## Protocol and Quality Assurance
- Standard operating procedures (protocols) ensure data comparability across sites
- An accompanying PDF explains data collection methods
- Quality assurance measures emphasize use of accompanying quality information when using data

## Usage Notes and Data Quality
- NO2 measurement method: Passive diffusion tubes deployed for two weeks
- Quality checks: Blank tubes are included and analyzed to assess background/instrument conditions
- Always reference accompanying quality information when analyzing data

## Data Download and Format
- Main data file fields:
  - SITECODE: Unique ECN site code
  - SDATE: Sampling date
  - TUBEID: Tube identifier (E = Experimental, B = Blank)
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting documentation files:
  - ECN_AN2.csv: Sample collection details (SITECODE, TUBEID, DEPDATE, DEPHOUR, DEPMINS, SDATE, SHOUR, SMINS)
  - ECN_AN_qtext.csv: Site manager quality notes and text explanations for quality issues (linked via SITECODE and FIELDNAME)
    - Quality code 999 indicates an unusual event; associated text in ECN_AN_qtext.csv

## Site Codes and Variables
- Site codes (examples):
  - T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted
  - T07 Sourhope; T08 Wytham; T09 Alice Holt; T10 Porton Down; T11 Snowdon; T12 Cairngorms
- Variables (FIELDNAME) and related units:
  - WEIGHTNO2: Weight of NO2 on the mesh (micrograms)
  - NO2: NO2 concentration (micrograms/m3)
  - NO2PPB: NO2 concentration (ppb)
  - TDIFF: Exposure time (minutes)
  - Q1–Q8: Quality codes (integers)

## Quality Codes
- A comprehensive enumerated list of quality codes is provided, including:
  - 100: No information available - data lost
  - 101–191, 200–239, 501–513: Various data issues and context (e.g., sample loss, equipment problems, contamination, transect disturbances, measurement issues)
  - 999: Unusual event - see corresponding quality text
- The quality codes are accompanied by detailed descriptions and, where applicable, continued applicability indicators (D, R, CONTINUING, etc.)

## How to Use and Reuse
- Use SITECODE, SDATE, TUBEID, FIELDNAME, and VALUE to reconstruct measurements by site and date
- Cross-reference ECN_AN2.csv for deployment metadata and timing
- Check ECN_AN_qtext.csv for qualitative notes related to quality codes (and view full explanations for 999 cases)
- Adhere to the protocol documentation to ensure comparability with other ECN data

## Access and Acknowledgement
- Data access is complemented by supporting files and quality metadata
- Proper acknowledgment to ECN and its funders is requested for any published work
- Consider providing ECN with a reprint of publications citing the data to illustrate impact and usage