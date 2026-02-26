# Integrated Hydrological Units of the United Kingdom

- The Integrated Hydrological Units (IHU) comprise a set of polygon layers at multiple spatial resolutions that model UK river catchments and hydrological units.
- Layers included:
  - Hydrometric Areas with Coastline
  - Hydrometric Areas without Coastline
  - Groups
  - Sections
  - Catchments
- The two Hydrometric Areas layers represent the same entities at the coarsest level; the difference is boundary treatment: coastline vs. alignment to the Integrated Hydrological Digital Terrain Model (IHDTM) for precise data alignment.

## Layers and Hierarchy

- Hydrometric Areas with Coastline
  - Covers Great Britain and Northern Ireland; used for cartography and administrative grouping of river catchments.
- Hydrometric Areas without Coastline
  - Same entities as with Coastline but boundaries follow IHDTM; better for exact data alignment with IHDTM data, not ideal for mapping.
- Groups
  - Medium-resolution units (typical size ~400 km²; range 4–3019 km²). Comprised of one or more Sections; can be combined to form Hydrometric Areas without Coastline.
  - Names derived from major rivers and local counties; key attributes include area totals and river metadata.
- Sections
  - Drainage area between confluences with named tributaries; each Section is linked to one Group and one Catchment.
  - Attributes include area within the section, river names, upstream/downstream references, and coordinates for the outlet.
- Catchments
  - Finest resolution; represent the full area upstream from the outlet of every Section.
  - Can overlap multiple Sections and Groups; only layer with polygon overlaps.
- Data model notes
  - Attributes are described across five tables (Areas with Coastline, Areas without Coastline, Groups, Sections, Catchments).
  - Preferred storage format is Geodatabase to preserve NULL values; Esri Shapefile will convert NULLs to zeros or empty strings.

## Data Creation and History

- Boundaries created from CEH’s IHDTM (50 m grid resolution) with in-house processing; Great Britain coastline aligned to Ordnance Survey Meridian2; Northern Ireland boundary/coastline from OS Panorama data.
- Islands and cross-border adjustments (2014) merged into the nearest existing Hydrometric Area to achieve full UK surface coverage (examples include Isles of Scilly, Lundy, St Kilda groupings, etc.).
- Hydrometric Areas were incorporated into the IHU framework in 2015, linking historical hydrometric boundaries to the integrated system.
- NRFA gauging station numbers are based on the hydrometric area scheme; this aids cross-referencing with national hydrometric data.

## Coverage, Scope, and Availability

- Hydrometric Areas with Coastline: GB and NI.
- Hydrometric Areas without Coastline: GB only (NI data not available at this boundary level).
- Northern Ireland catchments are clipped to the national boundary; not all cross-border catchments are hydrologically complete in the NI context.
- The dataset provides comprehensive UK coverage at various resolutions, suitable for hydrological analysis and data management.

## Quality, Limitations, and Maintenance

- Quality is tied to IHDTM (50 m resolution); some minor rivers may not be captured even in Great Britain.
- No routine periodic updates are planned; updates may occur if errors are found or if improvements to underlying river/drainage data are available.
- Data standards and metadata exist, but potential data gaps and inconsistencies are acknowledged, particularly for NI and for cross-border hydrology.

## Data Model, Attributes, and Access

- Primary format: Geodatabase (preserves NULL values); Esri Shapefile will convert NULLs to zeros or empty strings.
- Feature counts (summary):
  - Areas with Coastline: 115 features
  - Areas without Coastline: 105 features
  - Groups: 405 features
  - Sections: 584,556 features
  - Catchments: 584,556 features
- Key attribute themes:
  - Hydrometric Area: HA_NUM, HA_NAME, HA_ID
  - Groups: G_ID, G_NAME, G_AREA_KM2, G_CAT, RIVER and related river metadata
  - Sections: S_ID, S_NAME, S_AREA_KM2, RIVER relationships (RIVER, RIVER_DS, RIVER_US), spatial outlet coordinates (OUTF_X, OUTF_Y)
  - Catchments: spatial extent, S_ID linkage to downstream section, KMSQ (area in km²), centroid coordinates (CEAST, CNORTH)
- Boundary and topology
  - All UK boundaries processed to ensure topological correctness with no gaps/overlaps (except NI cross-border considerations).
  - Catchments may overlap sections and groups, unlike other layers which are strictly partitioned.

## Practical Implications for Data Leaders

- Data governance and strategy
  - Provides a scalable, multi-resolution framework for organizing hydrological data across the UK, enabling cross-department and cross-network collaboration.
  - Facilitates co-ownership and reuse of data products through standardized hydrological units.
- Data quality and integration
  - Aligns with IHDTM-based processing to ensure consistency with other CEH and NRFA datasets.
  - Be aware of NI limitations and the absence of routine NI-level updates; plan integration with cross-border data where needed.
- Data access and stewardship
  - Prefer Geodatabase for data integrity and NULL handling; shapefile users should treat NULLs cautiously.
  - Maintain metadata and lineage to support governance and auditability across data products.
- Use cases for Data Leaders
  - Organising hydrometric data management and reporting at multiple scales (areas, groups, sections, catchments).
  - Aligning policy, planning, and analytical workflows with a coherent, hierarchical hydrological framework.
  - Facilitating discovery, interoperability, and collaboration with external partners and national data archives (e.g., NRFA).