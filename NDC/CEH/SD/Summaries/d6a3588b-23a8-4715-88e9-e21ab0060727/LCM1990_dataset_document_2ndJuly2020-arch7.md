# Dataset documentation

- Overview
  - Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created by classifying Landsat-5 satellite imagery into 21 classes, aligned with UK Biodiversity Action Plan Broad Habitats.
  - Built to be compatible with newer LCM products (LCM2015) using an updated spatial framework; enables cross-temporal analysis (e.g., 1990–2015).
  - Data are delivered as vector polygons (core) with derived 25m rasters and 1km aggregated products for diverse GIS applications.

- Data products and structure
  - Vector data
    - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
    - 8 key attributes per polygon, including dominant class, source image, pixel breakdown by class, and per-polygon classification confidence.
    - Unique geometry identifier (gid) for unambiguous communication; recommended to retain.
  - Raster data
    - 25m raster: 3-band GeoTIFF (dominant class, mean per-polygon confidence, percentage cover of the modal class).
    - 1km raster: derived by aggregating 25m data to provide dominant and percentage cover for both 21 target classes and 10 aggregated classes.
    - Spatial extents: GB and NI provided separately with respective coordinate systems (GB: British National Grid; NI: TM75 Irish Grid).
    - Data dimensions and metadata specified (e.g., 25m GB: 28,000 x 52,000 pixels; 1km GB: 700 x 1,300 pixels; NI resolutions correspondingly smaller).
  - Class details and aggregation
    - 21 target classes derived from Broad Habitats; several classes are subdivided for improved discrimination (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
    - Laminated mapping to support both detailed and generalized analyses.

- Data quality, uncertainty, and metadata
  - Rich metadata per polygon, including dominant class, pixel composition per class, and mean classification probability (uncertainty).
  - Per-pixel and per-polygon uncertainty information from Random Forest classifier; included in both vector (via attributes) and 25m raster bands.
  - Quality assurance includes projection checks, spatial completeness, modal class presence, and range validation (0–100 for raster percentages).
  - Separate validation exercise against independent datasets described; full publication forthcoming.

- Spatial framework and comparability
  - LCM1990 uses the LCM2007 spatial framework for consistency across products.
  - Directly comparable with LCM2015; designed to enable a 25-year land cover change product (1990–2015).
  - Not all classes are directly comparable to earlier LCM versions (e.g., 2000, 2007) due to framework/class differences.

- Data access and citation
  - Access via CEH Environmental Information Platform (eip.ceh.ac.uk) for 25m and 1km rasters; full vector product available on request (license may apply).
  - Each product has a DOI for citation (GB vector, GB 25m raster, GB 1km targets/aggregates; NI vector, NI 25m raster, NI 1km products; some DOIs pending).

- Example usage notes
  - The 1km percentage cover products sum may deviate from 100% due to rounding and coastal edge effects.
  - The 25m raster contains three bands enabling both thematic and confidence-driven analyses; the 1km rasters enable broad UK-scale modeling with other datasets.

- Citing LCM1990
  - DOIs provided for Great Britain and Northern Ireland products; example citation format recommended includes author(s) and year in-text with full DOI in references.
  - Sample references include Rowland et al. (2020) for GB vector and raster products; additional DOIs pending for some 1km products.

- Access and contact
  - CEH EIP portal: https://eip.ceh.ac.uk/
  - Vector product requests: spatialdata@ceh.ac.uk
  - Project information and data pages: https://www.ceh.ac.uk/services/land-cover-map-1990
  - Further information and journal preparations: contact details and CEH pages provided in the document.

- Appendix highlights (key concepts)
  - Broad Habitat-based classification with definitions (Appendix 2) and class-specific notes (Appendix 1) to aid interpretation.
  - Color-mapping guidance (Appendix 3) for consistent visualization of LCM1990 classes.
  - Composite image details used for training and classification (Appendix 4).