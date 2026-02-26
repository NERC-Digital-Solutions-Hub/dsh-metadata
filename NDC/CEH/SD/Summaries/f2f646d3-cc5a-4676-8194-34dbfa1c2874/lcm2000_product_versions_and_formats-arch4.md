# LCM2000 specification

## Overview
- LCM2000 is a parcel-based thematic classification of satellite image data covering the entire United Kingdom, including Northern Ireland.
- It updates and upgrades LCMGB (1990) and is produced from Landsat imagery with additional ancillary data.
- Classified using a hierarchical nomenclature aligned to the Joint Nature Conservation Committee (JNCC) Broad Habitats, aiming to cover the full range of UK habitats and to provide extra detail where possible.
- Available in both vector and raster formats, with multiple versions offering different levels of detail and spatial resolutions.

## Product versions and formats
- Vector data format
  - Delivered as land parcel polygons with attached attribute lists.
  - Level 2: standard detail with 26 LCM2000 Subclasses (most widely used).
  - Level 3: detail down to 72 Variant levels; higher detail quality varies by area and requires special arrangement with CEH staff.
  - Typical format: ESRI shapefile; may require Spatial Analyst extension for ArcGIS analyses.
- Raster data format
  - Derived from the vector database; available at 25m and 1km resolutions.
  - 25m raster: 26 Subclasses.
  - 1km raster: two 1km detail options (Subclass level; Dominant values and Percentage values).
  - 1km Aggregate class level combines Subclasses into 10 simplified classes with Dominant and Percentage options.
  - Note: Raster data are not directly comparable to LCM1990 and are not suitable for estimating change over the 10-year period.
- Minimum mapping unit
  - >0.5 ha; parcels ≤0.5 ha are dissolved into surrounding land using spectral or thematic proximity rules.
- Coverage basis
  - Data compiled on a 100km tile basis; overlapping source tiles are mosaicked, with some parcels straddling tile edges.

## Dataset coverage and nomenclature
- 100km tile basis with a UK-wide all-tile mosaic; some tiles merged to simplify construction.
- Hierarchical nomenclature supports Subclass and Variant detail; Variant level 3 details depend on the dominant land cover at imaging time.
- Subclass and Variant codes are documented in detail; some GIS displays may show codes as Level 2 subclass codes rather than Level 2 codes.

## Classification and codes
- Vector data include a hierarchical coding system (Subclass and Variant) for land cover types (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, etc.).
- A Tabular mapping (Table 2) provides codes for Subclasses and Level 3 Variants (e.g., 1.1 Broad-leaved/mixed woodland; 1.1.1 deciduous, etc.).
- Contextual information and dominant cover at the imaging date influence the ability to distinguish Variant-level classes.

## Vector attributes and history
- Each parcel includes a set of attributes:
  - SegID: Unique parcel identifier (e.g., TQ005232).
  - BHSub: Dominant land cover type (Level 2 Subclass code).
  - BHSubVar: Dominant land cover type (Level 3 Variant code) [Level 3 present in BHSubVar].
  - PerPixList: Top-five spectral Subclasses per pixel as percentages (Level 3 only).
  - OpHistory: Processing history descriptor detailing input data and classification/KBC steps.
  - TotPixels: Total pixels within the parcel.
  - CorePixels: Pixels within the core area used for maximum likelihood classification.
- OpHistory (PHD) is a six-field descriptor describing scene number, sensor, acquisition dates, cloud patches, spectral probability metrics, and KBC rule applications.
- A detailed table (Table 4) lists scenes, sensors (TM, IRS, etc.), and acquisition dates; cloud-hole patch indicators (S, W, X) denote single-date usage adjustments.

## Colour and habitat descriptions
- Colour recipes (Tables 5 and 6) provide recommended visualization for the 26 Subclasses and Broad Habitat descriptions.
- Subclass colours are specified in terms of Hue/Saturation/Value and approximate RGB equivalents for display in GIS.
- Broad Habitats descriptions (Table 6) define the functional habitat classes, such as Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grassland, Bracken, Heath, Fen/marsh/swamp, Bog, standing water, Montane habitats, Inland bare ground, Built-up areas, Supra-littoral/littoral habitats, etc.

## Data usage cautions and accuracy
- Raster data are not directly comparable to LCM1990 and should not be used for 1990–2000 change assessment.
- LCM2000 aims to preserve information richness; users should document lineage and changes, retain SegID, and maintain metadata to support data provenance.
- Not all Level 3 Variant distinctions are guaranteed across all areas due to imaging conditions and predominant cover at capture time.
- The dataset includes inevitable inaccuracies due to data model, scale, resolution, interpretation, and target class definitions; users should be mindful of these when aligning to user needs.

## Edge overlaps, slivers, and artefacts (Appendix 1)
- Edge overlaps arise from mosaic of multiple images and cloud-hole patching; 100km tiles may contain multiple overlapping parcel layers.
- Artefacts are infrequent (<~0.1% of parcels) and can be mitigated by:
  - Visual tidying: dissolving boundaries between same-class parcels along edges (via GIS legend tools).
  - Edge clipping: clip to 100km square edge or merge tiles; note that this can affect parcel-level attributes preserved in the original data.
  - Dissolving boundaries between like classes at Level 2 or preserving Level 3 bhsubvar during dissolves to avoid losing classification detail.
  - For Level 3 data, ensure bhsubvar is considered during dissolves to protect Level 3 information.
  - When merging tiles, the first input tile often has precedence for edge parcels; this can influence edge classifications in some cases.
- Slivers and very small parcels can be removed by similar procedures (visual dissolve, intelligent dissolve based on boundary length, or context-based dissolution).

## Customisation and production philosophy
- LCM2000 is intended as a data storage and analysis framework, not just a map; users are encouraged to customize and expand the database while preserving provenance.
- Strong emphasis on unique parcel labeling (SegID) to enable unambiguous communication with data management teams and other users.
- Production philosophy prioritizes retaining as much information as possible; when altering data, maintain lineage metadata and provide copies of original attributes as needed.
- Fully documenting changes is essential for data management, quality, and security; use metadata to capture changes and process history.
- Be mindful of differences in data models, scale, resolution, and interpretation when communicating accuracy and suitability to user needs.

## Further information and references
- Land Cover Map home page: www.ceh.ac.uk/data/lcm
- Contacts: spatialdata@ceh.ac.uk or CEH phone numbers listed for sales and inquiries.
- Key methodological references:
  - Fuller et al. 2002; The UK Land Cover Map 2000: construction of a parcel-based map from satellite images.
  - Smith et al. 2001; Land Cover Map 2000: a parcel-based map from satellite images.
  - Jackson 2000; JNCC Guidance on Broad Habitat Classification (definitions and relationships).
- Appendix 2 (Good practice) mentioned but not included in the provided text.