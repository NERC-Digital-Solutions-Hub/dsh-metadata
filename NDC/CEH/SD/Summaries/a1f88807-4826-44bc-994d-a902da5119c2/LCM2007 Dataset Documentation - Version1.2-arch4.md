LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK-wide parcel-based land cover classification (LCM2007) using 23 classes aligned to Broad Habitats.
- Derived from 20-30 m satellite imagery; updates LCM2000 with OS-based spatial framework and image segmentation.
- Maps land cover (not strictly land use); minimum mappable area >0.5 ha; smaller parcels are dissolved into surrounding landscape.
- Vector data provides rich metadata and unique Parcel_IDs for unambiguous communication; validated with ground reference data (~83% average accuracy).

## Data Products and Structure
- Vector Data Set
  - Great Britain: 8.6 million polygons; Northern Ireland: 0.9 million polygons.
  - Each polygon has 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Includes Broad Habitat sub-classes (BHSub) and field codes; INTCODE is the display class (1-23).
  - Knowledge-based enhancements (KBE) and a ProbList with top spectral matches for each polygon.
  - All polygons carry a unique Parcel_ID for traceability.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI separate projections.
  - 1 km raster: aggregates derived from 25 m rasters; includes Dominant class and Percentage cover for both LCM2007 classes and Aggregates.
  - GB and NI raster products provided with appropriate metadata (grid size, extents, projection, data type Uint8).

## Data Access and Licensing
- 1 km raster data: available via the CEH Information Gateway.
- Full vector product and 25 m raster: available on request under licence from CEH; fees may apply.
- Access process: online application or direct contact (spatialdata@ceh.ac.uk).

## Technical Details
- Map Projection and Coordinate Systems
  - Great Britain: British National Grid (OSGB 1936); Transverse Mercator projection.
  - Northern Ireland: Irish National Grid; Irish Transverse Mercator (ITM) progression expected; reprojecting supported in GIS.
- File Sizes
  - Vector (GB): ~4.13 GB; Vector (NI): ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: GB 21–49 KB range for aggregated products (smaller files); NI similar scales for aggregated products.
- MMU and Coding
  - Minimum mapping unit >0.5 ha; features smaller than this dissolved.
  - 23 LCM2007 classes mapped from 25 m and structured to align with Broad Habitats; some subclasses (BHSub) are not QA’ed at the same level as primary LCM2007 classes.

## Data Quality and Validation
- Ground reference validation against polygons yielded about 83% average accuracy; disaggregated visibility may yield higher or lower local accuracy.
- Change detection across LCM1990, LCM2000, and LCM2007 is complex due to differing class definitions, spatial structure, and typical change detection errors (~20%).

## Usage Guidance for Data Leaders
- Choose dataset level based on application needs:
  - 25 m Vector: rich metadata and high thematic detail; suitable for analyses requiring per-polygon lineage and processing history (KBE, ProbList, etc.).
  - 25 m Raster: easier processing and smaller file sizes; suitable for workflows prioritizing uniform grid data with less metadata overhead.
  - 1 km Raster: suitable for national-scale modeling and integration with other large-scale datasets.
- Be mindful of:
  - LCM2007 maps land cover, not strictly land use; interpretation should account for spectral vs. functional distinctions (e.g., arable land vs. actual use).
  - The 0.5 ha MMU and dissolution rules can affect small features and linear features.
  - Sub-class information (BHSub) provides additional detail but may require local validation before use at that level.
  - Data accuracy can vary regionally; users should perform own validation for critical applications.
- Metadata richness supports traceability, reproducibility, and governance, enabling robust data stewardship and cross-team collaboration.

## Appendices (Content at a Glance)
- Appendix 1: LCM2007 Classes – high-level definitions and criteria for each class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grassland types, wetlands, urban, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes – mapping framework (class numbers, codes, and BHSub associations).
- Appendix 3: LCM2007 colour mapping – standard color recipes for display (useful for GIS styling and ArcGIS layers).
- Appendix 4: Updates to Products (Version 1.2, May 2014) – changes such as OS Tile additions (Fair Isle, Stranraer) and water class inclusion.

## Key Takeaways
- LCM2007 offers a rich, multi-resolution national land cover dataset built on robust vector and raster products with extensive metadata and QA groundwork.
- It is a mature, governance-friendly data resource suitable for data-driven leadership across policy, planning, and environmental analysis, with clear access paths and licensing considerations.