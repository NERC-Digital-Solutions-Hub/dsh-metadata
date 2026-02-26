# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created from Landsat-5 two-date composites (30 m resolution) and classified into 21 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Built to be compatible with later LCM products (LCM2007, LCM2015) using the same object-based spatial framework, enabling long-term land cover change assessments (e.g., 1990–2015).
- Spatial framework derived from OS MasterMap topographic data for Great Britain and Northern Ireland equivalents; designed to reflect real-world boundaries for interoperability.
- LCM1990 maps land cover (not strictly land use); minimum mapped unit is >0.5 ha; smaller parcels and very short linear features are dissolved into surrounding landscape.

## Data products and structure
- Core products: LCM1990 vector (parcel-based polygons) and derived 25 m raster; 1 km percentage cover products for both target (21) and aggregate (10) classes; dominant cover products.
- Classes: 21 LCM1990 target classes based on Broad Habitats; some are further divided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- Vector data set:
  - ~6.7 million polygons for Great Britain; ~0.9 million polygons for Northern Ireland.
  - Eight key attributes per polygon, plus a full history of class composition within the polygon (hist), a recommended display class (mode), confidence (conf), standard deviation (stdev), number of pixels (n), and the composite image source (cmp).
  - gid: unique parcel identifier; _hist: class composition; _mode: 1–21 target class; _purity: modal class coverage; _conf: mean per-polygon RF vote confidence (0–100); _stdev: uncertainty; other metadata.
- Raster data sets:
  - 25 m raster: 3 bands (band 1 = dominant LCM1990 class per polygon; band 2 = mean per-polygon confidence; band 3 = percentage of polygon area covered by the modal class).
  - 1 km rasters: aggregate percentage covers and dominant class per 1 km pixel for both target and aggregate classes; 21 target bands and 10 aggregate bands; integer values with occasional rounding inaccuracies to sum to ≈100%.
- Data access formats and projections:
  - Great Britain: British National Grid (EPSG 27700) for both 25 m and 1 km rasters.
  - Northern Ireland: Irish Grid (TM75) for both 25 m and 1 km rasters.
  - Data are distributed as uncompressed GeoTIFFs; vector product is available on request; licensing may apply.
- Spatial relationships:
  - 25 m raster and vector datasets are aligned; 1 km products summarize 25 m data to UK-scale maps suitable for integration with meteorological data or species distribution models.
- Uncertainty and prediction:
  - Random Forest per-pixel probability is carried through to per-polygon estimates, providing per-polygon confidence metrics.

## Access, licensing, and citation
- Data access:
  - 25 m and 1 km raster data for LCM1990 are available via the CEH Environmental Information Platform (EIP). Full vector product is available on request from CEH.
  - Some users may incur license fees; contact spatialdata@ceh.ac.uk for access details.
- Citing LCM1990:
  - All LCM1990 products have DOIs (GB vector, GB 25 m raster, GB 1 km target/dominant/aggregate products, NI vector, NI 25 m raster, NI 1 km target/dominant/aggregate products).
  - Example citation format: "Rowland et al. (2020). Land Cover Map 1990 (vector, GB). NERC Environmental Information Data Centre. DOI: ..."
  - Refer to Tables 5 and 6 in the document for the exact DOIs by product and region.
- Publication and reproducibility:
  - DOIs enable repeatable methods and traceable usage; more information at the CEH EIDP data citation pages.

## Quality Assurance and validation
- UK CEH Land Cover Maps are produced with defined methods and QA checks, including projection validation, spatial completeness, polygon modal class checks, value range checks (0–100 for raster percent), and pixel size verification.
- A full validation exercise against other datasets (e.g., Countryside Survey, National Forest Inventory) has been conducted; results to be reported in a separate publication.
- The parcel framework mirrors 2007 Mastermap-derived data; field boundary changes are relatively infrequent, limiting impact on overall mapping accuracy.

## Data access details
- Access portal: CEH Environmental Information Platform (https://eip.ceh.ac.uk/).
- Vector product: available under licence on request from CEH (spatialdata@ceh.ac.uk); license fees may apply.
- For more information and current access conditions: https://www.ceh.ac.uk/services/land-cover-map-1990 or contact the above email.

## Appendices (summary)
- Appendix 1: Comments on LCM1990 classes mapping to Broad Habitats; nuance notes on potential misclassifications and training considerations.
- Appendix 2: Summary of Biodiversity Action Plan Broad Habitats definitions (for context and interpretation of the 21 classes).
- Appendix 3: Standard LCM1990 colour mapping recipes (color codes for mapping results to display colors).
- Appendix 4: Composite images used during LCM1990 production (metadata on image paths, rows, dates).

## Further Information
- Project and datasets described here are part of the LCM1990 suite, with related works (LCM2007, LCM2015) used for cross-product compatibility and long-term change analysis.
- For queries and additional details, continue to consult the CEH LCM1990 data pages and contact CEH spatialdata@ceh.ac.uk.