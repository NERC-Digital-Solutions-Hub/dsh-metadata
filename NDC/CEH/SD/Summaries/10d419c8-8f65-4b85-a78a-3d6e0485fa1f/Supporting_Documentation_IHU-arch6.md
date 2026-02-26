# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) consist of five polygon layers that represent hierarchical hydrological units at different spatial resolutions:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments

- Key concepts and relationships
  - Hydrometric Areas with Coastline and without Coastline represent the same entities at the coarsest level; the difference is how coastlines are delineated (smooth UK coastline vs IHDTM boundary).
  - IHU Groups are medium-sized units consisting of one or more IHU Sections; Groups can be combined into Hydrometric Areas without Coastline.
  - A Section is the drainage area of a watercourse between two confluences with named rivers.
  - Catchments are the full area upstream from an outlet of every IHU Section (and are the finest level of detail), though some catchments may overlap with multiple IHU Sections or Groups.

- Coverage and constraints
  - Hydrometric Areas with Coastline cover Great Britain and Northern Ireland.
  - All other layers currently cover Great Britain only; Northern Ireland data for river geometries and names at detailed layers are not provided.
  - Minor rivers may be omitted even within Great Britain.
  - Catchments are topologically processed to avoid gaps or overlaps; NI catchments are clipped to the national boundary, so not all hydrological relationships are spatially complete across the UK.

- Data creation and maintenance
  - Boundaries are digitally derived from CEH's Integrated Hydrological Digital Terrain Model (IHDTM) with a 50 m grid; GB coastline uses Ordnance Survey Meridian2 coastline; NI boundaries/coastlines use GB Panorama data.
  - In 2014, islands with undefined Hydrometric Areas were merged into existing areas to achieve full UK coverage (examples: Isles of Scilly merged with HA 49, St Kilda group with HA 106, etc.).
  - No routine updates are planned; updates may occur to fix errors or improve the underlying drainage data or rivers grid.

- Layer content and attributes (high-level)
  - Tables describe the attributes for each layer:
    - Areas with Coastline: HA_NUM, HA_NAME, HA_ID; optional HA_ID derivation as HAXXX.
    - Areas without Coastline: similar identifiers for hydrometric areas.
    - Groups: G_ID, G_NAME, G_AREA_KM2, HA_ID, river-related fields, and area/catchment metrics.
    - Sections: S_ID, S_NAME, RIVER fields, S_AREA_KM2, cumulative area (CCA), coordinates of outlets, and links to parent group (G_ID) and downstream section (S_DS_ID).
    - Catchments: S_ID for downstream section, catchment area (KMSQ), centroid coordinates, and outlet coordinates.
  - Data formats: Primarily stored as a Geodatabase to preserve NULL values; Esri Shapefile exports convert NULLs to zeros or empty strings.

- Practical considerations for use
  - The GB and NI distinction is important for cartography vs analysis; use Hydrometric Areas with Coastline for mapping that includes NI, and use Areas without Coastline when exact IHDTM-aligned extents are required.
  - The NI data limitations mean cross-border hydrology may be incomplete in the dataset.
  - Be mindful that Catchments can overlap sections or groups; this is the unit with the highest spatial detail, and overlaps reflect upstream areas that may cross administrative boundaries.

- Historical context
  - The hydrometric area framework originated in the 1930s to facilitate integrated hydro-m meteorological data collection; the current IHU dataset became part of the integrated UK hydrological units in 2015, aligning with CEH and NRFA data standards.