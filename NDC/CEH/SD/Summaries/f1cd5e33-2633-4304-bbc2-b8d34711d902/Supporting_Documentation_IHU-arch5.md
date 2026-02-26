# Integrated Hydrological Units of the United Kingdom

- Purpose and scope
  - A multi-level set of polygon layers representing hydrological units in the UK, intended to support hydrometric data management and analysis.
  - Levels include: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
  - Coastal vs non-coastal delineations differ in boundary following (coastline vs IHDTM) to support different analytical and cartographic needs.

- Layer overview and how they relate
  - Hydrometric Areas with Coastline: administrative groupings of river catchments used for river flow measurement and hydrometric data management; covers GB and NI.
  - Hydrometric Areas without Coastline: same entities as above but boundaries follow IHDTM precisely for data alignment with gridded IHDTM data; better for data matching than for cartography.
  - Groups: medium-sized units (~400 km² typical; range 4–3019 km²); consist of one or more Sections; can be combined to form Hydrometric Areas without Coastline.
  - Sections: drainage area between two confluences with named watercourses; have associated rivers; each Group comprises one or more Sections; some names may be UNKNOWN or include Source/Sea indicators.
  - Catchments: finest level; represent full area upstream from outlets of every Section; can overlap with other IHU levels; used to characterize upstream extents.

- Coverage and regional notes
  - Great Britain and Northern Ireland: Hydrometric Areas with Coastline cover GB and NI; other layers currently cover Great Britain only due to data limitations for Northern Ireland.
  - NI cross-border catchments are clipped to the national boundary; not every hydrometric area is hydrologically complete in NI.
  - Islands have been merged into nearby hydrometric areas (examples: Isles of Scilly into HA 49; St Kilda and others into specified HAs) to achieve full UK surface area coverage.
  - Some minor rivers may not be captured even within GB.

- Data quality and underpinnings
  - Data quality is governed by the underlying IHDTM, which has a 50 m grid resolution.
  - Boundaries are topologically corrected to avoid gaps or overlaps; every point in the country is allocated to exactly one Hydrometric Area.
  - For Northern Ireland, NI boundaries and coastline are derived from GB Panorama; NI catchments are clipped to NI boundary.

- Data creation and maintenance
  - Boundaries are digitally derived from CEH’s IHDTM using in-house tooling; islands and cross-border adjustments performed (2014 adjustments noted).
  - Islands and edge cases merged to nearest appropriate hydrometric area using proximity and existing conventions.
  - No routine updates anticipated; updates may occur to fix errors or to incorporate improvements to underlying rivers or drainage grid data.
  - Original historical context and numbering conventions are described (legacy references and 1930s–1970s origins; the 2015 integration into IHU).

- Data formats and schema
  - Primary format: Geodatabase (preferred due to NULL preservation).
  - If downloading as Esri Shapefile, NULL values may be converted to zeros or empty strings.
  - Attribute tables summarize key fields per layer (examples below):
    - Areas with Coastline: HA_NUM, HA_NAME, HA_ID; optional HA_ID can be constructed as 'HA' + zero-padded HA_NUM.
    - Areas without Coastline: similar HA_NUM, HA_NAME, HA_ID.
    - Groups: fields include area metrics (CCAREA_KM2), alternative names, river connections, and identifiers (G_ID, G_NAME, HA_ID, etc.).
    - Sections: fields include catchment area (S_AREA_KM2), river names, outlet coordinates (OUTF_X/Y), S_ID, S_NAME.
    - Catchments: outlet coordinates (EAST/NORTH), centroid coordinates (CEAST/CNORTH), polygon area (KMSQ), downstream/upstream section IDs (S_ID, S_NAME).

- Practical considerations for Data Stewards
  - Ensuring data users’ needs are met by providing coherent, interoperable boundaries aligned with IHDTM data where appropriate.
  - Supporting data creators to maintain accuracy, complete metadata, and consistent formats; clear guidance on topological integrity and boundary definitions.
  - Documenting data processing steps, updates, and island/boundary adjustments to maintain traceability.
  - Adhering to sharing constraints and ensuring alignment with portal/catalogue practices when uploading datasets.
  - Being aware of limitations in NI data and cross-border catchment completeness when integrating across datasets.
  - Managing expectations about update frequency and the potential need for bespoke handling of non-interoperable regional variations.

- Additional notes
  - The dataset’s design supports both cartographic applications (coastline-based boundaries) and precise data alignment with gridded terrain data (IHDTM-based boundaries).
  - The documentation emphasizes historical context, naming conventions, and the evolution from older catchment representations to the current IHU framework (as of 2015).