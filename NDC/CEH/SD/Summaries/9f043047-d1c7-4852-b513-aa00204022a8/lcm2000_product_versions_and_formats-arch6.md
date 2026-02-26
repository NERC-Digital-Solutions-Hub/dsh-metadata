# LCM2000 specification

- Overview
  - LCM2000 is a parcel-based thematic land cover map for the entire United Kingdom, produced from satellite imagery (primarily Landsat) and enhanced with ancillary data.
  - It updates the Land Cover Map of Great Britain (LCMGB, 1990) and now covers Northern Ireland for an all-UK dataset.
  - Classified using a hierarchical nomenclature aligned with JNCC Broad Habitats, with added detail where possible; available in both vector and raster formats and in multiple detail levels and resolutions.

- Product versions and formats
  - Vector data (polygons/land parcels) with attributes
    - Level 2: 26 LCM2000 Subclasses (standard widely used)
    - Level 3: up to 72 Variants (more detailed; requires expert interpretation; special arrangement with CEH)
    - Standard vector format: ESRI shapefile; ArcGIS Spatial Analyst may be required for analysis
  - Raster data (derived from vector)
    - 25m resolution: 26 Subclasses
    - 1km resolution: Subclass, Dominant values, and Percentage values; also Aggregate class level with Dominant and Percentage
  - Raster outputs are GeoTIFFs; not directly comparable to LCM1990 due to differing methods; not suitable for long-term change estimation

- Dataset coverage and structure
  - Compiled on a 100km tile basis; parcels are classified per tile and then merged into a single dataset
  - Tiles may be edge-overlapped; edge artefacts can occur and may require user tidying

- Hierarchical nomenclature
  - Subclass codes and Level-3 Variant codes define land cover types (examples include broad-leaved/mixed woodland, coniferous woodland, arable crops, various grassland types, urban classes, aquatic and coastal habitats, etc.)
  - Subclass and Variant coding supports detailed mapping; some GIS packages display codes rather than human-readable subclass names

- Vector polygon attributes
  - SegID: unique parcel identifier (per parcel)
  - BHSub: dominant land cover code (Level 2)
  - BHSubVar: dominant land cover code (Level 3 Variant)
  - PerPixList: top-five spectral subclass percentages per parcel (level 3)
  - OpHistory: processing history descriptor detailing data inputs and classification steps
  - TotPixels: total pixels in the parcel
  - CorePixels: pixels in the parcel core used for maximum likelihood classification

- OpHistory (processing history descriptor)
  - Five fields (plus a sixth for other information) recording:
    - Scene/area number and input image data (sensors such as TM, IRS; acquisition dates)
    - Single-date cloud hole patch indicators
    - Spectral probability for the top choice subclass and any aggregation flags
    - Phase 1 KBC (knowledge-based correction) rules applied
    - Phase 2 KBC rules applied
  - Provides a detailed provenance trail for each parcel

- Colour mapping (colour recipes)
  - 26 Subclasses are assigned specific display colors (Hue/Saturation/Value or RGB equivalents) to aid visualization in GIS and mapping software

- Broad Habitat descriptions
  - 16 Broad Habitat descriptions (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water bodies, Montane habitats, Inland bare ground, Built-up areas, Coastal habitats)
  - Each habitat type includes qualitative descriptions and guidance on interpretation

- Further information and references
  - Contact details for CEH and LCM data inquiries
  - Methodology references for construction, parcel-based mapping from satellite images, and broad habitat classification guidance

- Appendix 1: Dealing with edge overlap problems
  - Edge overlaps arise from mosaic construction and cloud-hole patching; typically less than 0.1% of parcels are affected
  - Artefacts and approaches for visual and technical tidying:
    - Visual dissolving of boundaries between same-class parcels using GIS legend tools
    - Clipping data to tile edges or merging tiles (with implications for parcel-level attributes)
    - Using Union or dissolving with caution to preserve important Level 3 (bhsubvar) information
    - When merging tiles, the first input tile often takes precedence for edge parcels
    - Techniques to address “slivers” or parcels smaller than minimum mappable units, including visual removal, dissolving with adjacent parcels, or intelligent dissolution using the longest common boundary
  - Emphasizes preserving parcel-level attributes and provenance during edge fixes

- Appendix 2: Good practice
  - Content not provided in the excerpt; referenced as part of the document structure

- Production philosophy and data governance
  - Emphasizes retaining as much information as possible and documenting lineage
  - Parcel-level metadata should record provenance; when modifying attributes, preserve originals or create new attributes to maintain traceability
  - Encourages customization and expansion of the data framework by users

- Unique labeling and data quality notes
  - Each parcel has a unique Segid; recommended to retain this label
  - Distinguishes between true inaccuracies and differences due to data model, scale, resolution, interpretation, or definitions
  - Acknowledges inevitable inaccuracies and emphasizes alignment with user needs and data model considerations

- Practical implications for Data Support
  - Provides a rich, lineage-backed dataset suitable for self-service analysis and data product development
  - Supports integration with other data sources through detailed attributes and processing history
  - Highlights need for careful edge-artifact handling and preservation of original metadata during customization
  - Encourages end-user documentation and systematic change-tracking to ensure data governance and traceability