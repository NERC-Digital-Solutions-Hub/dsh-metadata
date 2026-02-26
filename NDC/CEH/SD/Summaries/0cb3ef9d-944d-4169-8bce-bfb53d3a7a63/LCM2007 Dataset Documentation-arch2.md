# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification using 23 classes based on Broad Habitats, derived from 20–30 m satellite imagery. It updates LCM2000 with a framework based on OS MasterMap and refined with image segments to produce polygons representing real-world objects.

## Key features for analysts

- Data focus: maps land cover (not directly land use); MMU is >0.5 ha; parcels <0.5 ha or linear features are dissolved.
- Thematic resolution: 23 LCM2007 classes with some Broad Habitat sub-classes (BHSub) offering additional detail, used primarily for spectral variation and metadata, not always with QA-level accuracy.

## Data products and structure

- Vector Data Set
  - Approximately 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon has 10 attributes including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class code 1–23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Parcel_ID provides a unique parcel identifier; recommended to retain for unambiguous communication.
  - Sub-classes and FieldCodes used for classification history; ProbList shows spectral-class likelihoods and should be validated for use at subclass level.
- Raster Data Sets
  - Derived 25 m and 1 km products from the vector data; Great Britain and Northern Ireland are provided in separate projections.
  - 25 m raster: 23 LCM2007 classes; 1 km raster products include:
    - Dominant cover at 1 km for LCM2007 classes
    - Dominant cover at 1 km for Aggregate classes
    - Percentage cover at 1 km for LCM2007 classes
    - Percentage cover at 1 km for Aggregate classes
- Class relationships
  - Table 2 provides the mapping between Broad Habitat, LCM2007 class numbers, and aggregate class numbers (for 1 km rasters).
  - Appendix 2 details relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Color mapping
  - Appendix 3 provides the standard LCM2007 colour mapping used in the Final Report (Morton et al., 2011).

## Metadata, validation, and quality

- Rich metadata: polygon-level records include processing history and a Knowledge-Based Enhancement (KBE) history.
- Validation: ground reference data with 9127 polygons yielded an average accuracy of 83%, acknowledging local discrepancies and lower accuracy at some subclass levels.
- LCM2007 is thematically validated at the 23 LCM2007 classes; sub-class accuracy is not uniformly QA-validated.

## Data access and licensing

- 1 km raster data are accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product are available under license on request from CEH.
- Fees may apply for some users/applications; application process detailed on the CEH data site or by contacting spatialdata@ceh.ac.uk.
- Northern Ireland data projections: Irish National Grid (with ongoing transition to ITM); GB data are in British National Grid (OSGB 1936).

## Spatial framework and file considerations

- Projections
  - GB: British National Grid; NI: Irish National Grid; NI is transitioning to ITM.
- File sizes (indicative)
  - Vector (GB 100 km x 100 km shapefile): ~4.13 GB; NI ~433 MB
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB
  - Raster 1 km: 21 MB to 49 KB depending on product
- Data scale and usage
  - Vector provides detailed polygon and metadata; suitable for high-resolution analyses but larger file sizes.
  - 25 m rasters preserve detail with less metadata overhead; 1 km rasters are suitable for UK-scale modelling and are often used with additional data (meteorology, species distributions).

## Guidance, limitations, and recommended use

- Consult Final Report: Morton et al. (2011) for a comprehensive methodology, limitations, and detailed descriptions of production and QA.
- Broad Habitat vs. LCM2007 classes
  - LCM2007 class numbers are preferred for QA; Broad Habitat sub-classes may be less consistent across datasets and should be validated by users if used at the subclass level.
- Practical use cases
  - Use 1 km rasters for national-scale modelling and when combining with other datasets.
  - Use 25 m rasters or vector data for detailed, site-specific analyses with richer attribute metadata.
  - Consider aggregating to Broad Habitat aggregates when uniform accuracy is required or when cross-dataset comparisons are needed.
- Related resources
  - Appendix 1: List of LCM2007 classes (definitions and nuances)
  - Appendix 2: Crosswalk between Broad Habitats, LCM2007 classes, and BH-subclasses
  - Appendix 3: Standard colour mapping for display

## Additional information

- Data provenance and acknowledgments emphasize Landsat, SPOT, AWIFS imagery, and collaboration with mapping authorities; data are produced by CEH in partnership with Countryside Survey.
- For more details, refer to:
  - Morton et al., 2011, Final Report for LCM2007
  - Jackson, 2000, Broad Habitat Classification guidance
  - Countryside Survey documentation and website

- Contact for data access and licensing: spatialdata@ceh.ac.uk; CEH data portal and online application at www.ceh.ac.uk/data