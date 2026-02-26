# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Objective and scope
  - Release three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed for wide comparability with LCM2015/LCM2007/LCM2000 lineage.
  - Automated production aims to deliver yearly UK-wide maps with rapid turnaround; no manual corrections in this release.
  - Emphasizes appropriate use, production choices, validation outcomes, and future development plans.

- Data structure and datasets (GB and NI)
  - 20m Classified Pixels: new per-pixel RF classification results with class probability. Preserves fine landscape detail without generalisation.
  - Land Parcels: intersects 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework; provides parcel-level attributes (gid, hist, mode, purity, conf, stdev, n).
  - 25m Rasterised Land Parcels: rasterised from Land Parcels into 25m pixels with 3 bands (dominant class, confidence, purity).
  - 1km Raster products:
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
  - Geographic extents and coordinates
    - Great Britain: British National Grid (EPSG: 27700)
    - Northern Ireland: Irish Grid (TM75, EPSG: 29903)
  - Dataset counts and year-specific structure
    - Each year includes GB and NI versions of datasets, leading to 42 primary datasets across the three years.

- Classification inputs and context
  - Seasonal Composite Images: Sentinel-2 TOA reflectance per season (winter, spring, summer, autumn) computed as medians; four-season data used to support phenology-based classification.
  - Context Rasters (20m): include terrain (height, aspect, slope) and proximity masks (distance to buildings, roads, sea, freshwater, foreshore, tidal water, woodland) to reduce spectral confusion.
  - Seasonal and contextual combination forms Classification Scenes (GB: 46-band; NI: 43-band).
  - Satellite data choices: TOA used for all years; SR (surface reflectance) not adopted due to no observed accuracy gains in this workflow.

- UKCEH Land Parcel Spatial Framework
  - Framework retained from LCM2007/LCM2015 lineage, with minor internal changes.
  - 0.5 ha minimum parcel size (MMU); parcels intended to represent discrete real-world units (fields, parks, urban areas, etc.).
  - gid identifiers do not match LCM2015 parcels; parcels comparable via spatial overlap or new gid aligning to the 2017–2019 framework.
  - The framework enables change detection and stable parcel-based summaries; supports use with alternative parcel schemes by providing 20m Classified Pixels as the base.

- Bootstrap Training and Random Forest (RF) classification
  - Bootstrap Training: automated training dataset built from historical LCMs (primarily LCM2015) to train RF classifiers for 2017–2019. Uses majority signal from 2017–2019 bootstrap samples for subsequent maps.
  - Training data selection: parcels from LCM2015 with purity ≥ 99% used to bootstrap; aims to balance training across 21 classes.
  - RF classifier: balanced sampling (10,000 samples per class per Classification Scene) to avoid dominance by common classes.
  - Production tools: bespoke UKCEH software integrating WEKA, PostGIS, and GDAL (open source components).

- Validation and quality assurance
  - UK-scale validation using GB countryside survey 2019, National Forest Inventory data, IACS, and bespoke LCM validation points (22,325 total).
  - Reported overall accuracy (consistency across years):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation notes: the same validation dataset used for all three products; accuracy figures reflect currency and class-mapping caveats. Approximately 80% overall correspondence is considered robust for an automatic, annual, 21-class product.

- Production decisions and notable changes
  - No manual corrections this release to enable annual production; visual checks and formal validation still conducted.
  - Full automation leads to occasional random year-to-year errors; true land cover changes should persist above background noise as the time series develops.
  - GID and Land Parcel Spatial Framework changes mean 2017–2019 parcel IDs do not align with LCM2015; cross-year comparisons should use the parcel framework’s gid where possible.
  - Appendix material links: 21 UKCEH Land Cover Classes; relationship to UK BAP Broad Habitats; guidance on class derivations and detection considerations; notes on common mapping confusions.

- Classification outputs and interpretation
  - 20m Classified Pixels provide per-pixel class and confidence scores (0–100); preserves narrow features and enables detailed mapping.
  - Land Parcels summarize pixel-level results into discrete parcels with attributes including:
    - _hist: breakdown of class counts within the parcel
    - _mode: most frequent class
    - _purity: modal proportion
    - _conf: mean class membership probability (0–100)
    - _stdev: standard deviation of confidence
  - 25m Rasterised Lands Parcels aggregate parcel data into 25m grid with three bands: _mode, _conf, _purity.
  - 1km rasters provide broad-scale summaries to support landscape-level analysis and change detection

- Practical considerations for analysts
  - Use 20m Classified Pixels for high-detail analyses and when preserving small patches matters.
  - Use Land Parcels or 25m raster products for streamlined, parcel-based or grid-based analyses and easier time-series comparisons.
  - When comparing with previous maps, account for the 2017–2019 Land Parcel Spatial Framework changes and gid differences from LCM2015.
  - For time-series consistency, leverage Bootstrap Training approach and the majority-signal bootstrap across 2017–2019; plan for 2020+ updates to follow the evolving bootstrap strategy.

- Future plans and ongoing development
  - Annual release model intended; LCM2020 planned for 2021 with continued refinement of Bootstrap Training and RF methods.
  - Consideration of additional input sources (e.g., Sentinel-1 SAR) and expanded regional data to improve classification under cloud cover and phenology variances.
  - Ongoing validation resource development to tighten accuracy and to improve cross-year comparability.

- Appendices and supplementary context
  - Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats; caveats for upland, peatland, and coastal classes.
  - Appendix 3: RGB colour mapping recommendations for displaying UKCEH Land Cover Classes.
  - Appendix 4: Full confusion matrices and validation statistics by year (illustrative accuracy and producer/user accuracies per class).
  - Appendix 5: Full list of datasets and their naming conventions by year and geography (GB vs NI).