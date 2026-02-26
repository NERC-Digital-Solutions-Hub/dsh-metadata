# LCM2000

## Overview
- LCM2000 is a parcel-based thematic map of UK land cover derived from satellite imagery, updating and expanding on LCMGB 1990 to cover all of the United Kingdom (including Northern Ireland).
- Classified using a hierarchical Broad Habitat framework (JNCC Broad Habitats) with additional subclass and variant detail where available.
- Produced in both vector (parcels with attributes) and raster formats, with multiple product versions offering different levels of detail and spatial resolutions.

## Data formats and product versions
- Vector data: polygons (land parcels) with attached attributes.
  - Level 2 (standard): 26 Subclasses.
  - Level 3: up to 72 Variant level details (requires special arrangement and support).
  - Standard vector format: ESRI shapefile (ArcGIS may need Spatial Analyst for analysis).
- Raster data (from vector): 25m and 1km resolutions.
  - 25m raster: 26 Subclasses.
  - 1km raster: Subclass level (26 Subclasses), Dominant values, and Percentage values; Aggregate class level (10 simplified aggregates) with Dominant and Percentage values.
- Note: Raster data are not directly comparable with LCM1990 due to different construction methods and should not be used for long-term change estimation.

## Coverage and data structure
- Coverage: UK-wide, produced on a 100km tile basis; data from summer/winter composites or single dates classified per parcel and assigned to tiles.
- Dataset organization: 100km tiles may contain overlapping parcels; edges between tiles can involve artefacts due to mosaic creation and edge eroding/merging.
- Hierarchical nomenclature: Vector data provides Subclass and Variant detail; codes (e.g., Subclass code, Variant codes) follow a defined mapping to a wide range of land-cover types.
- Attributes (vector parcels): SegID (unique parcel label), BHSub (dominant Broad Habitat subclass), BHSubVar (Variant level, Level 3), PerPixList (top-five spectral subclass percentages), OpHistory (processing history), TotPixels, CorePixels, among others. BHSub is present at Level 2; BHSubVar present at Level 3.

## Processing history and metadata
- OpHistory (processing history descriptor) per parcel includes:
  - Scene number, sensor type, acquisition dates, cloud-hole patches, and the sequence of knowledge-based correction (KBC) steps (Phase 1 and Phase 2).
  - Additional fields cover spectral probability metrics and flags for special cases (e.g., eroded/merged at tile edges, training data usage, hazes).
- The dataset retains detailed lineage through per-parcel metadata to support auditing and reproducibility.

## Colour recipes and habitat descriptions
- Colour recipes (Table 5) provide recommended display colors for the 26 Subclasses to aid visualization and interpretation.
- Broad Habitat descriptions (Table 6) define general habitat categories (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water bodies, Montane habitats, Inland rock, Built-up areas, Coastal habitats, etc.).

## Quality, edge artefacts and handling (Appendix 1)
- Edge overlap issues arise from mosaicked imagery and cloud-hole patches, leading to multiple layers of parcels within 100km tiles.
- Artefacts are rare (typically <0.1% of parcels) and can be mitigated by:
  - Dissolving boundaries between adjacent parcels of the same class (visual tidy-up with legend tools in GIS).
  - Clipping to tile edges, merging tiles, or dissolving at Level 2/Level 3 while being aware of loss of source attributes.
  - Using selective dissolves and spatial context to manage “slivers” (parcels smaller than the minimum mappable unit) by dissolving into neighboring parcels or intelligently dissolving based on boundary length.
- When merging tiles, the first input tile generally has precedence for edge parcels; some differences can occur if classifications differ at tile edges.
- For Level 3 data, preserve bhsubvar during dissolves to avoid losing important Level 3 information.

## Customisation, governance, and data management
- LCM2000 is designed as a data storage and analysis framework beyond a simple map; users are encouraged to customize, expand, and preserve parcel-level metadata to maintain traceability and lineage.
- Unique SegID labels should be retained to enable unambiguous communication with data managers and other users.
- Production philosophy emphasizes preserving information and documenting changes; always record lineage and process history when modifying data.
- Caution on accuracy: acknowledge inevitable inconsistencies due to data model, scale, resolution, interpretation, and target definitions; differences may reflect the data than user need shortcomings.

## Practical implications for Data Leaders
- Treat LCM2000 as an authoritative, richly attributed UK land-cover asset with explicit provenance, suitable for policy support, planning, and environmental analyses, with clear versioning and metadata.
- Ensure governance around:
  - Version control and change documentation (preserve original attributes and create new ones for any changes).
  - Metadata completeness (keep OpHistory, SegID, and per-pixel/parcel-level details).
  - Data discoverability and discoverable lineage to support accountability and collaboration across networks.
- Plan for data integration across platforms, including cross-walks between Subclass and Variant levels, and alignment with Broad Habitat classifications for multi-source analyses.
- Be mindful of edge artefacts and slivers when aggregating or integrating tiles; apply recommended GIS procedures, and communicate any artefact-related caveats to users.
- Consider data use policies and access constraints (paywalls and data protection barriers can affect data availability and granularity) and how they influence data strategy and collaboration across partners.

## Further information and contacts
- For access, methodology, and support, refer to the Land Cover Map 2000 resources and CEH contact channels.
- References include Fuller et al. (2002) on constructing parcel-based vector maps from satellite images and related methodological papers, and Jackson (2000) for Broad Habitat classification guidance.