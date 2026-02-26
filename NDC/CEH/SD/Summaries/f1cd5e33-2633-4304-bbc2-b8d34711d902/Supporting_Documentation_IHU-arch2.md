# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) comprise multiple polygon layers that represent different spatial resolutions:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Key concepts
  - Hydrometric Areas with Coastline and without Coastline cover the same entities at the coarsest level; the difference is how the coastline is drawn (smooth coastline vs. IHDTM-based coastline).
  - IHU Groups are the mid-level units, typically around 400 km², consisting of one or more IHU Sections and can be combined to form Hydrometric Areas without Coastline.
  - A Section is the drainage area between two confluences with named watercourses.
  - Catchments represent the full area upstream from an outlet of every IHU Section and may overlap other IHU layers (Catchments are the only layer with polygon overlaps).

- Purpose and use
  - Administratively group river catchments for UK river flow measurement and hydrometric data management.
  - Hydrometric Areas are numbered to support data linkage (e.g., NRFA gauging numbers align with this system).

- Geographical scope and layering
  - Hydrometric Areas with Coastline: covers Great Britain and Northern Ireland.
  - Hydrometric Areas without Coastline: similar entities but with boundaries aligned to IHDTM; better for analyses requiring exact data grid alignment, not ideal for cartography.
  - NI coverage: Northern Ireland catchments are clipped to the national boundary; not every hydrometric area is hydrologically complete for cross-border areas.

- History and data lineage
  - Origin traces to the Inland Water Survey Committee in the 1930s; naming/numbering formalised in historic publications.
  - Initial digital boundaries were created in the 1980s; later versions aligned catchments with IHDTM to ensure consistency with CEH and NRFA datasets.
  - In 2015, Hydrometric Areas became part of the Integrated Hydrological Units framework with multi-level resolution.

- Data creation and maintenance
  - Boundaries are digitally derived from CEH’s IHDTM using an in-house program; coastlines are derived from Ordnance Survey sources.
  - Islands were assigned to nearby hydrometric areas to achieve complete UK surface coverage (examples: Isles of Scilly merged to HA 49; St Kilda group merged to HA 106, etc.).
  - All Hydrometric Area boundaries are topologically correct with no gaps or overlaps; NI catchments are clipped to the national boundary.
  - No routine updates are expected; updates may occur to fix dataset errors or improve underlying river/drainage grid data.

- Data structure and attributes
  - Primary format: Geodatabase (preserves NULL values; shapefiles convert NULLs to zeros or empty strings).
  - Tables and key attributes (highlights):
    - Hydrometric Areas with Coastline: HA_NUM, HA_NAME, HA_ID (constructed as HA + zero-padded number)
    - Hydrometric Areas without Coastline: similar HA_NUM, HA_NAME, HA_ID
    - Groups: various attributes including area, main river, inflow/outflow details, unique IDs (G_ID), and cross-references to HA_ID
    - Sections: area, coordinates of outlet, river names, upstream/downstream identifiers, and unique section IDs (S_ID)
    - Catchments: geographic extent (EAST/NORTH, centroid coordinates, area KMSQ) and downstream S_ID (S_ID) for the most downstream section
  - Notes on usage: When downloading as Esri Shapefile, NULL values may be converted to zeros or empty strings; Geodatabase is recommended to preserve NULLs.

- Quality, limitations, and considerations for analysts
  - Quality is tied to the underlying IHDTM terrain model (50 m grid resolution).
  - Some minor rivers may not be captured even within Great Britain.
  - Northern Ireland data are less complete for hydrometric completeness due to clipping to national boundaries.
  - Some catchment boundaries may be complex (overlaps occur only in the Catchments layer) and require careful handling in analyses.

- Practical implications for environmental monitoring
  - Provides a standardized, hierarchical framework for aggregating and analyzing hydrological data across the UK.
  - Facilitates integration with CEH and NRFA datasets and supports consistent spatial analyses, trend monitoring, and policy performance assessment over time.