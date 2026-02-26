# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- Three new UKCEH land cover maps released: LCM2017, LCM2018, and LCM2019.
- Map 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; aligns with LCM2015 framework.
- Production is fully automatic, using Bootstrap Training with a Random Forest classifier; aims for annual updates.
- No manual corrections in this release; visual checks and formal validation indicate quality similar to LCM2015.
- Outputs include high-detail 20m data products and aggregated 1km products; 42 datasets in total (GB and NI, three years).

## Data Products and Structure
- 20m Classified Pixels: new 20m RF classification results with two bands per pixel (class label, and confidence/probability 0–100); preserves fine landscape detail.
- Land Parcels: 20m Classified Pixels intersected with the UKCEH Land Parcel Spatial Framework; parcel-level attributes include:
  - gid (parcel ID), _hist (histogram of class counts), _mode (dominant class), _purity (percent), _conf (mean per-pixel class confidence 0–100), _stdev, _n (number of pixels).
  - Note: new attribute names differ from LCM2015; gid values differ from LCM2015 for cross-year comparisons.
- 25m Rasterised Land Parcels: three-band raster (band1 _mode, band2 _conf, band3 _purity) derived from Land Parcels.
- 1km Raster Datasets (GB and NI summarized):
  - 1km Percent Cover: 21-band raster (percentage cover per UKCEH Land Cover Class per 1km).
  - 1km Percent Aggregate Cover: 10-band raster (aggregate-class percentages per 1km).
  - 1km Dominant Cover: single-band raster (dominant class per 1km).
  - 1km Dominant Aggregate Cover: single-band raster (dominant aggregate class per 1km).
- Dataset scope: 42 datasets total (GB and NI, across 2017–2019).

## Methodology and Data Flow
- Seasonal Composite Images: Sentinel-2 seasonal composites (TOA reflectance) at 20m used to form Classification Scenes; four seasons (Winter, Spring, Summer, Autumn).
- Context Rasters: 20m context layers (terrain, proximity to buildings/roads/sea, etc.) reduce spectral confusion when classifying.
- Classification Scenes:
  - GB: 74 overlapping 100x100 km tiles used to create 36-band Seasonal Composite Images; combined with context rasters to yield 46-band GB Classification Scenes; total of 74 scenes with overlaps to balance training data.
  - NI: single 43-band 2017/2018/2019 classification scene per year for NI, using minimum bounding rectangle of NI land mass.
- Bootstrap Training: automatic bootstrap from UKCEH LCM2015; uses majority signal over time (2017–2019 planned) to train RF classifier; sample balance ensures rare classes are well represented.
- UKCEH Land Parcel Spatial Framework: framework unchanged in area (≈0.5 ha MMU) but with reordering and new indices; gid differs from LCM2015; enables temporal comparison via parcel-based change detection.
- Validation:
  - UK-scale validation against GB countryside survey 2019 data, National Forest Inventory, IACS, and manual validation points (22,325 points total).
  - Reported overall accuracy: LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%.
  - Validation discussed with caveats: currency of points, mapping between validation classes and UKCEH classes, and subjectivity in conversions.
- Data Source Considerations:
  - Google Earth Engine provides Sentinel-2 data as land surface reflectance, but TOA was used as SR did not improve classification for these classes; potential future expansion with other data sources (e.g., Sentinel-1 SAR).

## Data Quality, Access, and Updates
- Data quality checks include visual inspection and formal validation; no manual corrections were applied this year.
- Outputs are designed for self-service and integration into dashboards, reports, or GIS workflows; 20m classified pixels preserve spatial detail, while 1km rasters provide higher-level summaries.
- Annual update plan: UKCEH aims to release a new LCM every year; future improvements may include filling seasonal gaps with alternative optical or SAR sources.
- GID and dataset alignment:
  - Gids are stable within a year but do not cross-match with LCM2015 parcel IDs; use gid for cross-year (2017–2019) parcel comparisons.
  - 1km and 25m products provide convenient multi-scale views (detailed 20m data plus 1km summaries).

## Class Definitions and Documentation
- 21 UKCEH Land Cover Classes derived from UK BAP Broad Habitats; maintained to preserve consistency for change detection (with caveats about spectral detection limits).
- Appendices provide:
  - Detailed UK BAP Broad Habitat definitions and how they map to UKCEH classes.
  - Color recipes for display of classes.
  - Validation confusion matrices and producer/user accuracy metrics.
  - Notes on key classes (e.g., woodland, arable, grasslands, peatlands, coastal habitats).
- Users should consult the Appendix for nuanced interpretation and potential class-confusion guidance.

## Practical Guidance for Data Support
- Data usage:
  - Use 20m Classified Pixels for detailed, location-specific analyses; leverage _mode and _conf to assess classification certainty.
  - Use Land Parcels attributes (_hist, _mode, _purity, _conf) to summarize parcel-level land cover distributions and confidence.
  - Use 1km Percent/Aggregate and Dominant datasets for regional assessments and trend analyses at coarser scales.
- Cross-year comparison:
  - Use gid to compare parcels between 2017–2019; be aware of gid changes relative to LCM2015.
  - Acknowledge that no manual patch corrections were applied; automated classifications reflect temporal changes and data quality variability.
- Caveats:
  - Some small or spectrally similar classes may be confounded (e.g., certain grassland types, peatland vs. acid grassland).
  - Seasonal gaps due to cloud are handled by the classifier but may affect some locations; future work may mitigate with additional data sources.
- Access and documentation:
  - Datasets provided in GB and NI extents with corresponding coordinate systems (GB: EPSG:27700; NI: EPSG:29903).
  - Appendix 5 lists the full dataset inventory and naming conventions.

## Summary for Data Support Practitioners
- The UKCEH Land Cover Maps for 2017, 2018 and 2019 deliver 21-class, UK-wide land cover maps produced automatically via Bootstrap Training and Random Forest, with year-to-year outputs designed for change detection.
- Products span detailed 20m rasters (Classified Pixels and Land Parcels) and multi-scale 1km rasters (Percent Cover, Percent Aggregate Cover, Dominant Cover) for GB and NI.
- The data framework emphasizes reproducibility, traceable lineage, and practical utility for policy and planning contexts, while acknowledging limitations in manual corrections and class separability.
- Validation shows ~80% overall accuracy across years, reinforcing suitability for broad-scale insights and trend analysis, with detailed guidance available in appendices for interpreting class results and confusion patterns.