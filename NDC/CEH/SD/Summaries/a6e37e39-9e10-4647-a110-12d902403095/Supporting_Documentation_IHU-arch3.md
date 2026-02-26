# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) comprise five polygon layers with varying spatial detail:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments

- Key concepts and relationships
  - Hydrometric Areas (coastline vs non-coastline) represent administrative groupings of river catchments used for organizing river flow measurement and data management.
  - Groups are medium-detail units that consist of one or more Sections; Groups can be combined to form Hydrometric Areas without Coastline.
  - Sections are drainage areas between two confluences with named watercourses; each Section belongs to one Group and one associated Catchment.
  - Catchments are the finest-level units, representing the full area upstream from each Section’s outlet; Catchments can overlap within the dataset (unlike other layers which are non-overlapping).

- Coverage and scope
  - Hydrometric Areas with Coastline cover Great Britain and Northern Ireland; other layers primarily cover Great Britain.
  - Northern Ireland data for river geometries and names at sufficient detail is not yet available for all layers.
  - Some minor rivers are not captured even in Great Britain; NI catchments are clipped to the national boundary, and cross-border catchments exist but are not always hydrologically complete in NI.

- History and lineage
  - Hydrometric Areas originated in the 1930s to facilitate integrated hydro-meteorological data collection.
  - Initial digital boundaries were created in the 1980s; later versions aligned with IHDTM to ensure consistency with CEH and NRFA datasets.
  - In 2015, Hydrometric Areas became part of the Integrated Hydrological Units (IHU) with multiple resolution levels.

- Data creation and maintenance
  - Boundaries are digitally derived from CEH’s IHDTM using in-house tooling; GB coastline uses the Ordnance Survey Meridian2 coastline; NI boundaries/coastlines use OS GB Panorama data.
  - Islands were assigned to the nearest appropriate Hydrometric Area in 2014 to achieve full UK coverage.
  - All Hydrometric Area boundaries are topologically correct with no gaps or overlaps (every UK point assigned to one IHU).
  - No routine dataset updates are planned unless errors are found or improvements to underlying rivers or drainage data become available.

- Data formatting and access
  - Primary format: Geodatabase (preserves NULL values); Esri Shapefile exports will convert NULLs to zeros or empty strings.
  - Tables describe attributes for each layer, including area codes, names, identifiers, and geographic coordinates.

- Attributes by layer (highlights)
  - Areas with Coastline: HA_NUM, HA_NAME, HA_ID
  - Areas without Coastline: HA_NUM, HA_NAME, HA_ID
  - Groups: G_ID, G_NAME, G_AREA_KM2, RIVER, HA_ID, OUTF_SC, and related descriptors
  - Sections: S_ID, S_NAME, S_AREA_KM2, RIVER, RIVER_US, RIVER_DS, HA_ID, G_ID, S_ID relationships, outlet coordinates
  - Catchments: KMSQ (area in km2), East/North coordinates, centroid coordinates, S_ID linkage to downstream section, and related identifiers

- Practical considerations for monitoring frameworks
  - The multi-level IHU structure supports scalable monitoring across national and sub-national scales, with clear lineage to the IHDTM terrain model for consistency with other datasets.
  - Data governance and openness: metadata detail is substantial, but NULL handling and potential data gaps (especially for NI) must be considered when designing dashboards and analyses.
  - Topology and completeness: non-overlapping layers (except catchments) simplify aggregation; awareness of NI clipping and cross-border catchments is essential for cross-border studies.
  - Historical context and naming conventions: numbering and naming conventions traceable to historical sources, aiding longitudinal analyses and data integration with NRFA and other hydrometric datasets.