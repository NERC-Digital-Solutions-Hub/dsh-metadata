# Land Cover Map 2007 Dataset documentation

- The Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification provided as multiple data products to support diverse user needs. It uses 23 Broad Habitat-based classes, derived from summer-winter satellite composites with 20–30 m pixels, and updates the earlier LCM2000 using a refined spatial framework linked to OS MasterMap and related vector data.
- LCM2007 maps land cover (not land use) and applies a minimum mappable unit of greater than 0.5 ha; parcels under 0.5 ha or linear features under 20 m are dissolved into surrounding landscape.

## Data products and formats

- Vector Data Set: polygons with 10 attributes each, totaling about 8.6 million polygons in Great Britain and 0.9 million in Northern Ireland. Includes Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels, and related metadata.
- Raster Data Sets:
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately due to different projections.
  - 1 km raster: derived from 25 m data; provides dominant class, dominant aggregate class, and percentage cover for both LCM2007 classes and their aggregates.
- Class relationships: LCM2007 classes are tied to UK Broad Habitats; spatial and spectral information allows conversion to coarser aggregates for broad-scale analyses.
- Data volumes: Vector in 100 km x 100 km blocks is large (GB about 4.13 GB; NI about 433 MB); 25 m rasters: GB about 1.36 GB; NI about 46 MB; 1 km rasters are smaller (up to 49 KB for the dominant cover and up to ~21 MB for the 23-class percentage products).

## Classification and content details

- 23 LCM2007 classes are based on Broad Habitats (JNCC Jackson 2000), with some subdivisions:
  - Built-up Areas and Gardens split into Urban and Suburban.
  - Dwarf Shrub Heath split into Heather and Heather grassland.
  - Littoral Sediment subdivided into Littoral sediment and Saltmarsh (Priority habitat).
- The dataset includes Broad Habitat sub-classes (BHSub) and FieldCode; caution is advised when using sub-classes for analysis, as their accuracy and consistency may be lower than the main LCM2007 classes.
- Ground reference validation: 9127 polygons validated LCM2007 against ground data, achieving an average accuracy of 83% (with expected local variation).

## Metadata and data quality

- Rich polygon metadata accompany the vector data, including processing history (KBE), spectral-class probability lists (ProbList), and catalogued provenance (OSMM or segmentation methods).
- The dataset is designed with QA in mind; however, the brochure notes that some Broad Habitat sub-classes are not covered by QA to the same extent as the primary LCM2007 classes and should be validated by users if used at that level.
- Documentation emphasizes familiarity with production methodology, metadata, and limitations before use.

## Data access and licensing

- 1 km raster data are available via the CEH Information Gateway (gateway.ceh.ac.uk).
- The full vector product and the 25 m raster product are available on request under licence from CEH; online application is available, with potential licence fees for some users and applications.

## Spatial reference and projection

- Vector and 25 m rasters for Great Britain use the British National Grid; Northern Ireland uses the Irish National Grid.
- NI data are in the process of switching to the Ireland Transverse Mercator (ITM) projection; reprojection in GIS packages is supported if required.

## Map content and usage guidance

- LCM2007 maps land cover rather than land use; for example, arable crops map to arable land, but land-use in some cases (e.g., grass used for recreation vs. grazing) may not be determinable from land cover alone.
- The dataset supports multi-scale environmental monitoring and policy evaluation by offering standardized outputs (23-class and aggregated 1 km products) and a robust, well-documented data lineage.
- Best practices recommended: retain Parcel_ID for communication across users; validate Broad Habitat subclasses as needed; combine LCM2007 outputs with other data sources for richer environmental analyses.

## Appendix highlights

- Appendix 1: LCM2007 Classes (definitions and examples for each Broad Habitat class, including nuances in classification such as grassland distinctions and bog/peat considerations).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (mapping guidance between 23 classes and corresponding Broad Habitat groupings).
- Appendix 3: Standard LCM2007 colour mapping (for visualization in reports and GIS).

## Additional information

- Recommended further reading includes the Final Report for LCM2007 (Morton et al., 2011) and the JNCC guidance on Broad Habitat interpretation (Jackson, 2000).
- Acknowledgements note the diverse satellite and cartographic data sources used to produce LCM2007, with copyright details and usage rights.