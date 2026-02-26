# UK Environmental Change Network (ECN) bird data: 1995-2012

## Overview
- ECN is a UK-wide environmental-change monitoring network funded by multiple government departments and agencies.
- Bird data were collected using transects within 1 km squares, recording bird distance from the transect and distance category.
- Methodology follows the Breeding Bird Survey (BTO); transects are walked twice per year.
- Data are designed for national-scale insights; site-based data have limitations for linking population levels to environmental change. Users are advised to supplement ECN data with broader monitoring programs (e.g., BTO) for fuller context.
- Original protocols included the Common Bird Census and Moorland Bird Survey before the Breeding Bird Survey replacement.
- Acknowledgement of data use is requested, including sending a reprint of any publication that cites ECN data.

## Data structure
- SITECODE, Description: Site code (e.g., T01).
- SITECODE, Data type: string.
- LCODE, Description: Location code.
- LCODE, Data type: string.
- VISIT, Description: Visit (E = early and L = late).
- VISIT, Data type: string.
- SDATE, Description: Sampling date.
- SDATE, Data type: date (dd-mmm-yyyy).
- TRANSECT, Description: Transect identifier.
- TRANSECT, Data type: integer.
- FIELDNAME, Description: Bird species code.
- FIELDNAME, Data type: string.
- VALUE, Description: Count value.
- VALUE, Data type: integer.
- DISTANCE, Description: Distance category from transect (1 = within 25 m; 2 = 25–100 m; 3 = >100 m; F = in flight).
- DISTANCE, Data type: string.

## Sites
- 12 ECN sites (T01–T12) with coordinates and date ranges.
- Example sites:
  - T01 Drayton: 52°11'37.95"N, 1°45'51.95"W; 29-APR-1995 to 14-JUN-2010.
  - T02 Glensaugh: 56°54'33.36"N, 2°33'12.14"W; 14-MAY-2002 to 26-JUN-2012.
  - T03 Hillsborough: 54°27'12.24"N, 6°04'41.26"W; 13-MAY-2006 to 19-JUN-2011.
  - T04 Moor House - Upper Teesdale: 54°41'42.15"N, 2°23'16.26"W; 08-MAY-1996 to 18-JUN-2012.
  - T05 North Wyke: 50°46'54.96"N, 3°55'4.10"W; 05-MAY-1997 to 29-MAY-2012.
  - T06 Rothamsted: 51°48'12.33"N, 0°22'21.66"W; 30-APR-1997 to 14-AUG-2009.
  - T07 Sourhope: 55°29'23.47"N, 2°12'43.32"W; 08-MAY-2002 to 21-JUN-2010.
  - T09 Alice Holt: 51°9'16.46"N, 0°51'47.58"W; 25-MAY-1998 to 25-MAY-2012.
  - T10 Porton Down: 51°7'37.83"N, 1°38'23.46"W; 10-MAY-1995 to 27-APR-2010.
  - T11 Y Wyddfa – Snowdon: 53°4'28.38"N, 4°2'0.64"W; 17-MAY-1996 to 20-JUN-2012.
  - T12 Cairngorms: 57°6'58.84"N, 3°49'46.98"W; 01-JUN-2002 to 02-JUN-2012.
- Data structure supports linking site and location codes to transect and species observations.

## Bird species codes
- The dataset provides a mapping table between species codes and species names.
- Codes are used in FIELDNAME to record bird observations; a comprehensive mapping from codes to species names is included in the ECN documentation.
- Note: The document lists a long, detailed mapping of species codes to names; for GIS use, join FIELDNAME to the provided species-code table to obtain common names.

## Additional metadata
- ECN_BB2.csv: Weather and observation timing metadata for transects.
  - SITECODE, LCODE, VISIT, SDATE, FROM_HOUR, FROM_MINS, TO_HOUR, TO_MINS.
  - CLOUD (cloud cover, 1–3), RAIN (rain, 1–3), WIND (wind, 1–3), VISIBILITY (visibility, 1–3).
- ECN_BB3.csv: Habitats observed on the transect.
  - SITECODE, LCODE, VISIT, YEAR, TRANSECT, FIRSTHL1–FIRSTHL4, SECONDHL1–SECONDHL4.
  - Habitat codes are hierarchical (levels 1–4) describing habitat types and features.

## Habitat codes (BTO habitat recording system)
- Level 1: One code (A–J) representing main habitat type (e.g., A = Woodland).
- Level 2: Category within the main habitat (e.g., A: Broadleaved, Coniferous, Mixed).
- Levels 3 and 4: Additional detail about the habitat (e.g., coppicing, disturbance, shrub/field layers, dead wood, grazing).
- Examples of Level 1 categories:
  - A - WOODLAND
  - B - SCRUBLAND (or young woodland <5 m)
  - C - Semi-natural Grassland/Marsh
  - D - Heathland and Bogs
  - E - Farmland
  - F - Human Sites
  - G - Water Bodies (freshwater)
  - H - Coastal
  - I - Inland Rock
  - J - Miscellaneous
- Each level includes specific codes for subcategories and habitat features (Levels 2–4), enabling detailed GIS-based habitat context around bird observations.

## Usage considerations for GIS workflows
- Data are collected on transects within 1 km squares; spatially enabling mapping of bird counts to sites and transects with associated habitat and weather metadata.
- Data exist in multiple related files (structure, species codes, habitat codes, weather/habitat metadata), requiring joining via SITECODE, LCODE, VISIT, and TRANSECT.
- Data quality and transformation may be needed:
  - Data are spread across multiple sources; ensure consistent field types and coordinate handling.
  - Use accompanying quality metadata when analyzing or visualizing results.
  - Integrate with broader monitoring datasets (e.g., BTO) to mitigate site-scale limitations.
- Acknowledgement and data citation are required when using ECN bird data; provide a reprint item if publishing.

## Access and citation
- ECN Data Centre: http://data.ecn.ac.uk; contact ecn@ceh.ac.uk.
- Reference: Rennie, S. et al (2015). Supporting documentation for UK Environmental Change Network (ECN) bird data: 1995-2012. DOI: 10.5285/c616149a-fb19-4d6b-a9e5-84363538ed7e. Please acknowledge use of datasets and send one reprint of any publication that cites the data.