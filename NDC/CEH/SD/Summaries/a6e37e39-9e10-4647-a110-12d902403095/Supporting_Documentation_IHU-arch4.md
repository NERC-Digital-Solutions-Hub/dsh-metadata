# Integrated Hydrological Units (IHU) of the United Kingdom

- The document documents the Integrated Hydrological Units (IHU) of the United Kingdom, comprising five polygon layers that represent different levels of spatial detail:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - IHU Groups
  - IHU Sections
  - IHU Catchments
- Core concepts:
  - Hydrometric Areas are administrative groupings of river catchments used for organizing hydrometric data.
  - IHU Groups are the medium-resolution units that can be combined to form Hydrometric Areas without Coastline.
  - A Section is the drainage area between two confluences with named watercourses.
  - Catchments are the full area upstream from an outlet of every IHU Section and are the finest level of detail (catchments can overlap other IHU units).

## Introduction and Purpose
- Hydrometric Areas with Coastline and without Coastline represent the same entities at the coarsest level; the boundary difference is how the coastline is represented.
- IHU provides multiple levels of spatial resolution to support hydrological analysis and data management across the UK.

## Quality and Known Limitations
- Data quality is tied to the underlying IHDTM 50m grid.
- Coverage:
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland.
  - All other layers: Great Britain only (Northern Ireland lacks a dataset with suitable river geometries/names at the required detail).
- Some minor rivers are not captured even in Great Britain.
- Updates: No routine updates are planned; updates may occur if errors are found or if improvements to underlying hydrological data become available.

## Updates and Maintenance
- No regular update cycle; updates occur only to correct errors or improve underlying data.

## Data Creation
- Boundaries are digitally derived from CEH IHDTM; coastline for GB follows Ordnance Survey Meridian2; NI boundaries from OS GB Panorama data.
- Each Hydrometric Area is a single feature.
- In 2014, certain islands were assigned to nearby areas to achieve full UK coverage (e.g., Isles of Scilly merged with HA 49; St Kilda group merged with HA 106, etc.).
- Boundaries are topologically correct with no gaps or overlaps; every point in the country is assigned to one Hydrometric Area.
- Northern Ireland catchments are clipped to the national boundary, so some hydrometric areas may not be hydrologically complete across borders.
- Hydrometric Areas without Coastline differ in boundary alignment (IHDTM) and are better for analyses requiring exact grid alignment, not for cartography.

## Layer Descriptions and Key Characteristics
- Hydrometric Areas with Coastline
  - Administrative groupings of river catchments for sub-national hydrometric data management.
  - Areas are numbered with a two-digit code; additional prefixes apply for island regions and Ireland.
  - NRFA gauging station numbers are based on this numbering system.
- Hydrometric Areas without Coastline
  - Same entities as with Coastline but boundaries follow IHDTM, enabling precise matching with gridded IHDTM data; not intended for cartographic use.
- Groups
  - Medium-resolution units (~400 km² typical; range from 4 km² to 3019 km²).
  - Each group comprises one or more Sections; groups can form Hydrometric Areas without Coastline.
  - Names derive from major rivers and local counties.
- Sections
  - Drainage area between two confluences with named watercourses.
  - Each Section is part of one Group and one Hydrometric Area.
  - Names constructed from rivers; “UNKNOWN” used where upstream rivers are not known; “Source” or “Sea” indicate special upstream/downstream status.
- Catchments
  - Finest level of detail; upstream area from each Section outflow.
  - May overlap multiple Sections and Groups; only layer with overlapping polygons.
  - Contains the most granular hydrological information.

## Attributes and Data Structure
- Primary format: Geodatabase (preserves NULL values; shapefiles convert NULLs to zeros or empty strings).
- Tables describe attributes for each layer (summary below):
  - Areas with Coastline: HA_NUM, HA_NAME, HA_ID, etc. (HA_ID is an identifier like HA000; can be constructed as HA + zero-padded number)
  - Areas without Coastline: Similar HA_NUM, HA_NAME, HA_ID
  - Groups: includes metrics like CCAREA_KM2 (catchment area upstream of the group outlet), G_AREA_KM2, G_NAME, RIVER, etc.; relationships to HA_ID and outflow/inflow sections
  - Sections: includes CCAREA_KM2 (cumulative catchment area), S_ID (section id), S_NAME (section name), RIVER fields, coordinates for outlet, and downstream/upstream identifiers
  - Catchments: includes location coordinates (EAST/NORTH, centroid coordinates), KMSQ (area), S_ID (most downstream section), and related identifiers
- Feature counts (as of the document):
  - Hydrometric Areas with Coastline: 115 features
  - Hydrometric Areas without Coastline: 105 features
  - Groups: 405 features
  - Sections: 584,556 features
  - Catchments: 584,556 features
- Notable notes:
  - Some rivers or sections near coasts use generic identifiers like UNKNOWN or Sea/Source.
  - The NI dataset indicates cross-border catchments may not be hydrologically complete due to clipping to the national boundary.

Data Leaders perspective: implications and actions
- Align data strategy with the multi-layer IHU structure to support scalable hydrological analytics and cross-agency collaboration.
- Ensure metadata and data governance support discoverability, lineage, and quality checks, especially given the lack of routine updates and regional coverage gaps.
- Leverage the Geodatabase format to preserve NULL values and minimize data loss during integration; account for potential NULL-to-zero/empty-string conversions in shapefile exports.
- Be aware of boundary distinctions between Coastline and Without Coastline layers when integrating with IHDTM-compatible datasets.
- Plan for data validation against IHDTM and be cognizant of potential gaps in NI data and minor rivers; consider commissioning updates if higher granularity or cross-border completeness is required.
- Use the relationship fields (HA_ID, G_ID, S_ID, S_NAME, etc.) to support lineage, attribution, and navigation across layers for end-user data products and analyses.