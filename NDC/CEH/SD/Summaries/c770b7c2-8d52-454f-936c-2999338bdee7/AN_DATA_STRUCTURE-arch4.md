# UK Environmental Change Network (http://www.ecn.ac.uk) Atmospheric Chemistry: Nitrogen Dioxide (AN)

## Overview
- Describes the ECN dataset for NO2 measured with passive diffusion tubes, deployed for two weeks per sample. Includes experimental and blank tubes; blank tubes are not exposed on arrival and are refrigerated and analyzed with experimental tubes as a quality check.
- Data cover 12 ECN sites in the UK, with measurements spanning approximately 1993–2012.
- Users should consult accompanying quality information; unusual events are captured with quality code 999 and described in dataset text.

## Data assets and structure
- Data stored in 12 site-specific tables in an Oracle database, named D1AN_xxx (core data) and D2AN_xxx (sample collection metadata), where xxx is the site code.
- Core data fields (example structure): SITECODE, SDATE (sampling date), TUBEID (E = Experimental, B = Blank), FIELDNAME, VALUE; with related reference tables (e.g., M_DESC, M_REFFIELD).
- Core measurement fields include WEIGHTNO2 (weight of NO2 on the mesh), NO2 (NO2 concentration in micrograms/m3), NO2PPB (NO2 in ppb), TDIFF (exposure time in minutes), and Q1–Q8 quality codes.
- Metadata fields describe sample deployment dates/times (DEPDATE, DEPHOUR, SDATE, SHOUR, SMINS) for the D2AN_xxx tables.
- The core metadata documentation should be consulted for full table structures; quality codes and their meanings accompany the data.

## Sites and coverage
- Twelve ECN sites with names, coordinates, and date ranges:
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
- Each site has a documented date range within the dataset (1993–2012 for many sites), and site-specific location coordinates are provided.

## Data collection and quality controls
- Measurement protocol: passive diffusion tubes deployed for two weeks to measure NO2 concentration.
- Quality controls: blank tubes accompany experimental tubes; blanks are not exposed on arrival and are stored refrigerated and analyzed with experimental tubes.
- Quality information: data users should apply the accompanying quality information; quality codes capture a wide range of potential data issues or events.

## Metadata and quality codes
- Quality is assigned by ECN site managers from a standard list of ECN quality codes; multiple codes may apply. If an unusual event is not covered by codes, code 999 is used with accompanying text.
- Standard ECN quality codes cover issues such as no information, no sample/readings, sample losses, contamination, measurement issues, environmental interferences, and other field/lab problems (e.g., codes 100–507 and 999 for unusual events).
- The dataset includes fields Q1–Q8 to store up to eight quality code indicators per observation; additional textual quality information is available in the accompanying quality documentation.

## Usage and attribution
- ECN requests acknowledgement of data use and asks researchers to send one reprint of any publication that cites the dataset.
- Protocol reference and data stewardship details are provided for proper usage and citation.
- Data originates from ECN with ongoing sponsorship from a consortium of UK government departments and agencies.

## Access and references
- Protocol Reference: http://www.ecn.ac.uk/measurements/terrestrial/an
- Data are managed by the ECN Data Centre (Centre for Ecology and Hydrology) with dataset ownership and sponsorship described in the document.