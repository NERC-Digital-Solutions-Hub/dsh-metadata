# Integrated Hydrological Units of the United Kingdom

## Overview
- A hierarchical set of five polygon layers representing UK hydrological units at increasing spatial detail:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- Used for organizing and analysing river flow measurement, hydrometric data management, and hydrological analyses.
- Administrative and hydrological relationships:
  - Groups contain one or more Sections.
  - Sections belong to a Group and to a Hydrometric Area.
  - Catchments represent the full area upstream from each Section’s outlet; Catchments can overlap multiple Sections and Groups (unique to this layer).
- Layers are produced with long-standing conventions and numbering, including regional identifiers for Irish hydrometric areas and NRFA gauging codes.

## Layer Details

- Hydrometric Areas with Coastline
  - Coarse to fine representation of hydrometric areas with a smooth coastline.
  - Covers Great Britain and Northern Ireland.
  - Used for cartography and general analyses.
  - All areas are single features; islands merged into adjacent areas when necessary.

- Hydrometric Areas without Coastline
  - Uses IHDTM boundaries rather than a coastline, enabling exact edge matching with IHDTM gridded data.
  - Primarily for analyses requiring precise extent/shape matching IHDTM data; less suitable for mapping.

- Groups
  - Medium spatial resolution (~a few hundred km2 typical).
  - Each group contains one or more Sections; groups can combine to form larger Hydrometric Areas without Coastline.
  - Names derived from major rivers and local counties.

- Sections
  - Drainage area between two confluences with named upstream rivers.
  - Each Section links to one Group and to one or more Catchments.
  - Names often composed from rivers; some sections use UNKNOWN when upstream names are lacking.

- Catchments
  - Finest level of detail; upstream area for each Section outlet.
  - Can overlap multiple Sections and Groups; only layer with overlapping polygons.
  - Attributes include upstream/outlet coordinates and area (KMSQ).

## Data Quality and Known Limitations
- Quality tied to the underlying IHDTM 50 m grid resolution.
- Hydrometric Areas with Coastline cover Great Britain and Northern Ireland; other layers currently cover Great Britain only (Northern Ireland not fully represented in those layers due to data availability).
- Some minor rivers may be omitted even in Great Britain.
- NI catchments are clipped to the national boundary; some cross-border hydrology may be incomplete.
- Data are topologically corrected with no gaps or overlaps; every point belongs to exactly one Hydrometric Area (except intended overlaps in Catchments).

## Updates and Maintenance
- No routine, ongoing updates expected.
- Updates may be produced to fix errors or improve underlying river/drainage grid data.

## Data Creation and Provenance
- Boundaries correspond to CEH’s IHDTM-derived catchments; Great Britain coastline aligned to Ordnance Survey Meridian2 coastline; Northern Ireland boundaries/coastlines derived from OS GB Panorama data.
- Islands assigned to the closest existing Hydrometric Area in 2014 to achieve full UK coverage.
- Hydrometric Area numbers follow historical conventions dating back to 1930s; Irish areas receive regional prefixes in numbering.
- The Inland Catchment boundaries are derived in-house from IHDTM data to ensure consistency with CEH and NRFA datasets.

## Attributes and Data Formats
- Primary format: Geodatabase (preserves NULL values; Shapefile converts NULLs to zeros/empty strings).
- Tables (illustrative fields):
  - Hydrometric Areas with Coastline: HA_NUM, HA_NAME, HA_ID
  - Hydrometric Areas without Coastline: HA_NUM, HA_NAME, HA_ID
  - Groups: G_ID, G_NAME, G_AREA_KM2, RIVER, HA_ID, etc.
  - Sections: S_ID, S_NAME, S_AREA_KM2, RIVER, HA_ID, G_ID, S_DS_ID, OUTF_X/Y, S_ID
  - Catchments: S_ID (downstream section), KMSQ (area in km2), EAST/NORTH (outlet coords), CEAST/CNORTH (centroid), etc.
- Some fields are computed or derivable (e.g., HA_ID, HA_NUM combinations).

## Practical Guidance for GIS Specialists
- Choose Hydrometric Areas with Coastline for straightforward cartography and presentation of coast-bound hydrometric units.
- Use Hydrometric Areas without Coastline when exact alignment with IHDTM-gridded data is essential for analysis.
- Leverage Groups and Sections to explore hydrological structure at intermediate resolutions; use Sections to relate to Catchments when analysing upstream drainage and flow relationships.
- Use Catchments for high-detail hydrological analyses, acknowledging potential minor overlaps with other Catchments and that it is the only layer with polygon overlaps.
- Be mindful of data completeness: Northern Ireland representation is limited in some layers; cross-border hydrology may not be fully captured.
- When exporting to Shapefile, expect NULL values to be converted to zeros or empty strings; prefer Geodatabase for preserving NULLs.

## Relationship to Related Datasets
- Underpinning IHDTM data drives boundary definitions.
- NRFA gauging station coding is aligned with hydrometric area numbering, facilitating integration with hydro-meteorological datasets.