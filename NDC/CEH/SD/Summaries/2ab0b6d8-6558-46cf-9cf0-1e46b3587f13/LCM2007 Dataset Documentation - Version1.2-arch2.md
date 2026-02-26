# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Aim and scope
- UK-wide parcel-based land cover classification (LCM2007) mapped to 23 classes based on UK Biodiversity Action Plan Broad Habitats.
- Uses summer-winter satellite composites at 20–30 m resolution; updates LCM2000 with improvements in spatial framework (OSMM/large-scale vector data) and segmentation.
- Maps land cover (not necessarily land use); minimum mappable unit >0.5 ha; smaller parcels dissolved into surrounding landscape.
- Designed to support a range of applications with data products in multiple formats and resolutions; extensive metadata and QA applied.

## Data products and formats
- Vector data set
  - ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Each polygon has 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels, Construct).
  - Includes unique Parcel_ID labels for unambiguous communication; Broad Habitat sub-classes (BHSub) provided but recommended users validate if using at sub-class level.
- Raster data sets
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately.
  - 1 km raster: aggregate products (dominant, percentage cover) for both GB and NI; summaries of class and aggregate class coverage.
  - 1 km products include dominant class, and percentage cover for both LCM2007 classes and their aggregate classes.
- Access and distribution
  - 1 km raster data accessible via CEH Information Gateway.
  - Full vector and 25 m raster available on request under licence from CEH (licensing and possible fees).

## Classification and class structure
- LCM2007 uses 23 Broad Habitat-based classes (Appendix 1 elaborates each class description).
- Some Broad Habitats are subdivided into more detailed classes (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Sand dune variants including Saltmarsh).
- Appendix 2 provides the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3 provides a standard colour mapping for visualization of the 23 classes.
- Appendix 4 lists product updates (Version 1.2, 2014) including new tile coverage and inclusion of a water class in the 1 km products.

## Attributes and metadata
- Vector dataset attributes (Table 1 highlights):
  - Parcel_ID: unique parcel identifier (includes source image).
  - BH: dominant Broad Habitat (e.g., Broadleaved woodland).
  - BHSub: Broad Habitat sub-class (text description of FieldCode).
  - FieldCode: short field-code string describing the sub-class.
  - INTCODE: integer class code (1–23) used for display and QA.
  - KBE: Knowledge-Based Enhancement history (processing history and changes).
  - ProbList: top 5 spectral-class probabilities for the polygon.
  - CorePixels and TotPixels: pixel counts used in classification.
  - Construct: history of how the polygon was created (OSMM-derived, segmented, etc.).
- Rich metadata accompanies polygons, enabling traceability of processing steps, classification history, and data provenance.
- Ground-truth validation against 9127 polygons yielded an average accuracy of ~83%, with expected local deviations.

## Validation and accuracy
- Ground reference data were collected to validate against spatial/thematic resolution of LCM2007.
- Reported average accuracy of 83% across the validation polygons; individual features may vary in accuracy.

## Change mapping and limitations
- Change detection across LCMs (1990, 2000, 2007) is complex due to:
  - Different class definitions and spatial structures across versions.
  - Spectral classification errors (~20%), whereas land cover change (BH) changes may be smaller.
- Consequently, LCM products are not well suited for robust change detection without careful cross-walking and validation.

## Data access, projections, and file sizes
- Projections
  - Great Britain: British National Grid (BNG); Northern Ireland: Irish National Grid.
  - NI transitioning to Ireland Transverse Mercator (ITM); reproject with GIS as needed.
- File sizes (guidance)
  - Vector (GB): ~4.13 GB; Vector (NI): ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: GB and NI products smaller (dominant/percentage targets/aggregates).
- Access points
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster data on request (licence may apply).

## Updates and version history
- Version 1.2 (May 2014)
  - GB vector, 25 m raster, and 1 km products updated to include OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer) where applicable.
  - Water class added to 1 km dominant/aggregate products for GB; NI 1 km dominant aggregate class updates.
- Background versions: Version 1.0 (July 2011) and Version 1.2 (May 2012) noted in documentation history.

## Appendices and technical references
- Appendix 1: LCM2007 class definitions (detailed descriptions for each of the 23 classes).
- Appendix 2: Mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Colour mapping recipe used in the Final Report (Morton et al., 2011) for visualization.
- Appendix 4: Updates to products (Version 1.2, May 2014).

## Acknowledgements
- Acknowledges data sources and datasets used for LCM2007 (Landsat-TM5, SPOT-4/5, AWIFS, OS Master Map, various cartographic data, soils, elevation, and administrative boundaries).
- Produced by CEH and Countryside Survey Partnership; copyright and licensing notices apply.

## Relevance for Analysts Monitoring the Environment
- Provides a standardized, rule-based land cover dataset suitable for long-term environmental health monitoring and policy performance evaluation.
- Rich metadata and QA enable transparent data provenance and reproducibility across monitoring programs.
- Multiple data products (vector with detailed attributes, 25 m fine-grain rasters, and 1 km aggregated rasters) support diverse analytical needs and scalable monitoring.
- Clear documentation on limitations (e.g., change detection challenges) and recommended validation practices supports rigorous scrutiny and responsible use.
- Data access through portals and licenced data through CEH aligns with the aim of enabling broad stakeholder access to underlying data for transparency and reuse.