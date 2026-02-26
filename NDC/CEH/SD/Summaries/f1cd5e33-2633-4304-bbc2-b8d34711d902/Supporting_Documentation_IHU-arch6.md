# Integrated Hydrological Units of the United Kingdom

- Overview
  - A multi-layer polygon dataset representing hydrological units at increasing levels of spatial detail: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
  - Distinguishes coastal versus IHDTM-based boundaries:
    - Hydrometric Areas with Coastline: suitable for cartography (coastlines).
    - Hydrometric Areas without Coastline: boundaries follow IHDTM precisely, good for data alignment with gridded datasets but not ideal for maps.
  - Layers collectively enable analysis from broad regions to fine upstream catchments.

- Layer structure and definitions
  - Hydrometric Areas with Coastline
    - Administrative groupings of river catchments used for hydrometric data management.
    - Areas are numbered (two-digit codes); Ireland areas have regional prefixes; NRFA gauging numbers are tied to these codes.
  - Hydrometric Areas without Coastline
    - Same entities as with Coastline but boundaries follow IHDTM; better for exact data matching.
  - Groups
    - Medium-resolution units (~400 km² typical; range 4–3019 km²).
    - Composed of one or more Sections; can be combined to form Hydrometric Areas without Coastline.
    - Names derived from major rivers and local counties.
  - Sections
    - Drainage areas between confluences of watercourses of known name.
    - Each Section belongs to a Group and is linked to a Catchment.
    - Section names often include river components; some sections labeled UNKNOWN, Source, or Sea.
  - Catchments
    - Finest-detail units; upstream area from every Section’s outlet.
    - May overlap multiple Sections/Groups; only layer where overlaps occur.

- Data creation and boundaries
  - Boundaries derived digitally from CEH’s Integrated Hydrological Digital Terrain Model (IHDTM) at 50 m resolution.
  - Coastlines from Meridian2; Northern Ireland boundaries/coastlines from OS Panorama data.
  - Islands reassigned in 2014 to nearest existing Hydrometric Areas to ensure full UK coverage (examples: Isles of Scilly merged to HA49; Lundy to HA51; St Kilda cluster to HA106, etc.).
  - All boundaries are topologically correct (no gaps or overlaps; every point allocated to one IHU). Northern Ireland catchments are clipped to the national boundary; some cross-border catchments are not hydrologically complete.
  - Updates: No routine updates; changes occur only to fix errors or incorporate improvements to rivers or drainage grid data.

- Quality, limitations, and maintenance
  - Quality tied to the 50 m IHDTM; some minor rivers may be missing even within Great Britain; NI data may be incomplete.
  - Primary maintenance appears limited to error corrections or data improvements rather than scheduled updates.

- Attributes and data formats
  - Primary format: Geodatabase (preserves NULL values); Esri Shapefile may convert NULLs to zeros or empty strings.
  - Key attribute tables:
    - Tables 1 (Areas with Coastline) and 2 (Areas without Coastline): HA_NUM, HA_NAME, HA_ID (HA_ID often constructed as 'HA' + zero-padded HA_NUM, e.g., HA054).
    - Table 3 (Groups): includes CCAREA_KM2, G_ALTNAME, G_AREA_KM2, G_CAT, G_DS_ID, G_ID, G_NAME, G_QUALIFY, HA_ID, OUTF_SC, RIVER, RIVER_DS, RIVER_US.
    - Table 4 (Sections): includes CCAREA_KM2, G_ID, HA_ID, HA_NUM, OUTF_X/Y, RIVER, RIVER_DS, RIVER_US, S_AREA_KM2, S_DS_ID, S_ID, S_NAME.
    - Table 5 (Catchments): includes EAST, NORTH, CEAST, CNORTH, KMSQ, S_ID (identifier of downstream section).
  - Feature counts: Sections and Catchments each contain 584,556 features.

- Practical usage notes for data support
  - For data integration and self-serve analyses, leverage the hierarchical structure (Areas → Groups → Sections → Catchments) to aggregate or drill down by scale.
  - When exact boundary alignment with gridded data is required, use Hydrometric Areas without Coastline; for map rendering and cartography, prefer Hydrometric Areas with Coastline.
  - Be mindful of NI limitations (incomplete hydrological completeness for some cross-border catchments) and possible missing minor rivers.
  - Plan for potential updates only if underlying IHDTM, drainage data, or boundary data improve; there is no routine update cycle.
  - When exporting to Shapefile, expect NULLs to be converted to zeros or empty strings; prefer Geodatabase for data integrity.

- History and provenance
  - Origins trace back to 1930s Inland Water Survey Committee; evolved through 1936–37 and 1971–73 publications.
  - Early digitisation in the 1980s; 2014 island reassignment to ensure full UK coverage.
  - Incorporated into the Integrated Hydrological Units of the United Kingdom in 2015.