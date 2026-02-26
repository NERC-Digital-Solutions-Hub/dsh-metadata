# Land Cover Map 2007 Dataset Documentation

## Overview
- Land Cover Map 2007 (LCM2007) is a UK-wide parcel-based land cover classification, mapped to 23 classes based on Broad Habitats.
- Built from summer-winter satellite composites (20-30 m pixels) and enhanced with OS MasterMap/large-scale vector frameworks; aims to align with real-world objects for GIS compatibility.
- Maps land cover (not strictly land use) with a minimum mappable unit of 0.5 ha; finer parcels dissolved to surrounding landscape.
- Validated at 23-class thematic resolution with an average accuracy around 83% against ground reference data; local discrepancies may occur.
- Not well suited for change detection across LCM generations due to class/structure differences and typical image classification errors (~20%).

## Data Products and Structure
- Vector Data Set
  - Great Britain: ~8.6 million polygons; Northern Ireland: ~0.9 million polygons.
  - Each polygon has 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Includes unique Parcel_ID for unambiguous communication; Broad Habitat sub-classes (BHSub) available but not guaranteed QA-validated at subclass level.
  - 23 LCM2007 classes with a mapping to Broad Habitats; Appendix 2 details relationships; Appendix 3 provides standard colour mapping.
- Raster Data Sets
  - 25 m raster for 23 LCM2007 classes and corresponding 25 m data for GB and NI; 1 km raster products provide dominant/percentage cover for both LCM2007 classes and Aggregate classes.
  - GB and NI data are separate due to different projections.
  - Metadata includes detailed grid dimensions, extents, pixel sizes, data types, projections, datums.
- Data Access
  - 1 km raster data accessible via CEH Information Gateway.
  - Full vector product and 25 m raster product available under licence on request from CEH (licensing fees may apply).
- Projections and Coordinate Systems
  - GB: British National Grid (OSGB 1936); NI: Irish National Grid (Ireland 1965).
  - Northern Ireland moving toward Ireland Transverse Mercator (ITM); reprojecting recommended as needed.
- File Sizes
  - Vector (GB 100 km x 100 km shapefile): ~4.13 GB; NI ~433 MB.
  - Raster (GB 25 m): ~1.36 GB; NI ~46 MB.
  - 1 km rasters: 21 MB to 49 KB depending on product.
- Data Formats and Access Considerations
  - Vector products: polygonal boundaries with attached metadata; larger file sizes can affect processing.
  - 25 m rasters provide similar land cover detail without polygon boundaries/metadata.
  - 1 km rasters suitable for national-scale modelling and integration with other datasets (e.g., meteorological, species distribution).

## Methodology and Quality Assurance
- Production methods include segmentation-based polygon construction, knowledge-based enhancements (KBE), and spectral class probability listings (ProbList).
- Ground reference validation involved 9,127 polygons, yielding an average accuracy of 83%.
- KBE history captures processing adjustments (e.g., soil, altitude, urban masks) for each polygon.
- Important caveats:
  - Sub-class accuracy may be lower than primary LCM2007 class accuracy; users are advised to validate sub-classes if used for fine-grained analysis.
  - Change detection across LCM2000/1990/2007 is challenging due to class/structure differences and varying spatial schemas; not ideal for change mapping.

## Classifications and Documentation
- 23 LCM2007 classes arranged under Broad Habitats (Appendix 1); some Broad Habitats are further subdivided (BHSub) to capture spectral variations.
- Appendix 2 provides the mapping between Broad Habitats, LCM2007 classes, and BH sub-classes.
- Appendix 3 provides a standard colour mapping (including an ArcGIS .lyr template) for visualization.
- Appendix 4 lists updates (Version 1.2, May 2014) including new tiles (Fair Isle, Stranraer) and the addition of water classes to 1 km products.

## Governance, Use and Licensing Considerations for Data Stewards
- Data stewardship considerations
  - Ensure governance around licensing for vector and 25 m raster products; manage access controls and usage rights (licensing fees may apply for some users/applications).
  - Maintain Parcel_ID and other identifying attributes to support clear communication and traceability across datasets.
  - Retain rich metadata per polygon to preserve processing history, source imagery, KBE actions, and probability information for robust provenance.
  - Be mindful of the recommended validation for Broad Habitat sub-classes before detailed sub-class analyses.
- Data maintenance and updates
  - Version 1.2 (May 2014) introduces area updates (e.g., OS tiles Fair Isle, Stranraer) and the inclusion of water class data for some products.
  - Users should reference Morton et al. (2011) Final Report for a comprehensive description of production methodology and limitations.
- Usage guidance for Data Stewards
  - When communicating across datasets, use the LCM2007 class (INTCODE) for display and QA-approved classifications; be cautious when interpreting BHSub.
  - For national-scale modelling or simple visualization, 1 km raster products may be more practical; use 25 m or vector products for higher-detail analyses with adequate processing capacity.
  - Direct users to follow the Final Report for in-depth methodology and validation details; consider revalidation when employing Broad Habitat sub-classes.

## Documentation and References
- Primary references: Morton et al., 2011, Final Report for LCM2007; Jackson, 2000, Guidance on interpretation of Biodiversity Broad Habitat Classification.
- Acknowledgements note data sources from Landsat, SPOT, AWIFS, Ordnance Survey, and other contributing datasets.