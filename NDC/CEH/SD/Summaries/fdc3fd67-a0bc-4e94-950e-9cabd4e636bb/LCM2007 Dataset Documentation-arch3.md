# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Overview
  - Land Cover Map 2007 (LCM2007) is a UK land cover parcel-based classification using 23 Broad Habitat–based classes, derived from 20–30 m satellite imagery. It updates LCM2000 with a GIS-friendly, object-based framework aligned to OS base maps, improving compatibility with other datasets. It maps land cover (not strictly land use).
  - Minimum mappable unit is >0.5 ha; parcels smaller than 0.5 ha or lines <20 m are dissolved into the surrounding landscape.

- Data products and structure
  - Vector data set
    - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
    - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class number), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
    - Unique Parcel_ID labels each parcel; recommended to retain this for communication and traceability.
  - Raster data sets
    - 25 m and 1 km resolutions, derived from the vector data.
    - 25 m rasters preserve 23 LCM2007 classes; 1 km rasters provide aggregated products: dominant class and/or percentage cover for both LCM2007 classes and Aggregate classes.
    - Separate data sets for Great Britain and Northern Ireland due to different projections.
  - Class framework
    - 23 LCM2007 classes; some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and other sediment types).
    - Aggregates (used in 1 km rasters) merge LCM2007 classes to support broader-scale analyses.

- Metadata, data quality, and validation
  - Rich per-polygon metadata capturing processing history, original spectral classification, and knowledge-based enhancements (KBE).
  - Validation against ground reference data: average accuracy approximately 83% across 9,127 polygons; local accuracy may vary.
  - Knowledge-based enhancements (KBE) document refinements (e.g., soil corrections, altitude-based adjustments, coastal/urban masks).
  - Sub-class (BHSub) information available, but not covered by QA at the LCM2007 class level; users should validate sub-class use independently if required.

- Data access and governance
  - Data access
    - 1 km raster data sets available via the CEH Information Gateway.
    - Full vector product and 25 m raster product available under licence on request from CEH; licensing fees may apply.
  - Data formats and sizes
    - Vector: shapefile-like with up to ~10 attributes per polygon; large file sizes (GB scale for GB vector; NI smaller).
    - Raster: GeoTIFF-like; GB 25 m and 1 km rasters; NI 25 m and 1 km rasters; sizes vary by product and region.
  - Projections
    - Great Britain: British National Grid (OSGB36).
    - Northern Ireland: Irish National Grid; NI transitioning toward ITM (Ireland Transverse Mercator).
  - Projections notes
    - Northern Ireland data can be reprojected to ITM; some tools may require reprojection adjustments.

- Practical considerations for monitoring frameworks
  - Use cases
    - Track changes in land cover by Broad Habitat classes and by aggregates at national to local scales.
    - Support policy evaluation, scenario analysis, and reporting with standardized, repeatable class definitions.
    - Leverage 1 km raster products for continental- or national-scale monitoring; utilize 25 m and vector data for finer-grained analyses and validation.
  - Data interpretation cautions
    - LCM2007 maps land cover, not strictly land use; inferring land use (e.g., arable crops vs. grassland) may require ancillary data.
    - Some habitats (e.g., Fen/Marsh/Swamp, Montane) present classification challenges or depend on auxiliary data (soil, altitude) for certain interpretations.
    - Sub-class level information (BHSub) should be validated independently if used for decision-making, as QA focuses on the main LCM2007 class.
    - The MMU (>0.5 ha) may exclude smaller patches relevant for certain local analyses.
  - Data governance implications
    - Retaining Parcel_ID enables traceability back to source imagery and processing steps; essential for audit trails in policy evaluation.
    - Metadata richness supports reproducibility but requires careful data management and sharing practices.
    - If sharing results or underlying data, account for licensing requirements and ensure appropriate metadata and provenance are preserved.

- Appendix highlights (for reference)
  - Appendix 1: Descriptions of the 23 LCM2007 classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Various Grassland types, Wetlands, Urban/Suburban) and key distinctions.
  - Appendix 2: Mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes to aid interpretation and crosswalks with other classifications.
  - Appendix 3: Standard LCM2007 colour mapping used in reporting and visualization (RGB values per class) to support consistent cartography.

- Additional information and disclaimers
  - The Final Report for LCM2007 (Morton et al., 2011) provides a more comprehensive description and assessment; this document focuses on data products and usage guidance.
  - The dataset is designed to serve a wide range of potential applications; users should consult the Final Report for detailed methodologies and limitations.

- Key takeaway for monitoring framework authors
  - LCM2007 provides a rich, metadata-dense land cover dataset aligned to Broad Habitats, with both fine (25 m vector) and broad (1 km raster) products suitable for policy evaluation and decision-support at multiple scales.
  - When implementing monitoring measures, leverage the 1 km aggregates for broad trend analyses and the 25 m/vector data for detailed, locally-grounded assessments, ensuring validation of sub-class interpretations where used.
  - Plan for data governance, access controls, and provenance tracking given the licensing, data volumes, and the need for transparent reporting in environmental monitoring.