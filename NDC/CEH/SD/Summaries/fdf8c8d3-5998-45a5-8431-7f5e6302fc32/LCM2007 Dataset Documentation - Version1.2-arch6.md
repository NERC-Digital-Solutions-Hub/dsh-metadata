# LAND COVER MAP 2007 DATASET DOCUMENTATION

- The Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification using 23 Broad Habitat (BH) classes, derived from summer–winter composite satellite imagery at 20–30 m resolution.
- It updates LCM2000 and is designed to be compatible with a range of GIS datasets, using objects that align with real-world features (polygons) and a rich metadata framework.
- LCM2007 maps land cover (not strictly land use) and applies a minimum mappable unit of 0.5 ha; parcels smaller than 0.5 ha or lines shorter than 20 m are dissolved into surrounding areas.

## Data Products and Structure

- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Each polygon includes a 10-attribute record (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - BHSub provides Broad Habitat sub-classes; FieldCode is an additional descriptor with caution on accuracy.
  - Unique Parcel_ID retained for unambiguous communication and potential product development.

- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately with their respective projections.
  - 1 km raster: aggregates of 25 m data (dominant class and percentage cover for both 23 classes and aggregates).
  - Aggregates are intended for applications where full 23-class detail is not required.

## Attributes and Classifications

- Table 1 (Vector attributes) includes Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels, among others.
- Appendix 1 lists the 23 LCM2007 classes with notes on how certain BHs are subdivided (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral sediment vs Saltmarsh).
- Appendix 2 provides the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes for crosswalks and validation, including detailed mappings (e.g., Broadleaf vs Coniferous Woodland, Arable and Horticulture, various grassland types, and coastal/urban categories).
- Appendix 3 offers the standard colour mapping for LCM2007 classes (color triplets for map visualization) used in the Final Report.

## Data Access and Licensing

- 1 km raster data sets are accessible via the CEH Information Gateway.
- The full vector product and 25 m raster product are available on request under licence from CEH; licensing fees may apply.
- Data access details: online application at CEH data portal or contact spatialdata@ceh.ac.uk.

## Data Quality, Validation, and Limitations

- Thematic validation: average accuracy of approximately 83% against ground reference polygons; individual polygon accuracy may vary, and local discrepancies are expected.
- Thematic resolution is validated only at the 23 LCM2007 classes; Broad Habitat sub-classes (BHSub) are provided primarily for information and may require user validation before use.
- Change mapping across LCM2007 updates is complex and not well suited for straightforward change detection due to differing class definitions and spatial structures across versions; typical classification errors in imagery are around 20%, which affects BH change interpretation.

## Methodology and Change Detection

- Production uses terrestrial generalised OS Master Map data, OSMM vector data, and segmentation to generate polygons with metadata on processing history, spectral classification, and knowledge-based enhancements (KBE).
- Change mapping across LCM2007 versions is not recommended as a sole change-detection approach due to class and spatial structure changes between LCM versions.

## Spatial Coverage, Projections, and File Sizes

- Projections:
  - Great Britain: British National Grid (OSGB 1936).
  - Northern Ireland: Irish National Grid (and progressing toward ITM in NI).
- File size guidance (geotiff formats):
  - Vector GB: ~4.13 GB; NI: ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: GB datasets range from ~21 MB (percent cover) to ~49 KB (dominant cover).
- The vector dataset comprises almost 10 million polygons with 10 attributes each.

## Appendices and Colour Mapping

- Appendix 1: Detailed descriptions of the 23 LCM2007 Broad Habitat classes, including subdivisions and notes on potential misclassifications (e.g., Neutral/Calcareous Grassland, Heather vs Heather grassland, Montane habitats, etc.).
- Appendix 2: Crosswalk between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Colour mapping recipe for standard LCM2007 visualization (RGB values per class); color mapping is also available as an ArcGIS .lyr file.
- Appendix 4: Updates to Products (Version 1.2, May 2014) including new tile coverage (Fair Isle, Stranraer) and the addition of water class for certain 1 km products.

## Updates and Version History

- Version 1.2 (May 2014)
  - Vector GB updated for OS Tile HZ (Fair Isle).
  - 25 m GB raster and 1 km GB products updated for Fair Isle and Stranraer; NI 1 km products updated to include water class.
- Version history indicates ongoing updates to tile coverage and data accuracy, with notes on water class addition for some products.

## Practical Guidance for Data Support

- Choose the product type based on needs:
  - Vector: use Parcel_ID and per-polygon attributes for detailed analysis and feature-level inquiries.
  - 25 m raster: useful when polygon boundaries and metadata are not required; retains land cover detail with less overhead.
  - 1 km raster: suitable for UK-scale modelling and integration with other gridded datasets (e.g., meteorology, species distributions) with percentage and dominant class information.
- Use the crosswalks (Appendix 2) to align LCM2007 classes with Broad Habitats when aggregating or comparing with other datasets.
- Utilize the 23-class BH/sub-class detail judiciously; where high confidence at sub-classes is required, perform independent validation as recommended.
- For visualization, apply Appendix 3 colour mappings or load the ArcGIS .lyr for consistent presentation.
- Be mindful of data access restrictions and potential licensing fees; factor in large vector file sizes in workflow planning.
- For users needing change analysis over time, consult the Final Report (Morton et al., 2011) for methodological guidance and consider limitations due to class and spatial structure changes.