# UK Environmental Change Network (http://www.ecn.ac.uk) Rabbits and Deer (BU)

## Overview
- ECN dataset focusing on rabbits and deer, using droppings counts as an index of relative abundance.
- Dropping counts collected twice yearly (late March and late September) to monitor environmental change indicators.
- Methodology also applied to Moor House for grouse as a parallel index.

## Data Origin and Ownership
- Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
- Dataset Owners: UK Environmental Change Network funded by a consortium of government departments and agencies (list includes Defra, Environment Agency, Natural England, Natural Environment Research Council, and others).
- ECN requests acknowledgement of data use and one reprint of any publication citing these data.

## Protocol and Purpose
- Protocol Reference: ECN terrestrial measurements (BU) protocol.
- Purpose: provide standardized, auditable data on environmental change indicators derived from animal droppings.
- Data should be used with accompanying quality information to interpret results.

## Data Structure and Access
- Data are stored in Oracle across 9 site tables per data type:
  - D1BU_xxx: site-level data (one table per site)
  - D2BU_xxx: droppings data (rabbit, deer, grouse counts by transect)
  - D3BU_xxx: transect and habitat data (transect details such as length, habitat description)
- Core fields (example concepts):
  - SITECODE, LCODE, SDATE (sampling date), PLOTID (transect), FIELDNAME, VALUE (counts/measurements)
  - D2BU includes CLEARDATE in addition to SDATE and PLOTID
  - D3BU includes LENGTH and HABDESC for transect characteristics
- Site codes and site-specific metadata are maintained for 10 sites (T01–T10).

## Site Codes and Date Range
- T01 Drayton: 01-APR-1993 to 11-OCT-2006
- T03 Hillsborough: 07-JUN-1995 to 02-MAY-2012
- T04 Moor House - Upper Teesdale: 14-MAY-1993 to 10-OCT-2012
- T05 North Wyke: 23-MAR-1993 to 28-SEP-2012
- T06 Rothamsted: 11-APR-1994 to 18-OCT-2010
- T07 Sourhope: 12-MAY-1993 to 28-SEP-1993
- T08 Wytham: 06-MAY-1993 to 01-OCT-2012
- T09 Alice Holt: 10-OCT-1994 to 10-NOV-2006
- T10 Porton Down: 22-APR-1994 to 17-APR-2012
- Site coordinates and detailed location data accompany each site entry.

## Field Names and Measurements
- Core measurement fields:
  - D: Deer droppings count
  - G: Grouse droppings count
  - R: Rabbit droppings count
  - S: Sheep droppings count
- Quality fields: Q1, Q2, Q3, Q4, Q5, Q6, Q7, Q8 (each with a quality code and a corresponding value/flag)
- Metadata fields include sampling date (SDATE), transect (PLOTID), location codes (LCODE), and field names (FIELDNAME) linked to predefined reference tables.

## Quality Codes
- ECN standard quality codes indicate data quality and potential issues (codes 100–513, plus 999 for unusual events).
- Examples of codes cover: no information available, sample lost, partial loss, debris in funnel, adverse weather, equipment issues, grazing impacts, non-standard sampling dates/times, laboratory data concerns, and other data integrity warnings.
- 999 indicates an unusual event; accompanying quality text provides the full description.

## Data Use and Access
- Data should be used with the accompanying quality information to assess data reliability.
- ECN requests acknowledgement of data use and sending a reprint of any publication citing the dataset.
- Outputs are typically prepared in clear formats (reports, maps, charts) and datasets are stored/uploaded to appropriate data portals.

## Practical Implications for Analysts Monitoring the Environment
- Provides a standardized, long-term index-based view of small mammal and bird presence via droppings as a proxy for environmental health.
- Allows time-series assessment of relative abundance across multiple sites with consistent protocol.
- Facilitates data integration by using consistent fields (SDATE, PLOTID, FIELDNAME, VALUE) and quality codes to filter or weigh observations.
- Enables cross-site comparisons and trend analysis when combined with other ECN or external environmental datasets.
- Emphasizes data quality and traceability through explicit quality codes and metadata standards.