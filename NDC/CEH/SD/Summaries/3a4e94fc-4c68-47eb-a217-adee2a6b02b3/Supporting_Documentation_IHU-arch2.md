# Integrated Hydrological Units (IHU) of the United Kingdom

- Aim and scope
  - A multi-layer set of polygon layers representing hydrological units at different spatial resolutions for UK river catchments.
  - Layers include: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
  - Purpose is to support consistent organisation and management of hydrometric data and environmental monitoring.

- What each layer represents
  - Hydrometric Areas with Coastline: administrative groupings of river catchments used for river flow measurement and hydrometric data management.
  - Hydrometric Areas without Coastline: same entities as with Coastline but boundaries follow the IHDTM rather than a smooth coastline; better for analyses requiring precise extent matching IHDTM data, less suitable for cartography.
  - Groups: medium-sized units (typical ~400 km²) comprising one or more Sections; can be combined to form larger Hydrometric Areas without Coastline.
  - Sections: drainage area between two confluences with named watercourses; each Section belongs to one Group and to one Catchment.
  - Catchments: finest level of detail, representing full area upstream from an outlet of every Section; may overlap with other IHU layers (the only layer where overlaps occur).

- Naming, coding, and identifiers
  - Hydrometric Areas are numbered with two-digit codes; Irish hydrometric areas are prefixed with regional numbers.
  - NRFA gauging station numbers build on this hydrometric area coding system.
  - Section names combine river names; Catchment S_ID links to downstream Sections.

- Geography and coverage
  - Coverages: Hydrometric Areas with Coastline cover Great Britain and Northern Ireland; without Coastline covers Great Britain only due to data limitations for NI.
  - Some minor rivers are not captured even in Great Britain.
  - In 2014, islands without defined Hydrometric Areas were assigned to nearby areas to achieve full UK coverage (examples: Isles of Scilly merged with HA 49; St Kilda group merged with HA 106, etc.).
  - Northern Ireland catchments are clipped to the national boundary, so not every hydrometric area is hydrologically complete across borders.

- Data creation and lineage
  - Boundaries derived from CEH's Integrated Hydrological Digital Terrain Model (IHDTM) using an in-house program.
  - Great Britain coastline based on Ordnance Survey Meridian2; NI coastline from OS GB Panorama data.
  - The dataset aligns with the historical convention of Hydrometric Areas and was incorporated into the IHU framework in 2015.
  - The hydrometric boundaries are topologically correct with no gaps or overlaps; all land area allocated to a single Hydrometric Area.

- Data quality, limitations, and caveats
  - Quality is tied to IHDTM resolution (50 m grid).
  - NI data and some GB minor rivers may be incomplete or missing.
  - The non-coastline layer is precise for data alignment with IHDTM but not ideal for cartographic presentation.
  - NI catchments are clipped to the national boundary, affecting hydrological completeness for cross-border catchments.

- Updates and maintenance
  - No routine updates anticipated.
  - Updates may be produced if errors are found or if improvements to underlying river or drainage grid data become available.

- Data formats and attributes
  - Primary format: Geodatabase (preserves NULL values; shapefiles convert NULLs to zeros or empty strings).
  - If downloading as Esri Shapefile, NULL values may appear as zeros or empty strings.
  - Attribute highlights by layer:
    - Areas with Coastline: HA_NUM, HA_NAME, HA_ID; optional computed HA_ID (e.g., HA054).
    - Areas without Coastline: HA_NUM, HA_NAME, HA_ID.
    - Groups: area metrics (e.g., CCAREA_KM2), identifiers (G_ID), names (G_NAME), river associations, and related identifiers (HA_ID, OUTF_SC, RIVER, etc.).
    - Sections: identifiers (S_ID), names (S_NAME), river associations (RIVER, RIVER_DS, RIVER_US), area (S_AREA_KM2), downstream linkage (S_DS_ID), geographic coordinates (OUTF_X, OUTF_Y; S_AREA_KM2; centroids).
    - Catchments: geographic and geometric metadata (EAST, NORTH, CEAST, CNORTH), area (KMSQ), downstream section reference (S_ID).
  - The dataset preserves various descriptive fields to support analysis and linking between layers.

- Practical implications for environmental analysts
  - Use as a consistent, hierarchical framework for organizing hydrometric data and environmental indicators over time.
  - Choose Coastline vs Without Coastline layers based on needs: cartography vs precise IHDTM-aligned analysis.
  - Leverage the topological integrity (no gaps/overlaps) to ensure complete country-wide coverage in analyses.
  - Be aware of NI data limitations and potential missing minor rivers when interpreting results.
  - Utilize the detailed attribute schema to link hydrometric units with specific rivers, catchments, and downstream/upstream relationships for monitoring and policy assessment.