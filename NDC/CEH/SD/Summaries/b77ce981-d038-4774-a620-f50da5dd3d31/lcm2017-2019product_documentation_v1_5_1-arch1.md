# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- User guide for three new UKCEH land cover maps: LCM2017, LCM2018 and LCM2019.
- Maps cover 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed to be comparable with earlier maps (LCM2015).
- Production is automatic (Bootstrap Training with Random Forest) to enable annual releases; no manual corrections were applied in these releases.
- Validation indicates maps are of similar quality to LCM2015; accuracy around 79% when compared with UK validation data; ongoing work to improve validation resources.

## Production approach and methodology
- Bootstrap Training: uses historic UKCEH LCM2015 data to automatically sample training observations; selects land parcels with ≥99% purity to bootstrap training data for 2017–2019 maps.
- Random Forest classifier: supervised learning with balanced sampling (10,000 samples per class per training batch); production software integrates Weka, PostGIS and GDAL.
- Classification Scenes and sampling: Sentinel-2 Seasonal Composite Images (TOA reflectance) aggregated into 20 m Classification Scenes, combined with 20 m Context Rasters to form 46-band GB Classification Scenes; 74 overlapping GB scenes classified; Northern Ireland uses a single 43-band scene per year.
- Link to land parcels: 20 m Classified Pixels intersected with the UKCEH Land Parcel Spatial Framework to generate Land Parcels; attributes include hist, mode, purity, conf, stdev, and n 픽셀 count.
- Outputs and data products (see datasets section for details).
- No manual corrections were performed this time to maintain rapid annual production; visual checks and formal validation were undertaken.

## Datasets and outputs
- 20 m Classified Pixels: new addition; RF classification results with per-pixel class and a second band indicating per-pixel confidence (0–100).
- Land Parcels: parcel-level attributes derived from 20 m pixels within the UKCEH Land Parcel Spatial Framework (gid, hist, mode, purity, conf, stdev, n).
- 25 m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) summarising parcel data.
- 1 km Rasters ( GB and NI): 
  - 1 km Percent Cover: 21-band raster of per-class percentages.
  - 1 km Percent Aggregate Cover: 10-band raster for Aggregate Classes.
  - 1 km Dominant Cover: single-band raster of the dominant class per 1 km grid.
  - 1 km Dominant Aggregate Cover: single-band raster for dominant aggregate class.
- Spatial extents and coordinates:
  - Great Britain uses British National Grid (EPSG: 27700); Northern Ireland uses Irish Grid (EPSG: 29903).
  - Datasets are produced per year for GB and NI, totaling 42 datasets across the three years (LCM2017, LCM2018, LCM2019).
- Dataset structure and minor differences from LCM2015 are documented; the 20 m Classified Pixels preserve fine landscape details, while higher-level rasters generalise to coarser grids.

## Satellite data, seasons and contextual information
- Seasonal Composite Images: derived from Google Earth Engine using Sentinel-2 bands across four seasons (winter, spring, summer, autumn); TOA reflectance at 20 m; cloud gaps exist and are represented as nulls.
- Context Rasters (20 m): 10 GB context layers (e.g., height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore, tidal water, woodland) and NI-specific context (urban mask, distance to coast/freshwater/roads).
- Sentinel-2 input and quality: SR (surface reflectance) data were reviewed but TOA data were retained for consistency and due to lack of observed gains in LCM classifications; potential future integration of additional data sources (e.g., Sentinel-1 radar) to fill gaps.

## UKCEH Land Parcel Spatial Framework and class structure
- Land Parcel Spatial Framework used across LCM2017–2019 is unchanged in geometry from LCM2015, but with restructured storage and new indices for faster processing; gid values do not match LCM2015 for parcel-level comparisons, though gid can be used to link across years within 2017–2019.
- Land parcels have a minimum area of ~0.5 ha (the MMU); parcels are intended to represent discrete real-world units (fields, parks, urban areas, etc.) and are designed to support change detection.
- The 20 m Classified Pixels dataset can be summarised by alternative parcel structures if users wish to apply their own boundaries.

## Validation and quality
- Validation data: GB countryside survey 2019, National Forest Inventory, IACS points, and bespoke LCM validation points (22,325 total points).
- Reported accuracy (UK scale, three years):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation points are not absolute truth and were converted to UKCEH classes; results provide best available indicators and will improve with evolving methods and data.
- Validation results include confusion matrices and producer/user accuracies by class (documentAppendix 4 contains full details).

## Class definitions and interpretation
- The 21 UKCEH Land Cover Classes are aligned with UK BAP Broad Habitats in Appendix 1 and 2, with careful labeling and some caveats about detectability with remote sensing (e.g., some BAP classes are designed for field detection).
- Appendix 1 and 2 discuss class-specific detection notes (e.g., woodland types, arable, grassland variants, peatland issues, coastal habitats, urban/suburban differentiation, saline/freshwater separation limits).
- The documentation acknowledges spectral confusion between certain classes and the role of Context Rasters in improving classification.

## Future plans and accessibility
- The producers aim to release a new LCM annually and to expand data inputs (including potential radar and additional optical sources) to improve accuracy and coverage.
- A full list of datasets per year and their metadata is provided in Appendix 5; outputs are designed to be discoverable and usable with accompanying metadata.

## Key takeaways for users
- LCM2017–2019 deliver an automated, annually updated UK-wide land cover map suite with 21 classes, using Bootstrap Training and Random Forest on Sentinel-2 seasonal composites plus 20 m context data.
- Outputs include both per-pixel classifications (with confidence) and aggregated parcel- and grid-based rasters (25 m and 1 km scales) for multi-resolution analyses.
- GB and NI datasets are aligned in concept but use different coordinate systems and spatial frameworks; 42 datasets in total across three years.
- Validation shows around 79% overall accuracy at the national scale, with detailed class-level performance provided in the appendices.