# The UKCEH Land Cover Maps for 2017, 2018 and 2019

## Purpose and scope
- UKCEH releases three new national land cover maps: LCM2017, LCM2018, and LCM2019.
- Land cover is represented by 21 UKCEH Land Cover Classes based on BAP Broad Habitats; designed to be compatible with LCM2015 methodologies and prior maps (LCM2007, LCM2000).
- Maps are produced automatically using Bootstrap Training plus a Random Forest classifier; Sentinel-2 Seasonal Composite Images (seasonal reflectance) are used to generate Classification Scenes.
- No manual corrections were applied in this release; visual checks and formal validation were conducted, indicating similar quality to LCM2015.
- Annual updates are planned going forward.

## Data content and structure
- Product suite comprises 42 datasets (3 years × GB & NI) with a consistent data structure per year.
- Core datasets:
  - 20m Classified Pixels: per-pixel classification with a confidence metric.
  - Land Parcels: 20m pixel classifications summarised within land parcel units; rich parcel-level attributes.
  - 25m Rasterised Land Parcels: aggregated parcel data at 25m resolution (3-band raster).
  - 1km Dominant Cover: 1km grid with a single dominant class per cell.
  - 1km Percent Cover: 21-band raster showing % cover per class within 1km cells.
  - 1km Percent Aggregate Cover: 10-band raster showing % cover of aggregated classes.
  - 1km Dominant Aggregate Cover: 1-band raster showing dominant aggregate class per 1km cell.
- Outputs provided for Great Britain (GB) and Northern Ireland (NI) with respective coordinate systems.

## Production methodology
- Bootstrap Training
  - Automatic, self-starting training using historic maps (Bootstrapping from LCM2015, which was itself bootstrap-derived from 1990–2007 data plus manual observations).
  - Training samples drawn from UKCEH Land Parcels with high purity (≥99%) to create robust spectral training for the RF classifier.
  - Future plans: bootstrap updates using majority signals from multiple years (e.g., 2017–2019, then 2018–2020).
- Random Forest classification
  - RF classifier trained on balanced samples (10,000 per class) to classify the 20m Classified Pixels.
  - Classifier is implemented with bespoke UKCEH software integrating WEKA, PostGIS, and GDAL.
- Seasonal inputs and context
  - Seasonal Composite Images: Sentinel-2 median TOA reflectance per season (winter, spring, summer, autumn), 20m resolution.
  - Context Rasters (20m): terrain (height, aspect, slope) and proximity masks (buildings, roads, coast, freshwater, foreshore, woodland) to reduce spectral confusion.
  - Classification Scenes: GB uses 100x100 km tiles producing 46-band scenes; NI uses a single 43-band scene per year.
- Data framework and parcel system
  - UKCEH Land Parcel Spatial Framework returns parcels ~0.5 ha MMU; parcels are consistent with LCM2015 but gid values differ, complicating cross-map parcel ID comparisons.
  - 20m Classified Pixels are summarized into Land Parcels with attributes detailing class composition, modal class, confidence, and distribution.
- Visualization and interpretation
  - Appendix materials provide color recipes for display and notes on class definitions and potential spectral confusion.

## Dataset specifics and data products
- 20m Classified Pixels
  - Per-pixel RF classification with band 1 = most likely class, band 2 = per-pixel confidence (0–100).
  - Maintains detailed landscape features not captured in parcel-based summaries.
- Land Parcels
  - Attributes include gid, _hist (histogram of class frequencies within parcel), _mode (dominant class), _purity (percentage of modal class), _conf (mean class membership probability), _stdev (uncertainty), and _n (number of 20m pixels).
  - Some attribute name changes compared with LCM2015 to align with production software.
- 25m Rasterised Land Parcels
  - 3-band rasters: band 1 = modal class (_mode), band 2 = confidence (_conf), band 3 = purity (_purity).
  - Provides a condensed representation of parcel-level data at 25m resolution.
- 1km Datasets
  - 1km Percent Cover: 21-band raster showing percentage cover per class per 1km cell.
  - 1km Percent Aggregate Cover: 10-band raster showing aggregate class percentages per 1km.
  - 1km Dominant Cover: single-band raster of the dominant class per 1km cell.
  - 1km Dominant Aggregate Cover: single-band raster of the dominant aggregate class per 1km cell.
- Perspectives for users
  - 20m Classified Pixels retain finer landscape detail; 1km products support broader-scale analyses; 25m rasterised parcels offer a balance between detail and handling efficiency.

## Context and data quality
- Validation
  - UK-scale validation against GB countryside survey 2019 data, National Forest Inventory data, IACS, and expert interpretation points.
  - Validation dataset: 22,325 points; LCM2017 accuracy 78.6%, LCM2018 accuracy 79.6%, LCM2019 accuracy 79.4%.
  - Validation figures reflect currency and class-mapping differences; results are indicative rather than absolute truth.
- Data quality notes
  - Automatic classification with alignment to UKCEH Class schemes; some spectral confusion remains between similar habitats.
  - No manual corrections applied this release; visual checks and formal validation performed to ensure reliability comparable to prior products.
- Spatial and temporal scope
  - UK-wide coverage on a coast-to-coast basis for GB; NI mapping determined by a single primary classification scene per year.
  - Annual map production aims to capture land cover change with high fidelity, leveraging higher temporal resolution of Sentinel-2 inputs.

## Data usage and limitations
- The 21-class scheme remains close to BAP Broad Habitats for continuity; some BAP categories were adapted to remote-sensing detection realities.
- Parcel-based comparison across years requires caution due to gid changes; spatial overlap is recommended for cross-year comparisons rather than relying on parcel IDs.
- The dataset design prioritizes self-serve data products and change-detection workflows, suitable for national-scale monitoring as well as local-scale analyses in policy or planning contexts.

## Appendices and additional resources
- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats definitions; guidance on class derivations and detection considerations.
- Appendix 3: Color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Full validation results and confusion matrices (for reference) including producer’s and user’s accuracies per class.
- Appendix 5: Full list of datasets included in LCM2017, LCM2018, and LCM2019.
- References to foundational methods and related work (e.g., Breiman 2001 on Random Forests; Carrasco et al. 2019; Jackson 2000; Morton et al. 2011).