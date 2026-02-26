# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview for Environment Analysts
- UK land cover is parcel-based with 23 classes aligned to Broad Habitats, mapped at 20–30 m resolution from summer–winter satellite composites.
- Emphasizes land cover (not land use) with a minimum mapping unit of 0.5 ha; parcels smaller than 0.5 ha or lines shorter than 20 m are dissolved.
- Designed to support diverse monitoring needs with rich metadata, validation, and multiple data formats for broad analytical use and integration with other datasets.

## Data and Products
- Data range includes vector (parcel-based polygons) and raster products (25 m and 1 km) for Great Britain and Northern Ireland.
- Vector product: polygons with 10 attributes per parcel, including Parcel_ID, Broad Habitat (BH), Broad Habitat subclass (BHSub), FieldCode, INTCODE, KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
- Raster products: 25 m and 1 km, with GB and NI datasets provided separately due to different projections. 23 LCM2007 classes in 25 m; 1 km rasters summarize to dominant and percentage cover for both LCM2007 classes and Aggregate classes.

## Vector Data Set
- Contains around 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
- Unique Parcel_ID labels each parcel; BH and BHSub provide the dominant Broad Habitat and its subclass.
- Attributes include: FieldCode (training/interpretation codes), INTCODE (class number 1–23 for display/QA), KBE (processing history), ProbList (top 5 spectral variants), CorePixels, TotPixels, and Construct method (OSMM-based segmentation variants).

## Raster Data Sets
- 25 m raster: full 23-class representation; pixel values correspond to LCM2007 classes as per a defined table (Table 2 in the documentation).
- 1 km raster: derived by aggregating 25 m data to provide:
  - Dominant cover at 1 km for LCM2007 classes
  - Dominant cover at 1 km for Aggregate classes
  - Percentage cover at 1 km for LCM2007 classes
  - Percentage cover at 1 km for Aggregate classes
- GB and NI rasters have separate metadata, projections, and extents (GB in British National Grid; NI in Irish National Grid).

## Map Projection and Spatial Information
- GB data: British National Grid
- NI data: Irish National Grid (transition to ITM ongoing)
- Table 3 provides the exact spatial grid specifications, extents, pixel sizes (25 m and 1000 m), data types, and datum/spheroid information.
- Note: For NI, ITM compatibility may require re-projection in GIS workflows.

## Data Access and Usage
- 1 km raster data: accessible via the CEH Information Gateway.
- Full vector and 25 m raster data: available under licence on request from CEH (application via CEH data site; fees may apply).
- Vector data are large (nearly 10 million polygons with 10 attributes each); plan storage and processing accordingly.

## Data Quality and Validation
- Ground reference validation: 9,127 polygons mapped to LCM2007 resolution; average accuracy around 83%, acknowledging local variability.
- LCM2007 is validated at the 23-class thematic resolution; users should validate Broad Habitat sub-classes if used, as these are not covered by QA in the same way as the main classes.

## Classification and Class Relationships
- LCM2007 uses 23 classes based on UK Broad Habitats (with some subdivisions, e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral sediment vs Saltmarsh).
- Appendix 1: provides detailed descriptions of each Broad Habitat class and its characteristics.
- Appendix 2: maps the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses (useful for cross-walking to alternative classifications).
- Appendix 3: standard color mapping used in the Final Report for visualizations.

## Practical Considerations for Monitoring and Analysis
- LCM2007 maps land cover, not land use; caution when inferring land use from cover classes.
- Minimum mappable area and dissolution rules affect small features and linear elements.
- Rich polygon-level metadata (KBE, ProbList, Construct) supports historical tracking and post-classification adjustments but requires careful handling for sub-class analyses.
- When using Broad Habitat subclasses, conduct independent validation to ensure accuracy not guaranteed by main QA.

## Documentation and References
- Primary source: Morton et al. 2011, Final Report for LCM2007 – the new UK Land Cover Map (Countryside Survey Technical Report No. 11/07).
- Broad Habitat classification guidance: Jackson 2000.
- The data are produced by CEH in collaboration with the Countryside Survey Partnership; acknowledgments and usage guidelines are included in the full documentation.

## Appendix Highlights
- Appendix 1: Detailed LCM2007 class descriptions and field-level considerations for each Broad Habitat category.
- Appendix 2: Crosswalk between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses (BHSub) with FieldCode mappings.
- Appendix 3: Colour mapping recipe for standard visualization of LCM2007 classes (R, G, B values per class). 

## Acknowledgements and Access Notes
- Datasets derived from multiple satellite sources and cartographic data; access governed by licences and data agreements with CEH and partner organizations.
- For data access and licensing details, contact spatialdata@ceh.ac.uk or visit CEH data portals.