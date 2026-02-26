# UK Environmental Change Network (http://www.ecn.ac.uk) Rabbits and Deer (BU)

## Overview
- A dataset from the UK Environmental Change Network (ECN) focusing on relative abundance of rabbits and deer estimated via dropping counts.
- Dropping counts are recorded on transects twice a year (late March and late September); direct population size is not measured.
- Moor House data also used to estimate relative abundance of Grouse.

## Data provenance and access
- Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Dataset owners: ECN programme funded by a consortium of UK government departments/agencies (list of sponsors provided).
- Protocol reference: ECN measurement protocol link (terrestrial/b/bu).
- Acknowledgement: ECN requests acknowledgement when data are used and a reprint of any publication citing the data.
- Usage note: Ensure accompanying quality information is consulted when using the data.

## Data structure and schema
- Data stored in Oracle database as 9 tables per dataset, with site-specific prefixes:
  - D1BU_xxx: Core data values (one table per site).
  - D2BU_xxx: Dropping counts data (deer, grouse, rabbit, sheep) plus quality fields.
  - D3BU_xxx: Transect information (transect segments, lengths, habitat descriptions).
- Tables are keyed by:
  - SITECODE: Site code (e.g., T01, T03, etc.), with site descriptions.
  - LCODE: Location code.
  - SDATE: Sampling date.
  - PLOTID: Transect section identifier.
  - FIELDNAME: Field name (optional in D1BU).
  - VALUE / other numeric fields (counts or measurements).
  - Additional fields in D2BU include CLEARDATE (date transects cleared) and SURVEY (survey reference).
  - LENGTH and HABDESC in D3BU describe transect length and habitat description.
- Metadata references:
  - M_DESC: Reference for site/location metadata.
  - M_REFFIELD: Reference for field names.
  - Core metadata documentation available for full structure.

## Site codes and coverage
- Nine site tables with location and date ranges:
  - T01 Drayton — 52°11'37.95"N 1°45'51.95"W; 01-APR-1993 to 11-OCT-2006
  - T03 Hillsborough — 54°27'12.24"N 6° 4'41.26"W; 07-JUN-1995 to 02-MAY-2012
  - T04 Moor House - Upper Teesdale — 54°41'42.15"N 2°23'16.26"W; 14-MAY-1993 to 10-OCT-2012
  - T05 North Wyke — 50°46'54.96"N 3°55'4.10"W; 23-MAR-1993 to 28-SEP-2012
  - T06 Rothamsted — 51°48'12.33"N 0°22'21.66"W; 11-APR-1994 to 18-OCT-2010
  - T07 Sourhope — 55°29'23.47"N 2°12'43.32"W; 12-MAY-1993 to 28-SEP-1993
  - T08 Wytham — 51°46'52.86"N 1°20'9.81"W; 06-MAY-1993 to 01-OCT-2012
  - T09 Alice Holt — 51° 9'16.46"N 0°51'47.58"W; 10-OCT-1994 to 10-NOV-2006
  - T10 Porton Down — 51° 7'37.83"N 1°38'23.46"W; 22-APR-1994 to 17-APR-2012

## Field names and data types
- D1BU_xxx (core values)
  - SITECODE: Site code
  - LCODE: Location code
  - SDATE: Sampling date
  - PLOTID: Transect section
  - FIELDNAME: Field name (optional)
  - VALUE: Value (numeric)
- D2BU_xxx (dropping counts and quality)
  - SITECODE, LCODE
  - CLEARDATE: Date droplets cleared (optional)
  - SDATE: Sampling date
  - PLOTID: Transect section
  - SURVEY: Reference number of survey
  - D, G, R, S: Count fields for deer, grouse, rabbit, sheep (as applicable)
  - Q1–Q8: Quality code fields (paired with integer quality scores)
- D3BU_xxx (transect details)
  - SITECODE, LCODE
  - PLOTID: Transect section
  - LENGTH: Transect length
  - HABDESC: Habitat description
- Quality codes (ECN standard)
  - A large enumerated list (e.g., 100, 101, 102, ..., 238, 239, 240, 241, 501–512, 513, 999)
  - 999 indicates an unusual event; a quality text field explains associated circumstances
  - Codes cover data loss, sampling issues, equipment problems, environmental disturbances, lab issues, and more
  - Site managers assign multiple applicable codes; accompanying quality information provides context

## Data quality and usage notes
- The dataset uses an index-based approach (dropping counts) due to the absence of practicable direct population size measurements.
- Data quality is tracked via standardized ECN quality codes and accompanying textual notes.
- Users should consult the quality metadata accompanying the dataset to interpret counts and potential biases.
- Emphasis on using the accompanying quality information when analyzing or visualizing the data.

## GIS considerations and how to use
- Spatial keys enable mapping of droppings and transects:
  - Use SITECODE and LCODE to join to site and location metadata for coordinates.
  - Map deer (D), grouse (G), rabbit (R) and sheep (S) counts by site-location-date.
  - Visualize transect locations and lengths from D3BU_xxx (LENGTH and PLOTID) to show sampling effort.
- Temporal analysis:
  - SDATE provides sampling dates; double-visit per year (late March and late September) allows seasonal trend assessment.
  - Use CLEARDATE where available to track data cleaning/clearing events.
- Data integration:
  - D1BU_xxx provides core numeric values keyed by SITE/LOCATION/DATE/TRANSECT, enabling joins across tables for aggregated maps (e.g., abundance by site, by transect, or by habitat).
  - Metadata references (M_DESC, M_REFFIELD) help enrich spatial layers with site descriptions, coordinates, and habitat information.
- Citations and reuse:
  - Acknowledge ECN data use and provide a reprint request for publications citing the data.

## Metadata and documentation notes
- Core metadata tables exist; for full structure, refer to the metadata documentation.
- Additional protocol details are available via the ECN measurements protocol link.
- The dataset includes explicit notes on methodology, sampling dates, and data interpretation to support GIS analysis and map-based storytelling.