# LCM2000

## Overview
- LCM2000 is a parcel-based thematic land cover map for the United Kingdom, updating and upgrading the Land Cover Map of Great Britain (LCMGB) 1990.
- It is derived from satellite imagery (primarily Landsat) with additional ancillary data, and covers Northern Ireland for the first time to provide an all-UK dataset.
- Produced in both vector and raster formats, with multiple versions at different levels of detail and spatial resolutions.
- Classified using a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, incorporating broad habitat groups and additional detail for wider data use.
- Not directly comparable with LCM1990 due to different methodologies.

## Data structure and formats
- Vector data: polygons (land parcels) with attached attributes.
- Raster data: available at 25m and 1km resolutions, derived from the vector dataset.
  - 25m raster: 26 Subclasses.
  - 1km raster: Subclass level (26), Dominant values, Percentage values; plus 10 Aggregate classes with Dominant and Percentage values.
- Data formats:
  - Vector: ESRI shapefile (standard); ArcGIS Spatial Analyst may be required for advanced analysis.
  - Raster: GeoTiff (standard); Spatial Analyst extension may be needed.
- Minimum mappable unit: >0.5 ha; parcels under 0.5 ha are dissolved into surrounding areas during production; some very small parcels may remain in limited areas.

## Dataset coverage and tile structure
- Compiled on a 100km tile basis; parcels are classified within their 100km tile and then assembled into a UK-wide mosaic.
- Some tiles are merged to simplify construction; edge-crossing parcels may be retained in adjacent tiles.

## Nomenclature and attributes
- Vector data provides Subclass and Variant detail (Level 2 and Level 3).
- Subclass and Variant codes map to a detailed table of land-cover types; an Alpha code is provided for each variant.
- Key vector attributes per parcel include:
  - SegID: unique parcel identifier (stable label to retain for communications and provenance).
  - BHSub: dominant land-cover type (Level 2).
  - BHSubVar: dominant land-cover type (Level 3, when present).
  - PerPixList: per-pixel percentage list of top spectral subclasses (Level 3 only).
  - OpHistory: processing history (input data, dates, KBC rules, etc.).
  - TotPixels: total pixels in the parcel.
  - CorePixels: pixels in the core area used for maximum likelihood classification.
- The dataset preserves a robust history and lineage, with SegID recommended to be retained for traceability.

## Processing history and quality information
- OpHistory (processing history descriptor, PHD) on each parcel captures input data and classification steps, including:
  - Scene number, sensor type, image acquisition dates.
  - Single-date cloud hole patches (flags for summer/winter data usage).
  - Spectral probability metrics and aggregation flags.
  - Phase 1 and Phase 2 KBC (knowledge-based correction) rules applied.
  - Additional status flags indicating edge conditions or special cases.
- The OpHistory supports understanding data provenance and the rationale behind classifications.

## Colour mapping and habitat descriptions
- Colour recipes define display colors for the 26 Subclasses to aid visualization.
- Broad Habitat descriptions (aligned with JNCC Broad Habitats) cover major habitat groups, including:
  - Broad-leaved/mixed and yew woodland
  - Coniferous woodland
  - Arable and horticulture
  - Improved grassland
  - Neutral and calcareous grasslands
  - Acid grassland
  - Bracken and dwarf shrub heath
  - Fen, marsh, swamp; Bog
  - Standing water and inland water
  - Montane habitats
  - Inland rocks and built-up areas
  - Coastal habitats ( Supra-littoral and Littoral; sea/estuary contexts)
  - Inland bare ground and urban/suburban areas
- These descriptions provide guidance for interpretation and analysis at the habitat level.

## Colour and habitat display considerations
- Color assignments are provided per Subclass for visualization purposes.
- Broad Habitat descriptions help contextualize Subclass-level classifications within larger ecological frameworks.

## Practical data governance, customization, and lineage
- LCM2000 is designed as a data storage and analysis framework, not just a map; users are encouraged to customise and expand their version with appropriate metadata.
- Unique Segid labeling supports unambiguous communication with the data management team and other users.
- Production philosophy emphasizes retaining as much information as possible; parcel-level metadata should be used to record lineage and processing history; changes should be captured in new attributes.

## Production notes and cautions
- LCM2000 raster data is not directly comparable with LCM1990 due to different construction methods; it is not suitable for estimating change over the 10-year period.
- Parcels smaller than 0.5 ha may be introduced during edge processing and cloud-hole patching; users should be aware of potential artefacts.
- Edge overlaps between 100km tiles can produce artefacts and differing classifications across tile boundaries; artefacts are typically <0.1% of parcels but may require user remediation.
- Common remediation approaches:
  - Visual tidying by dissolving boundaries between adjacent parcels of the same class (preserve parcel metadata when possible).
  - Clipping to tile edges or unioning tiles with caution, recognizing that some attribute data may be invalidated after such operations.
  - For Level 3 data, maintain bhsubvar during dissolves to preserve Level 3 info.
  - Use selective dissolves or spatial queries to manage edge areas efficiently.
- Small parcel issues (slivers): removable via visual dissolve, combining with neighboring parcels, or intelligent dissolution based on shared boundaries.
- When merging tiles, the first input tile typically dominates edge attributes; differences may occur if edge classifications differ.

## Further information and references
- Land Cover Map home page: www.ceh.ac.uk/data/lcm
- Contact: spatialdata@ceh.ac.uk; phone 01491 692315
- Key references:
  - Fuller et al. 2002: The UK Land Cover Map 2000 – construction of a parcel-based vector map from satellite images
  - Smith et al. 2001: Land Cover Map 2000 – a parcel-based map from satellite images
  - Jackson 2000: Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC)
- Appendix notes:
  - Appendix 1: Dealing with edge overlap problems (edge artefacts, tile merging, and recommended remediation)
  - Appendix 2: Good practice (guidance not detailed here)
- Important caveat: maintain data provenance; accuracy reflects data model, scale, resolution, and interpretation; differences from other data are expected and not solely due to errors.