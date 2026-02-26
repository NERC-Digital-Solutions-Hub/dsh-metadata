# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) are a set of polygon layers that provide multiple levels of spatial detail for UK hydrology:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Each level represents a different scale of hydrological detail, from coarse to fine.

## How the layers relate

- Hydrometric Areas with Coastline and Hydrometric Areas without Coastline represent the same entities at the coarsest level; the boundary difference is how coastlines are defined:
  - With Coastline uses a smooth UK coastline.
  - Without Coastline follows the IHDTM (Integrated Hydrological Digital Terrain Model) edge for precise alignment with terrain data.
- IHU Groups are mid-sized units consisting of one or more IHU Sections; Groups can form Hydrometric Areas without Coastline.
- A Section is the drainage area between two confluences with named watercourses; each Section is linked to one IHU Catchment.
- IHU Catchments are the finest detail and represent the full area upstream from an outlet of every IHU Section; Catchment polygons can overlap with other layers.

## Data creation, extent, and maintenance

- Boundaries are derived from CEH’s IHDTM (50 m grid resolution) for inland areas; GB coastline is from Ordnance Survey Meridian2; NI coastline/boundaries derived from OS GB Panorama data.
- The dataset covers:
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland
  - Hydrometric Areas without Coastline and higher levels: Great Britain only (no suitable NI river geometry dataset available)
- Islands were merged into nearby Hydrometric Areas in 2014 (e.g., Isles of Scilly, Lundy, Grassholm, St Kilda group).
- NI catchments are clipped to the national boundary, so not all cross-border catchments are hydrologically complete.
- There are no routine updates planned; updates may occur if errors are found or if underlying river/drainage data improve.

## Data quality, limitations, and challenges

- Quality is tied to the IHDTM 50 m grid; some minor rivers in Great Britain may be omitted.
- NI data are incomplete for several layers due to data availability.
- All points are allocated to one Hydrometric Area; NI catchments are clipped, affecting hydrological completeness across borders.
- Topological integrity is maintained:
  - No gaps or overlaps in Hydrometric Areas.
  - Catchments and their relationships are defined to reflect upstream/downstream geometry.

## Layer-specific characteristics and attributes

- Common structure:
  - Attributes are stored primarily in a Geodatabase (preserves NULL values); converting to Esri Shapefile may convert NULLs to zeros or empty strings.
- Hydrometric Areas with Coastline (115 features): HA_NUM, HA_NAME, HA_ID, and derived HA_ID-like identifiers; contains area-level descriptors.
- Hydrometric Areas without Coastline (105 features): Similar HA_NUM/HA_NAME/HA_ID fields tailored for coastline-free boundaries.
- Groups (405 features): Include area, River names, and connectivity attributes (e.g., G_ID, G_NAME, G_AREA_KM2, G_CAT, G_RIVER, etc.).
- Sections (584,556 features): Detailed section-level data including CCAREA_KM2 (cumulative upstream area), OUTF_X/Y (outlet coordinates), RIVER fields, S_ID, S_NAME, S_DS_ID (downstream section), and polygon area S_AREA_KM2.
- Catchments (584,556 features): Spatial extents with EAST/NORTH and CEAST/CNORTH coordinates, KMSQ (area in km^2), and associated downstream section S_ID.

## Practical implications for analysts

- The multi-level IHU framework enables scalable hydrological analysis, from broad regional aggregation (Areas) to fine-grained upstream catchment behavior (Catchments).
- The option to use without coastline boundaries is beneficial when aligning IHU with terrain-grid data or other IHDTM-based datasets.
- Data provenance relies on IHDTM and official mapping sources (Ordnance Survey); researchers should account for NI limitations and potential data gaps for small rivers.
- When using shapefiles, be aware of NULL value handling; prefer the Geodatabase where possible to preserve NULLs.

## Summary of purpose

- The IHU dataset provides a coherent, multi-resolution representation of UK hydrological units (areas, groups, sections, and catchments) derived from historical hydrometric classifications and modern terrain models, designed to support hydrometric data management, analysis, and reporting at various scales.