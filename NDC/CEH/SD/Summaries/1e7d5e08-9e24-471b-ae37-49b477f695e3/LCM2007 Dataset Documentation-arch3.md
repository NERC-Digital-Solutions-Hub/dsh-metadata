# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based classification of UK land cover using 23 Broad Habitat-based classes, derived from summer-winter satellite imagery at 20–30 m resolution.
- Provides a range of data products to support diverse monitoring needs and applications; final report Morton et al. 2011 (Final Report for LCM2007) recommended for detailed assessment.

## Data products and structure

- Vector Data Set
  - ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Each polygon has 10 attributes, including area, source images, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (class number for display), KBE history, ProbList, CorePixels, Construct, TotPixels.
  - Contains unique Parcel_ID for each parcel to enable unambiguous communication; recommended to retain.
  - Includes Broad Habitat sub-classes (BHSub) and FieldCode; KNOWN to be less consistently validated than LCM2007 classes; users should validate if using sub-classes.
- Raster Data Sets
  - 25 m and 1 km products derived from the vector data.
  - Great Britain and Northern Ireland provided in separate projections.
  - 25 m raster contains the 23 LCM2007 classes; 1 km raster products include dominant cover, percentage cover, and aggregate-class versions (for 1 km raster).
- Data access and licensing
  - 1 km raster data available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under license; fees may apply.

## Classification, classes, and mappings

- 23 LCM2007 classes are based on UK Broad Habitats and sometimes subdivided for greater distinction (e.g., Built-up Areas: Suburban/Urban; Dwarf Shrub Heath: Heather vs Heather grassland; Littoral Sediment: Saltmarsh vs other Littoral).
- Relationship to Broad Habitats is detailed (Appendix 2); 1 km rasters use Aggregate classes derived by merging LCM2007 classes.
- Appendix 1 describes each class; Appendix 2 and Appendix 3 map relationships and standard color mappings used in outputs.

## Data quality, metadata, and validation

- Rich metadata for each polygon, including processing history (KBE), original spectral classifications, and top spectral variants (ProbList).
- Ground reference validation: ~9,127 polygons validated; average accuracy around 83%, with potential local discrepancies.
- Accuracy and interpretation caution:
  - LCM maps land cover, not strictly land use.
  - 0.5 ha minimum mappable area applied; parcels below this threshold are dissolved into surrounding landscape.
  - Broad Habitat sub-classes are useful but not as rigorously validated as the main LCM2007 classes; users should perform their own validation for sub-classes if used.

## Technical specifics

- Data formats and scales
  - Vector: polygon features with 10 attributes; high-detail, large file sizes (~10 million polygons; examples: GB vector ~4.13 GB).
  - Raster: 25 m and 1 km products; GB and NI projections differ (GB in British National Grid; NI in Irish National Grid; NI moving toward ITM in the future).
- Projections and datums
  - GB: OSGB 1936, British National Grid, Transverse Mercator.
  - NI: Ireland 1965 for older NI data; movement toward ITM.
- Spatial resolution and MMU
  - 25 m vector polygons; MMU > 0.5 ha; smaller parcels dissolved.
- File size notes
  - Vector data are large due to attribute richness (GB ~4.13 GB; NI ~433 MB for 100 km x 100 km shapefiles).
  - Raster files: 25 m GB ~1.36 GB; NI ~46 MB; 1 km products smaller (21 MB to 49 KB, depending on product).

## Usage guidance and cautions for monitoring frameworks

- Governance and transparency
  - Strong metadata and processing history support data governance and provenance needs for monitoring frameworks.
  - Parcel_ID and KBE history enable traceability of classifications and re-analyses.
- Data integration and interoperability
  - Parallel vector and raster products allow integration with other GIS datasets; ensure consistent projections and MMU considerations.
  - Sub-class BHSub data can augment analysis but should be validated due to variable accuracy.
- Data availability and openness
  - Full vector and 25 m raster require licensing; 1 km raster is accessible via CEH gateway, enabling easier inclusion in monitoring dashboards.
- Scale and aggregation considerations
  - For national or regional monitoring, 1 km aggregates provide a practical view; for detailed local monitoring, 25 m vector or raster products are preferable.
- Limitations to consider
  - LCM2007 maps land cover, not always precise land use; some classes (e.g., arable land vs. grassland) can be spectrally similar and require ground-truth validation.
  - Some habitat classes (e.g., Montane Habitats) rely on altitude for some mappings; users should interpret these with awareness of potential methodological trade-offs.

## Accessing further information

- Final Report: Morton et al., 2011, Final Report for LCM2007 – the new UK Land Cover Map.
- Detailed Broad Habitat classifications: Jackson, 2000.
- Additional information and data access: CEH Information Gateway and CEH data portal (data requests and licensing).

## Acknowledgements

- Datasets derived from multiple satellite sources (Landsat-TM, SPOT, AWIFS, etc.) and Ordnance Survey cartographic data; CEH and Countryside Survey Partnership contributions acknowledged.