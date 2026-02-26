# Integrated Hydrological Units (IHU) of the United Kingdom

## Purpose and Scope
- Provides hierarchical hydrological units at multiple spatial resolutions for organizing UK river flow measurement and hydrometric data management.
- Five polygon layers representing increasing spatial detail:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Hydrometric Areas are administrative groupings of river catchments; Sections are drainage areas between confluences of named rivers; Catchments are full upstream areas from each Section outlet.

## Layer Overview and Relationships
- Hydrometric Areas with Coastline vs without Coastline
  - Both represent the same functional entities; difference is boundary treatment:
    - With Coastline uses a smooth UK coastline for cartography.
    - Without Coastline follows the IHDTM edges to match gridded data precisely.
  - Without Coastline is better for analyses requiring precise IHDTM boundary matching; not ideal for cartography.
- Groups
  - Medium-scale units (~4–4000 km2, commonly ~400 km2).
  - Comprised of one or more Sections; can form Hydrometric Areas without Coastline.
  - Named by major rivers and local areas.
- Sections
  - Drainage area between two confluences of named watercourses.
  - Each Section belongs to one Group and to one Catchment.
  - Names built from rivers; “UNKNOWN” used where upstream names are not known.
- Catchments
  - Finest detail; upstream area from each Section outlet.
  - Can overlap multiple Sections and Groups; only layer where overlaps occur.

## Coverage, Limitations, and Data Quality
- Coverage
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland.
  - Other layers: Great Britain only (no suitable detailed NI river geometries in these layers at present).
- Limitations
  - Some minor rivers not captured even in Great Britain.
  - Northern Ireland catchment boundaries are clipped to national boundary; some cross-border catchments may be incomplete hydrologically.
- Quality
  - Quality tied to the underlying IHDTM with a 50 m grid resolution.
- Islands and Boundaries
  - In 2014, islands with undefined Areas were merged into nearby Areas to achieve full UK coverage (examples: Isles of Scilly, Lundy, Grassholm, St Kilda cluster, etc.).

## Data Creation, Maintenance, and Updates
- Creation basis
  - Boundaries derived from CEH IHDTM via in-house tooling.
  - Great Britain coastline aligned to the Ordnance Survey Meridian2 coastline; Northern Ireland boundaries to OS GB Panorama.
  - All Hydrometric Areas created as single features; islands merged as described.
  - Islands merged based on geographic proximity and existing numbering conventions.
- Maintenance
  - No routine updates planned.
  - Updates may occur only to fix errors or incorporate improvements to underlying river or drainage data.
- Topology
  - All boundaries processed to be topologically correct with no gaps or overlaps.

## History and Provenance
- Hydrometric Areas originated in the 1930s framework for hydro-meteorological data collection; numbering conventions later formalized in national publications.
- The Inland Water Survey Committee established the framework; Northern Ireland designations followed later.
- The first digital Hydrometric Area boundary dataset emerged in the 1980s; current IHUs (as a multi-level dataset) were established in 2015.
- 2014 island merges and 2015 integration into the Integrated Hydrological Units framework.

## Attributes and Data Formats
- Primary format: Geodatabase (preserves NULL values; shapefiles convert NULLs to zeros or empty strings).
- Shapefile downloads will alter NULL values, so use Geodatabase to preserve NULLs.
- Attribute highlights (Tables 1–5, summarized):
  - Areas with Coastline: HA_NUM, HA_NAME, HA_ID, and generated HA_ID-like code (e.g., HA054).
  - Areas without Coastline: similar HA_NUM, HA_NAME, HA_ID as above.
  - Groups: include area metrics, alternative names, river-based identifiers, inflow/outflow references, and associated HA_ID.
  - Sections: include cumulative area, river names, upstream/downstream references, section identifiers (S_ID), section names, coordinates for outlet, and area of the section.
  - Catchments: include outlet coordinates (EAST/NORTH), centroid (CEAST/CNORTH), polygon area (KMSQ), downstream Section ID (S_ID), and other S_ID-related references.
- Note: If downloading as Shapefile, NULL values may convert to zeros or empty strings.

## Practical Notes for Analysts
- Use IHU layers to align and aggregate hydrometric data with standardized hydrological units for trend analysis and policy performance assessment.
- Prefer Hydrometric Areas without Coastline for analyses requiring exact IHDTM boundary alignment; use Areas with Coastline for cartographic outputs.
- Leverage the hierarchical structure (Areas → Groups → Sections → Catchments) to scale analyses from broad regional insights to fine-grained drainage areas.
- Be mindful of NI coverage and potential data gaps in small rivers; verify completeness for cross-border studies.
- When distributing or exporting data, prefer Geodatabase formats to preserve NULL values and data integrity.