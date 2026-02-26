# Dataset documentation

- LCM1990 is a parcel-based land cover map for the UK, created by classifying Landsat-5 satellite imagery (30 m) into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions. It replaces prior versions and uses an updated spatial framework to maximise interoperability with other LCM products (notably LCM2015) for long-term change analysis.

- Purpose and scope
  - Provides data products to support diverse user needs, including policy, planning, modelling, and research.
  - Available in vector and raster formats to support a range of applications, with guidance on when to use each.

- Data products and structure
  - Vector data set
    - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
    - Eight key attributes per polygon, including: land cover class (text and integer), source image, per-polygon uncertainty, pixel counts per class, and the dominance probability.
    - Unique geometry identifier (gid) for precise communication; recommended to retain gid.
  - Raster data sets
    - 25 m raster derived from the vector dataset (three-band product).
      - Band 1: dominant LCM1990 class per polygon.
      - Band 2: mean per-polygon confidence (from Random Forest vote counts).
      - Band 3: percentage of the polygon area covered by the modal class.
    - 1 km raster products
      - Dominant cover (21 target classes and 10 aggregate classes) and percentage cover (21 bands for target, 10 bands for aggregates).
      - Percentage data are integer-valued; sums may not exactly equal 100 due to rounding, coastal areas, and how areas are mapped.
  - Class mapping and aggregation
    - LCM1990 maps 21 classes; some broad habitats are split (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral/ Supra-littoral categories split for coastal detail).
    - Table 2 (not reproduced here) links aggregate classes to target LCM1990 classes and Broad Habitats.

- Spatial framework and comparability
  - Framework derived from generalised cartography (OSMM GB and LPS for NI) and aligned with LCM2007/LCM2015 methods to enable long-term change analysis (e.g., 25-year change product).
  - All mapping uses consistent polygon-based boundaries to improve interpretability and interoperability with other geospatial datasets.

- Metadata and uncertainty
  - Rich metadata accompany vector polygons, including dominant class, per-polygon class breakdown, and mean classification probability.
  - Uncertainty information is provided as mean per-polygon probability derived from the Random Forest classifier.
  - Per-pixel probability is available for the 25 m raster and as per-polygon statistics in the vector data.

- Data access and licensing
  - Access via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - 25 m and 1 km raster data are available; full vector product on request from CEH (licence fees may apply for some users/applications).
  - Each product has a Digital Object Identifier (DOI) for citation (GB and NI variants have separate DOIs; see Tables 5 and 6 in the document).

- Projections and extents
  - Great Britain: British National Grid (OSGB36, EPSG: 27700) for both vector and 25 m/1 km rasters.
  - Northern Ireland: Irish National Grid (TM75 Irish Grid, EPSG: 29903) for both vector and rasters.
  - Minimum mappable area: >0.5 ha; polygons smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding areas.

- Quality assurance and validation
  - Products produced with defined methods and QA checks for projection correctness, spatial completeness, polygon modal class presence, value ranges (0–100 for raster percent), and pixel size accuracy.
  - A full validation exercise against other datasets (e.g., Countryside Survey, National Forest Inventory) has been conducted; results published separately.

- Use and citation guidance
  - LCM1990 DOIs should be cited in publications to ensure reproducibility and traceability.
  - Example citation format provided in the document (author, date, title, DOI).

- Access to further information
  - CEH LCM1990 information page: https://eip.ceh.ac.uk/lcm/lcmdata
  - General queries: spatialdata@ceh.ac.uk
  - Acknowledgement of funding and programme details included in the document.

- Appendices and additional details
  - Appendix 1: Class interpretations and mapping notes for LCM1990 classes.
  - Appendix 2: Biodiversity Action Plan Broad Habitats definitions (JNCC Jackson 2000) used to interpret class names.
  - Appendix 3: Standard colour mapping recipe for LCM1990 classes.
  - Appendix 4: Composite images and their metadata used during classification.
  - Version: Dataset documentation, Version 1.0, 2 July 2020.