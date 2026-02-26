# LAND COVER MAP 2007 DATASET DOCUMENTATION

- UK land cover dataset (LCM2007) is a parcel-based classification using 23 Broad Habitat-based classes, derived from 20–30 m satellite imagery.
- Provides multiple data products (vector and raster) to support diverse GIS and environmental monitoring needs; builds on LCM2000 with improved spatial framework (OSMM/large-scale vector layers) and segmentation.

## Data Products and Resolutions

- Vector Data Set:
  - Polygons with rich attributes; ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- Raster Data Sets:
  - 25 m resolution: 23 LCM2007 classes; GB and NI provided separately with matching projections.
  - 1 km resolution: aggregate products for both dominant and percentage cover (class- and aggregate-class based).
  - Data formats support: 25 m and 1 km rasters; GB and NI differ in projection and grid layout.
- Minimum mappable unit:
  - >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surrounding landscape.

## Classification System

- 23 LCM2007 classes aligned with UK Broad Habitats (Jackson et al., 2000).
- Some Broad Habitats subdivided into sub-classes for enhanced detail:
  - Built-up Areas and Gardens: Suburban and Urban
  - Dwarf Shrub Heath: Heather and Heather grassland
  - Littoral Sediment: Littoral sediment and Saltmarsh
- Class labels are used for display (INTCODE) and are supported by a detailed Appendix mapping Broad Habitats to LCM2007 classes.
- Note: LCM2007 maps land cover (not direct land use); examples illustrate potential ambiguity between cover and use.

## Data Structure and Metadata

- Parcel_ID: unique parcel identifier (e.g., 11853977:c20); recommended to retain for unambiguous communication.
- BH (Broad Habitat) and BHSub (Broad Habitat sub-class) describe dominant class and sub-class.
- FieldCode and ProbList provide additional, but not QA-validated, detail; ProbList lists top five spectral matches with associated probabilities.
- KBE (Knowledge-Based Enhancements): processing history and classification adjustments (e.g., soil, altitude corrections).
- CorePixels and TotPixels: pixel counts used in classification; Constructs indicate data sources (OSMM, seg-based, etc.).
- Rich metadata: extensive processing history and QA notes, including spectral/classification lineage.

## Validation and Accuracy

- Ground-reference validation: average accuracy ~83% against 9,127 polygons; accuracy varies by area and subclass.
- Sub-class level caution: Broad Habitat sub-classes and FieldCodes are included for supplementary information but may be less robust; user validation advised for sub-class analyses.
- Quality assurance supports the recognised 23 LCM2007 classes; sub-class accuracy is not uniformly validated.

## Data Access and Licensing

- 1 km raster data sets available via CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH.
- Licensing: may incur fees for some users/applications; application via CEH data portal or via data contact.

## Spatial Reference and Projections

- Great Britain: British National Grid (OSGB 1936), Transverse Mercator projection.
- Northern Ireland: Irish National Grid; NI will move to ITM projection (GIS tools should reproject if needed).
- Data are designed for GIS interoperability and cross-border analyses.

## File Sizes and Storage

- Vector (GB shapefile, 100 km × 100 km): ~4.13 GB; NI: ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- Raster 1 km: GB/NI products: 21 MB to 49 KB depending on product type.
- Large datasets; storage considerations and data management practices recommended.

## Production Details and Limitations

- LCM2007 is an evolution from LCM2000; uses OSMM/large-scale vector frames with segmentation to better reflect real-world objects.
- Delivers land cover (not land use) classification; certain land-use distinctions (e.g., crops vs. pasture) may not be fully unambiguous from cover alone.
- Minimum mapping unit and dissolution rules may affect the representation of small features.
- The dataset emphasizes compatibility with other GIS datasets and supports a wide range of applications when used with appropriate validation.

## Appendices (Key References)

- Appendix 1: LCM2007 Classes – detailed descriptions of the 23 Broad Habitat–based classes (e.g., Broadleaved Woodland, Coniferous Woodland, Arable and Horticulture, Improved Grassland, Semi-natural Grassland, Bog, Saltwater, Freshwater, Urban/Suburban, Inland Rock, Montane Habitats, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (mapping between Broad Habitats and the LCM2007 class numbers; field codes for sub-classes).
- Appendix 3: Colour mapping recipe for standard LCM2007 display (class-specific RGB values used in final reports and visualizations).

- Acknowledgements and data sources (Landsat-TM5, SPOT, AWIFS, OS datasets) and copyright notes accompany the documentation.