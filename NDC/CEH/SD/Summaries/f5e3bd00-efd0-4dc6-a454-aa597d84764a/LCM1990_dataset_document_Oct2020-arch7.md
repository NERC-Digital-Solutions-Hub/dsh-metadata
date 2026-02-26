# Dataset documentation

- Purpose and scope
  - Describes Land Cover Map 1990 (LCM1990) data products to support diverse users of the LCM dataset.
  - UK-wide parcel-based land cover map classified into 21 classes, based on UK Biodiversity Action Plan Broad Habitat definitions.
  - Built to be compatible with the LCM2015 framework to enable long-term land cover change analyses (25 years).

- Data sources and methodology
  - Derived from two-date Landsat-5 composite images at 30 m resolution.
  - Classifications reflect real-world boundaries by using an updated spatial framework derived from Ordnance Survey MasterMap (GB) and Northern Ireland equivalents; aligned with methods used for LCM2015/LCM2007.
  - Training and classification emphasize object-based approaches, with per-polygon aggregation from pixel-level classifications.
  - LCM1990 uses 21 Broad Habitat-based target classes; some classes are subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).

- Data products and structure
  - Vector data set (core product)
    - Polygons with attached attributes, including:
      - gid: unique geometry identifier
      - _hist: list of classes present in polygon with pixel counts
      - _mode: dominant LCM1990 class (1–21)
      - _purity: percentage of polygon area covered by the modal class
      - _conf: mean per-polygon classifier confidence (0–100)
      - _stdev: standard deviation of uncertainty
      - _n: number of pixels in polygon
      - cmp: composite image used for classification
    - Great Britain: ~6.7 million polygons; Northern Ireland: ~0.9 million polygons
  - Raster data sets
    - 25 m raster: 3-band
      - Band 1: dominant class per polygon (per-polygon class code)
      - Band 2: mean per-polygon confidence (from Random Forest)
      - Band 3: percentage of polygon area covered by the modal class
    - 1 km raster products (GB and NI, separate projections)
      - Dominant cover at 1 km for target classes (1-band)
      - Dominant cover at 1 km for aggregate classes (1-band)
      - Percentage cover at 1 km for target classes (21 bands)
      - Percentage cover at 1 km for aggregate classes (10 bands)
      - Note: percentage sums may not exactly equal 100 due to rounding; coastal areas may sum to less than 100
  - Spatial references
    - Great Britain: British National Grid (EPSG 27700)
    - Northern Ireland: Irish Grid (TM75)/EPSG 29903
  - Data access formats and DOIs
    - 25 m and 1 km rasters; vector products; each product published with a Digital Object Identifier (DOI)
    - DOIs provided for GB vector, GB 25 m raster, GB 1 km target/aggregate, NI vector, NI 25 m raster, NI 1 km target/aggregate
    - Access and citation guidance provided (see Tables 5 and 6 in the document)

- Spatial extents and data scale decisions
  - Minimum mappable area: >0.5 ha
  - Polygons smaller than 0.5 ha and linear features <20 m dissolved into surrounding landscape during production
  - Data available as uncompressed GeoTIFFs; compression recommended for storage

- Data access, licensing, and citation
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector product available on request under licence from CEH (licensing fees may apply)
  - Guidance for citing DOIs in publications; example citation formats provided

- Quality assurance and validation
  - QA checks ensure correct projections, spatial completeness, modal class in polygons, metadata consistency, value ranges (0–100 for raster), and pixel sizes
  - Validation performed against multiple reference datasets (e.g., Countryside Survey, National Forest Inventory); results published separately
  - Land Cover Map framework based on 2007 Ordnance Survey MasterMap data; field boundary changes are infrequent

- Future information and references
  - Further information and data access: CEH eIP/Land Cover Map 1990 pages
  - Journal papers and appendices provide detailed class definitions, color mappings, and methodological notes

- Appendices (highlights relevant to GIS implementation)
  - Appendix 1: Detailed notes on how LCM1990 classes map to Broad Habitats, training methodology, and potential misclassifications (e.g., grassland confusion, Neutral/Calcareous misclassifications)
  - Appendix 2: Summary of JNCC Broad Habitat definitions (for context and interpretation)
  - Appendix 3: Color-mapping recipe for standard LCM colors (class numbers to RGB)
  - Appendix 4: Composite image metadata used during classification (paths, rows, dates)