# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification built from satellite imagery (summer-winter composites) at 20–30 m pixels.
- Provides 23 Broad Habitat-based classes (based on UK Biodiversity Action Plan) and supports various GIS analyses; maps land cover (not necessarily land use).
- Improves on LCM2000 via a spatial framework aligned with OS MasterMap/large-scale vector data and image segmentation, producing polygons that align with real-world objects.
- Minimum mappable unit is >0.5 ha; parcels smaller than 0.5 ha or very short linear features are dissolved into surrounding areas.
- Data are provided in multiple formats (vector, 25 m raster, 1 km raster) to support a range of applications and scales.

## Data Products and Structure
- Vector data set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - 10 polygon attributes per feature; includes Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (display class), Knowledge-Based Enhancements (KBE), ProbList (top 5 spectral class probabilities), CorePixels, Construct history, TotPixels.
  - Unique Parcel_ID retained for unambiguous communication between users.
  - Rich metadata per polygon; supports provenance and processing history.
- Raster data sets
  - 25 m raster: same 23 LCM2007 classes; GB and NI provided in separate projections.
  - 1 km raster: aggregated products (dominant class, percent cover) for both GB and NI; also includes 23-class and Aggregate-class variants.
  - 1 km products are designed for national-scale modelling and integration with other datasets (e.g., meteorology, species distributions).
- Class and aggregation
  - 23 LCM2007 classes aligned with Broad Habitats; some BHs subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
  - Aggregate classes exist for 1 km rasters to simplify analysis when full thematic detail is unnecessary.
- Data access and projections
  - Great Britain data: British National Grid (OSGB 1936) for vector and raster.
  - Northern Ireland data: Irish National Grid; NI is transitioning to Ireland Transverse Mercator (ITM).
  - Data access:
    - 1 km raster products via CEH Information Gateway.
    - Full vector and 25 m raster products available under licence on request from CEH (licence fees may apply).

## Metadata, QA, and Validation
- Rich metadata accompanying vector polygons (data sources, processing steps, KBE history, ProbList).
- Validation: ground reference data used to validate LCM2007 against spatially and thematically matched references; average accuracy around 83% (noting variability by location and class).
- Sub-class level (BHSub) information is provided but not QA-validated to the same standard as LCM2007 classes; users should perform their own validation for sub-classes if used.
- KBE and ProbList provide insight into spectral signatures and potential improvements; recommended to validate sub-class information before use.

## Accuracy, Limitations, and Change Mapping
- Overall accuracy: average 83% across validation polygons; local discrepancies can occur.
- Change detection caveats:
  - Complex mapping between LCMs from different years (1990, 2000, 2007) due to differing classes and spatial structure.
  - Classified image errors are typically around 20%; actual landscape change between periods is often smaller.
  - LC M2007 products are not well suited for robust change detection over time without careful cross-walking and validation.
- Users should exercise caution when comparing LCM2007 with ground references or other LC maps; Appendix 2 and Morton et al. provide detailed crosswalks and limitations.

## Practical Use for Monitoring Frameworks
- Baseline and trend indicators
  - 23-class and aggregated 1 km products offer scalable baselines for national and regional environmental indicators (e.g., woodland extent, arable land, urban expansion).
  - 25 m raster and 1 km products allow flexible integration with climate, biodiversity, and land-use datasets.
- Data provenance and governance
  - Parcel_ID and detailed KBE/processing histories support audit trails and reproducibility in monitoring frameworks.
  - Rich metadata facilitates data governance, quality assurance, and data sharing decisions.
- Uncertainty and validation needs
  - Sub-class information (BHSub) requires user validation for decision-making; core class labels (INTCODE) are the recommended display classes with QA-backed validation.
  - Where precise vegetation or habitat types are critical, rely on validation against local references before policy interpretation.
- Implementation considerations
  - Large vector datasets (~4.13 GB GB shapefile; NI ~433 MB) necessitate appropriate storage and processing capabilities.
  - Projection and resampling requirements should be considered when integrating with other datasets (ITM, ITM-compatible tools; reproject if needed).
  - When using for nationwide indicators, 1 km raster products provide efficient, harmonised inputs; for finer-scale management, 25 m or vector products offer greater detail with metadata.

## Data Access and Updates
- Version history
  - Version 1.2 (May 2014) updated vector and raster GB products to include additional OS tiles (Fair Isle, Stranraer) and added water class to 1 km aggregates.
- Access routes
  - 1 km raster: CEH Information Gateway.
  - Full vector and 25 m raster: licence on request from CEH; online form and contact details provided by CEH.
- Documentation and references
  - Final Report for LCM2007 (Morton et al., 2011) for a comprehensive methodology and assessment.
  - Broad Habitat classification guide (Jackson, 2000) for deeper understanding of BH mappings.

## Appendix Highlights (Referenced in Summary)
- Appendix 1: LCM2007 classes (descriptions and examples for each Broad Habitat class and subdivisions).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (crosswalks and field codes).
- Appendix 3: Colour mapping recipe for LCM2007 classes (color values for mapping and display).
- Appendix 4: Updates to products (notable changes in version 1.2, including new tiles and water class inclusion).

## Acknowledgements
- Acknowledges multiple data providers (Landsat, SPOT, AWIFS, Ordnance Survey, and others) and the Countryside Survey Partnership for data contributions and licensing.