# Integrated Hydrological Units of the United Kingdom

## Overview and purpose
- Provides a multi-level set of polygon layers representing UK hydrological units at varying spatial detail.
- Used for organizing river flow measurement, hydrometric data management, and hydrological analyses.

## Layers and hierarchy
- Hydrometric Areas with Coastline: broadest coastal/non-coastal units.
- Hydrometric Areas without Coastline: same entities as with coastline but boundaries follow IHDTM; preferred for precise IHDTM alignment, not ideal for cartography.
- Groups: medium-scale units (~4 km² to ~3019 km²) that comprise one or more Sections.
- Sections: drainage areas between confluences with named watercourses; part of a Group and linked to a Catchment.
- Catchments: finest detail; upstream area from each Section outlet; may overlap multiple Sections/Groups.

## Geography, coverage, and data quality
- Coarsest layers (with/without Coastline) cover Great Britain and Northern Ireland coastline differences relate to boundary delineation; NI catchments are clipped to national boundary.
- All other layers cover Great Britain only; some minor rivers may not be captured even in GB.
- Hydrography rooted in the 50 m resolution Integrated Hydrological Digital Terrain Model (IHDTM).
- Islands were merged into nearby hydrometric areas in 2014 to achieve full UK coverage (e.g., Isles of Scilly, Lundy, St Kilda group, etc.).
- Catchment boundaries in Northern Ireland are not hydrologically complete due to cross-border limitations.

## Data creation, history, and maintenance
- Boundaries created by digitising from IHDTM-derived catchments; GB coastline aligned with Ordnance Survey Meridian2; NI boundaries/coastlines from OS GB Panorama data.
- In 2014, islands with undefined areas were merged into the nearest existing Hydrometric Area.
- In 2015, Hydrometric Areas were incorporated into the Integrated Hydrological Units (IHU) framework.
- No routine dataset updates are planned; updates may occur if errors are found or underlying data improve.

## Attribute schema (highlights)
- Hydrometric Areas with Coastline (HA_NUM, HA_NAME, HA_ID; HA_ID present, with optional HA_ID that can be constructed as HA + zero-padded HA_NUM).
- Hydrometric Areas without Coastline: similar HA_NUM, HA_NAME, HA_ID structure.
- Groups: attributes include area measures (CCAREA_KM2, G_AREA_KM2), identifiers (G_ID), names (G_NAME), river context (RIVER, RIVER_DS, RIVER_US), and cross-reference to outflow (OUTF_SC).
- Sections: include cumulative area (CCAREA_KM2), group reference (G_ID), IHUA identifiers (HA_ID, HA_NUM), outlet coordinates (OUTF_X, OUTF_Y), river names (RIVER, RIVER_DS, RIVER_US), and identifiers (S_ID, S_NAME, S_DS_ID).
- Catchments: include spatial extent (KMSQ), outlet/centroid coordinates, and downstream section reference (S_ID).

## Data formats and access
- Primary format: Geodatabase (preserves NULL values).
- Esri Shapefile option may convert NULLs to zeros or empty strings; be mindful during data extraction.

## Practical considerations for analysts
- Use Hydrometric Areas with Coastline for cartographic display; use Hydrometric Areas without Coastline when you need exact IHDTM alignment for analyses.
- The dataset provides topologically valid boundaries with full UK coverage when including islands; NI boundaries may affect hydrological completeness for cross-border catchments.
- Be aware of potential data gaps (minor rivers not captured) and that routine updates are not planned unless errors or improvements are identified.
- Attribute fields enable identification, area calculations, river context, and cross-layer linking (Sections to Groups to Catchments), facilitating cross-referencing with hydrometric data and other CEH/NRFA datasets.