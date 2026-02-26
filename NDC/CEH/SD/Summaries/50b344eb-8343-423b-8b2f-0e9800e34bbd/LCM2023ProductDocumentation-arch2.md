# The UKCEH Land Cover Map for 2023

- Purpose and scope
  - User guide for LCM2023, the annual UK land cover map produced by UKCEH.
  - Product comprises seven geospatial datasets: three for Great Britain (GB) and three for Northern Ireland (NI), plus a cross‑region 1 km summary raster.
  - Outputs include: a 10 m classified pixel dataset, a dataset of land parcels, a 25 m pixel rasterised land parcels dataset, and a 1 km summary raster.
  - Aim is to support informed decision-making about environmental health and change, with emphasis on temporal consistency and change detection.

- UKCEH Land Cover Classes and relationship to biodiversity frameworks
  - 21 UKCEH Land Cover Classes, linked to Biodiversity Action Plan (BAP) Broad Habitats (not identical to BAP; some adjustments noted).
  - Appendix describes how UKCEH classes map to BAP Broad Habitats, including nuances for certain classes (e.g., water, urban, heather, bog).
  - General guidance on using the 21 classes alongside BAP concepts, with italicisation used to differentiate BAP terms when referenced.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI)
    - Derived from Classification Scenes using Bootstrap Training and Random Forest.
    - Output: two bands per pixel — first band is the most likely UKCEH Land Cover Class; second band is the class membership probability/confidence.
    - High spatial detail retained (no Land Parcel Spatial Framework generalisation) to preserve narrow features; validation performed against the 25 m parcel dataset.
  - Land Parcel datasets (GB and NI)
    - Result from intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
    - Includes Classified Land Parcels with parcel-level attributes (gid, _hist, _mode, _conf, _stdev, _agg, _n, etc.).
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterised representation of parcels at 25 m resolution.
    - Three bands: dominant land cover class (_mode), mean confidence (_conf), and mean purity (_purity) per parcel.
  - 1 km Summary Rasters (GB and NI)
    - Summary of 25 m data to 1 km cells: dominant class, dominant aggregate class, and percentage cover per class/aggregate.
    - Percentage values are integers; rounding may cause totals to deviate slightly from 100%.
  - Seasonal Composite Images
    - Sentinel-2-based seasonal composites (four seasons) used to create Classification Scenes.
    - Bands reflect spectral information across seasons; occasional gaps due to cloud are represented as nulls.
  - Context Rasters
    - 10 m context layers to reduce spectral confusion (GB: height, aspect, slope, proximity to buildings/roads/tidal waters/freshwater, foreshore mask, woodland mask, saltmarsh mask; NI: height, aspect, slope, urban mask, distances to coast/road/freshwater, foreshore mask, tidal water mask).
  - Classification Scenes
    - GB: 32 tiles using a modified OS 100 x 100 km grid; NI: single 49-band scene for Northern Ireland.
  - UKCEH Land Parcel Spatial Framework
    - Framework to generalise national cartography into land parcels (~0.5 ha minimum) to provide discrete units for comparison and change detection.
    - Also defines the MMU and processing workflow; note on non‑alignment of identifiers with LCM2015 for cross-year comparisons.

- Production method and workflow
  - Bootstrap Training
    - Automatic generation of training data from historic LCMs (LCM2020–LCM2022) where pixels had >80% probability and agreed on the same class across three years.
    - Enables classifier training without new field data; large bootstrap samples emphasize the dominant signal to improve learning.
  - Random Forest classification
    - Training uses 10,000 samples per class (bag) with replacement to balance class representation.
    - Classification yields the 10 m Classified Pixel product; confidence is captured in the second band.
    - Processing relies on UKCEH‑developed software integrating Weka, PostGIS, and GDAL (open source).
  - Data production and validation
    - Formal validation uses 33,107 reference points across the UK, covering all 21 classes; overall accuracy reported at 83%.
    - Validation data drawn from GB countryside survey, National Forest Inventory, Rural Payments Agency, and bespoke validation points.
  - Temporal consistency and change detection
    - Annual production enables differentiation between random classification errors and real land cover change; random errors are expected to flicker over time.
    - The project highlights potential improvements if newer methods yield meaningful accuracy gains.

- Accessibility, usage, and citation
  - Each LCM2023 dataset has a DOI; users are encouraged to cite the respective dataset DOIs and referenced publications.
  - Datasets available for GB and NI, with a shared 1 km summary raster for cross-region analyses.
  - A disclaimer notes that annual methodological changes can cause small changes in results beyond real land cover change.

- Validation details and known issues
  - Overall accuracy: 83% (21-class detail) from validation against a composite reference dataset.
  - Known issues:
    - A small number of polygons missing from vector land parcel products; negligible impact on 1 km summary rasters; 10 m datasets unaffected.
    - Some classification confusion remains among certain land cover types (notably within peat/peatland and transitional habitats); context rasters help mitigate this.
  - Confusion matrices and producer’s/user’s accuracy metrics are provided in appendices to support interpretation and quality assessment.

- Practical display and analysis considerations
  - Colour recipes and QGIS symbol files are provided (Appendix 5 and 6) to support consistent visualization, including color-blind friendly options.
  - The 10 m dataset is best for detailed landscape features; the 25 m parcel data supports standardized territorial units and change detection over time.
  - The 1 km rasters are suitable for broad-scale monitoring and trend analysis, with rounding considerations noted.

- Summary of key references and data sources
  - Core methodology and production context described (Bootstrap Training, RF classifier, seasonal composites, context rasters, and parcel framework).
  - Related literature and prior UKCEH LCM products referenced for continuity (LCM1990, 2000, 2007, 2015–2022).
  - Appendices provide detailed land cover definitions (UKCEH LCM Classes vs. UK BAP Broad Habitats) and data quality assessments.
  
- Supplementary materials
  - Appendix 5: Recommended color scheme for displaying UKCEH Land Cover Classes.
  - Appendix 6: Color‑blind friendly color scheme.
  - Appendix 4: Correspondence matrices and accuracy statistics (for interpretation of class-level performance).