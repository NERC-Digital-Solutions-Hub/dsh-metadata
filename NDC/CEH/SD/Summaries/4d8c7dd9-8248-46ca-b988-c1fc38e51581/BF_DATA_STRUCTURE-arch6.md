# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- Multi-site environmental dataset managed by the UK Environmental Change Network (ECN) with an emphasis on phenology-based frog spawning observations and related water chemistry data.
- Includes field measurements across sites, plus laboratory analyses of water samples.
- Data are collected under standardised procedures to ensure comparability across sites; accompanying quality information is essential for proper use.
- Acknowledgement of data use is requested, along with a copy of any publication citing the data.

## Dataset ownership and sponsorship
- ECN programme is funded by a consortium of UK government departments and agencies.
- Organisations contributing data include: AFBI, BBSRC, Cyfoeth Naturiol Cymru, Dstl, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, SEPA, Scottish Government, and others.
- Usage acknowledgement and one reprint request are requested for any publications citing ECN data.

## How to use and interpret the data
- Data are provided in a structured download with the following core fields:
  - SITECODE: Unique code for each ECN site
  - LCODE: Location code (unique within site)
  - FROMDATE: From date of last recording
  - SDATE: Sampling date
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Users should consult the accompanying quality information to understand data quality for each observation.

## Supporting documentation and quality information
- ECN_BF_qtext.csv: Site managers assign quality codes reflecting factors that may affect data quality. Affected observations may include an explanatory text (quality code 999) describing unusual events. The quality text is viewable in ECN_BF_qtext.csv.
- Quality codes overview: A comprehensive list (e.g., 100, 101, 102, …, 513, 999) describing issues from no information to laboratory and field-specific problems, including unusual events and data adjustments.
- Explanatory information for quality codes provides a wide range of conditions affecting samples (e.g., equipment issues, environmental disturbances, sampling anomalies, laboratory constraints).

## Site codes and locations
- Explanatory site codes include:
  - T01: Drayton
  - T02: Glensaugh
  - T03: Hillsborough
  - T04: Moor House - Upper Teesdale
  - T05: North Wyke
  - T06: Rothamsted
  - T08: Wytham
  - T09: Alice Holt
  - T10: Porton Down
  - T11: Y Wyddfa - Snowdon
- Each site includes precise latitude/longitude coordinates for spatial reference.

## Variables being measured (FIELDNAME)
- A broad suite of water chemistry and physical properties (e.g., ALKY, ALUMINIUM, CALCIUM, CHLORIDE, CONDY, COLOUR, DEPTH, pH, TEMP, NH4N, NO3N, TOTALN, TOTALP, SODIUM, SIO4S, POTASSIUM, PO4P, etc.).
- Frog spawning and biology metrics (e.g., CONGDATE, HATCHDATE, SPAWNDATE, NEWMASS, PERCDEAD, SPAWNAREA, STAGE).
- Multiple units are specified per variable (e.g., mg/L, °C, pH, cm, date).

## Explanatory notes for data users
- Phenology-based methodology focuses on spawning indicators (e.g., egg masses) as a health proxy for frog populations.
- Daily and laboratory measurements are included, with quality codes flagging data reliability.
- The accompanying data dictionary and quality documentation are essential for correct interpretation and any data cleaning or filtering.

## Data quality and usage considerations
- Expect variability in data quality due to field conditions, equipment, and environmental factors; always consult quality codes and the ECN_BF_qtext.csv for context.
- The dataset provides standardized protocols to ensure cross-site comparability; adhere to these when integrating data into analyses or dashboards.
- If outputs will be shared or reused, ensure proper attribution to ECN and the relevant site coordinators; consider sharing a reprint of publications using the data.

## Practical takeaways for data support and reuse
- Use the structured download fields (SITECODE, LCODE, FROMDATE, SDATE, FIELDNAME, VALUE) to build datasets and dashboards; layer on quality codes for filtering.
- Reference the site codes with coordinates to enable geospatial analyses or site-based comparisons.
- Leverage the quality codes and accompanying explanations to assess data reliability and to decide when to exclude or annotate questionable observations.
- Acknowledge ECN in any outputs and provide a reprint request if a publication arises from the data.