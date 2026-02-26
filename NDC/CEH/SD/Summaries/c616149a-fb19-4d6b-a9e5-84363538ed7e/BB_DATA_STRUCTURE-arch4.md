# UK Environmental Change Network (ECN) bird data: 1995-2012

- Purpose and context
  - ECN bird data documenting and supporting research into environmental change, funded by a consortium of UK government departments and agencies.
  - Data providers request acknowledgment of data use and one reprint of any publication citing the data.
  - Data are structured to support national-scale Breeding Birds Survey results but site-based data have limited detail on population-environment relationships; recommended use in combination with broader monitoring data (e.g., BTO).

- Data scope and methodology
  - Bird species recorded along transects within 1 km squares; distance from transect captured.
  - Methodology follows the Breeding Birds Survey (BTO); transect walked twice per year.
  - Early and late visits recorded (E and L).
  - At ECN start, two other protocols were used (Common Bird Census and Moorland Bird Survey); Breeding Bird Survey replaced them at ECN sites.

- Data structure and primary data fields
  - Core data table fields: SITECODE, SITECODE Notes, LCODE, LCODE Notes, VISIT, VISIT Notes, SDATE (date), TRANSECT, FIELDNAME (bird species code), VALUE, DISTANCE (distance category or flight), plus DISTANCE Notes.
  - Site and data range details for sites T01–T12 (site name, coordinates, date ranges).
  - Bird species codes map two-letter codes to full species names (e.g., AC = Arctic Skua, AV = Avocet, etc.), with XX indicating no birds present.
  - Example: SITECODE, LCODE, VISIT, SDATE, TRANSECT, FIELDNAME (species code), VALUE (count), DISTANCE (category or F for in flight).

- Additional metadata and data quality information
  - ECN_BB2.csv: survey timing (start/end), weather (cloud, rain, wind, visibility) with corresponding codes.
  - ECN_BB3.csv: habitat observations on transect, with Year, TRANSECT, and hierarchical habitat codes (FIRSTHL, SECONDHL, FIRSTHL3/4; SECONDHL3/4) describing habitat levels.
  - Habitat coding system (levels 1–4) covers broad categories such as:
    - A - Woodland (with Level 2–4 details on broadleaved, coniferous, coppice, disturbance, shrub/field layers, etc.)
    - B - Scrubland/young woodland
    - C - Semi-natural Grassland/Marsh
    - D - Heathland and Bogs
    - E - Farmland
    - F - Human Sites
    - G - Water Bodies
    - H - Coastal
    - I - Inland Rock
    - J - Miscellaneous
  - Each level provides increasing specificity for habitat and disturbance attributes.

- Site and data access details
  - ECN Data Centre: data.ecn.ac.uk; contact ecn@ceh.ac.uk.
  - Sponsoring bodies listed (e.g., DEFRA, Natural England, NERC, etc.).
  - Acknowledgment and reprint request instructions included.

- Key considerations for data use and data leadership
  - Data are valuable for long-term environmental change studies but are limited for precise linking to environmental variables at individual sites without supplementary data (e.g., BTO datasets).
  - Important to use accompanying quality and habitat metadata to accurately interpret counts and habitat associations.
  - Data discoverability and interoperability can be enhanced by consistent metadata (weather, habitat codes) and standard species codes.
  - Potential data governance needs include ensuring proper attribution, managing data versioning across site ranges, and coordinating with broader networks to contextualize site-level findings.