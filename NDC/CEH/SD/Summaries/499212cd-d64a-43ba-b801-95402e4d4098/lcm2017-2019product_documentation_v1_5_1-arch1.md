# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Overview
- Release of three national UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Each map contains 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; near-exact class matches to prior maps (LCM2007/LCM2015 lineage).
- Automatic production using Bootstrap Training + Random Forest classifier; aim for annual updates.
- Validation indicates maps are of comparable quality to recent predecessors, with formal checks and visual validation described.

## Data content and structure
- 21 UKCEH Land Cover Classes, aligned with UKCEH Land Cover Classes and UK BAP Broad Habitats (Appendix 1/2).
- Data packages per year include multiple products:
  - 20m Classified Pixels (new addition)
  - Land Parcels (with parcel-level attributes)
  - 25m Rasterised Land Parcels
  - 1km Dominant Cover (1km grid, single-band)
  - 1km Percent Cover (21-band)
  - 1km Percent Aggregate Cover (10-band)
  - 1km Dominant Aggregate Cover
- Datasets provided for:
  - Great Britain (GB): GBOW, GBParcels, GB 25m parcels, GB 1km products
  - Northern Ireland (NI): NI equivalents for each product
- Spatial framework:
  - UKCEH Land Parcel Spatial Framework with minimum mapping unit ~0.5 ha
  - gid: unique parcel identifier; changes mean LCM2017-2019 gid values do not match LCM2015
  - 21 classes are typically dominant within a parcel (with additional parcel attributes)

## Production methods and data lineage
- Bootstrap Training:
  - Automatic training dataset derived from historic UKCEH maps (LCM2015 bootstrap used to train 2017; then majority signal bootstrap planned for 2018–2019).
  - Uses land parcels from LCM2015 with high purity (≥99%) to seed training data.
  - Future bootstrap plans: 2020 from 2017–2019 majority signal; 2021 from 2018–2020 majority signal.
- Random Forest classification:
  - Training samples drawn with replacement to ensure class balance (10,000 samples per class per Classification Scene).
  - Classifier outputs 20m Classified Pixels; a probability per class (Band 2) and the top class (Band 1).
  - Production uses bespoke software integrating Weka, PostGIS, and GDAL.
- Datasets and inputs:
  - Seasonal Composite Images from Sentinel-2 (TOA reflectance, 20m) by season: winter, spring, summer, autumn.
  - Context Rasters (20m) to reduce spectral confusion: terrain (height, aspect, slope), proximity to buildings/roads/sea, freshwater, foreshore, tidal water, woodland masks.
  - Seasonality and context used to form Classification Scenes:
    - GB: 74 overlapping 100x100 km tiles, each yielding a 46-band Classification Scene (36 spectral bands + 10 context bands).
    - NI: single 43-band Classification Scene per year (36 spectral + 7 context).
- Validation and quality checks:
  - Visual checks and formal validation performed (Appendix 4).
  - UK-wide validation against countryside survey, National Forest Inventory, IACS, and interpreted points (22,325 points).
  - Reported accuracies (UK scale): LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%.
  - Validation data are a proxy; some misclassification expected due to class definition differences and temporal scope.

## Data targets, classes, and interpretation
- 21 UKCEH Land Cover Classes (not to be confused with exact BAP Broad Habitats in field, but closely aligned for change detection).
- Appendix 1 provides class notes and detection considerations for upland and coastal habitats, peatlands, and urban vs. suburban distinctions.
- Appendix 2 summarizes BAP Broad Habitats definitions used to frame the class interpretations.
- Appendix 3 provides recommended RGB color mapping for display.

## Outputs and practical use
- 20m Classified Pixels preserve detailed landscape features; 25m Land Parcels offer structured summary; 1km products enable broad-area change assessment.
- Land Parcels include:
  - gid (parcel ID)
  - _hist (histogram of class counts within parcel)
  - _mode (dominant class)
  - _purity (percentage of modal class)
  - _conf (mean per-pixel class membership probability)
  - _stdev (uncertainty of _conf)
  - n (number of 20m pixels in the parcel)
- 1km products summarize parcel data across 1km squares:
  - 1km Percent Cover (21 bands)
  - 1km Percent Aggregate Cover (10 bands)
  - 1km Dominant Cover (single-band)
  - 1km Dominant Aggregate Cover
- Outputs are produced in two regional coordinate frameworks:
  - GB: British National Grid (EPSG: 27700)
  - NI: Irish Grid (EPSG: 29903)

## Practical considerations and limitations
- No manual corrections were applied in this release; classification is fully automatic.
- Some classification errors persist due to spectral similarity, context dependence, and historical class definitions (Appendix 1 notes on specific habitats and detection challenges).
- gid values differ from LCM2015; cross-year parcel comparisons should use gid rather than parcel overlap for 2017–2019 comparisons.
- Some training data sources use historical mappings that required conversions to UKCEH classes; exact class mappings may involve subjective decisions.

## Validation details and Appendix highlights
- Appendix 4: Full confusion matrices and accuracy metrics per year; overall producer and user accuracies by class; discussion of validation limitations.
- Appendix 1: Detailed notes on UKCEH Land Cover Classes and detection nuances for each class.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitat definitions (for context and interpretation).
- Appendix 3: Recommended RGB color recipe for display of UKCEH Land Cover Classes.
- Appendix 5: Full dataset listing for LCM2017, LCM2018, and LCM2019 (dataset names, geographic scope, and status).