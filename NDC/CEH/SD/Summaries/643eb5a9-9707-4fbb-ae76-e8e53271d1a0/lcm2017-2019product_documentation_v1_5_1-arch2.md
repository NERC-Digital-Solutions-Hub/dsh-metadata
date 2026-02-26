The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Overview
  - Purpose: User guide for three new UKCEH land cover maps (LCM2017, LCM2018, LCM2019) built from geospatial datasets to support consistent monitoring of environmental conditions and change over time.
  - Core aim for analysts: provide a reproducible, standardized data suite to assess environmental health and policy performance across the UK.
  - Coverage and outputs: 21 UKCEH Land Cover Classes mapped across Great Britain and Northern Ireland; outputs include multiple raster and parcel-based products suitable for time-series analysis.

- Data and Class Structure
  - UKCEH Land Cover Classes: 21 classes derived from Biodiversity Action Plan (BAP) Broad Habitats; designed to be comparable with LCM2015 and earlier maps.
  - Relationship to BAP: classes are aligned with UK BAP Broad Habitats, with careful notes on detection via remote sensing and potential ambiguities.
  - Spatial framework: UKCEH Land Parcel Spatial Framework (parcels ~0.5 ha MMU) used to structure and generalize classified pixels into consistent land parcels for change detection.
  - Datasets included (per year, GB and NI):
    - 20m Classified Pixels (GB and NI): two-band rasters; band 1 = most likely class, band 2 = per-pixel confidence (0–100).
    - Land Parcels: parcel-level attributes (gid, hist, mode, purity, conf, stdev, n).
    - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity).
    - 1km rasters: Percent Cover (21-band), Percent Aggregate Cover (10-band), Dominant Cover (1-band), Dominant Aggregate Cover (1-band).
    - Total product set per year: 42 datasets (GB and NI, across the 5 main outputs).
  - Pixel and extent details:
    - 1km grids are used to summarize the 25m parcels; 20m pixels preserve finer features, including narrow patches below 0.5 ha MMU.
    - Great Britain extents use British National Grid; Northern Ireland uses Irish Grid.

- Production Process and Data Quality
  - Classification approach:
    - Bootstrap Training: automatic generation of training data from historic LCMs (primarily LCM2015) to bootstrap classifier for 2017–2019; goal is a robust majority signal over time.
    - Random Forest (RF) classifier: trained with balanced sampling to ensure rarer classes are learned effectively.
    - Sentinel-2 Seasonal Composite Images (TOA reflectance): four seasons (winter, spring, summer, autumn) with nine bands used to form Classification Scenes.
    - Context Rasters (20m): 10 layers providing terrain, proximity to buildings/roads/sea/freshwater, foreshore, tidal water, and woodland masks to reduce spectral confusion.
  - Seasonal classification:
    - Great Britain: 100x100 km classification tiles creating 74 overlapping GB Classification Scenes (46-band scenes when combined with context rasters).
    - Northern Ireland: single 43-band Classification Scene per year (36 spectral bands + 7 context layers).
  - Context and data fusion:
    - Each Classification Scene is combined with 20m Context Rasters to improve discrimination between spectrally similar classes (e.g., coastal vs. inland features).
  - Validation and quality:
    - UK-scale validation using 22,325 points from countryside survey, NFI, IACS, and manual interpretation.
    - Reported overall accuracy: LCM2017 ≈ 78.6%, LCM2018 ≈ 79.6%, LCM2019 ≈ 79.4%.
    - Validation acknowledges differences in class definitions and that manual corrections were not applied in this release (automatic classification only), but still provides a robust quality check.
  - Data governance and consistency:
    - The UK Land Parcel Spatial Framework was updated for performance, resulting in gid changes between LCM2015 and 2017–2019; parcel IDs (gid) do not match exactly with LCM2015, but cross-year comparisons can be performed via parcels using gid.
    - The production workflow emphasizes automation (no manual corrections this time) to enable annual map production, while maintaining validation checks.

- Practical Use for Environmental Analysts
  - Time-series and change detection:
    - A consistent 21-class framework across 2017–2019 enables trend analysis and detection of land cover change, with standardized parcel-based outputs for robust comparisons.
  - Data products and applications:
    - 20m Classified Pixels provide detailed per-pixel information with confidence; 25m Parcels summarize into stable units for long-term monitoring.
    - 1km rasters offer summary statistics (Percent Cover, Percent Aggregate Cover, Dominant Cover) suitable for large-scale analyses and policy reporting.
  - Accessibility and standards:
    - Clear documentation of data structure, band meanings, and attribute definitions (Tables and Appendices describe mapping to BAP habitats and data relationships).
    - Color recipe and visual guidance included to aid consistent map interpretation and visualization.
  - Future trajectory and plans:
    - Aimed for annual LCM releases (LCM2020 planned) using bootstrap from 2017–2019 majority signals; ongoing evaluation of training data sources and potential inclusion of additional data types.
    - Reference to supplementary materials: revised LCM1990 products and UK-wide change datasets for broader historical comparisons.

- Notes on Scope and Limitations
  - Automatic classification vs. manual correction:
    - No manual corrections were applied in this release to enable annual updates; visual checks and formal validations were still conducted.
  - Class detection limitations:
    - Some BAP Broad Habitats remain challenging to distinguish spectrally (e.g., peat-related upland vegetation, bracken vs. acid grassland); ancillary context layers help but do not fully resolve spectral ambiguities.
  - Change detection considerations:
    - The framework is designed to compare like with like over time; some older identifiers or class definitions may not map perfectly to newer naming conventions, hence descriptive consistency is emphasized.

- Appendices and Supporting Information (highlights)
  - Appendix 1 and 2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats, including how certain classes are derived and detected.
  - Appendix 3: Recommended RGB color mapping for displaying UKCEH Land Cover Classes.
  - Appendix 4: Validation details and confusion matrices for LCM2017, LCM2018, and LCM2019 (summary statistics and per-class performance).
  - Appendix 5: Full list of datasets per LCM year (GB and NI) and their respective dataset names and structures.

- Summary for Monitoring and Policy Analysis
  - The three LCMs provide a standardized, annually updated suite of land cover data optimized for monitoring environmental health and land cover change across the UK.
  - The combination of high-detail 20m pixels, parcel-based aggregation, and 1km summary rasters supports analyses at multiple scales, enabling policy performance evaluation, landscape-level assessments, and integration with other environmental datasets.
  - The production framework emphasizes reproducibility, data accessibility, and ongoing methodological evolution to improve accuracy and utility for analysts monitoring the environment.