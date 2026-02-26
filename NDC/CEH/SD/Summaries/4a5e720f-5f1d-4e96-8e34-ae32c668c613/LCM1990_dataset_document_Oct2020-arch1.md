# Dataset documentation

- What it is: Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map derived from Landsat-5 imagery (30 m) classified into 21 classes based on UK Biodiversity Action Plan Broad Habitat definitions. It uses a consistent spatial framework with LCM2015 and is designed for cross-compatibility and long-term change analysis.

- Data products and structure
  - Core vector data: polygons with rich metadata per parcel, including dominant class, per-polygon class breakdown, mean classification probability, and a unique geometry identifier (gid).
  - Raster data: 25 m raster derived from the vector, plus 1 km percentage/dominant cover products.
  - Data scales:
    - Vector: ~6.7 million polygons (GB) and ~0.9 million polygons (NI).
    - 25 m raster: three bands per pixel (dominant class, per-polygon confidence, and modal-coverage percentage).
    - 1 km raster: dominant class (target and aggregate) and percentage cover for 21 target classes and 10 aggregate classes.
  - Minimum mapping unit: >0.5 ha; polygons <0.5 ha or linear features <20 m dissolved into surrounding landscape.

- Class structure
  - 21 LCM1990 classes are aligned with Broad Habitats definitions; some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
  - Classes are designed to map land cover (not always exact land use); some spectral similarity between classes can occur.

- Metadata, uncertainty, and provenance
  - Each polygon includes:
    - hist: list of classes present in the polygon with pixel counts
    - mode: recommended dominant class
    - purity: percentage of polygon area covered by the modal class
    - conf: mean classifier confidence (0–100)
    - stdev: uncertainty standard deviation
    - n: number of pixels in polygon
    - cmp: source composite image
  - Uncertainty is quantified via Random Forest per-pixel probability, reported per polygon and in the 25 m raster.

- Data access and format details
  - Access: CEH Environmental Information Platform (eip.ceh.ac.uk); full vector product available on request; 25 m raster and 1 km products available via CEH platforms. Licence fees may apply for some users.
  - Coordinate systems:
    - Great Britain: British National Grid (EPSG 27700)
    - Northern Ireland: Irish National Grid / TM75 Irish Grid (EPSG 29903)
  - File formats:
    - Vector: geospatial vector with extensive attributes
    - 25 m raster: uncompressed GeoTIFF, 3 bands
    - 1 km rasters: uncompressed GeoTIFF, various 1-band and multi-band products

- DOIs and citation
  - Each LCM1990 product (GB NI vector, GB NI 25 m, 1 km target/aggregate, etc.) has an associated DOI to enable clear, repeatable citations in publications.

- Data quality and validation
  - QA checks cover projection correctness, spatial completeness, modal class presence, attribute consistency, value ranges (0–100 for rasters), and pixel size accuracy.
  - A full validation exercise compared LCM1990 against other datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately.
  - The dataset is built on the 2007 LCM framework with updates to maximise compatibility with later products (e.g., LCM2015).

- Citing and references
  - DOIs provide traceable references for each product; example citation guidance is included (author, date, DOI) to support repeatable methodology.

- Accessing further information
  - More details and data access: CEH Environmental Information Platform and the LCM1990 data page
  - Contact: spatialdata@ceh.ac.uk
  - Related literature: journal papers and technical reports on LCM1990, with ongoing developments and planned journal publication for validation results.

- Appendices (high-level)
  - Appendix 1 and 2 provide detailed descriptions of LCM1990 class mappings and Broad Habitat definitions (per JNCC Jackson 2000).
  - Appendix 3 outlines standard LCM color mappings for visual representation.
  - Appendix 4 lists composite images used in the classification process.