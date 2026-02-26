# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) comprise five polygon layers that represent different levels of spatial detail: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
- Hydrometric Areas with Coastline and without Coastline represent the same entities at the coarsest level; the difference is how the coast is delineated (smooth coastline vs IHDTM-based coastline). IHU Groups are the medium-resolution units, which combine to form Hydrometric Areas without Coastline. Sections are the drainage areas between confluences with named watercourses, and Catchments are the upstream areas from each Section outlet, with Catchments being the finest level of detail (notably overlapping with others).

## Data Layers and What They Represent
- Hydrometric Areas with Coastline: administrative groupings of river catchments used for UK river flow measurement and hydrometric data management; areas are numbered and named (HA_NUM, HA_NAME, HA_ID).
- Hydrometric Areas without Coastline: same entities as above but boundaries follow IHDTM; better for analyses that require exact matching with IHDTM grid data; not ideal for cartography.
- Groups: medium-sized units (~4 km² to ~3,019 km²); consist of one or more Sections; named from major rivers and local context; include attributes describing area, rivers, and flow connections.
- Sections: drainage areas between confluences; large attribute set including cumulative area (CCAREA_KM2), river names, inflow/outflow identifiers, and section identifiers (S_ID, S_NAME, S_DS_ID).
- Catchments: upstream areas from each Section outlet; smallest detailed units; includes extent and centroid coordinates, polygon area (KMSQ), and downstream section references (S_ID).

## Data Creation and Coverage
- Boundaries are digitally derived from CEH's IHDTM (50 m grid); land and coastlines defined using Ordnance Survey datasets (Meridian2 for GB coastline; Panoramа for NI boundary).
- Islands and undefined areas were allocated to the nearest appropriate Hydrometric Area in 2014 to ensure full UK coverage (examples include Isles of Scilly, Lundy, Grassholm, St Kilda group, etc.).
- All Hydrometric Area boundaries are topologically correct with no gaps or overlaps; however, catchments can overlap sections and groups.
- Northern Ireland catchments are clipped to the national boundary, potentially leaving some cross-border hydrological completeness out of scope.

## Quality, Limitations, and Maintenance
- Dataset quality depends on the IHDTM 50 m terrain model; NI data are limited by available river geometries and names; some minor rivers may be missing even in Great Britain.
- No routine updates are planned; updates may occur only if errors are found or if improvements to underlying rivers or drainage grid data become available.
- The dataset is designed to be stable for standard analyses and mapping, with potential updates driven by data quality improvements.

## Attributes and Data Formats
- Primary format: Geodatabase (preserves NULL values); Esri Shapefile may convert NULLs to zeros or empty strings.
- Areas with Coastline (115 features): HA_NUM, HA_NAME, HA_ID; HA_ID is a derived identifier like HA000.
- Areas without Coastline (105 features): HA_NUM, HA_NAME, HA_ID; similar identifiers as above.
- Groups (405 features): key fields include CCAREA_KM2 (catchment area upstream of the group), G_ID, G_NAME, RIVER fields (RIVER, RIVER_DS, RIVER_US), HA_ID, OUTF_SC, and others that describe relationships and alternative names.
- Sections (584,556 features): most extensive layer; fields include CCAREA_KM2, G_ID, HA_ID, OUTF_X/Y (outlet coordinates), RIVER names, S_AREA_KM2, S_DS_ID (downstream section), S_ID, S_NAME.
- Catchments (584,556 features): include EAST/NORTH (outlet coordinates), centroid coordinates (CEAST/CNORTH), KMSQ (area in km²), S_ID (downstream section reference), and other location fields.

## Practical Takeaways for Data Support
- Use Geodatabase delivery when possible to preserve NULL semantics; be cautious with Shapefiles due to NULL handling.
- Choose the appropriate layer depending on use case: Coastline variants for cartography, without Coastline variants for precise IHDTM-aligned analyses.
- Leverage the hierarchical structure: Catchments to Sections to Groups to Hydrometric Areas to understand river network context and data management.
- Be mindful of NI limitations and potential gaps in river geometries; NI catchments may be clipped to national boundaries.
- Expect stable datasets with infrequent updates; plan for error-driven or data-improvement updates rather than recurring releases.