# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

- Overview
  - User guide for three new UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019).
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; classes are aligned with LCM2015/2007 history but derived for remote sensing rather than field-based BAP definitions.
  - Production is automatic (no manual corrections this release) using Bootstrap Training with a Random Forest classifier.
  - Goal: enable rapid, nationwide land cover mapping with an emphasis on change detection and informing data use.

- Key products and data structure
  - 42 datasets total (Great Britain and Northern Ireland, for 2017–2019).
  - Core data families:
    - 20m Classified Pixels (new): RF classification results for 20m Sentinel-2 seasonal composites; includes per-pixel class and a confidence metric (band 2, 0–100).
    - Land Parcels: attributes describing parcel-level composition and confidence (gid, hist, mode, conf, purity, npix). MMU ~0.5 ha; parcels generalise landscape units and support time-series analyses. Changes from LCM2015 include renamed attributes and reorganised storage; gid differs from LCM2015.
    - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) derived from Land Parcels; used to summarise parcel data onto a coarser grid.
    - 1km Percent Cover: 21-band raster (per-class percentage cover per 1km square).
    - 1km Percent Aggregate Cover: 10-band raster (percentage cover for UKCEH Aggregate Classes per 1km).
    - 1km Dominant Cover: single-band raster (dominant class per 1km).
    - 1km Dominant Aggregate Cover: 1-band raster (dominant aggregate class per 1km).
  - Spatial coverage and formats
    - Great Britain: GB National Grid (EPSG 27700).
    - Northern Ireland: Irish National Grid (EPSG 29903).
    - Pixel resolution: 20m (classified pixels), 25m (land parcels), 1km (summary rasters).
    - Class totals: 21 UKCEH Land Cover Classes; 10 UKCEH Aggregate Classes.
  - Dataset naming and structure
    - Datasets duplicated annually (2017, 2018, 2019) and across GB/NI, yielding 42 datasets.
    - Appendix 6 lists full dataset naming conventions.

- Production methodology
  - Bootstrap Training
    - Training data derived from UKCEH LCM2015, selecting high-purity parcels (purity >= 99%) to form training samples.
    - Bootstrap approach uses historic maps to sample current satellite images, enabling automatic, iterative training without fresh field data.
    - Future maps planned to use 3-year majority signals (e.g., 2017–2019; 2018–2020) for bootstrap training.
  - Random Forest classification
    - RF classifier trained on balanced samples from Classification Scenes.
    - 10,000 samples per class per bag; ensures rarer classes are adequately learned.
    - Software stack: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL (open-source).
  - Imagery and feature engineering
    - Seasonal Composite Images: Sentinel-2 TOA reflectance, median per season (winter, spring, summer, autumn) at 20m resolution, produced in Google Earth Engine (GEE).
    - Context Rasters (20m): include terrain (height, aspect, slope) and proximity measures (distance to buildings, roads, sea, freshwater), plus coastal/foreshore and land-cover related masks.
    - Classification Scenes and tiling
      - Great Britain: 100x100 km tiles used to assemble 36-band Seasonal Composites plus contextual layers; 74 overlapping classification scenes classified independently; visual checks resolved minor precedence issues.
      - Northern Ireland: single 43-band classification scene per year determined by NI extent.
  - Classification output
    - Automatic classification without manual corrections; aims for consistent time-series signals across years.

- Context and data considerations
  - Context rasters help reduce spectral confusion between spectrally similar classes (e.g., bare rock vs urban).
  - Seasonal signals and high-frequency input improve discrimination of vegetation types and land cover transitions.
  - TOA vs SR: based on evaluation during production, TOA performed similarly to SR for UKCEH Land Cover Classes; SR data may be explored in the future for higher thematic detail.

- Validation and accuracy
  - Validation framework: UK-scale validation against GB countryside survey (2019), open Forest Inventory data, IACS data, and bespoke LCM validation points (n ~ 22k locations).
  - Reported accuracy (overall)
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Notes on validation
    - Validation points are not exact truth; they are best-available indicators with potential mismatches due to class mapping differences.
    - Approximately 80% correspondence across 21-class maps; expected improvements as methods evolve.
  - Detailed class-level metrics (producer’s and user’s accuracy) provided in Appendix 5, including confusion matrices for each year.

- Class definitions and presentation
  - 21 UKCEH Land Cover Classes derived from BAP Broad Habitats; not a one-to-one mapping to BAP, but aligned to enable change detection and historical comparability.
  - Appendix 2 provides BAP Broad Habitat definitions; Appendix 3/4 give recommended color recipes (including color-blind friendly variants) for map display.
  - The guide discusses nuances and potential confusion between UKCEH Land Cover Classes and BAP Broad Habitats, emphasizing consistent, comparable labeling over time.

- Practical considerations for use
  - Comparability and time-series
    - Land Parcel identifiers (gid) do not match LCM2015; time-series comparisons should use the gid framework or spatial overlap rather than direct id matching.
    - Bootstrap Training and 3-year majority bootstrap plans are positioned to improve consistency across years.
  - Data interpretation
    - 1km percent cover values are integers; sums may not equal exactly 100 due to rounding, especially near coastlines.
    - Some upland, peatland, and linear features may be underrepresented due to MMU and spectral limitations; class definitions reflect current training data and satellite detection capabilities.
  - Future directions
    - Annual LCM releases are intended; exploration of additional input data (e.g., Sentinel-1, multitemporal data) and potential gap-filling strategies for missing seasons.
    - Potential refinements to the UKCEH Land Parcel Spatial Framework as higher-resolution data become available.

- Appendices and supporting material
  - Appendix 1–2: Detailed relationships between UKCEH Land Cover Classes and BAP Broad Habitats.
  - Appendix 3–4: Colour recipes for displaying classes (including color-blind friendly options).
  - Appendix 5: Detailed confusion matrices and per-class accuracy metrics for LCM2017, LCM2018, LCM2019.
  - Appendix 6: Full list of datasets and naming conventions for LCM2017–LCM2019.