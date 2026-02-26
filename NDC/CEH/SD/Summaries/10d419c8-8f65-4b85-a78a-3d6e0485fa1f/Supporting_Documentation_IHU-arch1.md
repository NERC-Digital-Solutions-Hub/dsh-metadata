# Integrated Hydrological Units of the United Kingdom (IHU)

- Purpose and scope
  - A multi-layer dataset of UK hydrological units at increasing spatial detail, used for organizing river flow measurement and hydrometric data management.
  - Five polygon layers at different resolutions: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
  - The concept extends traditional Hydrometric Areas (circa 1930s) into Integrated Hydrological Units (IHU) with standardized structures and naming.

- Layer overview and key distinctions
  - Hydrometric Areas with Coastline
    - Covers Great Britain and Northern Ireland; used for cartography and broader analyses.
    - Some minor rivers not captured; boundaries based on a 50 m IHDTM grid resolution.
  - Hydrometric Areas without Coastline
    - Same entities as with Coastline but boundaries follow IHDTM, not a smooth coastline.
    - Better suited for analyses requiring exact alignment with IHDTM-gridded data; not ideal for mapping.
  - Groups
    - Medium-size units (~4 to ~3000 km2, typical ~400 km2) composed of one or more Sections.
    - Groups can be combined to form Hydrometric Areas without Coastline.
    - Names reflect major rivers and local areas.
  - Sections
    - Drainage area between two confluences with named watercourses.
    - Each Section belongs to one Group and is linked to one Catchment.
    - Section names often include river names; “UNKNOWN” used when upstream names are not known; “Source” or “Sea” indicate upstream or coastal endpoints.
  - Catchments
    - Finest level of detail; upstream area from the outlet of every Section.
    - Can overlap multiple Sections and Groups; only layer where polygon overlaps occur.
    - Catchments in NI are clipped to the national boundary, so not all hydrological areas are hydrologically complete.

- Data creation, coverage, and maintenance
  - Created by digitizing catchment boundaries from CEH’s IHDTM using an in-house process.
  - Great Britain coastline aligned to the Ordnance Survey Meridian2 coastline; Northern Ireland boundaries from OS GB Panorama data.
  - Islands were assigned to nearby Hydrometric Areas in 2014 to achieve full UK coverage (e.g., Isles of Scilly to HA 49; St Kilda to HA 106, etc.).
  - All boundaries are topologically correct with no gaps or overlaps; NI catchments clipped to national boundary.
  - No routine updates anticipated; updates released if errors are found or underlying data improves.
  - 2015: Hydrometric Areas incorporated into Integrated Hydrological Units (IHU).

- Data accessibility and formats
  - Primary format: Geodatabase (preserves NULLs). Esri Shapefile downloads convert NULLs to zeros or empty strings.
  - Dataset aims to be discoverable and usable with metadata; supports cross-dataset consistency with IHDTM-derived data used in CEH and NRFA.

- Layer-specific attributes (illustrative)
  - Hydrometric Areas with Coastline (HA_NUM, HA_NAME, HA_ID; HA_ID may be derivable as HA + zero-padded HA_NUM)
  - Hydrometric Areas without Coastline (HA_NUM, HA_NAME, HA_ID; similar structure)
  - Groups (e.g., G_ID, G_NAME, G_AREA_KM2, G_CAT, RIVER, RIVER_US/DS, HA_ID, OUTF_SC; area measures in KM2)
  - Sections (e.g., S_ID, S_NAME, HA_ID/HA_NUM, G_ID; S_AREA_KM2; CCAREA_KM2; river names; downstream/upstream relations S_DS_ID)
  - Catchments (e.g., S_ID linkage; geographic coordinates EAST/NORTH and centroids; KMSQ polygon area)
  - Notes: Available in Tables 1–5 within the documentation; attributes define identifiers, names, area measures, river associations, and spatial coordinates.

- Practical considerations for analysts
  - If selecting data formats, be mindful that Shapefile may convert NULLs to zeros or empty strings.
  - Use the Coastline vs Without Coastline layers depending on whether cartography or exact IHDTM alignment is required.
  - NI data limitations: NI catchments are clipped to the national boundary; some hydrological completeness considerations apply.
  - Historical context important for interpretation of numbers and naming conventions, including the long-running hydrometric area numbering system and cross-border considerations.

- Summary of limitations and caveats
  - Some very minor rivers are not captured, even in Great Britain.
  - Northern Ireland data are not as fully detailed (and NI NI-specific completeness concerns apply).
  - Updates are not routine; rely on error-correcting updates and IHDTM improvements.