# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide accompanying the release of three UKCEH Land Cover Maps (LCMs): 2017, 2018, and 2019.
  - Describes data content, production processes, validation, decisions behind production, and future plans to help users apply UKCEH LCM data effectively.

- Data content and class structure
  - 21 UKCEH Land Cover Classes used (based on Biodiversity Action Plan Broad Habitats), with a near-one-to-one relationship to earlier maps and Appendix notes clarifying terminology.
  - Also provides UKCEH Aggregate Classes (Table 2) for generalized reporting.
  - Product suite duplicates for each year (GB and NI variants), with a total of 42 datasets across the three years.
  - Main data products:
    - 20m Classified Pixels (GB and NI): 2-band rasters per pixel; band 1 = most likely class, band 2 = class membership probability (0–100).
    - Land Parcels: vector-style parcel attributes derived from the 20m dataset (with fields such as _hist, _mode, _purity, _conf, _stdev, _n). gid remains a stable identifier, but may not match LCM2015 parcels.
    - 25m Rasterised Land Parcels: 3-band rasters (band 1 = modal class, band 2 = conf, band 3 = purity).
    - 1km Percent Cover (21-band): per-1km grid.
    - 1km Percent Aggregate Cover (10-band): per-1km grid.
    - 1km Dominant Cover (1-band) and 1km Dominant Aggregate Cover (1-band).
  - Spatial references and extents
    - Great Britain: GB British National Grid (EPSG: 27700), extents defined for GB plotting.
    - Northern Ireland: NI Irish Grid (EPSG: 29903), extents defined for NI plotting.
    - Pixel sizes: 20m (classified pixels), 25m (land parcels), 1km (percent/aggregate/dominant products).
  - Classification framework and workflow
    - Automatic classification using Bootstrap Training with a Random Forest (RF) classifier.
    - Sentinel-2 Seasonal Composite Images (four seasons) are created per year, combined with 20m Context Rasters to form Classification Scenes.
    - 100x100 km GB Classification Scenes (36-band Seasonal Composite Images + 20m Context Layers) used to build 74 overlapping scenes; NI uses a single 43-band scene per year.
    - No manual corrections were performed for LCM2017-2019 to enable rapid annual updates; visual checks and formal validation were conducted.
    - All data products are derived automatically from the scenes, with ongoing exploration of additional satellite inputs for future improvements.

- Production methodology and technical details
  - Bootstrap Training
    - Training data sampled from UKCEH LCM2015 with >= 99% purity; used to bootstrap the classifier for 2017–2019.
    - Ensures a large, majority-signal training set to stabilize RF learning across years.
    - Future plans: bootstrap from 2017–2019 majority signal for subsequent maps.
  - Random Forest classification
    - RF classifier trained on balanced samples (10,000 pixels per class per training cycle) to mitigate dominance by common classes.
    - Production software integrates WEKA, PostGIS, and GDAL; open-source stack.
  - Context and seasonal inputs
    - Seasonal Composite Images built from Sentinel-2 TOA reflectance; TOA selected over Surface Reflectance (SR) after evaluation.
    - 20m Context Rasters include terrain and proximity features (height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore and tidal masks, woodland mask) to reduce spectral confusion.
  - Land Parcel Spatial Framework
    - Framework follows LCM2007 lineage and LCM2015 adjustments; parcels have a 0.5 ha minimum mapping unit.
    - gid identifies parcels but does not match LCM2015 identifiers; comparison across years should use spatial overlap rather than gid.
  - Classification Scene concept
    - GB uses multiple overlapping tiles (74 scenes) to ensure training sample balance; NI uses a single scene per year.
  - Validation and quality
    - UK-scale validation using 22,325 points from countryside survey 2019, National Forest Inventory, IACS, and interpretation points.
    - Reported accuracies (across the three years on the same validation set):
      - LCM2017: 78.6%
      - LCM2018: 79.6%
      - LCM2019: 79.4%
    - Validation figures are indicative; classes and mappings may differ slightly from validation sources; full details in Appendix 4.

- Data quality, limitations, and considerations
  - Automated production means no manual region-wide corrections this year; errors are generally random across space.
  - Some upland peatland and peat vegetation classes are challenging to distinguish spectrally; persistence of misclassifications may occur for certain classes (e.g., bog, heather, peatland mosaics).
  - Saltwater vs freshwater separation relies on coastal context rasters; some tidal/coastal edge confusions may occur.
  - The 20m Classified Pixels dataset provides the most detailed representation, while 25m and 1km products generalize to coarser scales.
  - A note on data provenance: Appendix 4 provides detailed confusion matrices and producer’s/user’s accuracies by year and class.

- Future plans and ongoing improvements
  - Move toward annual LCM releases with potential expansion of input data (e.g., including Sentinel-1 SAR data) and exploration of gap-filling approaches for complete seasonal coverage.
  - Ongoing assessment of Land Parcel Spatial Framework refinements and alternative parcel-based aggregation for change detection.
  - Continued validation and refinement of class definitions and training data to improve cross-year comparability and accuracy.

- Accessibility and appendices
  - Appendix highlights
    - Appendix 1: Notes on UKCEH Land Cover Classes (class definitions and detection nuances).
    - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and mappings.
    - Appendix 3: Recommended RGB color recipes for displaying UKCEH Land Cover Classes.
    - Appendix 4: Validation details and full confusion matrices for LCM2017, LCM2018, and LCM2019.
    - Appendix 5: Full dataset lists and structure per year.
  - Data availability and structure
    - 42 datasets total across three years (GB and NI variants for each year), with explicit data products and attribute schemas described in the main text and Appendix 5.

- Practical takeaways for data leadership
  - The UKCEH LCM suite provides a consistent, automated, annual map series with rich multi-resolution outputs (20m pixel classifications, parcel-level attributes, 1km summaries).
  - Bootstrap Training and RF classification enable rapid production while maintaining nationally comparable outputs; validation suggests ~80% overall accuracy across years.
  - Clear documentation of data structures, coordinate systems, and production workflows supports governance, discovery, and integration into data strategy and policy work.
  - Users should be aware of gid changes and the necessity to compare across years via spatial overlap rather than parcel identifiers; cross-year analyses benefit from the 20m Classified Pixels as the most detailed dataset.