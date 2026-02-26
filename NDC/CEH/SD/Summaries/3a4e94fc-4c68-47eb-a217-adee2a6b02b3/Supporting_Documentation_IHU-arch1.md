# Integrated Hydrological Units of the United Kingdom

## Overview and purpose
- The Integrated Hydrological Units (IHU) comprise multiple polygon layers that represent different levels of spatial detail for UK hydrology: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
- Hydrometric Areas with Coastline and without Coastline cover the same entities; the difference lies in coastal boundary treatment. The without-coastline version follows the IHDTM boundary for precise matching to gridded data rather than a smooth coastline.
- IHUs were developed to provide hierarchical, scalable hydrological units for organizing river flow measurement, data management, and analyses. They extend the traditional Hydrometric Areas concept (in use since the 1930s) by adding higher-resolution layers.

## Layers and spatial hierarchy
- Hydrometric Areas with Coastline
  - Covers Great Britain and Northern Ireland; used for cartography and broad analyses.
  - Some minor rivers may not be captured.
- Hydrometric Areas without Coastline
  - Same entities as with Coastline but boundaries align with IHDTM; best for analyses requiring exact IHDTM-grid alignment.
- Groups
  - Medium-scale units (~400 km² typical; ranges from ~4 km² to ~3019 km²).
  - Consist of one or more Sections; can be combined to form Hydrometric Areas without Coastline.
  - Names derive from major rivers and local counties.
- Sections
  - Drainage area between two confluences of named watercourses.
  - Each Section is associated with one Group; contains fields indicating upstream/downstream relationships and section-specific attributes.
  - Some sections use UNKNOWN for river names; SOURCE indicates no upstream sections; SEA indicates outflow to the sea.
- Catchments
  - Finest level of detail; upstream area from the outlet of every Section.
  - Catchment polygons may overlap multiple Sections and Groups; this is the only layer where overlaps occur.

## Data creation and processing
- Boundaries are digitally derived from CEH's IHDTM using an in-house program; coastline for Great Britain uses the Ordnance Survey Meridian2 coastline; Northern Ireland boundaries come from OS GB Panorama data.
- 2014: Islands without defined Hydrometric Areas were merged into the nearest existing area to achieve full UK coverage (examples: Isles of Scilly merged with HA 49; St Kilda group merged with HA 106).
- All Hydrometric Area boundaries are topologically correct with no gaps or overlaps; every point in the country belongs to exactly one Hydrometric Area.
- Northern Ireland catchments are clipped to the national boundary, so some cross-border catchments are not hydrologically complete.
- Data creation notes also include historical context about numbering conventions and the evolution from earlier datasets to the current IHU framework.

## Attributes and data format
- Primary format is Geodatabase (preferred for preserving NULL values); Esri Shapefile exports convert NULLs to zeros or empty strings.
- Layer-specific attributes (highlights):
  - Areas with Coastline: HA_NUM, HA_NAME, HA_ID, (HA_ID usable as HA and number-based identifier; HA_ID may be omitted in some exports).
  - Areas without Coastline: HA_NUM, HA_NAME, HA_ID, similar structure to with Coastline.
  - Groups: CCAREA_KM2 (catchment area upstream of the group outflow), G_ALTNAME, G_AREA_KM2, G_CAT, G_ID, G_NAME, G_QUALIFY, HA_ID, OUTF_SC, RIVER, RIVER_DS, RIVER_US.
  - Sections: CCAREA_KM2, G_ID, HA_ID, HA_NUM, OUTF_X/Y (outlet coordinates), RIVER, RIVER_DS, RIVER_US, S_AREA_KM2, S_DS_ID, S_ID, S_NAME.
  - Catchments: EAST/NORTH (outlet coordinates), CEAST/CNORTH (centroid coordinates), KMSQ (area), S_ID (downstream section identifier).
- Dataset includes a large number of features (e.g., 584,556 features in Sections and Catchments combined).

## Quality, limitations, and maintenance
- Quality depends on the IHDTM (50 m grid resolution).
- Coverage limitations: Northern Ireland data lack suitable river geometry detail for some layers; thus not all NI rivers are included at the same level as GB.
- Some minor rivers may be omitted even in Great Britain.
- No routine weekly/annual updates are planned; updates may occur to correct errors or incorporate improved underlying river/drainage data.
- NI catchments are clipped to the national boundary, so some cross-border hydrological completeness is not represented.

## Practical use for analysts
- Layer choice matters:
  - Use Hydrometric Areas with Coastline for cartographic outputs and broad-scale analyses.
  - Use Hydrometric Areas without Coastline when exact IHDTM-grid alignment is required for data integration with gridded datasets.
- Analyses can leverage the hierarchical structure (Areas > Groups > Sections > Catchments) to aggregate or disaggregate data, track upstream areas, and relate hydrometric measurements to specific hydrological units.
- Be mindful of data provenance and metadata; remember the handling of NULLs in shapefile exports and the potential absence of NI detail.
- When interpreting section data, account for labels like UNKNOWN, SOURCE, and SEA to understand river naming and connectivity.
- If combining with NRFA data, note that NRFA gauging station numbers align with the hydrometric area numbering system described in the documentation.