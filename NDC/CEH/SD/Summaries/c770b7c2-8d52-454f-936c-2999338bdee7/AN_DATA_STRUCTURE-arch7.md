# UK Environmental Change Network (http://www.ecn.ac.uk) Atmospheric Chemistry: Nitrogen Dioxide (AN)

## Scope and purpose
- Passive diffusion tubes measure NO2 concentration over a two-week deployment.
- Data are intended to support environmental change research and to enable mapping and analysis of NO2 at multiple ECN sites.
- Data users are requested to acknowledge ECN and to send one reprint of any publication citing ECN data.

## Data origin, ownership, and access notes
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Dataset Owners: UK ECN programme sponsored by a consortium of UK government departments and agencies.
- Acknowledgement and publication request: authors should acknowledge ECN data use and provide one reprint of citing publications.
- Protocol reference: ECN measurement protocol for terrestrial NO2.

## Data structure and storage
- Data are stored in an Oracle database.
- Core data structure:
  - For each site there are 12 tables named D1AN_xxx and D2AN_xxx (xxx = site code).
  - Common fields include SITECODE, SDATE, TUBEID, FIELDNAME, VALUE.
  - Additional deployment-related fields present in D2AN_xxx: DEPDATE, DEPHOUR, SDATE, SHOUR, SMINS.
  - TUBEID distinguishes Experimental (E) and Blank (B) tubes.
  - FIELDNAME references a set of measured attributes; VALUE holds the numeric measurement.
- Data types and units vary by field (e.g., NO2, NO2PPB, WEIGHTNO2, TDIFF).

## Site codes and metadata
- Twelve ECN sites (T01 to T12) with names, coordinates, and date ranges:
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
  - T11 Snowdon (Y Wyddfa)
  - T12 Cairngorms
- Each site includes precise latitude/longitude coordinates and the dataset date range (varies by site, spanning 1993–2012 in the provided details).

## Data fields and units
- Weight of NO2 on the mesh: WEIGHTNO2 (micrograms).
- NO2 concentration: NO2 (micrograms per cubic meter).
- NO2 concentration (alternative unit): NO2PPB (ppb).
- Exposure time: TDIFF (minutes).
- Quality codes: Q1–Q8 (integers) referencing quality codes.

## Quality codes
- ECN quality codes indicate data quality factors; codes are drawn from a standard list with an option for text in addition to codes (code 999 signals an unusual event with accompanying quality text).
- Representative examples (categories include):
  - 100–105, 106–118, 119–135, 136–139, 140–149, 150–169, 170–177: field/atmospheric interference or sampling issues (e.g., no information, sampling issues, debris in sample, weather-related effects).
  - 200–237, 238–241: observational or measurement issues (e.g., adverse weather, instrument issues, data edits, uncertainty in identification).
  - 501–509: laboratory-related issues (e.g., no sample, sample lost, contamination, insufficient sample, instrument failure).
  - 510–513: additional laboratory/measurement concerns.
  - 999: unusual event – see accompanying quality text.
- The full list covers a wide range of potential field, sample, and lab conditions affecting data quality; detailed explanations accompany the dataset.

## Usage notes and best practices
- Always consult the accompanying quality information when using the data to interpret NO2 measurements correctly.
- The dataset links field measurements to site metadata and deployment details, enabling GIS-style mapping and temporal analyses.

## Citation and acknowledgement
- ECN requests acknowledgement of data use and the submission of one reprint for each publication citing the ECN data.