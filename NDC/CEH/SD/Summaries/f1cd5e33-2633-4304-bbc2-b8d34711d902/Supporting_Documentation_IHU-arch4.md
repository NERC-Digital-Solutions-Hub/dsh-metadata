# Integrated Hydrological Units of the United Kingdom

- Overview
  - A multi-layered hydrological dataset for the UK, comprising: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
  - Coarse vs fine boundaries: Areas with Coastline and without Coastline share the same entities at the broadest level; the boundary difference is how the coastline is represented (smooth UK coastline vs IHDTM-based coastline).
  - Catchments represent the finest detail and upstream extent from each Section’s outlet; sections are drainage areas between confluences; Groups aggregate Sections; Areas aggregate Groups into larger hydrological units.
  - Coverage: Hydrometric Areas with Coastline cover Great Britain and Northern Ireland; other layers cover Great Britain only due to data limitations for Northern Ireland. Minor rivers may be missing even in Great Britain.

- Layer Details and Relationships
  - Hydrometric Areas with Coastline and without Coastline: contain area-level boundaries and identifiers (HA_NUM, HA_ID) and names (HA_NAME); without Coastline uses IHDTM-based boundaries for precise matching with gridded data.
  - Groups: medium-resolution units (~400 km² typical). Comprise one or more Sections; can combine to form Hydrometric Areas without Coastline. Attributes include G_ID, G_NAME, G_AREA_KM2, RIVER-related fields, and HA_ID linkage.
  - Sections: drainage areas between named downstream/upstream waterways; most numerous features; linked to Groups (G_ID) and to Catchments (S_ID). Attributes include S_ID, S_NAME, RIVER fields, S_AREA_KM2, and geographic coordinates for outlet and centroid.
  - Catchments: finest-level units upstream from each Section outlet; may overlap multiple Sections/Groups. Attributes include spatial extent (KMSQ), S_ID (downstream section identifier), and coordinate data (EAST/NORTH, CEAST/CNORTH).

- Data Creation, Coverage, and Topology
  - Boundaries derived from CEH’s Integrated Digital Terrain Model (IHDTM); GB coastline based on Meridian2, NI boundary/coastline from OS GB Panorama.
  - Islands reassigned to nearest existing hydrometric areas in 2014 to achieve full UK coverage.
  - Topology: datasets are processed to ensure no gaps or overlaps; every point in the country belongs to exactly one Hydrometric Area. NI catchments are clipped to the national boundary; some cross-border catchments are not hydrologically complete.

- Quality, Limitations, and Maintenance
  - Dataset quality depends on IHDTM quality (50 m resolution). Some minor rivers may be omitted.
  - No planned routine updates; updates occur only if errors are identified or underlying river/drainage grid data improve.
  - NI data availability is limited for some layers; caution needed when combining layers across the full UK.
  - Metadata and naming conventions are standardized, with explicit identifiers for ease of cross-referencing (HA_ID, G_ID, S_ID).

- Data Formats and Attributes
  - Primary format: Geodatabase (preserves NULL values); Esri Shapefile option may convert NULLs to zeros or empty strings.
  - Attribute schemas include:
    - Hydrometric Areas with Coastline: HA_NUM, HA_NAME, HA_ID (and computed HA_ID like HA054)
    - Hydrometric Areas without Coastline: HA_NUM, HA_NAME, HA_ID
    - Groups: multiple fields including G_ID, G_NAME, G_AREA_KM2, RIVER-related fields, HA_ID, OUTF_SC, etc.
    - Sections: S_ID, S_NAME, G_ID, HA_ID, S_AREA_KM2, S_DS_ID, coordinates (OUTF_X/Y), river names
    - Catchments: S_ID (downstream section), KMSQ, EAST/NORTH (outlet), CEAST/CNORTH (centroid), etc.
  - Detailed table descriptions provided for Tables 1–5 (Areas with Coastline, Areas without Coastline, Groups, Sections, Catchments).

- History and Context
  - Origins trace back to the 1930s Inland Water Survey Committee for hydrometric areas; modern IHUs formalized in 2015.
  - The 1980s digitization efforts led to catchment-based boundaries; subsequent refinements ensure alignment with IHDTM and other CEH/NRFA datasets.
  - The dataset uses a naming/numbering convention tied to regional identifiers and hydrometric area numbers; NRFA gauge numbers are derived from this system.

- Strategic and Governance Implications for Data Leaders
  - Data orchestration: supports a holistic data system for river flow measurement and hydrometric data management; enables cross-layer analysis from catchments to large hydrometric areas.
  - Discoverability and interoperability: consistent identifiers (HA_ID, G_ID, S_ID) and metadata aid integration with other data sources (e.g., NRFA).
  - Data quality governance: reliance on IHDTM quality necessitates monitoring updates to terrain and drainage data; plan for potential NI data enhancements and cross-border consistency.
  - Stakeholder engagement: layers are useful for policy colleagues and broader networks; potential for co-ownership of data products across teams due to layered structure.
  - Gaps and risk management: NI data limitations and possible omissions of minor rivers; maintain awareness of data gaps when informing policy, planning, or analytics.
  - Operational guidance: be aware of topology rules (no gaps/overlaps; full UK coverage at aggregate levels) and the implications of using either coastline-based or IHDTM-based boundaries for analyses and cartography.
  - Update strategy: establish procedures for error correction and incorporation of improved IHDTM or drainage data; ensure metadata remains aligned with any changes.