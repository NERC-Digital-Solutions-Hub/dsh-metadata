# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map represents a range of geospatial datasets with 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) consistent with LCM2015.
  - Aims to help users understand data production, validation, decisions, and future plans for informed application.

- Key data products and structure
  - 21 UKCEH Land Cover Classes (GB and NI versions)
  - Datasets per year (total 42 datasets: GB and NI versions, for multiple product types)
  - Dataset families:
    - 20m Classified Pixels (new in these products)
      - 2-band, 8-bit rasters: band 1 = most likely class, band 2 = per-pixel probability (0–100)
      - Preserves fine detail; not generalised by parcel framework
    - Land Parcels
      - Attributes: gid, _hist (histogram of pixel counts per class), _mode (dominant class), _purity (percent of modal class), _conf (mean class membership probability), _stdev, _n (pixel count)
      - Notes: gid unique within the UKCEH Land Parcel Framework; some attribute naming changes vs LCM2015
    - 25m Rasterised Land Parcels
      - 3-band raster: band 1 = _mode, band 2 = _conf, band 3 = _purity
    - 1km Raster datasets (derived from parcel data)
      - 1km Percent Cover (21-band)
      - 1km Percent Aggregate Cover (10-band)
      - 1km Dominant Cover (1-band)
      - 1km Dominant Aggregate Cover (1-band)

- Methodology and production workflow
  - Bootstrap Training + Random Forest (RF) classification
    - Bootstrap Training uses historic UKCEH LCM observations to automatically generate a large spectral training set.
    - RF classifier trained on balanced samples to produce 20m Classified Pixels.
  - Sentinel-2 Seasonal Composite Images
    - Median TOA reflectance per season (winter, spring, summer, autumn) at 20m resolution.
    - 9 bands used from Sentinel-2 for classification.
  - Context Rasters
    - 20m context layers to aid disambiguation of spectrally similar classes (e.g., terrain, urban proximity, distance to features).
  - Classification Scenes and tile strategy
    - GB: 100 x 100 km tiles; 74 overlapping Classification Scenes classified independently (46-band per scene, 36 spectral + 10 context + others)
    - NI: single 43-band Classification Scene per year (36 spectral + 7 context)
  - UK Land Parcel Spatial Framework
    - Framework to summarise 20m Classified Pixels into land parcels (~0.5 ha minimum) for stable change-detection units.
    - Gid-based linkage; parcel boundaries generalised from prior cartography.
  - Bootstrap Training evolution and future plans
    - Bootstrap Training uses majority signal across recent maps; LCM2020/2021 planned with 3-year majority bootstrap.
  - Validation
    - UK-scale validation against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke validation points (22,325 points)
    - Reported overall accuracy: LCM2017 ≈ 78.6%, LCM2018 ≈ 79.6%, LCM2019 ≈ 79.4%
    - Notes on validation: point data vary in currency; conversions between schemes; not an absolute truth but useful guidance.

- Data details and harmonisation notes
  - Class nomenclature and relationships
    - 21 UKCEH Land Cover Classes linked to UK BAP Broad Habitats; tables and appendices describe mappings and notes on detection and spectral differences.
  - Spatial referencing and extents
    - Great Britain: GB National Grid (EPSG: 27700)
    - Northern Ireland: Irish Grid (TM75; EPSG: 29903)
    - GB extent: min East 0, max East 700,000 m; min North 0, max North 1,300,000 m
    - NI extent: East 180,000–400,000 m; North 300,000–500,000 m
  - Parcel framework and data compatibility
    - Land Parcel identifiers (gid) exist, but new LCM2017–2019 gid values do not match LCM2015 parcel IDs; comparisons should use gid-based spatial overlap for consistency.
  - Data presentation and packaging
    - 20m Classified Pixels preserve fine features (e.g., narrow patches) not present in land parcels; 25m parcels offer a coarser summary.
    - 1km rasters provide aggregated views (percent cover, dominant class) for broad-scale analyses.

- Relationship to UKCEH Landscape Classification
  - UKCEH Land Cover Classes vs UK BAP Broad Habitats
    - Appendix notes explain how to interpret and map between the two classifications and their contextual meanings.
    - Several nuanced distinctions and caveats are given (e.g., limitations in detecting some habitat types via remote sensing).

- Practical guidance for GIS specialists
  - Primary data formats to incorporate into map products
    - 20m Classified Pixels for high-detail mapping and feature-level analysis
    - Land Parcels and 25m Rasterised Land Parcels for parcel-based summaries
    - 1km raster products for rapid overviews and regional-scale analyses
  - Use cases
    - Change detection over time via parcel framework
    - High-resolution mapping of land cover types for policy, planning, conservation
    - Cross-year comparisons using gid-based parcel alignment
  - Validation and quality
    - Expect around 80% correspondence at 21-class level; consider local validation for critical applications
    - Be mindful of class definition nuances and training data provenance when interpreting results

- Appendices and supplementary resources
  - Appendix 1–2: UKCEH Land Cover Classes and UK BAP Broad Habitats descriptions
  - Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes
  - Appendix 4: Validation details, confusion matrices, and producer/user accuracies (per class and year)
  - Appendix 5: Full list of datasets by year and dataset type
  - Glossary and terminology clarifications throughout the document

- Future plans and note on updates
  - A new LCM is planned annually; ongoing assessment of data inputs and potential integration of additional data sources (e.g., Sentinel-1 SAR) to improve gap-filling and robustness.