# LCM2000

- LCM2000 is a UK-wide parcel-based thematic land cover map derived primarily from Landsat satellite imagery, expanding the prior LCMGB to cover Northern Ireland and delivering an all-UK dataset. It employs a hierarchical nomenclature aligned with the JNCC Broad Habitats and includes additional detail where possible. Output formats include vector (parcels) and raster (2 resolutions), with multiple detail levels to suit different use cases. The raster dataset is not directly comparable with LCM1990 for change detection.

## Overview of purpose and scope
- Purpose: provide a robust set of environmental health measures for scrutinising and evaluating policy, and to inform future decisions.
- Coverage: all of the United Kingdom, including Northern Ireland; all-UK dataset produced from satellite imagery plus ancillary data.
- Formats and detail: vector (parcel-based) and raster (25m and 1km), with Level 2 (26 Subclasses), Level 3 (72 Variants) in vector; corresponding 26 Subclasses in raster plus aggregate and dominant/percentage values.
- Minimum mapping unit: 0.5 ha (parcels and smaller features dissolved into surrounding matrix).
- Classification: hierarchical Target/Subclass/Variant structure; broader Broad Habitat alignment with note that Variant-level distinctions depend on imaging contemporaneity and may be incomplete.

## Product versions and data formats
- Vector data (parcels with attributes):
  - Level 2: 26 Subclasses (standard, widely used).
  - Level 3: up to 72 Variants; requires special arrangement and more user support.
- Raster data (GeoTIFF):
  - 25 m: 26 Subclasses.
  - 1 km: aggregates include Subclass level, Dominant values, and Percentages; 10 Aggregate classes with Dominant and Percentage values.
- ArcGIS considerations: Vector uses ESRI shapefile; Raster may require Spatial Analyst extension for analysis.
- Important note: Raster data are derived from vector and are not directly comparable to LCM1990 for change estimation.

## Dataset coverage and structure
- Compiled on a 100 km tile basis; per-parcel classification added to their 100 km tile.
- Tiles may be merged; some tiles are redacted/merged to simplify construction.
- Hierarchical nomenclature (Subclass and Variant codes) is embedded in attribute fields; variant detail exists where 3-level detail is available and reliable.

## Vector polygon attributes and key fields
- SegID: Unique parcel identifier (including tile code and segment number).
- BHSub: Dominant land cover type (Subclass).
- BHSubVar: Dominant land cover type (Variant) when Level 3 data is used.
- PerPixList: Top five spectral Subclasses per pixel percentages (Level 3 only).
- OpHistory: Detailed processing history (image dates, KBC rules, etc.).
- TotPixels: Total pixels in the parcel.
- CorePixels: Pixels in the core area used for maximum likelihood classification.
- OpHistory fields provide a concise record of input data, sensor, dates, processing steps, and rule counts.

## OpHistory (processing history) details
- Five-field process history descriptor (plus a sixth for other notes) per parcel, capturing:
  - Scene number, sensor (e.g., TM, IRS), acquisition dates (summer/winter), cloud hole patch indicators, and other flags.
  - Scene and sensor combinations, plus knowledge-based corrections (KBC) and rule counts for both phase 1 (scene-dependent) and phase 2 (UK-wide) processing.
  - Spectral probability indicators and aggregation flags that reflect confidence and processing decisions.
- The OpHistory structure supports traceability of data lineage and reproducibility for monitoring frameworks.

## Colour mapping and Broad Habitat descriptions
- Colour recipes (Table 5) provide standardized visualization for the 26 Subclasses to aid interpretation and presentation.
- Broad Habitat descriptions (Table 6) explain the meanings of major classes such as Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Various grassland types, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water bodies, Montane habitats, Inland bare ground, Built-up areas, and Coastal/Marine habitats.
- Aims to support consistent interpretation and cross-walk to biodiversity and habitat classifications.

## Broader habitat framework and descriptions
- Clear definitions for each Broad Habitat category to aid comparability with other classifications, including:
  - Woodland types (Broad-leaved/mixed, Coniferous)
  - Grasslands (Improved, Neutral, Calcareous, Acid)
  - Heritage and disturbance features (Bracken, Dwarf shrub heath)
  - Wetlands (Fen, Marsh, Swamp, Bog)
  - Water-related categories (Standing water, Rivers/streams)
  - Coastal and littoral habitats (Supra-littoral, Littoral)
  - Montane and bare ground
  - Built-up areas and urban vegetation

## Edge overlaps, slivers, and artefacts (Appendix 1)
- Edge overlap problems arise from mosaic of overlapping images and cloud-hole filling, creating multi-layered parcel data within 100 km tiles.
- Artefacts are infrequent (generally <0.1% of parcels) but can occur at tile edges.
- Guidance on remediation:
  - Visual tidying by dissolving boundaries between same-class parcels is possible but should not be applied globally to preserve attribute integrity.
  - Clipping, merging, union, and subsequent dissolving can introduce attribute inconsistencies; Level 3 data requires maintaining bhsubvar.
  - Use selective editing (e.g., select edge parcels, then dissolve) to minimize data quality loss.
  - When merging tiles, first input tile often takes precedence for edge parcels; if different classifications occur, the earlier tile’s class is retained.
- Suggestions for handling slivers and small parcels:
  - Visual removal, dissolve into adjacent similar class parcels, or intelligent dissolve based on shared boundary length.
  - Maintain context and avoid dissolving across the entire dataset to preserve parcel-level metadata.

## Production philosophy and governance
- The production philosophy emphasizes retaining as much information as possible, resulting in an information-rich dataset.
- Parcel-level meta-data is foundational; when modifying attributes, keep originals in new attributes to maintain provenance.
- Unique SegID labeling provides unambiguous communication with data management and users.
- Customisation is encouraged: LCM2000 can be extended and used as a data storage and analysis framework for further research and applications.
- Emphasis on documenting changes for data management and security, and acknowledging inherent inaccuracies due to data model, scale, resolution, interpretation, and classification definitions.

## Practical considerations for monitoring frameworks
- Use OpHistory and per-pixel attribute data to assess data provenance, processing history, and confidence levels in monitoring outputs.
- Leverage the 100 km tile structure and Level 2/Level 3 detail to match monitoring needs (broad habitat monitoring vs. fine-grained habitat detail).
- Be aware of limitations for change detection when comparing with older datasets (LCM1990) due to methodological differences.
- Ensure metadata about data lineage, processing steps, and edge handling is captured in monitoring reports.
- Consider retaining SegID and related attributes to support audit trails and traceability in monitoring workflows.

## Further information and references
- Data access and contact: Land Cover Map home page, CEH; spatialdata@ceh.ac.uk; phone numbers provided.
- Methodology references:
  - Fuller et al. 2002; Smith et al. 2001; Jackson 2000 (Broad Habitat guidance).
- Additional sections and appendices provide more detail on edge handling, good practices, and data governance considerations.