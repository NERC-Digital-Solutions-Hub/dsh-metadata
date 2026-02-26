# LAND COVER MAP 2007 DATASET DOCUMENTATION

- The Land Cover Map 2007 (LCM2007) provides a range of map-based data products describing UK land cover (not land use) using 23 classes aligned to UK Broad Habitats. It uses 20–30 m satellite imagery and a parcel-based, object-oriented vector framework built on OS MasterMap/topographic segmentation for Great Britain and Land & Property Services large-scale vector data for Northern Ireland.
- LCM2007 is an upgrade to LCM2000 with a spatial framework that supports GIS data integration by representing real-world objects (e.g., fields, woodland blocks) as polygons. It includes extensive metadata and a rich QA framework.

- Scope and purpose
  - Intended for GIS data users needing detailed map-based land cover visualisations and analyses.
  - Emphasises compatibility with other GIS data through object-based polygons, rich attributes, and metadata.
  - Important caveat: the dataset maps land cover, not necessarily land use; spectral signatures may not perfectly distinguish some land-use types.

- Data products and formats
  - Vector data set (GB and NI): polygons with 10 attributes per polygon; ~8.6 million GB polygons and ~0.9 million NI polygons.
  - Raster data sets (GB and NI):
    - 25 m raster (23 LCM2007 classes; full thematic resolution; GB and NI separate projections)
    - 1 km raster products (aggregated, suitable for large-area modelling; includes dominant class, percentage cover by class, both for full 23-class and aggregated classes)
  - Scale and resolution considerations:
    - 25 m vector/raster provides detailed class information with rich metadata.
    - 1 km raster provides broader-scale summaries (dominant class and percentage cover) suitable for national and regional analyses.
  - Aggregated (1 km) classes are provided to simplify usage where full 23-class detail is not required.

- Classification and class structure
  - 23 LCM2007 classes are based on Broad Habitats (with some sub-class refinements):
    - Examples: Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural Grassland, Neutral/Calcareous/Acid Grasslands, Fen/Marsh/Swamp, Bog, Montane Habitats, Inland Rock, Saltwater, Freshwater, Supra-littoral Rock/Sediment, Littoral Rock/Sediment, Saltmarsh, Built-up Areas and Gardens (Urban and Suburban).
  - Some Broad Habitats are further divided into sub-classes (BHSub) and are represented in the vector with additional attributes (e.g., field codes).
  - Attribute set (vector; typical core fields):
    - Parcel_ID: unique parcel identifier (including source image)
    - BH: Dominant Broad Habitat
    - BHSub: Broad Habitat sub-class
    - FieldCode: short text field code
    - INTCODE: 1–23 LCM2007 class code (recommended display class)
    - KBE: Knowledge-Based Enhancement history
    - ProbList: top 5 spectral class probabilities
    - CorePixels: number of core pixels used for classification
    - Construct: polygon construction history (OSMM-based or segmentation variants)
    - TotPixels: total pixels in polygon
  - Parcel_ID is recommended to be retained for unambiguous communication among users.
  - The vector schema includes 10 attributes per polygon and supports detailed QA history and spectral interpretation records (KBE, ProbList).

- Data quality, validation, and limitations
  - Ground reference validation: ~9,127 polygons with an average accuracy of 83%, acknowledging variability by area and local misclassifications.
  - Change mapping across LCM1990/2000/2007 is complex due to differing classes and spatial structures; LCM products are not well suited for change detection without careful cross-walking and validation.
  - Sub-class resolution (BHSub) and FieldCode interpretations require user validation for precise use beyond the primary 23 LCM2007 classes and recommended cautions when using sub-classes.
  - LCM2007 maps land cover and may not reliably infer land use in all cases (e.g., grass used for recreation vs. grazing).

- Projections, extents, and coordinate systems
  - GB data: British National Grid (OSGB 1936)
  - NI data: Irish National Grid (Ireland 1965)
  - NI is transitioning toward Ireland Transverse Mercator (ITM); re-projection is supported by GIS software as needed.

- Data access and licensing
  - 1 km raster data (GB and NI) available via the CEH Information Gateway.
  - Full vector product and 25 m raster product are available on request under licence from CEH (fees may apply).
  - Access details: CEH data portal and data contact points provided in the documentation.

- File sizes and practical considerations
  - Vector data: very large (almost 10 million polygons; GB vector ~4.13 GB, NI ~433 MB for 100 km x 100 km shapefiles)
  - Raster data: 25 m GB ~1.36 GB; NI ~46 MB
  - 1 km raster products: 21 MB to 49 KB (depending on product type)
  - Large data volumes require careful storage planning and efficient GIS workflows.

- Practical guidance for GIS specialists
  - Choose data product based on analysis scale and need for metadata:
    - Use vector (GB/NI) when detailed polygon-level attributes and QA history are required.
    - Use 25 m rasters for consistent 23-class detail with simpler geometry (no polygon boundaries) when processing efficiency is needed.
    - Use 1 km rasters for national/regional analyses, trend modelling, or when working with ancillary datasets (e.g., meteorology, species distributions).
  - Decide between full 23-class detail and aggregated 1 km products depending on application and computational resources.
  - Preserve Parcel_ID and other QA-related attributes for communication and reproducibility.
  - Validate Broad Habitat sub-classes if used for high-precision analyses; be aware of limitations and the need for ground truthing or independent validation.
  - Be mindful that change detection across LCM versions requires careful methodological matching due to class and structural differences.

- Appendices and mapping resources
  - Appendix 1: Detailed LCM2007 class descriptions (Broad Habitat definitions and distinctions)
  - Appendix 2: Relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
  - Appendix 3: Colour mapping for LCM2007 classes (mapping to RGB values; includes an ArcGIS .lyr file)
  - Appendix 4: Updates to products (Version 1.2, 2014; notable additions include new tile coverage and water class updates)

- Version history
  - Version 1.0 (July 2011): Original release
  - Version 1.2 (May 2012; updated to include dataset updates and change-detection discussion)
  - Version 1.2 (May 2014; GB/NI tile updates, water class additions, licensing notes)

- Acknowledgements
  - Data sources include Landsat-TM5, SPOT-4/5, AWIFS, OS and other cartographic datasets; compilation and QA conducted by CEH with Countryside Survey Partnership involvement.