# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) comprise five polygon layers representing different spatial resolutions:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Core concept:
  - Hydrometric Areas (coastline vs. non-coastline) are the top-level units; non-coastline boundaries align with the underlying Integrated Hydrological Digital Terrain Model (IHDTM) rather than a smooth coastline.
  - Groups are medium-sized units consisting of one or more Sections; Groups can form Hydrometric Areas without Coastline.
  - A Section is the drainage area between two confluences with named watercourses.
  - Catchments are the full area upstream from an outlet of every Section (they may overlap Sections and Groups; Catchments are the finest detail).

## Scope and Coverage

- Coverage:
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland (subject to data availability; minor rivers may be missing).
  - Other layers: Great Britain only; Northern Ireland data constrained by available river geometries and names.
- NI catchments are clipped to the national boundary; not all hydrometric areas are hydrologically complete for cross-border contexts.
- The UK National River Flow Archive (NRFA) gauging station numbering follows the hydrometric area system.

## History and Data Creation

- Historical basis:
  - Traces back to the Inland Water Survey Committee in the 1930s; naming/numbering published in 1936–37 and 1971–73.
  - The first digital boundary datasets were produced in the 1980s; current IHU boundaries derived to be consistent with CEH and NRFA datasets using IHDTM.
- Integration and updates:
  - In 2014, islands lacking hydrometric areas were merged into the nearest appropriate area (e.g., Isles of Scilly merged with HA 49; St Kilda with HA 106, etc.).
  - In 2015, Hydrometric Areas became part of the Integrated Hydrological Units framework.
- Data creation method:
  - Inland Hydrometric Area boundaries are digital derivations from CEH’s IHDTM using an in-house tool.
  - Coastlines for Great Britain follow the Ordnance Survey Meridian2 coastline; NI boundaries/coastlines from OS GB Panorama data.
  - All boundaries are topologically correct with full UK surface area coverage (subject to the NI cross-border caveat).

## Quality, Limitations, and Maintenance

- Quality baseline:
  - Depends on the IHDTM with a 50 m grid resolution.
  - Some minor rivers are not captured even in Great Britain.
- Known limitations:
  - No routine updates expected; updates only if errors are found or if underlying river/drainage data improve.
  - Some NI data may be incomplete due to cross-border hydrology and dataset availability.
- Data governance:
  - Datasets are primarily distributed as Geodatabase to preserve NULL values; Esri Shapefiles will convert NULLs to zeros or empty strings.

## Layers and Attributes (Overview)

- Hydrometric Areas with Coastline (Table 1)
  - Key fields: HA_NUM, HA_NAME, HA_ID; HA_ID unique; HA_NUM is the area number.
- Hydrometric Areas without Coastline (Table 2)
  - Key fields: HA_NUM, HA_NAME, HA_ID; similar structure to with-coastline layer.
- Groups (Table 3)
  - Key fields: G_ID, G_NAME, HA_ID, OUTF_SC, RIVER, RIVER_US/DS, area metrics (CCAREA_KM2, G_AREA_KM2), categorisation (G_CAT), and qualifiers.
- Sections (Table 4)
  - Key fields: S_ID, S_NAME, HA_ID, G_ID, RIVER information, S_AREA_KM2, S_DS_ID (downstream section), coordinates of outlet (OUTF_X/Y).
  - CCAREA_KM2 provides cumulative catchment area upstream from the section outlet.
- Catchments (Table 5)
  - Key fields: S_ID (downstream section), EAST/NORTH (outlet coordinates), CEAST/CNORTH (centroid coordinates), KMSQ (polygon area in km²).

## Usage and Implications for Monitoring Frameworks

- Purpose:
  - Provide standardized, hierarchical units for organizing river flow measurement, hydrometric data management, and environmental monitoring at sub-national scales.
- Practical considerations for monitoring work:
  - Choose layer(s) appropriate to analysis scale (coastline vs. without coastline depending on data alignment needs).
  - Be mindful of NI data limitations and cross-border hydrology when aggregating or comparing areas.
  - When combining layers (e.g., Groups into Hydrometric Areas without Coastline), ensure topological integrity and alignment with the IHDTM-based boundaries.
  - Validate that metadata and attribute definitions align with project needs, especially given NULL handling in Geodatabases vs. Shapefiles.