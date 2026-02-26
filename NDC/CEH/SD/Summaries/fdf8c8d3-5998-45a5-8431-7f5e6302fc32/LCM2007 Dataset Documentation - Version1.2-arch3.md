# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Purpose and scope
  - Parcel-based classification of UK land cover using 23 classes aligned to Broad Habitats; maps land cover (not land use) from summer–winter satellite composites at 20–30 m resolution.
  - Represents a major upgrade from LCM2000, using a GIS-friendly framework with real-world object polygons; not designed for fine-grained land-use inference.
  - Version 1.2 (May 2014) provides updates and guidance on production methodology, metadata, and limitations.

- Data products and structure
  - Vector data set
    - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
    - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct).
    - Includes Broad Habitat sub-classes (BHSub) and FieldCode with recommendations to validate before use.
  - Raster data sets
    - 25 m raster: 23 LCM2007 classes; GB and NI provided separately with corresponding projections.
    - 1 km raster: summary products including dominant cover and percentage cover for both LCM2007 classes and Aggregate classes (for broad-scale analysis).
    - Aggregate classes used for 1 km rasters; 25 m rasters provide detailed class information.

- Classification and metadata
  - 23 LCM2007 classes linked to Broad Habitats; some classes subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban).
  - Rich polygon metadata: processing history, KBE (knowledge-based enhancements), ProbList (top 5 spectral class matches), and core/pixel counts.
  - Parcellation with unique Parcel_ID for traceability to source imagery.

- Quality assurance and validation
  - Ground reference validation against polygons; average thematic accuracy around 83%.
  - Change detection between LCM1990, LCM2000, and LCM2007 is complex due to class/structure differences; not well suited for monitoring change between versions.
  - Minimum mappable unit (MMU) of >0.5 ha; smaller features dissolved into surrounding landscape.

- Data access, licensing, and scale
  - 1 km raster data accessible via the CEH Information Gateway.
  - Full vector product and 25 m raster product available on request under licence; licence fees may apply.
  - Large file sizes: vector (~4.13 GB GB shapefile; NI ~433 MB); 25 m raster GB ~1.36 GB; NI ~46 MB; 1 km products range from ~21 MB to ~49 KB depending on product.

- Projections and geographic coverage
  - Great Britain: British National Grid (OSGB36) / Transverse Mercator.
  - Northern Ireland: Irish National Grid (and Irish ITM projection transitioning underway).
  - Users should reproject NI data as needed; NI moving toward ITM.

- Practical considerations and limitations
  - Data can be time-consuming to use due to file size and the richness of metadata.
  - Sub-class level (BHSub) information is not QA-validated to the same standard as main LCM2007 classes; users should validate for analyses at the sub-class level.
  - Change mapping between LCM products is not straightforward; about 20% typical image classification error relative to actual BH changes.

- Appendices (reference material)
  - Appendix 1: List and definitions of the 23 LCM2007 classes (with Broad Habitat context and example distinctions).
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; field codes and mapping details.
  - Appendix 3: Colour mapping for standard visualization (recipe for 23 classes) and ArcGIS color file availability.
  - Appendix 4: Updates to products (Version 1.2, May 2014) – additions include OS tiles (Fair Isle, Stranraer) and inclusion of water class in 1 km products; separate updates for GB and NI datasets.

- How this supports environmental monitoring and policy evaluation
  - Provides standardized, metadata-rich land cover layers aligned with UK Broad Habitats for spatial monitoring and policy appraisal.
  - Enables multi-resolution analysis (25 m detail vs. 1 km broader views) suitable for national to regional assessments.
  - Facilitates traceability to source imagery via Parcel_ID and comprehensive processing history (KBE), aiding reproducibility and governance.
  - Cautions on change detection and subclass use encourage explicit validation and careful interpretation in monitoring frameworks.