# Breeding Birds Survey Data (ECN)

- Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk), Centre for Ecology and Hydrology
- Dataset Owners: UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies (e.g., DEFRA, Natural England, NERC, etc.)
- Acknowledgement and citation: ECN requests acknowledgment of data use and a reprint of any publication citing ECN data.

## What the data are and how they are collected
- Standardized protocol: ECN uses standard operating procedures to ensure comparability across sites (bb.pdf accompanies this document for data collection details).
- Data scope and purpose: National-scale breeding bird monitoring; ECN provides site-based data that should be complemented with broader monitoring programmes (e.g., BTO) for detailed population-environment relationships.
- Survey method: Birds recorded along a transect within a 1 km square; distance of birds from transect recorded.
- Frequency: Transects are walked twice per year (early and late visits).
- Data design note: The Breeding Bird Survey is designed for national-scale insights; site-level data may be limited for precise relationships between populations and environmental change.
- Data quality: Use accompanying quality information when using the data.

## How the data are structured for GIS use
- Data download fields (core observations):
  - SITECODE (site code), LCODE (location ID), VISIT (early/late), SDATE (sampling date)
  - TRANSECT (transect identifier/year), FIELDNAME (bird species code), VALUE (count), DISTANCE (distance category)
  - F (bird in flight)
- Supporting documentation:
  - ECN_BB2.csv: survey timing, start/end times, and weather indicators (CLOUD, RAIN, WIND, VISIBILITY)
  - ECN_BB3.csv: habitat information along transects (FIRSTHL/SECONDHL levels)
  - ECN_BB_qtext.csv: site managers’ quality notes (quality text about data quality)

## Site, species, and habitat coding
- Site codes and locations:
  - Explanatory Information: Site codes (e.g., T01–T12) with site names and geographic coordinates
  - Example sites include Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Alice Holt, Porton Down, Snowdon, Cairngorms
- Bird species codes:
  - A comprehensive list of species codes and names (e.g., AC = Arctic Skua, AF = Spotted Crake, etc.)
  - A code for no birds present: XX
- Habitat codes (BTO habitat recording system):
  - Level 1: main habitat type (A–J)
  - Level 2: subcategory of the main habitat type
  - Level 3 and Level 4: further detail about habitat features
  - Examples of major habitat groups include:
    - A: Woodland (with Level 2–4 subcodes for broadleaved, coniferous, coppice, shrub layers, etc.)
    - B: Scrubland/young woodland
    - C: Semi-natural Grassland/Marsh
    - D: Heathland and Bogs
    - E: Farmland
    - F: Human Sites
    - G: Water Bodies (freshwater)
    - H: Coastal
    - I: Inland Rock
    - J: Miscellaneous
  - Each level adds increasingly specific habitat detail (e.g., disturbance from people, shrub density, grazing, distance to roads, etc.)

## Practical guidance for GIS specialists
- How to use the data:
  - Join site-level observations to site coordinates via SITECODE/LCODE for spatial visualization.
  - Map counts (VALUE) by transect and by distance category (DISTANCE) to analyze spatial distribution of birds within transects.
  - Use VISIT, SDATE to animate temporal changes or create time-series maps.
  - Enrich maps with habitat classifications (FIRSTHL, SECONDHL, THIRD/Fourth level codes) from ECN_BB3.csv to study habitat associations.
  - Incorporate weather/temporal context from ECN_BB2.csv (cloud, rain, wind, visibility) as additional attributes for spatial analyses.
  - Integrate accompanying quality notes (ECN_BB_qtext.csv) to filter or annotate data quality concerns.
- Considerations and limitations:
  - Data are designed for national-scale inference; be cautious about over-interpreting site-level relationships without supplementary data (e.g., BTO datasets).
  Use quality information to understand data reliability for specific site-years.
- Outputs to consider:
  - Map layers of transects with bird counts by species (or aggregated by a group) and by distance category.
  - Habitat-layer overlays using Level 1–4 habitat codes to explore habitat associations.
  - Time-enabled GIS visualizations to show seasonal and inter-annual patterns.

## Access and further information
- Data fields and structure:
  - Core fields: SITECODE, LCODE, VISIT, SDATE, TRANSECT, FIELDNAME, VALUE, DISTANCE, F
  - Supporting CSVs: ECN_BB2.csv, ECN_BB3.csv, ECN_BB_qtext.csv
- Explanatory data:
  - Site codes with coordinates
  - Comprehensive bird species codes and names
  - Detailed habitat codes (Level 1–4) with examples and definitions
- Additional information:
  - The accompanying site and habitat coding guidelines are available within the supporting documentation and the ECN site catalogue