# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A parcel-based classification of UK land cover (LCM2007) using 23 classes derived from Broad Habitats; created from summer-winter satellite composites at ~20–30 m resolution.
- Supports multiple data products (vector and raster) to meet diverse GIS applications; distinguishes land cover (not strictly land use).

## Key Data Content

- Vector Data Set
  - ~8.6 million polygons for Great Britain; ~0.9 million for Northern Ireland
  - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels
  - Unique Parcel_ID retained for unambiguous communication
  - Broad Habitat sub-classes present but less reliable for QA; recommended only with independent validation
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately with appropriate projections
  - 1 km raster: derived summaries for dominant and percentage cover (both LCM2007 classes and Aggregate classes)
  - Aggregate classes used for 1 km products to simplify applications

## Product Details and Resolution

- LCM2007 Classes
  - 23 classes based on UK Broad Habitats; some are subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland)
  - Minimum mappable unit: >0.5 ha; parcels <0.5 ha and lines <20 m dissolved
- Broad Habitat Relationships
  - Appendix 2 explains mappings between Broad Habitats, LCM2007 classes, and sub-classes
  - Appendix 3 provides standard colour mappings used in the Final Report
- Data Formats and Access
  - Vector: polygon features with rich metadata
  - Raster: 25 m and 1 km products; GB and NI projections differ (British National Grid vs Irish National Grid); NI transitioning to ITM
  - Data access: 1 km rasters via CEH Information Gateway; full vector and 25 m products on request from CEH (licensing may apply)

## Quality, Validation, and Limitations

- Validation
  - Ground reference data driving QA; 9,127 polygons used for validation
  - Average accuracy around 83%; local discrepancies possible
- Data Quality Considerations
  - LCM2007 maps land cover (not strictly land use); some areas may be misclassified with spectral similarity
  - Broad Habitat subclasses exist primarily for supporting ProbList and KBE history; they are not covered by complete QA at subclass level
  - Grassland classes (Neutral, Calcareous, Acid) and some peat-related classes can be misclassified; users should validate for their specific needs
- Use Guidance
  - Familiarise with production methodology and metadata; consult Final Report (Morton et al., 2011) for comprehensive details
  - For high-precision needs, prefer LCM2007 class level with QA validation or aggregate classes for reduced misclassification risk

## Data Projection, Size, and Packaging

- Projections
  - GB: British National Grid (OSGB36); NI: Irish National Grid
  - NI may be migrating to ITM; reprojecting recommended as needed
- File Sizes (guidance)
  - Vector (shapefile, 100 km x 100 km): GB ~4.13 GB; NI ~433 MB
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB
  - Raster 1 km: 21 MB to 49 KB (depending on product)
- Data Access and Licensing
  - 1 km rasters: CEH Information Gateway
  - Full vector and 25 m products: license on request from CEH; online application available
  - Fees may apply; contact spatialdata@ceh.ac.uk for details

## Where to Find More Information

- Core references
  - Morton et al. 2011, Final Report for LCM2007 (Countryside Survey Technical Report No. 11/07)
  - Jackson 2000, Guidance on Broad Habitat Classification (JNCC Report 307)
- Appendices
  - Appendix 1: LCM2007 Classes (descriptions and nuances)
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
  - Appendix 3: LCM2007 colour mapping (RGB values for each class)

## Practical Takeaways for GIS Specialists

- Choose between vector (rich metadata) and raster (faster processing, less metadata) according to application needs
- For detailed, communication-ready outputs, retain Parcel_ID and consider using BHSub with caution and validation
- Use 1 km rasters for regional analyses and rapid modelling; use 25 m rasters or vector data for finer-scale analyses
- Validate Broad Habitat sub-classes if used for analysis beyond the 23-class QA scope
- Be mindful of MMU limitations and potential classification ambiguities in grassland and peat-related areas
- Leverage Appendix 2 and Appendix 3 when translating LCM2007 classes to other classifications or visual representations