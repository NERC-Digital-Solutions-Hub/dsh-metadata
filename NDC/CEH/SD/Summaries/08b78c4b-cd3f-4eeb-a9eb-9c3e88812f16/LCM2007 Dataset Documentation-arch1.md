# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification using 23 classes based on Broad Habitats, derived from summer-winter satellite composites with 20-30 m pixels. It updates LCM2000 using OSMM-based generalised cartography and image segments to create polygons aligned with real-world objects.

- Important scope note: LCM2007 maps land cover (not strictly land use); minimum mappable unit is >0.5 ha; parcels <0.5 ha or linear features <20 m are dissolved into the surroundings.

- Documents and data are complex; consult the Final Report for comprehensive methodology and limitations (Morton et al., 2011).

## Data Products and Coverage

- Data range supports diverse applications with multiple thematic and spatial resolutions.
- Vector data set: 8.6 million polygons for Great Britain, 0.9 million for Northern Ireland; 10 attributes per polygon.
- Raster data sets: 25 m and 1 km products derived from the vector; Great Britain and Northern Ireland provided separately due to different projections.
- The 1 km rasters provide dominant class and percentage cover; 25 m rasters preserve 23 LCM2007 classes with full metadata in the vector.

## Vector Data Set: Structure and Attributes

- Parcel_ID: Unique parcel identifier (e.g., 11853977:c20); retains image source.
- BH (Broad Habitat): Dominant Broad Habitat level (e.g., Coniferous Woodland).
- BHSub: Broad Habitat sub-class from Appendix 2 (described with FieldCode).
- FieldCode: Short string identifying the field code used in LCM2007 construction; not always QA-validated.
- INTCODE: Integer class code (1–23) recommended for display and QA-validated class.
- KBE: Knowledge-Based Enhancement history (processing history and changes).
- ProbList: Top 5 spectral class probabilities; used for sub-class level information (not QA-validated for sub-classes).
- CorePixels / TotPixels: Pixel counts used in classification core and total polygon.
- Construct: Polynomial history of polygon derivation (OSMM, OSMM:SEG, etc.).

- BHSub and FieldCode provide additional detail but require user validation for certain analyses; Sub-classes reflect spectral variants not always as accurate as LCM2007 classes.

## Raster Data Sets

- 25 m raster: 23 LCM2007 classes; GB and NI have separate grids; pixel values correspond to the 23 classes (per Table 2).
- 1 km raster: Aggregated products from 25 m data; includes dominant class, aggregate classes, and percent cover at 1 km resolution.
- Metadata include grid dimensions, extents, pixel sizes, projections, and datums for GB and NI.

## Classification and Validation

- Ground reference validation against a set designed to match LCM2007 resolution; 9,127 polygons used for QA.
- Average accuracy: approximately 83% at the 23-class thematic level; local discrepancies may occur.
- Broad Habitat subclass information (BHSub) is provided primarily to support ProbList usage; not uniformly validated at the subclass level.
- Users are advised to perform their own validation if analyses rely on Broad Habitat sub-classes.

## Map Projections and File Sizes

- Vector and 25 m raster: GB uses British National Grid (OSGB 1936); NI uses Irish National Grid.
- NI is transitioning toward the Ireland Transverse Mercator (ITM); reprojection may be necessary in GIS environments.
- File sizes (typical guidance):
  - Vector (GB) shapefile: ~4.13 GB; NI: ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB depending on product (dominant vs. percentage).

## Data Access and Licensing

- 1 km raster data sets: available via CEH Information Gateway.
- Full vector product and 25 m raster: available under licence on request from CEH; licensing fees may apply.
- Access process: online application via CEH data portal or contact spatialdata@ceh.ac.uk.

## Practical Guidance for Analysts

- Use 1 km rasters for large-scale modelling and integration with climate or species datasets; use 25 m and vector data for finer-scale analyses with richer metadata.
- Leverage Parcel_ID and metadata history (KBE) to trace origin and processing steps; retain Parcel_ID for clear communication.
- When using Broad Habitat sub-classes (BHSub), validate against site data due to potential misclassification or lower QA confidence.
- Consider the MMU and the fact that some land cover types may be misclassified in spectral terms (e.g., certain grassland types).

## Appendix Highlights (Context for Class Interpretation)

- Appendix 1: LCM2007 23 Broad Habitat classes with concise definitions and field-based caveats for woodland, grasslands, wetlands, montane, inland rock, littoral/shoreline habitats, freshwater, saltwater, urban/suburban, and more.
- Appendix 2: Relationship mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (BHSub) for cross-walks and interpretation guidance.
- Appendix 3: Colour mappings for LCM2007 classes (standard palette used in the Final Report) to aid visual interpretation.

## Further Information and Acknowledgements

- Final Report for LCM2007 (Morton et al., 2011) provides comprehensive methodology and evaluation.
- Detailed Broad Habitat definitions and cross-walk guidance (Jackson, 2000) referenced for interpretation.
- Datasets derived from multiple satellite sources (Landsat, SPOT, AWIFS) and Ordnance Survey cartography; acknowledgements detail data sources and licensing.

- Access the Countryside Survey context and related materials at www.countrysidesurvey.org.uk.