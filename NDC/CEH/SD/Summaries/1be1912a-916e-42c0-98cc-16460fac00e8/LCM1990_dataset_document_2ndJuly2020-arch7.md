# Dataset documentation

- Overview
  - Land Cover Map 1990 (LCM1990) is a parcel-based land cover map for the UK, created by classifying Landsat-5 satellite imagery (30 m resolution) into 21 classes aligned with UK Biodiversity Action Plan Broad Habitats.
  - Built using two-date image composites; designed to be compatible with LCM2007/LCM2015 frameworks to support a 25-year land cover change product.
  - Data are polygon-based (vector) with a connected 25 m raster and 1 km aggregated products; designed to be easily interpreted and interoperable with other geospatial datasets.
  - Spatial framework relies on generalised cartography (OS MasterMap GB and Northern Ireland equivalents), refined with rural boundary data.

- Data products and structure
  - Core products
    - Vector data set: polygons with attached attributes for each parcel.
    - 25 m raster: derived from the vector, used to generate 1 km products.
  - Raster data sets
    - 25 m raster (GB and NI separately due to different projections): 3-band GeoTIFFs (band 1 dominant class per polygon, band 2 mean per-polygon confidence, band 3 percentage of polygon area covered by modal class).
    - 1 km raster products: dominant cover (21 target classes and 10 aggregate classes) and percentage cover (21 bands for target classes; 10 bands for aggregate classes). Values are integer percentages; sums may deviate 0–100 due to rounding and coastal edge effects.
  - Resolution and extents
    - 25 m data provide fine-grained mapping; 1 km products enable UK-wide modelling with other datasets (e.g., meteorology, species distribution).
    - 1 km products cover UK-wide percentage and dominant class information derived from the 25 m raster.
  - Minimum mapping unit
    - Minimum mappable area > 0.5 ha; polygons smaller than 0.5 ha and linear features < 20 m are dissolved into surrounding landscape.
  - File counts and structure
    - Vector: 6.7 million polygons in Great Britain and 0.9 million in Northern Ireland.
    - Raster: 25 m (GB and NI) and 1 km products with metadata in Table 4 (pixel dimensions, coordinate systems, extents).

- Class scheme and labelling
  - 21 LCM1990 classes based on UK Broad Habitats (see Appendix 2 for definitions).
  - Some Broad Habitats subdivided for spectral distinctiveness:
    - Built-up Areas and Gardens: Suburban and Urban.
    - Dwarf Shrub Heath: Heather and Heather grassland.
    - Littoral Sediment: Littoral sediment and Saltmarsh.
  - Vector attributes
    - gid: unique geometry identifier for each parcel.
    - hist: list of classes present in the polygon and pixel counts per class (e.g., "20:1, 21:9").
    - mode: recommended display class (1–21).
    - purity: percentage area of the polygon represented by the modal class.
    - conf: mean per-polygon vote confidence from the Random Forest classifier (0–100).
    - stdev: standard deviation of uncertainty.
    - n: number of pixels in the polygon.
    - cmp: composite image number from which the classification is derived.
  - Raster metadata
    - Includes per-pixel confidence (band 2) and modal-class coverage (band 3) to reflect per-polygon uncertainty and vegetation dominance.

- Data access, citation, and rights
  - Data access: 25 m and 1 km raster data available via the CEH Environmental Information Platform (eip.ceh.ac.uk). Full vector product available on request; licensing may apply.
  - DOIs: Each LCM1990 product has a DOI for citation (GB vector, GB 25 m raster, GB 1 km percent/dominant/class products; NI equivalents listed). DOIs should be cited in publications with author/date (e.g., Rowland et al., 2020).
  - Example citation format: Rowland, C.S.; Marston, C.G.; Morton, R.D.; O'Neil, A.W. (2020). Land Cover Map 1990 (vector, GB). NERC Environmental Information Data Centre. https://doi.org/10.5285/304a7a40-1388-49f5-b3ac-709129406399.
  - Map projections
    - Great Britain vector/raster in British National Grid (EPSG 27700).
    - Northern Ireland vector/raster in TM75 Irish Grid (EPSG 29903).

- Quality assurance and validation
  - QA checks cover projections, spatial completeness, polygon modal class presence (vector), header consistency, value ranges (0–100 for raster), and pixel sizes.
  - Data are based on the 2007 OS MasterMap-derived parcel framework; field boundary changes are infrequent, minimizing impact on accuracy.
  - A full validation exercise has been conducted against external datasets (Countryside Survey, National Forest Inventory, validation points); results to be reported separately.

- Temporal and methodological context
  - LCM1990 uses the same methods as LCM2015 to enable a 25-year land cover change product (1990–2015) for the UK.
  - The dataset emphasizes land cover mapping (not strictly land use); some land cover classes may not directly indicate land use (e.g., grassland used for recreation vs grazing).

- Usage notes and guidance for GIS specialists
  - For detailed reporting and communication, retain the gid attribute in the vector dataset to ensure unambiguous communication about parcels.
  - Choose data product level based on application:
    - Vector data for high-detail analyses requiring per-polygon metadata.
    - 25 m raster for applications requiring raster processing and reduced attribute load.
    - 1 km products for UK-scale modelling with other gridded datasets; aggregation may introduce small rounding discrepancies.
  - Be mindful of 0.5 ha MMU and potential misclassification in complex habitat patches; use _hist and per-polygon uncertainties to assess confidence.

- Appendix highlights (high level)
  - Appendix 1: Class interpretations and caveats for several Broad Habitat categories (e.g., woodland composition, grassland ambiguity, water bodies, urban vs suburban distinctions).
  - Appendix 2: Summary of Biodiversity Action Plan Broad Habitats (JNCC definitions) corresponding to LCM1990 classes.
  - Appendix 3: Standard LCM color mapping recipes for visualization.
  - Appendix 4: Composite images used in the LCM1990 workflow (metadata on dates and paths).

- References and contact
  - Primary references include Jackson (2000) on Broad Habitat definitions and Morton et al. (2011) on LCM2007 methods; Rowland et al. (2020a, 2020b) on land cover change 1990–2015.
  - For access inquiries: spatialdata@ceh.ac.uk; more information at https://eip.ceh.ac.uk/lcm/lcmdata.

- Acknowledgement
  - Supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.