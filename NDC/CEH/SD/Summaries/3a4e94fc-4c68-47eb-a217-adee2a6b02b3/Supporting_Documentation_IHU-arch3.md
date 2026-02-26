# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) dataset provides hierarchical hydrological units for the UK at multiple spatial resolutions: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
- Hydrometric Areas with Coastline and without Coastline represent the same entities; the difference is how coastal boundaries are defined (coastline vs IHDTM edge), affecting cartography vs. precise extent matching.
- IHU Groups are medium-sized units that contain one or more IHU Sections and can be combined to form Hydrometric Areas without Coastline; Sections are the drainage areas between confluences with named watercourses; Catchments are the full area upstream from each IHU Section outlet (finest level), though Catchments can overlap multiple Sections/Groups.

- Quality and Known Limitations
  - Dataset quality depends on the underlying Integrated Hydrological Digital Terrain Model (IHDTM) with 50 m grid resolution.
  - Coverage: Hydrometric Areas with Coastline covers Great Britain and Northern Ireland; other layers cover Great Britain only due to data limitations for Northern Ireland.
  - Some minor rivers may be omitted even within Great Britain.
  - Data may require metadata enhancements and ongoing data governance to ensure standards, storage, and updates.

- Updates and Maintenance
  - No routine updates are planned.
  - Updates may be produced if errors are found or if improvements to rivers or drainage grid data become available.
  - The documentation date is January 20, 2015.

- Data Creation and Provenance
  - Hydrometric Area boundaries are digitally derived from CEH’s IHDTM using an in-house program; GB coastline uses Ordnance Survey Meridian2, while NI boundaries/coastlines come from OS GB Panorama data.
  - Islands were assigned to existing Hydrometric Areas in 2014 to achieve full UK coverage (examples include Isles of Scilly, Lundy, Grassholm, St Kilda group).
  - Boundaries are topologically correct with no gaps or overlaps; every point in the country is assigned to a single Hydrometric Area.
  - NI catchments are clipped to the national boundary, so some cross-border catchments may not be hydrologically complete.
  - In 2015, Hydrometric Areas became part of the broader Integrated Hydrological Units dataset.

- Layer Details (What each layer represents)
  - Hydrometric Areas with Coastline: administrative groupings of river catchments used for organizing UK river flow measurement and hydrometric data management; named with two-digit codes; NRFA gauging numbers use the same scheme with regional prefixes.
  - Hydrometric Areas without Coastline: identical entities as with Coastline but boundaries follow the IHDTM; more suitable for analyses requiring exact IHDTM geometry alignment, less suitable for cartography.
  - Groups: medium-scale units (~4 to ~3,000 km2, typical ~400 km2) consisting of one or more Sections; used to form larger Hydrometric Areas; named by major rivers and local areas.
  - Sections: drainage area between two confluences; Section names combine river names; each Section belongs to one Group and one Catchment.
  - Catchments: upstream area from each Section outlet; represents the finest detail and can overlap multiple Sections/Groups; only layer with polygon overlaps.

- Data Model and Attributes (high-level)
  - The primary format is a Geodatabase to preserve NULL values; Esri Shapefiles convert NULL to zeros or empty strings if chosen for download.
  - Attribute tables (summarized):
    - Tables for Areas with Coastline and without Coastline include identifiers (HA_ID, HA_NUM), names (HA_NAME), and related fields.
    - Groups table includes area metrics (CCA R A_KM2), alternative names, river context, and identifiers linking to parent/child relationships.
    - Sections table includes area metrics, outlet coordinates, river names, downstream/upstream relationships, and a unique section ID.
    - Catchments table includes outlet coordinates, centroid coordinates, area in KM2, and downstream section linkage.

- Practical Considerations for Monitoring Framework Authors
  - Useful for structuring environmental monitoring programs by providing consistent, multi-scale hydrological units for data aggregation, analysis, and reporting.
  - Facilitates linkage between hydro-meteorological observations (e.g., NRFA/Ni data) and catchment-scale analyses.
  - Important to account for data gaps (e.g., NI coverage, minor rivers) and to plan for metadata quality and data governance, given the emphasis on accurate, well-documented datasets.

- Access and Format Notes
  - Core data are provided in a Geodatabase; if downloading as Esri Shapefile, be aware of NULL value handling (converted to zeros or empty strings).
  - The dataset emphasizes topological integrity (no gaps/overlaps, full UK coverage with caveats for NI).
  - Data should be used in conjunction with IHDTM-based analyses for precise grid-aligned work and with coastline-based representations for cartographic purposes.