# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- A user guide accompanying the release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map uses 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
- Production is automatic (Bootstrap Training with Random Forest), enabling rapid, coast-to-coast mapping.
- No manual corrections were applied for this release; nevertheless, visual checks and formal validation were performed.
- Validation against GB countryside survey data, National Forest Inventory, IACS, and validation points yields ~78–79% overall accuracy across the three years.
- Aims to support users in making informed decisions about using UKCEH LCM data now and for future updates.

## Data inputs and production workflow
- Input data
  - Sentinel-2 Seasonal Composite Images (TOA reflectance; 20 m resolution; four seasons)
  - Ten Context Raster layers (e.g., terrain, proximity to buildings/roads/seas, water bodies, woodland)
  - Google Earth Engine used to generate seasonal composites
- Classification approach
  - Bootstrap Training: historical maps (LCM2015) provide a large, automatically sampled training set
  - Training set: parcels from LCM2015 with purity ≥ 99%
  - Random Forest classifier trained with balanced sampling (10,000 samples per class per patch)
- Production specifics
  - GB classification uses overlapping 100 x 100 km tiles, yielding 74 GB Classification Scenes (46-band per scene)
  - NI uses a single 43-band Classification Scene per year
  - Output products are generated for GB and NI for each year

## UKCEH Land Parcel Spatial Framework and classifications
- Land Parcel Spatial Framework
  - Fixed framework with minimum parcel size ~0.5 ha (MMU)
  - gid provides a unique parcel identifier; framework geometry unchanged since LCM2015
  - gid values do not match LCM2015 parcels; comparability across 2017–2019 is via spatial overlap, not gid
- UKCEH Land Cover Classes
  - 21 classes for detailed maps; 21-class outputs align with UKCEH LCM2015 and earlier equivalents
  - Appendix notes detail class definitions, relationships to UK BAP Broad Habitats, and detection considerations (e.g., upland peat, bracken, saltwater vs freshwater)

## Datasets and product structure
- Total datasets: 42 (GB and NI for three years across major products)
- 20 m Classified Pixels
  - New in this release; RF outputs with per-pixel class probability
  - Band 1 = most likely class; Band 2 = probability (0–100) indicating classification confidence
  - Preserves fine landscape details not captured in parcel-smoothed products
- Land Parcels
  - Attributes include gid, _hist (class frequency per parcel), _mode, _purity, _conf, _stdev, _n
  - Some attribute naming differences vs LCM2015 to align with production software
- 25 m Rasterised Land Parcels
  - 3-band rasters: band 1 = _mode, band 2 = _conf, band 3 = _purity
- 1 km Raster products
  - 1 km Percent Cover: 21-band raster (percentage cover per class)
  - 1 km Percent Aggregate Cover: 10-band raster (aggregate class percentages)
  - 1 km Dominant Cover: 1-band raster (dominant class per 1 km grid)
  - 1 km Dominant Aggregate Cover: 1-band raster (dominant aggregate class)
- Extents and coordinate systems
  - Great Britain: EPSG:27700 (British National Grid)
  - Northern Ireland: EPSG:29903 (TM75 Irish Grid)
  - Pixel sizes: 20 m (classified pixels), 25 m (land parcels), 1 km (percent/dominant rasters)
- Documentation and metadata
  - Appendix 5 provides full dataset list; Appendix 4 includes validation details
  - Colour recipes and class relationships documented for visualization

## Model, validation, and limitations
- Validation approach
  - 22,325 validation points from GB countryside survey, National Forest Inventory, IACS, and expert interpretation
- Reported accuracies
  - LCM2017: ~78.6% overall accuracy
  - LCM2018: ~79.6% overall accuracy
  - LCM2019: ~79.4% overall accuracy
- Notes on validation
  - Validation points were the same across the three products; currency of observations relative to each product varies
  - Some class conversions and labeling differences due to mapping from different sources
  - Approximately 80% correspondence is considered strong for an automatically produced 21-class map
- Data quality considerations
  - 4-season gaps due to cloud are handled by the classifier and partial data are common
  - No manual accuracy corrections were performed in this release to retain rapid, automated production
  - Coastal and peatland classes can exhibit confusion with neighboring classes; context rasters help mitigate spectral confusion
- Validation details
  - Confusion matrices and accuracy metrics are provided in Appendix 4

## Governance, stewardship, and future directions
- Data governance and stewardship
  - Clear documentation of data sources, processing steps, and validation
  - Automated production with explicit methodology details (Bootstrap Training, RF, context features)
  - Open-source tools used (Weka, PostGIS, GDAL) and Google Earth Engine for seasonal composites
- Update cadence and planning
  - Published plan to release a new LCM annually
  - Future bootstrap plan evolving: 2020 bootstrap from 2017–2019 majority signal; 2021 from 2018–2020 majority
- Data comparability and metadata
  - gid changes mean cross-year comparisons with LCM2015 require spatial overlap rather than parcel IDs
  - Attribute naming changes in 2017–2019 outputs reflect production software alignment
- Opportunities and future improvements
  - Gap-filling possibilities with Sentinel-1 SAR data and alternative optical sources if seasonal gaps expand
  - Ongoing work on upland habitat discrimination; potential refinement of peatland-related classes
  - Exploration of finer parcel structures or alternative summaries beyond the standard Land Parcel Spatial Framework
- Appendices and supporting materials
  - Appendix 1–3: Notes on UKCEH Land Cover Classes and BAP Broad Habitats
  - Appendix 4: Validation results with detailed confusion matrices and accuracy metrics
  - Appendix 5: Full dataset list and mappings for LCM2017, LCM2018, LCM2019

## Practical takeaways for data stewards
- The three-year LCM release represents an automated, scalable framework for national land cover mapping, balancing detail (20 m Classified Pixels) with generalized summaries (25 m parcels, 1 km rasters).
- Governance considerations include clear provenance, reproducibility using Bootstrap Training and RF, and explicit documentation of changes in data structure and attributes.
- For time-series work, use Appendix 5 and gid-based cross-year comparisons within 2017–2019; cross-warranty comparisons with LCM2015 require spatial overlap since parcel IDs differ.
- Expect annual updates with potential improvements in training data, gap-filling strategies, and habitat detection as methods evolve.