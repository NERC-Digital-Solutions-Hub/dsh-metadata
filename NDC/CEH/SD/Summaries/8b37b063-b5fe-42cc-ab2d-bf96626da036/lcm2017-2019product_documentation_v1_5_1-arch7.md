# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- Release accompanying three new UKCEH LCMs: LCM2017, LCM2018 and LCM2019.
- Maps use 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed for cross-year change detection.
- Production is automatic, using Bootstrap Training with a Random Forest classifier; Sentinel-2 Seasonal Composite Images (TOA) processed in Google Earth Engine; 20m Classified Pixels plus derived parcel-based products.
- Aim: enable rapid, nationwide mapping with annually updated products.

## Data products and formats
- Total datasets: 42 (GB and NI for each year) across multiple scales.
- 20m Classified Pixels (GB and NI): 2-band 8-bit rasters per year; band 1 = most-likely class, band 2 = classification confidence (0–100).
- Land Parcels: fixed spatial framework; parcel-level attributes; 0.5 ha minimum parcel size (MMU).
  - gid: unique parcel ID (not stable across 2015 vs 2017–2019).
  - _hist: histogram of class frequencies within parcel (tuples left:right).
  - _mode: dominant class; _purity: share of dominant class (0–100); _conf: mean class membership probability (0–100); _stdev: std dev of _conf; _n: number of 20m pixels in parcel.
- 25m Rasterised Land Parcels: 3-band rasters with bands for _mode, _conf, _purity.
- 1km Rasters (GB and NI):
  - 1km Percent Cover: 21-band, 8-bit (per-class percentage).
  - 1km Percent Aggregate Cover: 10-band, 8-bit (aggregate classes).
  - 1km Dominant Cover: 1-band (dominant class).
  - 1km Dominant Aggregate Cover: 1-band (dominant aggregate class).
- Coordinate systems and extents:
  - GB: Great Britain, British National Grid (EPSG 27700).
  - NI: Northern Ireland, Irish Grid (EPSG 29903).
- Pixel and band details:
  - 20m Classified Pixels: core 21-class product; 2 bands.
  - 25m Land Parcels: 3 bands; parcel-level attributes.
  - 1km rasters: multiple bands as above.

## Production approach and workflow
- Bootstrap Training: automatic training data sourced from UKCEH2015 (greater-than-99% purity parcels) to bootstrap 2017–2019; creates spectral training observations from historic maps.
- Random Forest classification: large-scale RF classifier trained with 10,000 samples per class per Classification Scene; balanced learning to reduce bias toward common classes.
- Classification Scenes and tiling:
  - Great Britain: 100x100 km tiles; 36-band Seasonal Composite Images combined with 20m Context Rasters to create 46-band GB Classification Scenes; 74 overlapping scenes classified independently.
  - Northern Ireland: single 43-band Classification Scene per year.
- Seasonal composites: four-season Sentinel-2 TOA-based medians; some cloud gaps (treated as nulls); algorithm tolerates gaps; future exploration of SAR or alternative sources.
- Context Rasters (20m): include terrain (Height, Aspect, Slope) and proximity masks (buildings, roads, sea, freshwater, foreshore, tidal water, woodland).
- UK Land Parcel Spatial Framework: unchanged geometry from LCM2015 (min MMU ~0.5 ha); gids differ from LCM2015; designed to reduce noise and support time-series comparisons.
- Manual corrections: none applied in these years to preserve rapid production; visual checks and formal validations performed.

## Spatial framework and geographic coverage
- UK-wide coverage for GB and NI; data produced in parallel for 2017–2019.
- Land Parcels framework provides a stable structure for time-series analyses; however, cross-year parcel IDs (gid) do not match LCM2015; gid-based comparisons are possible only between 2017–2019.

## Validation and accuracy
- Validation against GB countryside survey 2019, National Forest Inventory, IACS, and bespoke LCM validation points (22,325 points).
- Reported overall accuracy (UK scale):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation data are not absolute truth; acknowledged uncertainties due to class mappings between historical datasets and current UKCEH classes.
- Appendix 4 contains full confusion matrices and accompanying accuracy metrics.

## Practical guidance for GIS Specialists
- Data are map-centric and suitable for national-scale GIS analyses and change detection across years.
- Use 20m Classified Pixels for high-detail mapping; aggregate to 25m parcels or 1km rasters for summary analyses.
- When comparing years, use gid for 2017–2019 parcel-level comparisons; cross-year comparison with LCM2015 parcel IDs is not possible.
- Familiarize with the 21 UKCEH Land Cover Classes and their relationships to BAP Broad Habitats ( Appendix 1 & 2 ).
- Refer to Appendix 3 for RGB color recipes when visualizing classes.
- Access through Appendix 5: full list of datasets per year and product type.
- Expect occasional spectral confusion among grassland and upland habitats; context rasters help reduce misclassification (see Appendix 1 notes).
- Seasonal and contextual data inclusion reduces spectral confusion and enables robust classification without manual gap-filling.

## Appendices (highlights)
- Appendix 1: Notes on UKCEH Land Cover Classes and BAP Broad Habitats; guidance on interpretation and common spectral confusions.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and crosswalks).
- Appendix 3: Recommended RGB color mappings for display of UKCEH Land Cover Classes.
- Appendix 4: Validation matrices (confusion matrices, producer’s and user’s accuracies) for LCM2017–2019.
- Appendix 5: Full dataset list by year and dataset type (GB and NI).