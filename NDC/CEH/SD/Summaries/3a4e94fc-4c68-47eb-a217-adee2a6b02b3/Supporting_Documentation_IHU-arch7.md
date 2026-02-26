# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) of the United Kingdom comprise multiple polygon layers that represent hydrological units at different spatial resolutions:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Purpose
  - Administrative groupings of river catchments used for organizing UK river flow measurement and hydrometric data management.
  - Hydrometric Areas are active catchment units with one or more tidal outlets or contiguous catchments with similar topography.
  - Hydro-numbering and identifiers support integration with related datasets (e.g., NRFA gauging station numbers use the same regional/hydrometric area scheme).

- Key Concepts and Relationships
  - Groups are the mid-scale units; they contain one or more Sections.
  - Groups can be combined to form Hydrometric Areas without Coastline.
  - Sections are drainage areas between two confluences with named watercourses.
  - Catchments represent the full area upstream from an outlet of every Section (the finest level of detail), and Catchment polygons may overlap with multiple Sections/Groups.
  - Hydrometric Areas with Coastline are a broader, coastal-friendly representation; Hydrometric Areas without Coastline align to the IHDTM boundaries for precise data alignment (useful for analyses requiring exact IHDTM grid matching).

- Coverage and Scale
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland.
  - Hydrometric Areas without Coastline, Groups, Sections, and Catchments: Great Britain only (NI excluded due to data availability for river geometries/names at required detail).

- Data Creation and Processing
  - Boundaries are derived from CEH IHDTM using an in-house tool; GB coastline follows the Ordnance Survey Meridian2 coastline; NI boundaries/coastlines from OS GB Panorama data.
  - Islands that lacked defined Hydrometric Areas (as of 2014) were assigned to nearby areas to achieve complete UK coverage (examples: Isles of Scilly merged with HA 49; Lundy with HA 51; St Kilda group with HA 106, etc.).
  - All Hydrometric Area boundaries are topologically correct with no gaps or overlaps; NI catchments are clipped to the national boundary (note: cross-border catchments may not be hydrologically complete).

- Quality, Limitations, and Maintenance
  - Dataset quality is tied to the underlying IHDTM at 50 m grid resolution.
  - Minor rivers may be omitted even within Great Britain.
  - NI data for some layers are incomplete due to lack of suitable detail in river geometries/naming.
  - No routine updates planned; updates may occur only if errors are found or if improvements to underlying river or drainage grid data become available.

- Layer Details and Attributes (summary)
  - Hydrometric Areas with Coastline (115 features)
    - Core fields include HA_NUM (Hydrometric Area Number), HA_NAME, HA_ID; optional computed ID like HA054.
  - Hydrometric Areas without Coastline (105 features)
    - Core fields mirror the with-coastline layer (HA_NUM, HA_NAME, HA_ID).
  - Groups (405 features)
    - Key attributes: CCAREA_KM2 (upstream catchment area in km2), G_ID, G_NAME, G_AREA_KM2, G_CAT (core/marginal/estuarine), G_DS_ID, G_ALTNAME, G_QUALIFY, HA_ID, OUTF_SC, RIVER, RIVER_DS, RIVER_US.
  - Sections (584,556 features)
    - Key attributes: CCAREA_KM2, G_ID, HA_ID, HA_NUM, OUTF_X/Y (outlet coordinates), S_AREA_KM2, S_ID, S_NAME, S_DS_ID (downstream section), RIVER, RIVER_DS, RIVER_US.
  - Catchments (584,556 features)
    - Key attributes: S_ID (downstream section identifier), S_NAME, EAST/NORTH (outlet coordinates), CEAST/CNORTH (centroid coordinates), KMSQ (area in km2).

- Data Accessibility and Formats
  - Primary format: Geodatabase (preserves NULL values).
  - Esri Shapefile downloads will convert NULLs to zeros or empty strings; be aware of this when using Shapefiles.

- Historical Context
  - Hydrometric Areas originated in the 1930s for integrated hydro-meteorological data collection.
  - The internal digitisation history progressed from paper maps to digital boundaries, aligned with IHDTM in CEH datasets.
  - In 2015, Hydrometric Areas became part of the Integrated Hydrological Units dataset, enabling multi-level hydrological units across the UK.