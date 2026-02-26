# Land Cover Map 2007 Dataset Documentation

- UK-wide parcel-based land cover dataset (LCM2007) providing 23 classes aligned to UK Broad Habitats, created from summer–winter satellite composites at ~20–30 m resolution.
- Designed as a range of data products to support diverse user needs; final report Morton et al. (2011) recommended for in-depth evaluation.

## Data products and structure

- Vector Data Set
  - Polygons with 10 attributes each; unique Parcel_ID; includes Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (1–23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, and Construct history.
  - ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Includes BHSub and FieldCode for detailed interpretation; INTCODE is the recommended display class.
- Raster Data Sets
  - 25 m and 1 km rasters derived from the vector data; separate projections for GB and NI.
  - 23 LCM2007 classes at 25 m; 1 km rasters provide dominant and percentage cover (for both LCM2007 classes and Aggregates).
- Class structure
  - 23 LCM2007 classes based on Broad Habitats; where possible, some Broad Habitats are subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
  - MMU: minimum mappable area > 0.5 ha; parcels < 0.5 ha or linear features < 20 m dissolved into surrounding landscape.

## Relationship to Broad Habitats and labeling

- Appendix 1 and Appendix 2 define the 23 LCM2007 classes and their relationship to Broad Habitats and sub-classes.
- Parcel labels (Parcel_ID) link polygons to source images; ProbList provides the top five spectral class matches.
- Broad Habitat Sub-classes (BHSub) provide additional detail but are not as consistently accurate as the primary LCM2007 classes; users are advised to validate subclass information as needed.

## Metadata, quality assurance, and validation

- Rich metadata per polygon, including processing steps, KBE history, and probability data.
- Validation conducted against ground reference polygons (9127 polygons) with an average accuracy of 83%; local variations may occur.
- Knowledge-based enhancements (KBE) applied to refine classifications; accuracy varies by class and region.

## Data access, licensing, and how to obtain

- 1 km raster data available via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; online application at ceh.ac.uk/data or via spatialdata@ceh.ac.uk.
- Licence fees may apply for some users/applications.
- All data are supported by detailed documentation and appendices; final report Morton et al. (2011) provides comprehensive methodology and validation context.

## Projections, file sizes, and data formats

- Projections
  - Great Britain: British National Grid (OSGB 1936).
  - Northern Ireland: Irish National Grid (with NI transitioning to ITM in progress).
- File sizes (approximate guidance)
  - Vector (shapefile, 100 km × 100 km tiles): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB depending on content.
- Data formats
  - Vector: polygon features with 10 attributes; supports detailed attribute analysis and metadata-rich communication.
  - Raster: 25 m and 1 km products suitable for broad-scale modelling and aggregation.

## Practical guidance and caveats

- LCM2007 maps land cover, not strictly land use; interpretation should consider context (e.g., crops vs. actual land use).
- Some classes can be challenging to distinguish spectrally; Broad Habitat subclasses (BHSub) may require independent validation for fine-grained analyses.
- Data integration considerations
  - 0.5 ha MMU and 20 m line features may cause fragmentation in some landscapes.
  - Spatial alignment with other datasets may require reprojection where necessary.
- Recommended usage patterns
  - Use 25 m vector data for detailed, metadata-rich analyses; 25 m rasters for applications requiring non-vector formats; 1 km rasters for nationwide modelling and broad-scale analyses (percent cover and dominant class per pixel).

## Appendices and additional information

- Appendix 1: LCM2007 Classes – detailed definitions and examples for all 23 classes.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Colour mapping (LCM2007 class → RGB) used in the final report.
- Acknowledgements include data sources (Landsat, SPOT, AWIFS, Ordnance Survey, and other datasets) and copyright information.
- References for deeper methodological context: Morton et al. (2011) Final Report for LCM2007; Jackson (2000) guidance on Broad Habitat classifications.