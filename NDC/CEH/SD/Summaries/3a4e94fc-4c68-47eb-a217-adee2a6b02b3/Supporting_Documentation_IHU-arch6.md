# Integrated Hydrological Units of the United Kingdom

- A multi-layer spatial dataset representing hydrological units at varying scales:
  - Hydrometric Areas with Coastline (coastal boundaries)
  - Hydrometric Areas without Coastline (IHDTM-aligned boundaries)
  - Groups (medium-scale units)
  - Sections (drainage areas between confluences)
  - Catchments (upstream areas from each section outlet)
- Purpose: support UK river flow measurement, hydrometric data management, and hydrological analyses by providing consistent, hierarchical hydrological boundaries.

## Layers and relationships

- Hydrometric Areas with Coastline and without Coastline cover the same entities at the coarsest level; differences lie in boundary depiction (coastline vs IHDTM edge).
- IHU Groups are a mid-level aggregation of one or more Sections; Groups can be combined to form Hydrometric Areas without Coastline.
- A Section is the drainage area between two confluences with named watercourses; each Section belongs to one Group.
- Catchments are the full upstream area from an outlet of every Section and are the finest detail; Catchments can overlap multiple Sections and Groups.

## Coverage and boundaries

- Coverage:
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland
  - Hydrometric Areas without Coastline, Groups, Sections, Catchments: Great Britain only (Northern Ireland lacks suitable river geometry data for these layers)
- Boundary specifics:
  - Without Coastline: boundaries follow the IHDTM grid edges to enable exact matching with gridded data
  - With Coastline: boundaries follow a smooth UK coastline for cartographic purposes
- Special notes:
  - Some minor rivers are not captured even in Great Britain
  - Catchment boundaries in Northern Ireland are clipped to the national boundary, so not all hydrometric areas are hydrologically complete
  - Islands were merged to nearby hydrometric areas in 2014 to achieve full UK coverage

## Data creation and history

- Data creation:
  - Inland Hydrometric Area boundaries derived from CEH’s IHDTM using an in-house program
  - Great Britain coastline aligned to Ordnance Survey Meridian2 coastline; Northern Ireland boundary/coastline from OS GB Panorama
  - Islands merged to closest hydrometric areas based on proximity and existing numbering (examples: Isles of Scilly to HA 49; Lundy to HA 51; St Kilda group to HA 106, etc.)
  - All boundaries are topologically correct with no gaps or overlaps
- History:
  - Hydrometric Areas designated in the 1930s; later continuity with catchment boundaries
  - The Inland Water Survey Committee established the framework; numbering conventions published in the 1936–37 and 1971–73 references
  - The current IHU dataset was established in 2015, integrating prior datasets with IHDTM-derived boundaries

## Attributes, formats, and data structure

- Primary format: Geodatabase (preserves NULL values; Shapefile will convert NULLs to zeros or empty strings)
- Attribute tables (examples):
  - Areas with Coastline: HA_NUM, HA_NAME, HA_ID (and a derived HA_ID like HA054)
  - Areas without Coastline: HA_NUM, HA_NAME, HA_ID
  - Groups: G_ID, G_NAME, HA_ID, RIVER, area metrics, outflow/inflow details, etc. (fields include CCAREA_KM2, G_AREA_KM2, G_CAT, OUTF_SC, RIVER, etc.)
  - Sections: S_ID, S_NAME, HA_ID, HA_NUM, OUTF_X/Y, RIVER/RIVER_DS/RIVER_US, S_AREA_KM2, CCAREA_KM2, S_DS_ID, G_ID
  - Catchments: S_ID (downstream reference), EAST/NORTH/CENTROID coordinates, KMSQ (area), etc.
- Data use notes:
  - If downloading as Shapefile, NULL values may be converted to zeros or empty strings; Geodatabase recommended to preserve NULLs

## Quality, limitations, and maintenance

- Quality basis: dependent on the underlying IHDTM, which has a 50 m grid resolution
- Known limitations:
  - NI datasets limited due to the lack of suitable river geometry data
  - Some small rivers may be omitted even in Great Britain
  - NI catchments are clipped to the national boundary, so cross-border continuity may be incomplete
- Updates and maintenance:
  - No routine updates anticipated; updates may occur if errors are found or if improvements to rivers or drainage grid data become available

## Practical considerations for data users

- Choose between layers based on use case:
  - Use Hydrometric Areas with Coastline for general mapping and cartography
  - Use Hydrometric Areas without Coastline for precise alignment with IHDTM-based gridded data
- Be aware of cross-boundary data gaps in Northern Ireland and potential missing minor rivers
- When performing analyses, account for potential overlaps in Catchments and ensure consistency with S_ID references across Sections and Groups