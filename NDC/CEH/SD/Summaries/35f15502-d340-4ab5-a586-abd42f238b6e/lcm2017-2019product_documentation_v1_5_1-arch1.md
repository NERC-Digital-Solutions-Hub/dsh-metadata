# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- User guide for three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Products are produced automatically using Bootstrap Training and Random Forest (RF) classification to enable rapid, near-annual map updates.
- 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; 21 classes align with legacy classifications; 10 UKCEH Aggregate Classes provided as a generalized schema.
- Aims to support wide-scale, repeatable land cover change monitoring with explicit validation and data provenance.

## Data Content and Class Mapping
- 21 UKCEH Land Cover Classes (matching LCM2015/2007 lineage; not identical to BAP but closely aligned for comparability).
- Datasets per year include:
  - 20m Classified Pixels (new in 2017–2019): RF-derived per-pixel class with a second band indicating classification confidence (0–100).
  - Land Parcels: parcel-level attributes derived from the UKCEH Land Parcel Spatial Framework (gid, hist, mode, purity, conf, stdev, n; with updated attribute naming).
  - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) summarising parcel data at 25m resolution.
  - 1km Raster datasets: 
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
- Geographic coverage and coordinate systems:
  - Great Britain (GB): EPSG 27700 (British National Grid)
  - Northern Ireland (NI): EPSG 29903 (TM75 Irish Grid)
  - Data duplicated for each year, totaling 42 primary datasets across GB and NI.
- Data structure:
  - Classification Scenes: GB uses 100x100 km tiles with 36-band Seasonal Composite Images plus 20m Context Rasters to form 46-band GB Classification Scenes; NI uses a single 43-band scene per year (36 spectral + 7 context layers).
  - UKCEH Land Parcel Spatial Framework: unchanged parcel geometries from LCM2015 with indexing/ storage updates; gid identifiers differ year-to-year, but gid can be used for cross-year parcel comparisons (apart from exact matching with LCM2015 parcels).

## Production Approach and Methodology
- Seasonal Composite Images:
  - Sentinel-2 TOA reflectance media across four seasons (winter, spring, summer, autumn) at 20m resolution.
  - Nine Sentinel-2 bands used; seasonal gaps due to cloud are accepted and handled by the classifier.
  - SR (Surface Reflectance) data via Google Earth Engine were considered but TOA performed similarly for current class definitions; SR may be explored for finer thematic detail in the future.
- Contextual Information:
  - 20m Context Rasters to reduce spectral confusion (e.g., height, aspect, slope; distances to buildings, roads, sea, freshwater; foreshore and tidal masks; woodland masks).
- Bootstrap Training:
  - Fully automatic training using Bootstrap Training, sampling from historic maps (primarily LCM2015) to train the RF classifier.
  - For each year, a bootstrap from Land Parcel Training data with high purity (>= 99%) from LCM2015 used to sample pixels for RF training (10,000 samples per class; balanced learning across classes).
  - Future bootstrap plans anticipate using majority signals across multiple years (e.g., 2017–2019 for LCM2020; 2018–2020 for 2021).
- Classification and Validation:
  - RF classifier implemented with open source tools (WEKA, PostGIS, GDAL) integrated into UKCEH production software.
  - Validation performed against UK-scale data (GB countryside survey 2019, open-source National Forest Inventory, IACS, and bespoke validation points; total of 22,325 points).
  - Reported overall accuracy: LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%.
  - Validation notes emphasize that accuracy is an indicator rather than an absolute truth, with subjectivity in class conversions from validation sources.

## Spatial Framework and Data Details
- UK Land Parcel Spatial Framework:
  - About 0.5 ha minimum parcel size; designed to reduce classification noise and enable change detection.
  - Parcel identifiers (gid) do not exactly match LCM2015 parcels; cross-year parcel comparisons should use gid within the updated framework.
  - Parcel attributes updated to align with current production uses; main attributes include _hist, _mode, _purity, _conf, _stdev, _n.
- Dataset Specifics and Evolution Since LCM2015:
  - 20m Classified Pixels retained as a high-detail dataset; un-generalised to preserve narrow features below MMU.
  - Land Parcels provide rich per-parcel statistics for downstream analyses.
  - 25m Rasterised Land Parcels provide compact, parcel-averaged summaries for mapping and analysis at coarser scales.
  - 1km rasters summarize parcel data to enable efficient regional or national-scale analyses.
- Class Descriptions and Note on Detection:
  - Appendix and notes detail how each UKCEH Land Cover Class relates to BAP Broad Habitats, including known difficulties in remote sensing-based separation (e.g., Bracken vs Acid Grassland; upland peatland vegetation; Saltwater vs Freshwater in coastal zones).
  - Some classes (e.g., Linear Features) are not mapped as separate UKCEH Land Cover Classes due to spectral limitations; these features may appear in higher-resolution datasets or future iterations.
- Visualization and Colour Coding:
  - Appendix 3 provides RGB color recipes for displaying each class (useful for map authors and visualization).

## Validation, Quality and Limitations
- Validation Conclusions:
  - Approximate overall accuracies around 79% across 2017–2019; close to the 80% target for many broad habitat classes.
  - Validation points come from multiple sources with potential mismatches in class definitions; conversions introduce some subjectivity.
- Known Limitations:
  - Some classes remain challenging to separate spectrally (e.g., Saltwater vs Freshwater; certain upland and peatland vegetation types).
  - Coastal and aquatic zones are subject to context-layer influences, with occasional misclassification in dynamic tidal environments.
  - The MMU and parcel-based framework can affect detection of very small or fragmented habitats.

## Usage, Access and Future Plans
- Documentation and Appendices:
  - Appendix 4 provides full validation tables and detailed class-wise performance (per-class confusion matrices and accuracy metrics).
  - Appendix 5 lists complete datasets per year and platform-specific details.
- Future Plans:
  - Annual LCM releases continued; 2020 map will be generated using bootstrap from the 2017–2019 majority signal, with 2021 using 2018–2020 majority signal.
  - Ongoing evaluation of new data sources (e.g., Sentinel-1 radar, alternative optical sources) and potential refinements to the training sets and class definitions.

## Key Takeaways for Analysts
- The three maps deliver a consistent, automatic, year-on-year land cover dataset across GB and NI, with detailed 20m pixel data and parcel-level summarization to support change detection and modelling.
- The production pipeline emphasizes reproducibility, transparency of inputs (Sentinel-2 seasonal composites, context rasters), and explicit validation to ~80% accuracy at national scale.
- Users should consider class crosswalks and potential validation caveats when comparing with older maps (LCM2015/LCM2007) or applying to local-scale decision-making, especially in coastal, upland, peatland, and urban-suburban interfaces.
- Access to 42 primary datasets (three years x GB/NI x dataset types) enables both high-resolution analyses and aggregated, policy-relevant assessments, with clear metadata and provenance controls.