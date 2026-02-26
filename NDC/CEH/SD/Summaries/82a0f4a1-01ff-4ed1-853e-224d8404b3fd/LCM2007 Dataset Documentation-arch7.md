# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview for GIS Specialists
- UK parcel-based land cover classification (LCM2007) using 23 classes aligned with UK Broad Habitats; based on summer-winter satellite composites at ~20–30 m resolution.
- Provides a range of data products (vector and raster) to support diverse GIS applications (policy, client projects, public mapping).
- Aims to be GIS-friendly: polygons with rich metadata and a consistent spatial framework to enable integration with other datasets.

## Data Products and Structure
- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland
  - 10 attributes per polygon (Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels)
  - Unique Parcel_ID for unambiguous communication; BHSub provides Broad Habitat sub-classes; FieldCode for detailed coding
  - Includes Knowledge-Based Enhancements (KBE) history and a 5-item ProbList (top spectral class matches)
  - MMU: minimum mappable unit > 0.5 ha; features under 0.5 ha dissolved
  - Relationship to Broad Habitats and sub-classes can be complex; Appendix 2 clarifies groupings
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes
  - 1 km raster: aggregates for national-scale analyses; dominant class and percentage cover for both LCM2007 classes and Aggregate classes
  - GB and NI provided separately due to differing projections
  - 1 km products include multiple outputs (dominant cover, percentage cover for both class schemes)
- Data Relationships
  - Table and appendix describe how LCM2007 classes map to Broad Habitats and to Broad Habitat sub-classes
  - Aggregate classes used for 1 km rasters to support broader-scale applications

## Spatial Framework and Projections
- Vector and raster products for Great Britain: British National Grid (OSGB36)
- Northern Ireland: Irish National Grid
- NI transitioning to Ireland Transverse Mercator (ITM); reprojection supported by GIS software as needed

## Data Quality and Validation
- Ground reference validation: average accuracy around 83% across polygons matched to the spatial/ thematic resolution
- Local discrepancies may occur; accuracy figures are averages across polygons
- Sub-class level (Broad Habitat sub-classes) not covered by standard QA; recommended user validation if using Broad Habitat sub-classes
- Broad Habitats and sub-classes may be confused in some cases (e.g., certain grassland types); Appendix 1–3 provide detailed definitions and colour mapping

## Classification and Metadata Details
- 23 LCM2007 classes derived from Broad Habitat classifications; some Broad Habitats split into sub-classes (e.g., Built-up Areas into Urban and Suburban)
- The vector dataset includes extensive metadata per polygon: source imagery, processing history (KBE), and spectral likelihood
- Class numbers used for display (INTCODE) are the recommended display classes and QA-backed
- LCM2007 maps land cover (not strictly land use); examples show differences (arable crops vs. grassland use may differ)

## Data Access and Licensing
- Data Access
  - 1 km raster data accessible via CEH Information Gateway
  - Full vector product and 25 m raster product available on request from CEH (licensing may apply)
- Licensing Considerations
  - Fees may apply for some users/applications
  - Documentation encourages online application or direct contact for licensing

## Data Sizes and Formats (Guidance)
- Vector (Shapefile, 100 km x 100 km): GB ~4.13 GB; NI ~433 MB
- Raster 25 m: GB ~1.36 GB; NI ~46 MB
- Raster 1 km: 21 MB to 49 KB depending on product
- Large file sizes reflect 10 attributes per polygon and nearly 10 million polygons; plan storage and processing accordingly

## Practical Guidance for GIS Workflows
- Use Vector Data Set when you need detailed polygon-level attributes, KBE history, and ProbList-based spectral context
- Use 25 m raster for simpler processing with the same land cover detail but without polygon boundaries and some metadata
- Use 1 km rasters for national-scale analyses, model inputs, or when integrating with other large-scale datasets (e.g., meteorology, species distributions)
- Retain Parcel_ID for clear communication and traceability between datasets and analyses
- When working with Broad Habitat sub-classes, perform local validation before relying on these details
- Be mindful of MMU and dissolution of small parcels; some fine-scale features may be generalized

## Appendices and Colour Mapping
- Appendix 1: LCM2007 Classes (detailed definitions for each Broad Habitat)
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
- Appendix 3: Standard LCM2007 colour mapping (for map display)

## Additional Information and References
- Final Report for LCM2007 and Morton et al. (2011) for comprehensive methodology and assessment
- Broad Habitat classification guidance and relation to ground-truth datasets
- Acknowledgements for data sources and licensing

## Limitations and Considerations for Use
- Sub-class level analysis requires caution; not all sub-classes have QA-style validation
- Classification is based on spectral data and KBE rules; ground conditions and temporal changes may affect accuracy
- Some habitats (e.g., Fen, Marsh and Swamp; Montane Habitats) have complex boundaries or altitude-based components that require contextual interpretation
- Users should validate critical classifications against local knowledge or additional datasets when precision is essential