# LAND COVER MAP 2007 DATASET DOCUMENTATION

- The Land Cover Map 2007 (LCM2007) provides a range of data products to support diverse user needs and complements earlier LCM versions. Final report (Morton et al., 2011) is recommended for in-depth assessment.
- LCM2007 is a parcel-based land cover classification for the UK using 23 classes based on UK Biodiversity Action Plan Broad Habitats. It uses 20–30 m satellite imagery and updates LCM2000 with a GIS-friendly, object-based (polygon) framework via OS MasterMap (GB) and Large-scale Vector (NI).

Introduction and Background
- LCM2007 maps land cover (not always land use) and uses a minimum mapping unit (MMU) of >0.5 ha; parcels <0.5 ha or linear features <20 m are dissolved into surrounding areas.
- The 23 classes derive from Broad Habitats; some classes are subdivided (e.g., Built-up Areas; Dwarf Shrub Heath; Littoral Sediment).
- LC M2007 provides a rich metadata framework and a unique Parcel_ID for unambiguous communication.

Data Products

- Vector Data Set
  - Contains ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Each polygon has 10 attributes, including:
    - Parcel_ID: unique parcel identifier (includes source image)
    - BH: Broad Habitat (dominant level)
    - BHSub: Broad Habitat sub-class (descriptive)
    - FieldCode: short code describing sub-class
    - INTCODE: 1–23 LCM2007 class (display-ready)
    - KBE: Knowledge-Based Enhancements history
    - ProbList: top 5 spectral-class probabilities
    - CorePixels, TotPixels: pixel counts used in classification
    - Construct: polygon construction history (OSMM-derived, segmentation)
  - Includes Broad Habitat sub-classes (BHSub) and FieldCode; users are advised to validate sub-class level analyses.
  - Parcel_ID should be retained for clear communication and data lineage.
- Raster Data Sets
  - 25 m raster (23 LCM2007 classes) and 1 km raster products derived from the 25 m data.
  - GB and NI provided separately with distinct projections (GB: British National Grid; NI: Irish National Grid; NI transitioning to ITM).
  - Aggregate classes exist for 1 km rasters (merging 23 LCM2007 classes to coarser categories).
  - 1 km products include:
    - Dominant cover for 23 classes
    - Dominant cover for Aggregate classes
    - Percentage cover for 23 classes
    - Percentage cover for Aggregate classes
  - 25 m raster and 1 km raster metadata include pixel counts, extents, projections, and data types (unsigned 8-bit).

Validation, Accuracy, and Limitations

- Validation
  - Ground reference data were used to validate LCM2007 against polygons matching its spatial and thematic resolution.
  - Average accuracy reported around 83% across 9,127 polygons (note: average accuracy, with local variations possible).
- Limitations and caveats
  - LCM2007 is not ideal for change detection due to differences in class definitions and spatial structure across years (1990, 2000, 2007) and typical image classification errors (~20%).
  - The 0.5 ha MMU and dissolve rules mean small features may be omitted or generalized.
  - Broad Habitat sub-classes (BHSub) provide additional detail but are not validated to the same standard as LCM2007 classes; users should validate sub-class level analyses as needed.
  - Grassland and some other classes (e.g., Neutral/Calcareous Grassland) may be confused with Improved Grassland; consider aggregating classes if appropriate.
  - Some data details (e.g., FieldCode accuracy) require user validation.

Data Access and Projections

- Access
  - 1 km raster data sets are available via the CEH Information Gateway.
  - The full vector product and 25 m raster product are available on request under license from CEH; license fees may apply.
- Projections
  - GB data use British National Grid; NI data use Irish National Grid (with ongoing NI ITM transition).
  - Users may need to reproject NI data to ITM as required.

File Sizes

- Vector data (GB shapefile, 100 km × 100 km chunks)
  - GB: ~4.13 GB
  - NI: ~433 MB
- Raster data (Geotiff format)
  - 25 m: GB ~1.36 GB; NI ~46 MB
  - 1 km: sizes range from ~21 MB to ~49 KB depending on product
- Large data volumes reflect ~10 million polygons globally and extensive metadata per polygon.

Data Access Details

- CEH Information Gateway provides the 1 km raster products.
- The full vector product and the 25 m raster product are available on request; apply online via CEH or contact spatialdata@ceh.ac.uk.

Appendices and Technical Details

- Appendix 1: LCM2007 Classes (detailed definitions and Broad Habitat mapping guidance)
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings)
- Appendix 3: LCM2007 colour mapping (visualization scheme for 23 classes; also provided as an ArcGIS .lyr file)
- Appendix 4: Updates to products (Version 1.2, May 2014) – updates include OS tiles, water class inclusion, and other dataset refinements
- Color coding and mapping are provided to support standard visualization across platforms.

Product Version History

- Version 1.2 (May 2014) – updates across vector, 25 m, and 1 km products; added water class for 1 km; added Fair Isle and Stranraer tiles
- Version 1.1 (July 2011) – original release for GB and NI products across vector and rasters

Notes

- LCM2007 delivers land cover at multiple resolutions and formats to accommodate diverse applications, from detailed analyses with vector data to broad-scale modelling with 1 km rasters.
- For best results, users should consult the Final Report (Morton et al., 2011) for methodological context, validation details, and recommended practices.