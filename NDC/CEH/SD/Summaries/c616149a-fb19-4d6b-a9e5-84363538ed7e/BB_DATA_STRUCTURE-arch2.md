# Supporting documentation for UK Environmental Change Network (ECN) bird data: 1995-2012 (Rennie, S. et al (2015) http://doi.org/10.5285/c616149a-fb19-4d6b-a9e5-84363538ed7e)

## Purpose and scope
- Documents the ECN bird data collection and structure for 1995–2012.
- Supports understanding causes and consequences of environmental change through standardized bio-survey data.
- Encourages acknowledgement and citation of ECN data; requests one reprint of any publication citing ECN data.

## Data collection methodology
- Birds recorded on transects within 1 km2 squares; distance from transect recorded.
- Methodology based on the Breeding Birds Survey (BBS) by the British Trust for Ornithology (BTO).
- Transects are walked twice per year (early and late visits).
- ECN’s early surveys used BTO’s Common Bird Census (lowland) and Moorland Bird Survey (upland); the Breeding Bird Survey later replaced these.
- Data are designed for national-scale interpretation; site-based data have limited detail on precise population-environment relationships.
- Data should be used alongside broader monitoring programs (e.g., BTO) to mitigate limitations.

## Data structure and fields
- Core dataset fields:
  - SITECODE (site code) and SITECODE Notes
  - LCODE (location code) and LCODE Notes
  - VISIT (E = early, L = late) and VISIT Notes
  - SDATE (sampling date)
  - TRANSECT (transect number)
  - FIELDNAME (bird species code)
  - VALUE (count or value)
  - DISTANCE (distance category or flight)
- DISTANCE categories:
  - 1 = within 25 m of transect (either side)
  - 2 = 25–100 m from transect
  - 3 = greater than 100 m from transect
  - F = bird in flight (any distance)
- Metadata tables accompany the dataset:
  - ECN_BB2.csv: survey observed times and weather (FROM_HOUR, FROM_MINS, TO_HOUR, TO_MINS; CLOUD, RAIN, WIND, VISIBILITY)
  - ECN_BB3.csv: habitat observations (FIRSTHL1–FIRSTHL4A/B and SECONDHL1–SECONDHL4B; YEAR; TRANSECT; habitat codes)

## Site codes and time range
- 12 sites with specific coordinates and date ranges:
  - T01 Drayton (1995–2010)
  - T02 Glensaugh (2002–2012)
  - T03 Hillsborough (2006–2011)
  - T04 Moor House - Upper Teesdale (1996–2012)
  - T05 North Wyke (1997–2012)
  - T06 Rothamsted (1997–2009)
  - T07 Sourhope (2002–2010)
  - T09 Alice Holt (1998–2012)
  - T10 Porton Down (1995–2010)
  - T11 Snowdon (1996–2012)
  - T12 Cairngorms (2002–2012)
- Data structure supports site, location, visit, and date range information for longitudinal analysis.

## Bird species codes
- Extensive codified list mapping species codes to full names (e.g., AC = Arctic Skua; AE = Arctic Tern; AF = Little Tern; etc.).
- Codes cover a wide range of species, enabling standardized aggregation and cross-site comparisons.
- The dataset uses two-letter or short codes (FIELDNAME) to denote species occurrences/counts.

## Metadata and habitat coding
- Additional metadata captures surveying times and weather conditions (ECN_BB2.csv).
- Habitat information captured for transects (ECN_BB3.csv), including:
  - FIRSTHL1–FIRSTHL4B: Habitat codes at multiple levels (1–4)
  - SECONDHL1–SECONDHL4B: Secondary habitat level codes
- Purpose: enable analyses of habitat associations with bird occurrences.

## Habitat coding details
- BTO habitat recording system with hierarchical levels:
  - Level 1: One code A–J for main habitat type
  - Level 2: More specific category under Level 1
  - Levels 3 and 4: Further codes detailing features of the main habitat type
- Examples by major habitat groups:
  - A - WOODLAND
    - Level 2: broadleaved, coniferous, mixed, and water-logged variants
    - Level 3/4: features such as coppicing, disturbance, canopy structure, shrub/field layers, dead wood presence
  - B - SCRUBLAND (young woodland <5 m)
    - Level 2: regenerating woodland, downland, heath scrub, coppice types, etc.
    - Levels 3/4: tree composition, boundary features, disturbance, shrub/field layers
  - C - Semi-natural Grassland/Marsh
  - D - Heathland and Bogs
  - E - Farmland
  - F - Human Sites
  - G - Water Bodies (freshwater)
  - H - Coastal
  - I - Inland Rock
  - J - Miscellaneous
- Level 2–4 codes provide granular habitat context (e.g., disturbance, vegetation structure, grazing, proximity to roads).

## Data usage considerations
- Data usage should acknowledge ECN data sharing and cite the publication.
- For robust environmental-change analyses, supplement ECN site data with broader national datasets (e.g., BTO) to interpret population-environment relationships.
- The ECN dataset emphasizes standardized reporting formats (reports, maps, charts) and data quality, with data stored/uploaded to appropriate data portals.

## Access, attribution, and contact
- ECN Data Centre: ECN Data Centre, Centre for Ecology and Hydrology (data.ecn.ac.uk; ecn@ceh.ac.uk)
- Publication citation and data usage acknowledgement are requested.
- Users should send one reprint of any publication citing ECN data.