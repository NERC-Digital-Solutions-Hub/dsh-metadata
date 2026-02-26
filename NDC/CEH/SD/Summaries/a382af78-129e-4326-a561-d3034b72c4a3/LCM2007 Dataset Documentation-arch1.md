# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based classification of the UK with 23 classes based on Broad Habitats, derived from 20–30 m satellite imagery. It maps land cover (not land use) and uses a 0.5 ha minimum mapping unit.
- The dataset updates LCM2000 and aligns with a GIS-friendly spatial framework (OSMM/LDSS), producing polygons that represent real-world objects.

## Data Products and Structure

- Vector Data Set
  - Approximately 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon has 10 attributes, including Parcel_ID (unique per parcel), BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class for display), KBE (processing history), ProbList (top 5 spectral class matches), CorePixels, Construct, TotPixels.
  - Parcel_ID should be retained for unambiguous communication; BH/Sub-class codes aid interpretation but may require user validation for sub-classes.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes (GB and NI in separate projections).
  - 1 km raster: aggregated products for UK-wide modelling, including dominant class and percentage cover (both for LCM2007 classes and their aggregates).
  - Metadata for all raster products includes grid size, extent, projections, pixel size, data type, and datum.
- Relationship and Validation
  - Appendix 2 provides the mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Ground-reference validation used 9,127 polygons, yielding an average accuracy of 83%, with expected local variations.

## Classifications and Metadata Details

- LCM2007 uses 23 classes aligned to UK Broad Habitats; some Broad Habitats are further subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and other).
- Each vector polygon includes:
  - BH (dominant Broad Habitat)
  - BHSub (Broad Habitat sub-class)
  - FieldCode (short textual code; not all are QA-validated)
  - ProbList (top spectral matches with probabilities)
  - KBE (knowledge-based enhancements applied)
  - Construct history (OSMM-based segmentation, etc.)
- Appendix 1 describes the 23 LCM2007 classes; Appendix 2 details the correspondence with Broad Habitats and sub-classes; Appendix 3 provides standard RGB color mappings for visualization.

## Data Access and Licensing

- 1 km raster data sets are accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product are available under license on request from CEH; licensing fees may apply.
- Data access details: online application via CEH site or direct contact to spatialdata@ceh.ac.uk.
- Data sizes are large (vector ~4.13 GB GB shapefile; NI ~433 MB; 25 m raster GB ~1.36 GB; NI ~46 MB; 1 km products range 21 MB to 49 KB).

## Spatial Details and Scale

- Projections
  - GB: British National Grid
  - NI: Irish National Grid (with ongoing transition to ITM in NI)
- Resolution and MMU
  - 25 m raster derived from 23 LCM2007 classes
  - 1 km raster provides dominant and percentage cover for both LCM2007 and aggregated classes
  - Minimum mappable unit: >0.5 ha; parcels smaller than 0.5 ha or lines shorter than 20 m dissolved into surroundings
- Data Volume and Handling
  - Vector data comprises many features with rich metadata; large file sizes require appropriate storage and processing capabilities
- Data Coverage and Use Considerations
  - LCM2007 maps land cover (not strictly land use); spectral classes may not perfectly indicate land use in all cases
  - Sub-class information (BHSub) can be informative but may require local validation due to QA limitations
  - For detailed grassland and coastal classes, be aware of potential mis-classifications and consult Morton et al. 2011 Final Report for guidance

## Quality, Limitations, and Guidelines

- Accuracy
  - Average ground-reference accuracy around 83%, with local deviations expected
  - Broad Habitat sub-classes and some spectral variants may have lower reliability; users should validate sub-class decisions for specific applications
- Limitations
  - 0.5 ha MMU may exclude many small features or narrow linear features
  - Coastal, freshwater, and certain rural features can be challenging due to spectral similarity and mosaic patterns
  - Some field codes (FieldCode) lack robust QA; use ProbList and KBE history to inform validation
- Recommendations for Analysts
  - Retain Parcel_ID to ensure unambiguous communication across datasets
  - Use the 1 km raster products for UK-wide modelling and the 25 m vector/raster products for finer-scale analyses where needed
  - Validate Broad Habitat sub-classes if used for precise habitat-specific analyses
  - Refer to Morton et al. 2011 Final Report for production methodology, metadata, limitations, and validation details

## Additional Information and Acknowledgements

- Primary reference: Morton et al. 2011, Final Report for LCM2007 – Countryside Survey Technical Report No. 11/07
- Related background: Jackson 2000 (JNCC) for Broad Habitat classification
- Acknowledgements to data providers and collaborators (Landsat, SPOT, AWIFS, OS, etc.)