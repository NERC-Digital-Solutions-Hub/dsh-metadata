# Integrated Hydrological Units of the United Kingdom

- Overview
  - The Integrated Hydrological Units (IHU) comprise five polygon layers that represent different levels of spatial detail:
    - Hydrometric Areas with Coastline
    - Hydrometric Areas without Coastline
    - Groups
    - Sections
    - Catchments
  - The IHU concept extends the historic Hydrometric Areas (dating back to the 1930s) by providing multiple resolution levels for hydrological units.

- Layer Descriptions and Key Characteristics
  - Hydrometric Areas with Coastline
    - Covers Great Britain and Northern Ireland.
    - Administrative groupings of river catchments used for organizing river flow measurements and hydrometric data.
  - Hydrometric Areas without Coastline
    - Same areas as with Coastline but boundaries follow the IHDTM rather than a smooth coastline.
    - Better for analyses requiring precise matching with IHDTM grid data; not ideal for cartography.
  - Groups
    - Medium-resolution units (~roughly 400 km2 typical; range 4 km2 to 3019 km2).
    - Composed of one or more Sections; can be combined to form Hydrometric Areas without Coastline.
    - Names derived from major rivers and local counties.
  - Sections
    - Drainage area between two confluences with named watercourses.
    - Each Section belongs to one Group and is associated with one Catchment.
    - Section names are built from constituent rivers; placeholders like UNKNOWN, Source, and Sea appear where data is incomplete.
  - Catchments
    - Finest level of detail; represent the full area upstream from an outlet of every Section.
    - Catchment polygons may overlap with other layers (notably Sections).
    - Each Catchment references the downstream Section (S_ID).

- Data Creation, History, and Boundaries
  - Boundaries derived from CEH’s Integrated Digital Terrain Model (IHDTM) with a 50 m grid resolution.
  - Great Britain coastline alignment uses Ordnance Survey Meridian2; Northern Ireland boundaries/coastlines derived from OS GB Panorama data.
  - Islands and offshore landmasses were assigned to adjacent Hydrometric Areas in 2014 to ensure full UK coverage.
  - The current IHU dataset (introduced in 2015) ensures topological correctness with no gaps or overlaps; all points allocated to one Hydrometric Area.
  - Northern Ireland catchments are clipped to the national boundary, so not all hydrometric areas are hydrologically complete across borders.

- Data Coverage and Limitations
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland.
  - Hydrometric Areas without Coastline and Groups/Sections/Catchments: Great Britain only (due to data availability for NI river geometries/names).
  - Some minor rivers may not be captured even within Great Britain.
  - NI cross-border catchments may be incomplete hydrologically.

- Data Quality, Metadata, and Access
  - Data quality tied to the underlying IHDTM quality (50 m resolution); no routine ongoing updates anticipated unless errors found or improvements to underlying grids arise.
  - Primary data format: Geodatabase (preserves NULL values). If downloaded as Esri Shapefile, NULLs are converted to zeros or empty strings.
  - Attribute schemas:
    - Hydrometric Areas with Coastline: HA_NUM, HA_NAME, HA_ID; derived identifier HAx with padding (e.g., HA054).
    - Hydrometric Areas without Coastline: similar identifiers and naming.
    - Groups: fields include area measures (CCAREA_KM2, G_AREA_KM2), identifiers (G_ID, HA_ID), river-related fields (RIVER, RIVER_DS, RIVER_US), and categorization (G_CAT).
    - Sections: extensive fields including cumulative area (CCAREA_KM2), group ID (G_ID), hydrometric area ID (HA_ID), outlet coordinates (OUTF_X, OUTF_Y), river names (RIVER, RIVER_DS, RIVER_US), polygon area (S_AREA_KM2), and identifiers (S_ID, S_DS_ID, S_NAME).
    - Catchments: spatial coordinates for outlet and centroid (EAST/NORTH, CEAST/CNORTH), polygon area (KMSQ), downstream section ID (S_ID).
  - Tables and fields are detailed in the documentation (Tables 1–5) accompanying the dataset.

- Maintenance and Updates
  - No routine updates expected; updates may be released to correct errors or incorporate improvements to underlying rivers or drainage grids.
  - NI-related updates rely on cross-border data availability and may reflect clipping/adjustments to national boundaries.

- Practical Implications for Data Leaders
  - Use Layer Choice:
    - Use Hydrometric Areas with Coastline for cartography and intuitive boundary visualization.
    - Use Hydrometric Areas without Coastline for analyses requiring exact IHDTM grid alignment.
  - Data Governance and Interoperability:
    - Align analyses with IHDTM to ensure consistency across CEH and NRFA datasets.
    - Be mindful of the potential for NULL values in Shapefile exports and plan for Geodatabase usage when possible.
  - Data Quality and Gaps:
    - Be aware of potential gaps in NI data and minor rivers missing in GB; verify coverage for critical analyses.
  - Cross-Border Considerations:
    - Northern Ireland catchments may not be fully hydrologically complete; exercise caution in cross-border studies and when aggregating at higher levels.
  - Documentation and Metadata:
    - Leverage the accompanying tables (Tables 1–5) for detailed schema and field meanings to support data governance, lineage, and reuse.

- Use Cases
  - Hydrological data management and harmonization at multiple spatial scales (from catchments to large hydrometric areas).
  - Integration with NRFA and CEH datasets for river flow measurements, drainage basin studies, or policy-related water resource analyses.
  - Analyses requiring precise IHDTM grid matching (preferable with the without-Coastline layer).