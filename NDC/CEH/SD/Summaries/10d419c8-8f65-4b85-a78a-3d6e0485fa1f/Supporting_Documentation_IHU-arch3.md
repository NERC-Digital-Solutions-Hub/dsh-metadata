# Integrated Hydrological Units of the United Kingdom

## Overview
- The Integrated Hydrological Units (IHU) of the United Kingdom consist of five polygon layer levels that represent different spatial resolutions: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
- The coarsest two layers (with/without coastline) represent the same entities; the boundary difference is that the coastline version uses the smooth UK coastline, while the without-coastline version follows the IHDTM 1 boundary.
- IHUs provide a hierarchical framework for organizing UK river catchments and hydrometric data management.

## The IHU Layers
- Hydrometric Areas with Coastline: administrative groupings of river catchments used for river flow measurement and data management; nationwide coverage for Great Britain and Northern Ireland.
- Hydrometric Areas without Coastline: same entities as above but boundaries follow IHDTM for precise extents, better suited for matching gridded IHDTM data.
- Groups: medium-resolution units (typical size ~400 km²) that comprise one or more Sections; Groups can be combined to form Hydrometric Areas without Coastline.
- Sections: drainage areas between two confluences with named watercourses; each Section belongs to one Group and to one Catchment.
- Catchments: the finest level, representing the full area upstream from an outlet of every Section; these are the only IHU layer where polygons may overlap.

## Data Quality, Coverage, and Limitations
- Quality is tied to the underlying IHDTM, which has a 50 m grid resolution.
- Coverage: Hydrometric Areas with Coastline covers Great Britain and Northern Ireland; other layers cover Great Britain only due to data availability for river geometries and names in Northern Ireland.
- Some minor rivers are not captured even in Great Britain.
- No routine updates are expected; updates may occur if errors are found or if improvements to underlying river or drainage grid data become available.
- Northern Ireland catchments are clipped to the national boundary, so not every hydrometric area is hydrologically complete across borders.
- Islands were merged into nearby areas in 2014 to achieve full UK coverage (e.g., Isles of Scilly merged with HA 49; St Kilda group merged with HA 106, etc.).

## History and Data Provenance
- Hydrometric Areas have their origins in the 1930s Inland Water Survey Committee framework; numbering conventions are described in historical publications.
- The initial digital boundary dataset was developed in the 1980s; subsequent versions realigned inland catchment boundaries with IHDTM to ensure consistency with CEH and NRFA datasets.
- In 2015, Hydrometric Areas became part of the Integrated Hydrological Units framework, enabling multi-level hydrological units.

## Data Creation and Processing
- Inland Hydrometric Area boundaries are derived from CEH's IHDTM using an in-house program.
- Coastal and NI boundaries are sourced from the Ordnance Survey Meridian2 coastline and OS GB Panorama respectively.
- Islands and offshore areas were allocated to the nearest appropriate hydrometric area (as of 2014).
- All Hydrometric Areas are topologically correct (no gaps or overlaps); every point in the country is allocated to exactly one Hydrometric Area.
- For Great Britain, NI cross-border catchments are not always hydrologically complete due to clipping to national boundaries.

## Attributes and Data Formats
- Primary format is Geodatabase to preserve NULL values (Esri Shapefile converts NULL to empty strings or zeros).
- Coordinate/identity schemas and descriptive attributes are defined for each layer (see Tables 1–5 in the documentation):
  - Areas with Coastline: HA_NUM, HA_NAME, HA_ID, etc.
  - Areas without Coastline: HA_NUM, HA_ID, HA_NAME, etc.
  - Groups: identifiers, areas, river references, and descriptive fields (G_ID, G_NAME, G_AREA_KM2, etc.).
  - Sections: spatial extent, upstream/downstream identifiers, river names, area, and topology fields (S_ID, S_NAME, RIVER, S_DS_ID, etc.).
  - Catchments: outlet coordinates, centroid, area (KMSQ), downstream section ID, etc.
- Naming conventions link to hydrometric areas (HA_ID), groups (G_ID), sections (S_ID), and downstream relations (S_DS_ID).

## Updates and Maintenance
- No routine dataset updates are expected; updates may occur if data errors are found or if improvements to underlying terrain or river data become available.
- Some correctional updates may be implemented to maintain topological consistency or to reflect data improvements.

## Implications for Monitoring Framework Authors
- Use the hierarchical structure (Areas → Groups → Sections → Catchments) to organize monitoring programs and to aggregate or disaggregate environmental indicators.
- Choose the appropriate layer for analysis:
  - Use Hydrometric Areas with Coastline for cartography and broad territorial analyses.
  - Use Hydrometric Areas without Coastline for precise matching with IHDTM-based gridded data.
- Ensure data governance considerations:
  - Track data provenance and lineage (IHDTM-derived boundaries; boundary derivation steps).
  - Be mindful of NULL handling when exporting to Shapefiles; prefer Geodatabase for analyses requiring NULL preservation.
  - Recognize potential data gaps in Northern Ireland and minor rivers; document any caveats in monitoring reports.
- Maintain consistency in identifiers (HA_ID, G_ID, S_ID) to enable reproducible analyses and integration with NRFA and other datasets (e.g., gauging station references).
- Plan for data quality and metadata improvements, as updates are not routine and depend on error corrections or better underlying data.
- Acknowledge boundary-related caveats:
  - NI catchments clipped to national boundary; cross-border hydrology may require supplementary data for hydrological completeness.
  - Island mergers implemented in 2014; verify current assignments if using historical analyses.