# UK Environmental Change Network (ECN) bird data: 1995-2012

## Overview
- ECN bird data documenting UK Environmental Change Network observations from 1995 to 2012.
- Managed by the ECN Data Centre (Centre for Ecology and Hydrology) with sponsorship from UK government departments and agencies.
- Purpose: support research on environmental change through standardized transect-based bird surveys; data intended for broader data use and policy-relevant insights.
- Users are asked to acknowledge data use and to send one reprint of any publication citing ECN data.

## Data collection and methodology
- Birds recorded on a transect within a 1 km square; distance from transect is also recorded.
- Methodology follows the Breeding Birds Survey (BBS), organized by the British Trust for Ornithology (BTO).
- Transects are walked twice per year (early and late visits).
- ECN data are site-based and designed for national-scale interpretation; recommended to be used in conjunction with data from broader monitoring programs (e.g., BTO) to better relate population levels to environmental change.
- Early ECN bird protocols (BTO Common Bird Census at lowland sites and Moorland Bird Survey at upland sites) were replaced by the Breeding Bird Survey at ECN sites.

## Data structure (core dataset)
- SITECODE, Description: Site code
- SITECODE, Notes: string
- LCODE, Description: Location code
- LCODE, Notes: string
- VISIT, Description: Visit (E = early, L = late)
- VISIT, Notes: string
- SDATE, Description: Sampling date
- SDATE, Notes: dd-mmm-yyyy
- TRANSECT, Description: Transect
- TRANSECT, Notes: integer
- FIELDNAME, Description: Bird species code
- FIELDNAME, Notes: string
- VALUE, Description: Value
- VALUE, Notes: integer
- DISTANCE, Description: Distance category
- DISTANCE, Notes: codes:
  - 1 = within 25 metres either side of transect
  - 2 = between 25 and 100 m of transect
  - 3 = greater than 100 m from transect
  - F = Bird in flight, any distance
- DISTANCE, Notes: string

## Site codes
- T01 Drayton: 52°11'37.95"N 1°45'51.95"W; Date range 29-APR-1995 to 14-JUN-2010
- T02 Glensaugh: 56°54'33.36"N 2°33'12.14"W; 14-MAY-2002 to 26-JUN-2012
- T03 Hillsborough: 54°27'12.24"N 6°04'41.26"W; 13-MAY-2006 to 19-JUN-2011
- T04 Moor House - Upper Teesdale: 54°41'42.15"N 2°23'16.26"W; 08-MAY-1996 to 18-JUN-2012
- T05 North Wyke: 50°46'54.96"N 3°55'4.10"W; 05-MAY-1997 to 29-MAY-2012
- T06 Rothamsted: 51°48'12.33"N 0°22'21.66"W; 30-APR-1997 to 14-AUG-2009
- T07 Sourhope: 55°29'23.47"N 2°12'43.32"W; 08-MAY-2002 to 21-JUN-2010
- T09 Alice Holt: 51° 9'16.46"N 0°51'47.58"W; 25-MAY-1998 to 25-MAY-2012
- T10 Porton Down: 51°7'37.83"N 1°38'23.46"W; 10-MAY-1995 to 27-APR-2010
- T11 Y Wyddfa - Snowdon: 53°4'28.38"N 4°2'0.64"W; 17-MAY-1996 to 20-JUN-2012
- T12 Cairngorms: 57°6'58.84"N 3°49'46.98"W; 01-JUN-2002 to 02-JUN-2012

## Bird species codes
- The dataset includes an extensive mapping of species codes to common names (e.g., AC = Arctic Skua, AE = Arctic Tern, etc.).
- A comprehensive species-code table is provided with the data to enable consistent species identification across sites and years.

## Additional metadata
- ECN_BB2.csv: survey observed on the transect (structure includes)
  - SITECODE, LCODE, VISIT, SDATE
  - FROM_HOUR, FROM_MINS, TO_HOUR, TO_MINS: start and end times of surveys
  - CLOUD, RAIN, WIND, VISIBILITY: BTO weather codes (categorized)
- ECN_BB3.csv: habitat observations on the transect
  - SITECODE, LCODE, VISIT, YEAR, TRANSECT
  - FIRSTHL1/SECONDHL1: Habitat Level 1 codes
  - FIRSTHL2/SECONDHL2: Habitat Level 2 codes
  - FIRSTHL3A/3B, SECONDHL3A/3B, FIRSTHL4A/4B, SECONDHL4A/4B: Habitat Levels 3 and 4
- Habitat coding system:
  - Level 1 codes: A - J (main habitat type)
  - Each Level 1 has Level 2, Level 3, Level 4 codes detailing subcategories (examples below)
    - A - WOODLAND: Level 2 = Broadleaved, Coniferous, Mixed, etc.; Level 3/4 codes describe age, disturbance, shrub/field layers, dead wood, etc.
    - B - SCRUBLAND: Level 2-4 codes describe regeneration status, verge types, shrub density, disturbance, and management
    - C - Semi-natural Grassland/Marsh: Level 2-4 codes cover grazing, hedgerows, field boundaries, montane status, and disturbance
    - D - HEATHLAND AND BOGS: Level 2-4 codes cover bog types, montane status, disturbance, and grazing
    - E - FARMLAND: Level 2-4 codes cover grassland types, boundaries, vegetation, and crops
    - F - HUMAN SITES: Level 2-4 codes cover urban/suburban/rural contexts and man-made features
    - G - WATER BODIES (freshwater): Level 2-4 codes cover water body type and disturbance
    - H - COASTAL: Level 2-4 codes cover coastal environment, substrate, vegetation, and proximity to roads
    - I - INLAND ROCK: Level 2-4 codes cover rock types and disturbance
    - J - MISCELLANEOUS: Codes reserved/ unspecified

## Quality and usage notes
- Use the accompanying quality information when utilizing ECN bird data.
- The dataset is designed for national-scale interpretation but has site-level limitations; integration with broader datasets (e.g., BTO) is recommended to strengthen analyses.
- When publishing, acknowledge ECN data use and provide one reprint of the publication.

## Access, attribution and limitations
- Data Centre: ECN Data Centre (data.ecn.ac.uk); contact ecn@ceh.ac.uk
- Coverage spans 1995-2012 across multiple UK sites with transect-based bird observations and habitat/weather metadata.
- The documentation emphasizes careful interpretation due to site-based structure and encourages combining ECN data with larger-scale datasets to mitigate limitations.

## Practical takeaways for data support work
- ECN bird data provide standardized transect-based bird counts with distance class, timing, and habitat context, suitable for exploring environmental-change-related trends when integrated with broader monitoring programs.
- Key steps for use:
  - Align ECN transect data (SITECODE, LCODE, VISIT, SDATE, TRANSECT, FIELDNAME, VALUE, DISTANCE) with ECN_BB2 weather metadata and ECN_BB3 habitat metadata for richer analyses.
  - Use the BTO Breeding Bird Survey methodology context to interpret site-based results.
  - Acknowledge data usage and submit reprints as required.