# Integrated Hydrological Units of the United Kingdom

- Purpose and scope
  - A hierarchical set of polygon layers representing UK hydrological units at multiple spatial resolutions.
  - Used for organizing UK river flow measurement and hydrometric data management.
  - Layers cover: with coastline, without coastline, groups, sections, and catchments.

- What the layers represent
  - Hydrometric Areas with Coastline: administrative groupings of river catchments used for hydrometric data management; coastal outline used for cartography.
  - Hydrometric Areas without Coastline: same entities as with coastline but boundaries follow IHDTM edges; suitable for analyses requiring exact IHDTM boundary alignment, not ideal for mapping.
  - Groups: medium-sized units (~4xx km² typical) made up of one or more Sections; can combine to form Hydrometric Areas without Coastline.
  - Sections: drainage area between two confluences with named rivers; each section belongs to a group and an associated catchment; names often include river names; some are labeled UNKNOWN, Source, or Sea.
  - Catchments: finest detail; represent full area upstream from each section’s outlet; can overlap multiple sections and groups (the only layer with overlaps).

- Naming, coding, and structure
  - Hydrometric Areas are numbered with two-digit codes; additional regional prefixes used for some areas in Ireland.
  - NRFA gauge numbers are based on the same regional and hydrometric area coding system.
  - Sea/outlet and river naming conventions are embedded in the section and catchment attributes.

- Data creation and integration
  - Boundaries derived from CEH’s Integrated Hydrological Digital Terrain Model (IHDTM) using in-house tools.
  - Great Britain coastline aligned to Ordnance Survey Meridian2; Northern Ireland boundaries/coastlines from OS GB Panorama data.
  - Islands historically with undefined areas were assigned to the nearest appropriate hydrometric area (e.g., Isles of Scilly merged into HA 49).
  - Islands and cross-border adjustments listed (e.g., St Kilda merged to HA 106; Lundy to HA 51).
  - Islands and cross-border catchments treated to ensure full UK surface area coverage; NI catchments clipped to national boundary (not all cross-border hydrological completeness guaranteed).

- Quality, limitations, and coverage
  - Data quality is limited by the underlying IHDTM resolution (50 m grid).
  - Coverage: Hydrometric Areas with Coastline covers Great Britain and Northern Ireland; other layers currently cover Great Britain only due to river geometry data limitations for NI.
  - Some minor rivers may be omitted even in Great Britain.
  - No routine updates; updates may occur if errors are found or underlying data improve.
  - All boundaries are topologically correct with no gaps or overlaps (except catchments may overlap across sections/groups as noted).

- Data maintenance and accessibility
  - Datasets are primarily provided as Geodatabases (preferred to preserve NULL values).
  - If download options include Esri Shapefile, NULL values may be converted to zeros or empty strings, which users should account for.
  - NI catchments are clipped to the national boundary; not every hydrometric area is hydrologically complete for NI.

- Attributes and data structure
  - The document outlines five attribute tables corresponding to each layer (Areas with Coastline, Areas without Coastline, Groups, Sections, Catchments).
  - Example attributes include: HA_NUM, HA_ID, HA_NAME for Hydrometric Areas; G_ID, G_NAME, G_AREA_KM2, RIVER, and related fields for Groups; section-specific fields like S_ID, S_NAME, S_AREA_KM2, RIVER_US/DS, and outlet coordinates; catchment fields including KMSQ (area in square kilometres) and S_ID (downstream section reference).
  - The datasets are designed to be topologically cohesive, with clear relationships: Sections belong to Groups and connect to Catchments; Catchments aggregate upstream areas.

- Practical implications for analysts
  - Useful for aggregating river flow and hydrometric data at multiple spatial scales (coarse to fine).
  - The Coastline vs. without Coastline distinction affects cartographic vs. analytical needs; choose layer accordingly.
  - Be mindful of NI data limitations and potential missing minor rivers when conducting nationwide analyses.
  - When combining datasets from different layers, respect the hierarchical relationships (Areas → Groups → Sections → Catchments) and the potential overlaps in Catchments.