# Integrated Hydrological Units of the United Kingdom (IHU)

## Purpose and Overview
- Describes the Integrated Hydrological Units (IHU) of the UK, a set of polygon layers at varying spatial detail used to organize river catchments and hydrometric data management.
- Layers include: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
- IHU extends the traditional Hydrometric Area concept (in use since the 1930s) to provide a structured, multi-resolution framework for environmental monitoring and data governance.

## Layers and What They Represent
- Hydrometric Areas with Coastline
  - Administrative groupings of river catchments at sub-national scale used for river flow measurement and hydrometric data management.
  - Each area is a single feature with a two-digit HA number; Ireland and the UK have an extended numbering scheme (area numbers prefixed by regional identifiers for non-GB areas).
  - Catchments may have one or more tidal outlets to the sea or estuaries.
- Hydrometric Areas without Coastline
  - Same entities as with Coastline but boundaries follow the IHDTM (Integrated Hydrological Digital Terrain Model) edges, ensuring precise alignment with terrain-derived data; not ideal for cartography.
- Groups
  - Medium-resolution units (~400 km² typical; range from ~4 km² to 3019 km²).
  - Composed of one or more Sections; can be combined to form larger Hydrometric Areas without Coastline.
  - Names derive from major rivers and local area names; include attributes such as catchment area, river names, and identifiers.
- Sections
  - Drainage area between two confluences of watercourses with known names.
  - Each Section belongs to one Group and one Catchment; contains identifiers and river name fragments used in naming.
  - Attributes include S_ID, S_NAME, upstream/downstream river names, and area.
- Catchments
  - Finest level of detail; upstream area from an outlet of every Section.
  - Can overlap multiple Sections and Groups; represents full upstream area.
  - Attributes include spatial extents (East/North), centroid coordinates, polygon area (KMSQ), and linkage to downstream Section (S_ID).

## Data Quality, Coverage, and Limitations
- Quality tied to the underpinning IHDTM with a 50 m grid resolution.
- Coverage:
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland.
  - Other layers: Great Britain only (no NI river geometry/names with suitable detail for NI in those layers).
  - Some minor rivers may be missing even in Great Britain.
- Data limitations:
  - Certain NI catchments are clipped to national boundaries, so not every hydrometric area is hydrologically complete.
  - Some rivers or confluences may lack names (represented as UNKNOWN or SOURCE/SEA in Section names).
  - Updates are not routine; updates occur only to fix errors or incorporate improvements to underlying terrain or hydrographic data.
- Data format caveat:
  - Primary format is Geodatabase to preserve NULL values; Esri Shapefile may convert NULLs to zeros or empty strings.

## Updates and Maintenance
- No routine updates anticipated.
- Updates occur if errors are found or if improvements to the underlying rivers or drainage grid data become available.

## History and Data Creation
- History:
  - Originated in the 1930s via the Inland Water Survey Committee to facilitate integrated hydrometeorological data collection.
  - Early digitisation in the 1980s led to boundaries that were adjusted to align with later IHDTM-derived catchments (via Centre for Ecology & Hydrology, CEH).
  - In 2015, Hydrometric Areas became part of the Integrated Hydrological Units framework.
- Data creation:
  - Inland Hydrometric Area boundaries are digitally derived from CEH’s IHDTM using an in-house program.
  - Great Britain coastline uses Ordnance Survey Meridian2; Northern Ireland boundary and coastline derived from OS GB Panorama data.
  - Island adjustments (2014) merged to the nearest, most appropriate Hydrometric Area (examples include Isles of Scilly to HA 49, St Kilda archipelago to HA 106, etc.).
  - All boundaries are topologically correct with full UK surface coverage; NI catchments are clipped to the national boundary.

## Attribute Schema Overview
- Tables describe metadata for each layer, with key fields including:
  - Hydrometric Areas with Coastline: HA_NUM, HA_NAME, HA_ID; derived identifier HA053, etc.
  - Hydrometric Areas without Coastline: HA_NUM, HA_NAME, HA_ID; identifier-like HA000.
  - Groups: G_ID, G_NAME, G_AREA_KM2, G_CAT, RIVER, and related fields; attributes describing catchment upstream/downstream relationships.
  - Sections: S_ID, S_NAME, RIVER, RIVER_US/RIVER_DS, S_AREA_KM2, CCAREA_KM2, OUTF_X/OUTF_Y, HA_ID, G_ID.
  - Catchments: East/North centroid coordinates (EAST/NORTH, CEAST/CNORTH), area (KMSQ), and linkage to downstream section (S_ID).
- Data format note:
  - Geodatabase preferred for preserving NULLs; Shapefile option will convert NULLs to zeros or empty strings.

## Practical Considerations for Monitoring Frameworks
- The IHU framework provides a scalable, multi-resolution basis for organizing hydrometric data, enabling policy evaluation and monitoring at appropriate spatial scales (catchment, section, group, area).
- Useful for aligning UK hydro-meteorological datasets (CEH/NRFA) and for ensuring data governance consistency across the monitoring program.
- Be mindful of NI data limitations and cross-border hydrological completeness when designing analyses that span the entire UK.
- Consider data availability and metadata quality (e.g., gaps in river names, incomplete catchments) when designing indicators and dashboards.