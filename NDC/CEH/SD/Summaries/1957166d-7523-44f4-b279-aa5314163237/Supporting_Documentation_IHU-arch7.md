# Integrated Hydrological Units (IHU) of the United Kingdom

## Overview and Layer Structure
- The IHU dataset comprises five polygon layers representing hierarchical hydrological units at different spatial resolutions:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- The two Hydrometric Areas layers represent the same entities; the difference is how coastal boundaries are drawn:
  - with Coastline: uses a smooth UK coastline
  - without Coastline: boundaries follow the IHDTM grid, aligning with gridded data but less suitable for cartography
- IHU Groups are medium-resolution units consisting of one or more Sections; Groups can be combined to form Hydrometric Areas without Coastline
- A Section is the drainage area between two confluences with named watercourses
- Catchments represent the full area upstream from an outlet of every Section; Catchments are the finest detail and can overlap with other IHU layers

## Purpose and Use
- IHUs are administrative groupings of river catchments used to organize UK river flow measurement and hydrometric data management
- Hydrometric Areas are numbered with a two-digit code (and prefixes for certain islands); NRFA gauging station numbers are based on this system
- Data are designed to support GIS analyses and map-based visualisations, facilitating integration with CEH and NRFA datasets

## Data Creation and Lineage
- Boundaries are digitally derived from CEH’s Integrated Hydrological Digital Terrain Model (IHDTM) with a 50 m grid resolution
- Coastlines for the main GB layer are derived from the Ordnance Survey Meridian2 coastline; NI boundaries and coastlines from OS GB Panorama
- The 2014 island reassignment ensured full UK coverage by merging undefined islands into nearby areas (examples include Isles of Scilly to HA49, St Kilda group to HA106, etc.)
- All Hydrometric Area boundaries are topologically correct (no gaps or overlaps); every location is allocated to a single IHU
- Northern Ireland catchments are clipped to the national boundary and may not be hydrologically complete within the dataset

## Layer Details and Attributes
- Primary format: Geodatabase (preserves NULL values; Shapefile converts NULLs to zeros or empty strings)
- Attribute summaries:
  - Areas with Coastline (HA): HA_NUM, HA_NAME, HA_ID
  - Areas without Coastline: HA_NUM, HA_NAME, HA_ID
  - Groups: fields include catchment area, alternative names, river information, identifiers, and hierarchy (G_ID, G_NAME, HA_ID, RIVER, etc.)
  - Sections: includes cumulative area (CCAREA_KM2), flow identifiers (G_ID, HA_ID), outlet coordinates (OUTF_X/Y), river names, section identifiers, and area (S_AREA_KM2, S_ID, S_NAME)
  - Catchments: outlet coordinates (EAST/NORTH), centroid coordinates (CEAST/CNORTH), area (KMSQ), downstream section ID (S_ID)
- The dataset contains 115 HA features with Coastline, 105 HA features without Coastline, 405 Groups, and 584,556 Sections and Catchments each

## Quality, Limitations, and Coverage
- Quality tied to the IHDTM’s 50 m resolution
- Coverage:
  - Hydrometric Areas with Coastline: Great Britain and Northern Ireland
  - Hydrometric Areas without Coastline, Groups, Sections, Catchments: Great Britain only (NI data not at suitable resolution)
- Limitations:
  - Some minor rivers are not captured even in Great Britain
  - NI hydrometric areas may not be completely hydrologically coherent within this dataset
- Updates:
  - No routine updates are planned
  - Updates may occur if errors are found or if improvements to rivers or drainage data become available

## How to Use in GIS Workflows
- For cartographic products, prefer Hydrometric Areas with Coastline
- For analyses requiring exact alignment with IHDTM-gridded data, use Hydrometric Areas without Coastline
- When downloading as Shapefile, account for NULL value handling (they may be converted to zeros or empty strings)
- Use the hierarchical structure (Areas > Groups > Sections > Catchments) to aggregate or downscale hydrological information as needed
- Be aware of cross-border limitations in NI data and the potential for incomplete hydrological completeness in NI catchments

## Notable Notes
- The dataset reflects historical conventions and numbering tied to UK hydrometric data governance
- Islands were explicitly reassigned in 2014 to ensure complete UK coverage, with explicit mappings to nearby hydrometric areas
- Catchments are the only IHU layer where polygons can overlap