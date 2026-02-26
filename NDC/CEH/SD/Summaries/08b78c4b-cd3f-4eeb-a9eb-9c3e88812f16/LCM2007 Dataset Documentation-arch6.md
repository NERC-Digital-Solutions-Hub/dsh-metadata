# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Overview
  - UK parcel-based land cover classification (LCM2007) produced from satellite imagery (20–30 m pixels) with 23 classes based on Broad Habitats.
  - Upgrades from LCM2000; integrates a spatial framework using Ordnance Survey MasterMap and image segmentation for real-world object representation.
  - Maps land cover (not strictly land use) and is validated at 23-class thematic resolution; final evaluation available in Morton et al. 2011.
  - Range of data products to support diverse applications; consult the Final Report for comprehensive details.

- Data products and formats
  - Vector Data Set
    - ~8.6 million polygons for Great Britain; ~0.9 million for Northern Ireland.
    - Each polygon has 10 attributes (Table 1): Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class for display), KBE (knowledge-based enhancements), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
    - Unique Parcel_ID allows linking to source data and processing history; BHSub provides additional subclass information; ProbList indicates spectral class probabilities.
    - 23 LCM2007 classes mapped to Broad Habitats (and sub-classes) with a defined QA process.
  - Raster Data Sets
    - 25 m and 1 km products derived from the vector data.
    - 25 m raster: 23 LCM2007 classes.
    - 1 km raster: aggregates multiple 25 m classes into dominant class per 1 km cell and percentage cover per class (and per Aggregate class).
    - Separate datasets for Great Britain and Northern Ireland due to different projections.
  - Data access
    - 1 km raster data accessible via CEH Information Gateway.
    - Full vector and 25 m raster products available on request under license from CEH; fees may apply.

- Spatial details and projections
  - Projections
    - Great Britain: British National Grid (OSGB36).
    - Northern Ireland: Irish National Grid (and transitioning toward ITM for NI).
  - Data scale and resolution
    - Vector: polygon-based with detailed per-polygon metadata; MMU: minimum mappable area >0.5 ha (smaller parcels dissolved into surrounding landscape).
    - Raster: 25 m and 1 km resolutions; 1 km rasters provide dominant class and percentage cover.

- Attributes, taxonomy, and mapping
  - LCM2007 classes
    - 23 classes based on Broad Habitats; several Broad Habitats split into sub-classes (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
    - Appendix 1 describes each Broad Habitat class; Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 provides the colour mapping for visualization.
  - QA and uncertainties
    - Ground-reference validation involved 9,127 polygons; average accuracy around 83%, with local variations.
    - Sub-class level (Broad Habitat sub-classes) may be less reliable and should be validated by users before fine-scale use.
    - LCM2007 maps land cover, not guaranteed land use; some confusion may occur (e.g., grass used for recreation vs. grazing).

- Metadata and data quality
  - Rich metadata at polygon level, including processing history (KBE), original spectral classification, and top spectral variants (ProbList).
  - Parcel_ID preserves linkage to original imagery and processing steps; encourages keeping Parcel_ID intact for traceability.

- File sizes and data management
  - Vector data: nearly 10 million polygons; large file sizes; example sizes (approximate):
    - GB vector (100 km x 100 km shapefile): ~4.13 GB
    - NI vector: ~433 MB
  - Raster data
    - GB 25 m: ~1.36 GB
    - NI 25 m: ~46 MB
    - 1 km products: 21 MB to 49 KB depending on product
  - Implications for storage, processing, and software handling; consider data format and metadata requirements.

- How to use and best practices
  - Choose product by need:
    - Vector: rich attribute data, processing history, and detailed class information; larger file sizes; suitable for detailed analyses and custom mapping.
    - 25 m raster: smaller footprint than vector for processing; still contains full class detail but with less per-polygon metadata.
    - 1 km raster: suitable for national-scale modeling, integration with meteorological or species distribution data; uses aggregated class information.
  - Use the crosswalks and color mappings (Appendix 2 and Appendix 3) to interpret classes and visualize outputs.
  - Be mindful of the recommended reading (Morton et al. 2011 Final Report) for methodology, limitations, and detailed classification rules.

- Data access and licensing details
  - 1 km raster data: publicly accessible via CEH Information Gateway.
  - Full vector and 25 m raster data: licensing required; apply online via CEH data portal or contact spatialdata@ceh.ac.uk.
  - Fees may apply depending on user type and application.

- Appendix highlights (for reference)
  - Appendix 1: LCM2007 class definitions and notes on grassland, Montane, bog, and other Broad Habitats; guidance on class interpretation and potential misclassifications.
  - Appendix 2: Detailed mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (for interpretation and validation).
  - Appendix 3: Standard LCM2007 colour mapping (RGB) for visualization in maps and analyses.

- Further information and acknowledgements
  - Primary reference: Morton et al. 2011, Final Report for LCM2007.
  - Related guidance: Jackson 2000 on Broad Habitat classification relationships.
  - Data sources and acknowledgements covering Landsat, SPOT, AWIFS, OS datasets, and other supporting materials.