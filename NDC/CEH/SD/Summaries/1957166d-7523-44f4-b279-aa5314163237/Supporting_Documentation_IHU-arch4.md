# Integrated Hydrological Units (IHU) of the United Kingdom

## Overview
- A multi-layer polygon dataset describing UK hydrological units at increasing levels of detail.
- Five layers: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, Catchments.
- Designed to support administration of river flow measurement and hydrometric data management.

## Layers and Core Concepts
- Hydrometric Areas with Coastline: GB+NI; coastal boundary uses smooth UK coastline for cartography; administrative groupings of river catchments with one or more outlets to the sea or tidal estuaries.
- Hydrometric Areas without Coastline: same entities as with Coastline but boundaries follow the IHDTM; better for analyses requiring precise boundary alignment with IHDTM data; not ideal for cartography.
- Groups: medium-resolution units (~400 km² typical); composed of one or more Sections; can be aggregated to form Hydrometric Areas without Coastline.
- Sections: drainage area between two confluences with named rivers; linked to a single catchment; Section names derive from river names.
- Catchments: finest detail; upstream area from each Section outlet; may overlap multiple Sections and Groups (unique among layers for potential overlap).

## Data Quality, Coverage, and Maintenance
- Quality tied to the underpinning IHDTM with a 50 m grid resolution.
- Coverage: Hydrometric Areas with Coastline covers GB+NI; other layers cover Great Britain only due to data limitations for Northern Ireland.
- Gaps: some minor rivers not captured even in GB; NI catchments may be incomplete due to clipping to national boundaries.
- Updates: no routine ongoing updates; updates occur only to fix errors or incorporate improvements to rivers/drainage data.
- Data creation: boundaries derived from CEH IHDTM; NI boundaries derived from OS data; 2014 island mergers (e.g., Isles of Scilly, Lundy, etc.) integrated to maintain full UK coverage; topological correctness ensured (no gaps/overlaps).

## Data Model and Attributes
- Primary format: Geodatabase (preserves NULL values); Esri Shapefile converts NULLs to zeros or empty strings.
- Attribute highlights by layer:
  - Areas with Coastline: HA_NUM (Hydrometric Area Number), HA_NAME, HA_ID; HA_ID can be formed as 'HA' + padded HA_NUM.
  - Areas without Coastline: HA_NUM, HA_NAME, HA_ID (similar).
  - Groups: CCAREA_KM2, G_ALTNAME, G_AREA_KM2, G_CAT, G_DS_ID, G_ID, G_NAME, G_QUALIFY, HA_ID, OUTF_SC, RIVER, RIVER_DS, RIVER_US.
  - Sections: CCAREA_KM2, G_ID, HA_ID, HA_NUM, OUTF_X, OUTF_Y, RIVER, RIVER_DS, RIVER_US, S_AREA_KM2, S_DS_ID, S_ID, S_NAME.
  - Catchments: EAST, NORTH, CEAST, CNORTH, KMSQ, S_ID (S_ID links to downstream Section; S and KMSQ indicate polygon area and location details).
- Notes: Tables document the full schema; named fields provide unique identifiers and contextual names for each hydrological unit.

## Data Creation and Provenance
- Boundaries derived digitally from CEH’s IHDTM; Great Britain coastline aligned to OS Meridian2; NI boundaries/coastlines from OS GB Panorama data.
- Islands re-assigned to nearby Hydrometric Areas in 2014 to ensure full UK surface coverage.
- NI catchments clipped to national boundary, so some hydrological areas may be incomplete for cross-border analysis.
- 2015 integration elevated Hydrometric Areas into the Integrated Hydrological Units framework.

## Practical Implications for Data Leaders
- Data governance: ensure alignment with IHDTM, track versioning, and document any NI-specific limitations.
- Data quality management: communicate potential data gaps (e.g., minor rivers, NI completeness) to stakeholders; plan for updates only when errors/improvements are identified.
- Metadata and accessibility: prefer Geodatabase to preserve NULLs; be cautious with Shapefile exports that may alter NULL values.
- Cross-domain use: use the hierarchical structure (Areas → Groups → Sections → Catchments) to scale analyses, while noting Catchments may overlap and require careful interpretation.
- Coordination: align with NRFA and other hydrological data custodians; consider co-ownership and clear documentation of data lineage and limitations.

## History and Context
- Originating from the Inland Water Survey Committee in the 1930s; formal naming/numbering published in the Surface Water Year-Book of 1936-37 and later documents.
- Digital hydrometric boundaries developed in the 1980s; current IHU relationships reflect ongoing refinement and standardization with CEH NRFA datasets.
- 2015 adoption of the Integrated Hydrological Units framework, consolidating multiple hydrological spatial representations into a unified multi-resolution dataset.