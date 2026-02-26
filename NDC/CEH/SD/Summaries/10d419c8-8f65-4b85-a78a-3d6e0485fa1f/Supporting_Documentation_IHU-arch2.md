# Integrated Hydrological Units (IHU) of the United Kingdom

## Aim and scope
- A hierarchical set of polygon layers representing hydrological units at multiple spatial resolutions for UK river catchments and hydrometric data management.
- Layers include: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
- Enables consistent, time-based assessment of environmental health and policy performance through standardized spatial units.

## Layer descriptions

- Hydrometric Areas with Coastline
  - Represents administrative groupings of river catchments with one or more sea outlets or tidal estuaries.
  - Boundaries cover Great Britain and Northern Ireland; numbering is national and regionally prefixed for Ireland.
  - Each feature corresponds to a single hydrometric area (HA) with identifying codes (HA_NUM, HA_ID, HA_NAME).

- Hydrometric Areas without Coastline
  - Same entities as with Coastline but boundaries follow the IHDTM coastline edges, not a smooth coast.
  - Better suited for analyses requiring precise matching to IHDTM-gridded data; less cartographically suitable.

- Groups
  - Medium-resolution units (~400 km2 typical; range 4–3019 km2) comprising one or more Sections.
  - Groups can be combined to form Hydrometric Areas without Coastline.
  - Attributes include area measures, rivers, identifiers (G_ID, HA_ID), and outflow/inflow relationships.

- Sections
  - Drainage area of a watercourse between two confluences with named rivers.
  - Each Section belongs to one Group and one Hydrometric Area; contains outlet and inflow/outflow river information.
  - Attributes include S_ID, S_NAME, S_AREA_KM2, RIVER fields, and topology (S_DS_ID).

- Catchments
  - Finest level of detail; upstream area from the outlet of every Section.
  - Catchment polygons may overlap multiple Sections/Groups (unique to this layer).
  - Attributes include local coordinates (EAST/NORTH, CEAST/CNORTH), KMSQ (area), and S_ID (downstream Section).

## Data creation and boundaries

- Boundaries derived from CEH’s Integrated Hydrological Digital Terrain Model (IHDTM) with a 50 m grid; coastline for Great Britain uses Ordnance Survey Meridian2, NI coastline from GB Panorama data.
- Islands assigned to nearby hydrometric areas (e.g., Isles of Scilly merged into HA 49) to ensure full UK coverage (2014 update).
- All boundaries topologically correct with no gaps or overlaps; every point belongs to one Hydrometric Area.
- Northern Ireland catchments are clipped to the national boundary; some cross-border catchments are not hydrologically complete within NI.

## Data formats, access, and attributes

- Primary format: Geodatabase (preserves NULL values; Shapefile converts NULLs to zeros or empty strings).
- Attribute tables outline (highlights):
  - Areas with Coastline: HA_NUM, HA_NAME, HA_ID (HA and HA_NUM concatenation possible, e.g., HA054).
  - Areas without Coastline: HA_NUM, HA_NAME, HA_ID, with similar identifiers.
  - Groups: area notes (CCAREA_KM2, G_AREA_KM2), river-based naming (RIVER, RIVER_DS, RIVER_US), identifiers (G_ID, HA_ID), and outflow/inflow info (OUTF_SC).
  - Sections: area (CCA REA_KM2, S_AREA_KM2), river naming (RIVER, RIVER_DS, RIVER_US), spatial refs (OUTF_X, OUTF_Y), identifiers (S_ID, G_ID, HA_ID, S_DS_ID).
  - Catchments: spatial coordinates (EAST/NORTH, CEAST/CNORTH), polygon area (KMSQ), and downstream section reference (S_ID).
- Use for standardised data sharing and integration with NRFA hydrometric data and other CEH/NRFA datasets.

## Quality, limitations, and maintenance

- Data quality tied to the IHDTM 50 m grid; potential omissions of minor rivers even in Great Britain.
- Northern Ireland coverage is incomplete for river geometries; some Irish hydrometric areas do not have sea outlets.
- No routine updates planned; updates may occur only to fix errors or incorporate improvements to underlying drainage data.
- Historical context: origins in the Inland Water Survey Committee (1930s) with subsequent digitisation and alignment to IHDTM; integrated into IHU in 2015.

## Practical considerations for analysts monitoring the environment

- Provides a consistent, hierarchical framework to aggregate or disaggregate environmental data over time for trend analysis and policy assessment.
- Enables data integration across multiple sources while maintaining standardized units for comparison.
- Be mindful of NI limitations and coastline vs IHDTM boundary differences when aligning with other datasets.
- When exporting, note that Shapefile outputs replace NULL values with zeros or empty strings; prefer Geodatabase for preserving NULLs.