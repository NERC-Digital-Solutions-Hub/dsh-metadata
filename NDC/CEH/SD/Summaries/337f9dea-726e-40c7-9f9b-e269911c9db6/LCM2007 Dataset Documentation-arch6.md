# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A UK parcel-based land cover dataset produced in 2007 (LCM2007), using 20–30 m satellite imagery to map 23 Broad Habitat-based classes across Great Britain and Northern Ireland.
- Purpose: provide multiple data products to support diverse uses, including policy, planning, and environmental reporting. Data are intentionally mapped as land cover (not strictly land use) with a minimum mappable unit (MMU) of >0.5 ha and dissolution of parcels smaller than 0.5 ha or <20 m into surrounding areas.
- Key caveat: consult the Final Report (Morton et al., 2011) for production methodology, metadata, and limitations to guard against inappropriate use.

- Coverage and product range
  - 23 LCM2007 classes (based on UK Broad Habitats) with some subdivisions for enhanced detail.
  - GB and NI data available in vector and raster formats, plus various resolutions to suit applications.
  - Final products include:
    - Vector data set (polygons with rich attributes)
    - Raster data sets at 25 m and 1 km resolutions (GB and NI separately)
    - 1 km rasters provide dominant and percentage cover for LCM2007 and Aggregate classes (for 1 km products)

- Data products in detail
  - Vector Data Set
    - Nearly 10 million polygons (GB ~8.6M; NI ~0.9M) with 10 attributes per polygon.
    - Core attributes include Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (class for display), KBE (knowledge-based enhancements), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
    - Each polygon has a unique Parcel_ID and a BHSub description; ProbList aids interpretation but requires user validation for subclass-level use.
    - Sub-classes (BHSub) are included primarily for information and probability context, not QA of subclass-level classification.
  - Raster Data Sets
    - 25 m raster: 23 LCM2007 classes; GB and NI provided separately with corresponding metadata.
    - 1 km raster: derived by summarising 25 m data; presents dominant class and percentage cover for both LCM2007 classes and Aggregate classes.
    - File metadata (extent, pixel size, data type, coordinate system, projection, and datum) is detailed in the documentation.
  - Data Access
    - 1 km rasters are available via the CEH Information Gateway.
    - Full vector product and 25 m product licensing is available on request from CEH (licence fees may apply).
    - Access: online application at ceh.ac.uk/data or via spatialdata@ceh.ac.uk.

- Classification and relationship across data
  - 23 LCM2007 classes are aligned to Broad Habitats (as per Jackson 2000). In some cases, Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather Grassland).
  - Appendix 2 provides a mapping relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses; Appendix 3 details the standard LCM2007 colour mapping used in reporting.
  - A table (Table 2) documents the relationships between Aggregate classes, Broad Habitats, and LCM2007 classes for 1 km and 25 m rasters.

- Data quality and validation
  - Ground reference validation involved 9,127 polygons; average accuracy reported at 83%.
  - Accuracy is an average across the thematic resolution; local discrepancies may occur.
  - Broad Habitat subclass accuracy is not fully QA-validated; users should perform their own validation if subclass-level use is intended.
  - The dataset is designed to be thematically robust at 23 classes; caution advised when interpreting finer subclass distinctions.

- Technical details and implementation considerations
  - Output formats: vector (polygons with attributes) and raster (25 m and 1 km); GB and NI datasets are separately projected.
  - Map projections: GB data in British National Grid; NI data in Irish National Grid (with NI moving toward ITM in the future).
  - Small patch handling: patches below MMU are dissolved into surrounding areas; vector products include 0.5 ha threshold for minimum mapping unit.
  - Data volume: vector shapefiles are large (GB ~4.13 GB; NI ~433 MB). Raster sizes vary by resolution and region (e.g., GB 25 m ~1.36 GB; NI ~46 MB).
  - Metadata richness: vector polygons include processing history, KBE changes, and a detailed attribute history; ProbList provides top spectral matches with associated probabilities and is intended for guidance rather than definitive classification.

- Usage guidance and limitations
  - LCM2007 maps land cover, not necessarily land use; inferring land use from cover may be misleading in some cases.
  - Grassland classifications can be spectrally similar (e.g., Neutral vs Improved Grassland; Calcareous vs Neutral vs Acid Grassland); user validation and possible aggregation may be appropriate.
  - Montane habitats are altitude-based in addition to spectral classification; cross-check with altitude data if specific Montane analyses are required.
  - Many small or mosaic features may fall below the MMU; consider using 25 m raster or higher-level aggregates for nationwide modelling.
  - For detailed grassland interpretation and Broad Habitat subclass decisions, consult Morton et al. 2011 Final Report sections (3.9 and Chapter 4) and related Jackson 2000 guidance.

- Appendices and colour mapping
  - Appendix 1: LCM2007 class descriptions and broad habitat interpretations (e.g., Broadleaved Woodland, Coniferous Woodland, Arable and Horticulture, etc.).
  - Appendix 2: Detailed relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings and class numbers).
  - Appendix 3: Standard LCM2007 colour mapping for 23 classes (RGB values provided for each class) as used in the Final Report.

- Additional information and acknowledgements
  - Documentation references: Morton et al. 2011 Final Report; Jackson 2000 Broad Habitat guidance.
  - Data providers include Landsat, SPOT, AWIFS, Ordnance Survey, and various map and soil data sources; acknowledges licensing, rights, and data source provenance.
  - For more information on Countryside Survey and LCM2007, refer to the CEH and Countryside Survey project pages.