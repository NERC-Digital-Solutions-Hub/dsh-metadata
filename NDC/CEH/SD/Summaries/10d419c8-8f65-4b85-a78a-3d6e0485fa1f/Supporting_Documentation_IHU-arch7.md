# Integrated Hydrological Units (IHU) of the United Kingdom

## Introduction and Purpose
- IHU comprises polygon layers representing hydrological units at multiple spatial resolutions.
- Layers included: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, Catchments.
- Without Coastline boundaries follow the Integrated Hydrological Digital Terrain Model (IHDTM) edges rather than a smooth coastline; useful for data alignment with IHDTM rasters, though less suited for cartography.
- Hydrometric Areas are administrative groupings used to organize UK river flow measurement and hydrometric data management.
- Area numbering: GB hydrometric areas are 2-digit codes (1–97) around the coast; islands have prefixed regional identifiers (e.g., Isle of Wight 101). Ireland uses 1–40 with a regional prefix of 2. NRFA gauging station numbers are based on this system with extra digits.
- History: Hydrometric Areas originated in the 1930s; initial digital boundaries produced in the 1980s; current IHU dataset established in 2015.

## Layers and Structure (What each layer represents)
- Hydrometric Areas with Coastline: broad administrative catchment groupings with coastal boundaries.
- Hydrometric Areas without Coastline: same entities as above but boundaries align to IHDTM; better for analytic alignment with grid data, not ideal for mapping.
- Groups: medium-resolution units (typical size ~400 km²; ranges 4–3019 km²). A Group contains one or more Sections and can combine to form Hydrometric Areas without Coastline.
- Sections: drainage area of a watercourse between two confluences with named watercourses; each Group contains one or more Sections; each Section links to one Catchment.
- Catchments: finest-level detail; upstream area from every Section outlet; can overlap with multiple Sections/Groups; only layer permitting overlaps.

## Data Creation and Coverage
- Boundaries created from CEH IHDTM using an in-house program.
- GB coastline defined by Ordnance Survey Meridian2; NI boundary/coastline from OS GB Panorama data.
- Islands merged in 2014 to fit existing hydrometric areas (e.g., Isles of Scilly → HA 49; Lundy → HA 51; St Kilda group → HA 106, etc.).
- All hydrometric boundaries are topologically correct with no gaps or overlaps; every point allocated to exactly one IHU.
- NI catchments are clipped to the national boundary; cross-border catchments may not be hydrologically complete.
- Data coverage: Hydrometric Areas with Coastline includes GB and NI; other layers cover GB only (NI not fully represented due to lack of suitably detailed river geometries/names).

## Quality and Known Limitations
- Overall quality tied to the IHDTM 50 m resolution.
- Even in Great Britain, some minor rivers are not captured.
- No routine updates planned; updates may occur only if errors are found or improvements to underlying rivers or drainage grid data become available.

## Attributes and Data Formats
- Primary format: Geodatabase (preserves NULL values); Esri Shapefile may convert NULLs to zeros or empty strings.
- Tables and key fields:
  - Table 1: IHU Areas with Coastline (HA_NUM, HA_NAME, HA_ID; HA_ID can be derived as HA + zero-padded HA_NUM).
  - Table 2: IHU Areas without Coastline (HA_NUM, HA_NAME, HA_ID; similar to Table 1).
  - Table 3: IHU Groups (fields include CCAREA_KM2, G_ALTNAME, G_AREA_KM2, G_CAT, G_DS_ID, G_ID, G_NAME, G_QUALIFY, HA_ID, OUTF_SC, RIVER, RIVER_DS, RIVER_US).
  - Table 4: IHU Sections (fields include CCAREA_KM2, G_ID, HA_ID, HA_NUM, OUTF_X, OUTF_Y, RIVER, RIVER_DS, RIVER_US, S_AREA_KM2, S_DS_ID, S_ID, S_NAME).
  - Table 5: IHU Catchments (fields include EAST, NORTH, CEAST, CNORTH, KMSQ, S_ID).
- Notes:
  - Tables document Type descriptions (e.g., Name), and provide both descriptive and numeric representations.
  - S_NAME provides the public full section name; S_ID is the unique section identifier; S_DS_ID indicates downstream section (NULL for sea-outlet).

## History
- Origin in the 1930s with Inland Water Survey Committee establishing hydrometric areas in Great Britain; Northern Ireland added later.
- Original naming and numbering published in 1936–37 (GB) and 1971–73 (NI).
- 1980s: initial digital hydrometric boundary dataset digitised; later refinements aligned with IHDTM by CEH and NRFA datasets.
- 2015: Hydrometric Areas incorporated into Integrated Hydrological Units of the United Kingdom (multi-resolution hydrological units).

## Updates and Maintenance
- No routine ongoing updates anticipated.
- Updates may occur if errors are found or if improvements to rivers or drainage grid data become available.

## Practical Guidance for GIS Work
- Choose Coastline vs Without Coastline layers based on cartographic needs vs precise boundary alignment with IHDTM data.
- Use Groups, Sections, and Catchments for hierarchical aggregation, downstream/upstream relationships, and detailed hydrological analysis.
- Pay attention to NI limitations and potential gaps in NI river geometry/name data.
- When exporting to Shapefile, expect NULL values to be converted to zeros/empty strings; prefer Geodatabase for preserving NULLs.
- Ensure topological integrity when editing or integrating with other datasets.