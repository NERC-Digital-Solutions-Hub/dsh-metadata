# LAND COVER MAP 2007 DATASET DOCUMENTATION

- UK land cover map (LCM2007) is a parcel-based classification using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Data are derived from summer-winter satellite composites at 20–30 m pixel size.
- Upgrades LCM2000 using an OS MasterMap-based spatial framework and image segmentation to map real-world objects (fields, woodland blocks).
- Distinguishes land cover (not strictly land use); minimum mappable unit is >0.5 ha; parcels <0.5 ha or linear features <20 m are dissolved.

## Data products and structure

- Vector data set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Parcel_ID is a unique label for communication clarity; BHSub provides Broad Habitat sub-classes; INTCODE is the 1–23 LCM2007 class for display and QA.
  - Probability list (ProbList) shows top 5 spectral class matches; KBE records knowledge-based enhancements (processing history and changes).
  - Sub-classes (BHSub) add information but are not always as reliable as LCM2007 classes; recommended validation when used at subclass level.

- Raster data sets
  - 25 m and 1 km products; GB and NI provided separately due to different projections.
  - 25 m raster contains 23 LCM2007 classes; 1 km rasters summarize 25 m data to provide dominant and percentage cover for both 23 classes and 10 Aggregate classes.
  - Metadata summarizes spatial extents, pixel counts, and projection details.

## Class structure and mapping

- 23 LCM2007 classes built from Broad Habitats; some Broad Habitats subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Appendix 1: detailed descriptions of the 23 classes.
- Appendix 2: mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: standard color mapping (RGB values) used in the Final Report.

## Data quality, validation, and caveats

- Ground reference validation against 9127 polygons yielded an average accuracy of 83%; local variations possible.
- LCM2007 focuses on spectral/class accuracy at the 23-class level; Broad Habitat sub-classes are provided but may require user validation.
- Knowledge-based enhancements (KBE) may reclassify Rough Grassland, Neutral/Calcareous/Acid Grasslands, and other grassland types; use these with caution and validate for specific analyses.
- Grassland class distinctions (Neutral/Calcareous/Acid) can misclassify relative to Improved Grassland; consider aggregation if needed.

## Data access and file sizes

- Access
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster data available on request under license; online application process or contact spatialdata@ceh.ac.uk.
  license fees may apply for some users/applications.

- File size guidance (geotiff/vector shapefile)
  - Vector (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km products: ranges from ~21 MB to ~49 KB depending on product.

- Projections
  - Great Britain: British National Grid (OSGB 1936) for vector and 25 m rasters.
  - Northern Ireland: Irish National Grid; NI moving toward Ireland Transverse Mercator (ITM); reprojecting supported in GIS.

- Data provenance and credits
  - Imagery and cartography from Landsat, SPOT, AWIFS; OS Master Map and related OS data; various national authorities for boundaries and ancillary data.
  - Acknowledges CEH and Countryside Survey Partnership; copyright and licensing notes apply.

## Practical guidance for analysts

- Use 23-class LCM2007 where detailed land cover distinctions are needed; use 1 km rasters for national-scale modeling or when linking with large-scale datasets (meteorology, species distributions).
- When combining datasets or modeling across scales, prefer vector data for high detail but be mindful of larger file sizes and processing load; 25 m rasters offer similar detail with reduced metadata overhead.
- Retain Parcel_ID for unambiguous communication; also keep BH and BHSub where relevant, but validate sub-class results for critical decisions.
- Consult Morton et al. 2011 Final Report for comprehensive methodology, limitations, and guidance on Broad Habitat classifications and knowledge-based enhancements.

## Additional resources

- Final Report for LCM2007 (Morton et al., 2011) for in-depth methodology and assessment.
- Guidance on Broad Habitat classification (Jackson, 2000) for interpreting relationships with LCM2007 classes.
- Online data access via CEH portal and data application process for full vector/25 m products.