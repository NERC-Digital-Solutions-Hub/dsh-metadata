# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created by classifying two-date Landsat-5 imagery (30 m resolution) into 21 classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- It aligns with the LCM2015/LCM2007 spatial framework to enable cross-product compatibility and long-term change analysis (goal of enabling a 25-year land cover change product).
- The dataset supports multiple data products and levels of detail, including rich metadata and uncertainty information, to aid diverse user needs.

## Data products and structure

- Vector data set
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Each parcel has attributes: dominant class, source image, pixel breakdown by class, modal class proportion, uncertainty metrics, and a unique geometry identifier (gid).
  - Key attributes include: gid, hist (class breakdown per polygon), mode (recommended display LCM1990 class), purity, conf, stdev, n, and cmp (composite image source).
- Raster data sets
  - 25 m raster: three-band 8-bit GeoTIFF (band 1: dominant class per polygon, band 2: mean per-polygon confidence, band 3: percent cover of modal class).
  - 1 km raster: aggregates from 25 m to provide dominant cover (21 target classes and 10 aggregate classes) and percentage cover (21 target bands and 10 aggregate bands). Percentages are integer values; sums may not exactly equal 100 due to rounding and coastal edge effects.
- Class structure
  - 21 LCM1990 target classes, mapped from 21 Broad Habitat definitions.
  - 10 aggregate classes used for 1 km rasters.
  - Some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland).

## Data details and standards

- Spatial framework and compatibility
  - Built to be directly comparable with LCM2015 and LCM2007 where possible, enabling retrospective and future comparisons.
- Minimum mapping unit
  - Minimum mappable area is >0.5 ha; polygons smaller than 0.5 ha or linears under 20 m are dissolved into surrounding landscape.
- Metadata and uncertainty
  - Rich polygon metadata; per-polygon mean probability from the Random Forest classifier is included (in both vector and 25 m raster).
  - Per-pixel probability uncertainty is provided as part of the data.
- Location and projections
  - Great Britain: British National Grid (OSGB 27700).
  - Northern Ireland: Irish National Grid (TM75, EPSG: 29903).
- DOIs and citation
  - Each LCM1990 product has its own DOI for citation in publications (vector GB, 25 m GB, 1 km GB targets, 1 km GB aggregates; NI equivalents also provided or pending). Publication citations should include author and year.
- Data access and licensing
  - 25 m and 1 km raster data are available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request; licensing fees may apply for some users/applications.
  - Contact: spatialdata@ceh.ac.uk; more information at CEH LCM1990 page.

## Quality assurance and validation

- CEH applies defined methods and code with trained staff.
- QA checks cover: correct projections, spatial completeness, modal class presence in polygons (vector), metadata consistency, value ranges (0–100 for raster percent covers), and correct pixel sizes.
- A full validation exercise compares LCM1990 with other datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately.
- The parcel framework derives from 2007 Ordnance Survey MasterMap data; field boundary changes have limited impact on overall mapping accuracy.

## Practical considerations for data use

- LCM1990 maps land cover rather than definitive land use; some land uses cannot be inferred from cover alone (e.g., recreation grass vs. grazed grass).
- The dataset is static/archived (stable with DOIs) but designed to support long-term land-cover-change studies.
- Users should retain the gid attribute in vector data for unambiguous communication and reproducibility.
- The documentation includes guidance on class interpretations (Appendix 1) and broad habitat definitions (Appendix 2), plus standard color mappings (Appendix 3) and details on composite images used (Appendix 4).

## Access and contact

- CEH Environmental Information Platform: https://eip.ceh.ac.uk/
- Dataset information and access: https://www.ceh.ac.uk/services/land-cover-map-1990
- Contact for access and queries: spatialdata@ceh.ac.uk

## References and further information

- Foundational literature and related LCM documentation (Appendices 1–4 provide class interpretations, color mapping, and dataset specifics).
- Examples of DOIs and citation guidance provided for GB and NI products.
- A forthcoming journal article will present detailed validation results and methodological details.