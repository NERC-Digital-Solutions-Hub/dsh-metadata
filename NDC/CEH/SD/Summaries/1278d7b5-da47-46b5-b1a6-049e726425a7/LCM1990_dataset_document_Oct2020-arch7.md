# Dataset documentation

- Overview
  - Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created by classifying Landsat-5 satellite data (30 m) into 21 classes, aligned with UK Broad Habitat definitions.
  - Built to be compatible with LCM2007 and LCM2015 frameworks to enable long-term land cover change analysis (25-year product series).
  - Data available in multiple formats and resolutions to suit diverse GIS applications.

- Data products and formats
  - Vector data set (core product)
    - Polygons with attached attributes representing dominant class, source image, pixel counts, and per-polygon uncertainty information.
    - Spatially delivered for Great Britain and Northern Ireland as separate vector layers.
  - Raster data sets
    - 25 m raster (GB and NI separately) derived from the vector data; three-band 25 m product: band 1 = dominant class, band 2 = mean per-polygon confidence, band 3 = percent coverage of the dominant class.
    - 1 km raster products (GB and NI) summarise the 25 m data to give dominant class per 1 km pixel and percentage cover per class (21 target classes and 10 aggregate classes).
  - Aggregates and comparison
    - Aggregate classes merge 21 LCM1990 classes for 1 km rasters to support applications needing coarser resolution.

- Class structure and mapping
  - 21 LCM1990 target classes based on UK Broad Habitats; some classes subdivided for better spectral separation:
    - Built-up Areas and Gardens split into Urban and Suburban
    - Dwarf Shrub Heath split into Heather and Heather grassland
    - Littoral Sediment split into Littoral sediment and Saltmarsh
  - 0.5 ha minimum mapping unit
    - Parcels smaller than 0.5 ha or linear features under 20 m are dissolved into surrounding areas.
  - Vector attributes
    - gid: unique polygon identifier
    - hist: list of all classes present in the polygon with pixel counts per class
    - mode: recommended display class (1–21)
    - purity: percentage of polygon covered by the modal class
    - conf: mean per-polygon classifier confidence (0–100)
    - stdev: uncertainty standard deviation
    - n: number of pixels in the polygon
    - cmp: composite image source index

- Uncertainty and quality assurance
  - Random Forest outputs per-pixel probability used to derive per-polygon confidence (and raster band 2).
  - Comprehensive QA checks cover projections, completeness, modal class presence, value ranges (0–100 for raster), and pixel size accuracy.
  - Full validation conducted against other datasets; results to be published separately.

- Data access and licensing
  - Access via CEH Environmental Information Platform (eip.ceh.ac.uk); some products licensed on request.
  - Full vector product available on request; license fees may apply for certain uses.
  - DOIs are provided for all LCM1990 products to enable proper citation (GB and NI, for vector, 25 m raster, 1 km products, and aggregated classes).

- Projections and data scope
  - Projections:
    - Great Britain: British National Grid
    - Northern Ireland: Irish National Grid (TM75)
  - Coverage: GB and NI; datasets include separate spatial references to accommodate different projections.
  - Minimum mapping unit and dissolution rules ensure consistent polygon sizing across the dataset.

- Documentation and usage notes
  - LCM1990 maps land cover (not strictly land use); interpretation of land cover vs land use may vary by polygon.
  - Rich metadata per polygon supports detailed analysis; vector products are larger due to attributes, while 25 m raster provides lightweight alternatives.
  - Appendix materials provide class definitions (BAP Broad Habitats), color mapping recipes, and documentation of composite imagery used during classification.
  - Guidance on citation emphasizes citing DOIs and including authors and dates in references.

- Further information
  - CEH LCM1990 information and data access: https://eip.ceh.ac.uk/lcm/lcmdata
  - Contact: spatialdata@ceh.ac.uk
  - A journal paper and additional publications are in development to provide further methodological details and validation results.