# Integrated Hydrological Units of the United Kingdom

- Purpose and scope
  - Provides a hierarchical set of polygon layers representing hydrological units at multiple spatial resolutions for the United Kingdom.
  - Layers include: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
  - Hydrometric Areas with Coastline and without Coastline cover Great Britain; Northern Ireland coverage is partial due to river geometry data availability.
  - Catchments represent the full area upstream from outlets of every Section and are the finest level of detail (with some overlaps between Catchments and Sections/Groups).

- Layer definitions and relationships
  - Hydrometric Areas with Coastline: administrative groupings of river catchments for hydrometric data management; numbered codes (HA_NUM, HA_ID, HA_NAME).
  - Hydrometric Areas without Coastline: same entities as with Coastline but boundaries follow IHDTM; better for alignment with IHDTM-based data but less suitable for cartography.
  - Groups: medium-sized units (~4 km² to ~3019 km² typical; around 400 km² common); consist of one or more Sections; can combine to form Hydrometric Areas without Coastline.
  - Sections: drainage areas between confluences; each Section links to a Group and to a Catchment; names often include river names; some portions marked UNKNOWN or SEA.
  - Catchments: upstream area from the outlet of every Section; smallest and most detailed unit; Catchments can overlap multiple Sections/Groups.

- Data creation and lineage
  - Boundaries derived from CEH Integrated Hydrological Digital Terrain Model (IHDTM, 50 m resolution).
  - Coastlines for Great Britain based on Ordnance Survey Meridian2; NI boundaries/coastlines from GB Panorama data.
  - Islands incorporated in 2014 by assigning to the nearest appropriate Hydrometric Area (e.g., Isles of Scilly, Lundy, St Kilda group, etc.).
  - All Hydrometric Area boundaries are topologically correct with no gaps or overlaps; catchment boundaries in Northern Ireland are clipped to the national boundary (not necessarily hydrologically complete across borders).
  - Data creation and integration occurred around 2014–2015; Hydrometric Areas became part of IHU in 2015.

- Quality, limitations, and known issues
  - Quality tied to underpinning IHDTM (50 m grid); minor rivers may be omitted even in Great Britain.
  - NI coverage is incomplete for hydrometric detail; cross-border hydrology not fully represented.
  - Some river names in Sections may be UNKNOWN or have limited upstream information.
  - NI catchments are clipped to the national boundary; not all hydrological boundaries are complete across the entire island of Ireland.
  - The dataset does not include routine updates; updates occur only if errors are found or if improvements to underlying river/draingage data become available.

- Attributes and data model
  - Primary format: Geodatabase (preserves NULL values; Shapefile may convert NULLs to zeros or empty strings).
  - Tables (summarized):
    - Hydrometric Areas with Coastline: HA_NUM, HA_NAME, HA_ID, with derived HA_ID and codes.
    - Hydrometric Areas without Coastline: HA_NUM, HA_NAME, HA_ID, with equivalent identifiers.
    - Groups: attributes include area measures (CCAREA_KM2), group name (G_NAME), river context (RIVER), identifiers (G_ID, HA_ID), and hierarchical links (OUTF_SC, etc.).
    - Sections: attributes include cumulative area (CCAREA_KM2), river names (RIVER, RIVER_DS, RIVER_US), spatial extents (OUTF_X/Y, S_AREA_KM2), section IDs (S_ID), and downstream/upstream references (S_DS_ID).
    - Catchments: spatial extents and identifiers related to downstream Section (S_ID), along with coordinates (EAST/NORTH, CEAST/CNORTH) and area (KMSQ).
  - NULL handling: Shapefile conversion may convert NULLs to zeros or empty strings; consider using Geodatabase for preserving NULLs.

- Practical considerations for data stewards
  - Ensure metadata remains aligned with IHDTM-derived lineage and 2014 island-merging decisions.
  - Monitor for updates only when underlying IHDTM or hydrographic data improve; plan for occasional data ingests rather than routine updates.
  - Be aware of coverage gaps in Northern Ireland and potential non-hydrologically complete cross-border areas when conducting analyses.
  - When distributing data, prefer Geodatabase to preserve NULLs; warn users about potential NULL-to-zero/empty-string conversions in shapefile downloads.
  - Document any interpretation notes for areas with UNKNOWN river names or coastal boundaries, and maintain provenance for island mergers and boundary adjustments.
  - Consider alignment needs with IHDTM-based data users; the "without Coastline" layer provides precise IHDTM boundary matching, while the "with Coastline" layer is better for cartography.