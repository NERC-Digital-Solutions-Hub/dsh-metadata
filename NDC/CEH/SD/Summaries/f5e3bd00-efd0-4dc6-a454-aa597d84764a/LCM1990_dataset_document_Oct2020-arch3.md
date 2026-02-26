# Dataset documentation

- Purpose and scope
  - Land Cover Map 1990 (LCM1990) provides a range of data products to support diverse user needs and monitoring applications.
  - Focuses on LCM1990 data products (vector and raster) and their metadata, quality, and access.
  - Built to be compatible with other LCM products (e.g., LCM2007, LCM2015) to enable long-term change analyses.

- Background and methodology
  - Parcel-based land cover map for the UK, classified into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
  - Derived from two-date Landsat-5 composites (30 m resolution); uses an updated LCM2007 spatial framework for polygonal real-world boundaries.
  - Spatial framework derived from OS MasterMap/large-scale vector layers and refined with boundary data; designed for cross-product compatibility and change mapping (25 years).

- Data products and structure
  - Vector data set
    - Polygons with rich attributes; 6.7 million polygons in Great Britain, 0.9 million in Northern Ireland.
    - Eight key attributes, including:
      - gid: unique parcel identifier
      - _hist: list of classes present in the polygon with pixel counts
      - _mode: recommended dominant LCM1990 target class (1–21)
      - _purity: percentage of polygon covered by the dominant class
      - _conf: mean per-polygon confidence from Random Forest (0–100)
      - _stdev: standard deviation of uncertainty
      - _n: number of pixels in the polygon
      - cmp: composite image index from which classification is derived
  - Raster data sets
    - 25 m raster: 3-band product
      - Band 1: dominant LCM1990 class per polygon
      - Band 2: mean per-polygon confidence
      - Band 3: percentage of polygon covered by the modal class
    - 1 km raster: derived by aggregating 25 m raster
      - Dominant cover (1-band) for target and aggregate classes
      - Percentage cover (21-band target classes; 10-band aggregate classes)
    - Great Britain and Northern Ireland datasets are separate to accommodate different projections
  - Aggregates and mapping
    - 21 LCM1990 target classes aligned with Broad Habitat definitions
    - 10 aggregate classes used for 1 km products
  - Spatial details
    - Minimum mappable area: >0.5 ha; sub-0.5 ha polygons and lines < 20 m dissolved into surrounding landscape
    - DOIs exist for each product to enable stable citation and reproducibility

- Data formats, projections, and access
  - Data formats and resolutions
    - Vector: polygon features with attached metadata
    - 25 m raster: three-band GeoTiff (dominant class, confidence, percent coverage)
    - 1 km raster: aggregate and percentage cover products (GeoTiff, unsigned 8-bit)
  - Projections
    - Great Britain: British National Grid
    - Northern Ireland: Irish National Grid (TM75)
  - Access and licensing
    - 25 m and 1 km raster data available via CEH Environmental Information Platform (EIP)
    - Full vector product available on request from CEH (licence may apply)
    - DOIs provided for all products to facilitate citation

- Quality assurance, uncertainty, and validation
  - QA checks cover projections, spatial completeness, modal class presence in polygons (vector), data headings, value ranges (0–100 for rasters), and pixel sizes
  - Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) performed; results published separately
  - Uncertainty reported per-polygon (via _conf and _stdev) and per-pixel (in 25 m raster) from Random Forest probability estimates

- Metadata, provenance, and citation
  - Rich metadata retained for processing steps, polygon attributes, and per-polygon class breakdown
  - Each product has a Digital Object Identifier (DOI) for stable citation
  - Guidance provided for citing data in publications (author, date, DOI)

- Practical usage notes and considerations
  - Vector vs. raster trade-offs
    - Vector provides detailed per-polygon metadata but larger file sizes; raster offers easier processing and integration with other gridded data
  - Coherence with other LCM products
    - Methods align with LCM2007 and LCM2015 to enable historical and future-change analyses
  - Coastal and edge areas
    - Coastal areas and some complex mosaics may exhibit mapping uncertainties or lower accuracy due to spectral limitations
  - Data interpretation
    - LCM1990 maps land cover, not strictly land use; some land-use inferences may be ambiguous from land cover alone
  - Documentation scope
    - Appendix materials (e.g., class definitions, colour mapping, composite image details) support interpretation and reproducibility

- Further information and contact
  - Data access: eip.ceh.ac.uk (CEH Environmental Information Platform)
  - Contact: spatialdata@ceh.ac.uk
  - Related publications and validation studies referenced; journal paper in preparation
  - Acknowledgement: supported by NERC UK-SCAPE National Capability program

- Appendices overview (contextual)
  - Appendix 1: Class mapping notes and interpretation guidance for LCM1990 classes
  - Appendix 2: Biodiversity Action Plan Broad Habitats definitions
  - Appendix 3: Standard LCM color mapping recipe
  - Appendix 4: Composite image details used in LCM1990