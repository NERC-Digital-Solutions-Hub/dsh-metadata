# UK Environmental Change Network (http://www.ecn.ac.uk) Frogs (BF)

## Overview
- Phenology-based protocol monitoring spawning of Common Frogs in selected pools/ditches by counting egg masses as an indicator of frog population health.
- Laboratory analyses are conducted on pool water observed via this protocol.
- Data usage should include accompanying quality information; ECN requests acknowledgment and a reprint of any publication citing the data.

## Provenance and governance
- Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
- Dataset Owners: ECN programme sponsored by a consortium of UK government departments and agencies funding site monitoring or network coordination (e.g., Agri-Food and Biosciences Institute; BBSRC; Natural Resources Wales; DEFRA; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; SNH; SEPA; Scottish Government; etc.).
- Acknowledgment and citation: Please acknowledge ECN data usage and send one reprint of publications citing the data.
- Protocol Reference: http://www.ecn.ac.uk/measurements/terrestrial/b/bf

## Protocol and data collection notes
- Methodology: Phenology-based frog spawning monitoring; assess the number of egg masses as an indicator of population health.
- Supplements: Laboratory analyses of water from observed pools.
- Quality information: Use the accompanying quality metadata when using the data.

## Data structure and storage
- Core data: Stored in Oracle database, split into 10 site-specific tables for each data type.
  - D1BF_xxx: Core field data (one table per site; xxx is site code).
  - D2BF_xxx: Laboratory/analyte data (one table per site; xxx is site code).
- Metadata: Structure documented in core metadata tables (referenced by site and field codes).

## Site codes and characteristics
- T01 Drayton (52°11'37.95"N, 1°45'51.95"W); date range in dataset 01-JAN-1994 to 22-FEB-2012.
- T02 Glensaugh (56°54'33.36"N, 2°33'12.14"W); date range 01-JAN-1994 to 19-JUN-2012.
- T03 Hillsborough (54°27'12.24"N, 6° 4'41.26"W); date range 01-JAN-1994 to 25-FEB-2011.
- T04 Moor House - Upper Teesdale (54°41'42.15"N, 2°23'16.26"W); date range 01-JAN-1994 to 10-OCT-2012.
- T05 North Wyke (50°46'54.96"N, 3°55'4.10"W); date range 05-JAN-1994 to 28-MAR-2012.
- T06 Rothamsted (51°48'12.33"N, 0°22'21.66"W); date range 17-FEB-1994 to 14-JUL-2010.
- T08 Wytham (51°46'52.86"N, 1°20'9.81"W); date range 01-JAN-1994 to 17-JUN-1994.
- T09 Alice Holt (51° 9'16.46"N, 0°51'47.58"W); date range 28-FEB-1995 to 14-MAR-2001.
- T10 Porton Down (51° 7'37.83"N, 1°38'23.46"W); date range 14-FEB-2001 to 07-APR-2010.
- T11 Y Wyddfa - Snowdon (53° 4'28.38"N, 4° 2'0.64"W); date range 31-DEC-1995 to 30-MAY-2012.

## Key fields and variables (examples)
- Common field names across data sets include:
  - Alkalinity (ALKY), Aluminium, Calcium, Chloride, Conductivity (CONDY), Colour (absorbance), Depth, Dissolved Organic Carbon (DOC), pH measurements, temperature (MaxTMP, MINTMP), nutrient measures (TOTALN, TOTALP, NH4N, NO3N, PO4P), major ions (SODIUM, POTASSIUM, MAGNESIUM, IRON), spawn-related metrics (SPAWNDATE, NEWMASS, CONGDATE, LEAVEDATE, HATCHDATE), spawn area metrics (SURFAREA), quality codes (Q1–Q8), and other laboratory-derived or field-derived metrics.
- Quality codes: Each data point is annotated with standard ECN quality codes to indicate issues affecting data quality (e.g., sample loss, equipment problems, environmental disturbances, etc.). The list includes codes 100–513 and 999 for unusual events; 999 signifies an unusual event with accompanying quality text.

## Quality management
- ECN quality codes are selected from a standard list by site managers; multiple codes may apply.
- If a situation is not covered by standard codes, a text note is attached (identified by code 999), accessible alongside the quality information.

## Usage and citation guidelines
- Acknowledge ECN data usage in publications.
- Provide one reprint of any publication that cites ECN data.