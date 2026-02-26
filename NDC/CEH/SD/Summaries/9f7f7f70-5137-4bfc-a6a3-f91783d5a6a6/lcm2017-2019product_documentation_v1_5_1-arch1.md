# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Aim
- Release three UKCEH land cover maps (LCM2017, LCM2018, LCM2019) with 21 UKCEH Land Cover Classes, aligned with prior maps.
- Produce maps automatically (Bootstrap Training + Random Forest) to enable annual updates.
- Achieve validation quality comparable to LCM2015; avoid manual corrections to maintain rapid, annual production.

## Data products and structure
- Maps describe 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) and a near-identical lineage to earlier LCMs; a separate UKCEH Aggregate class set (10 classes) is also provided.
- Each year yields multiple products (20m classified pixels, land parcels, 25m rasterised parcels, 1km percent/aggregate/dominant datasets), totaling 42 datasets across three years (GB + NI per year).
- Classification results are accompanied by metadata and spatial framework information to enable cross-year comparisons.

## Input data and imagery
- Sentinel-2 Seasonal Composite Images (TOA reflectance) generated in Google Earth Engine for four seasons; medians per season form the basis for classification.
- Seasonal data may have cloud gaps; the Random Forest classifier tolerates partially incomplete spectral information.
- Contextual information (20m Context Rasters) aids disambiguation of spectrally similar classes (e.g., urban proximity, coast, terrain).

## Classification methodology
- Bootstrap Training: automatic, data-driven sampling from historic maps (primarily LCM2015) to train classifiers for newer maps; selects training observations from existing maps to bootstrap new maps.
- Training data: from UKCEH LCM2015 parcels with high purity (≥99%); ensures majority-signal learning for subsequent maps.
- Random Forest: custom RF pipeline (with balanced sampling, 10,000 samples per class per bag) using open-source tools (WEKA, PostGIS, GDAL).
- Outputs:
  - 20m Classified Pixels: new 2-band raster per location; band1 = most probable class, band2 = per-pixel class membership probability (0–100) for confidence.
  - Land Parcels: attributes per parcel (gid, hist, mode, purity, conf, stdev, n); some attribute names updated from LCM2015.
  - 25m Rasterised Land Parcels: 3-band raster (mode, conf, purity).
  - 1km rasters: 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band), 1km Dominant Aggregate Cover (1 band).

## Datasets, formats, and extents
- Great Britain: GB National Grid (EPSG 27700); Northern Ireland: Irish Grid (EPSG 29903).
- 20m Classified Pixels: primary fine-detail dataset (GB + NI per year).
- Land Parcels: linked to UKCEH Land Parcel Spatial Framework; MMU ~0.5 ha; parcel-centric summaries and diagnostic attributes.
- 25m Rasterised Land Parcels: parcel-level summaries at 25m grid.
- 1km rasters: coarse-scale summaries (percent, dominant) derived by aggregating 25m parcels within 1km squares.
- Spatial organization: GB uses 100x100 km tile system to select and train Seasonal Composite Images; NI uses a single 43-band scene per year for its land mass.
- The UKCEH Land Parcel Spatial Framework remains structurally the same as LCM2015, but parcel identifiers (gid) have been reordered; cross-year parcel ID matching relies on gid within the new framework.

## Production framework and data management
- Bootstrap Training: leverages historic maps for large-scale, automatic training data; intended to adapt to changing land cover dynamics with short update intervals.
- Classification Scenes: GB uses 74 overlapping 100x100 km tiles; NI uses a single tailored scene per year; overlapping regions may yield slight variations, resolved by visual precedence in final cut.
- The framework emphasizes enabling users to summarize or reframe land cover with their own parcel structures if desired.

## Validation and accuracy
- Validation dataset: 22,325 points from GB countryside survey, open Forest Inventory data, IACS, and manual interpretation.
- Reported overall accuracy (UK-wide, 21-class): 
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes: the same validation points were used for all three products; accuracy is a robust indicator but not absolute truth; class mappings between validation data and UKCEH classes required interpretation.

## Notable changes and considerations
- No manual corrections were performed for LCM2017–2019 to enable annual production; errors are expected to be randomly distributed over time.
- Gid values for parcels do not match LCM2015; cross-map comparisons should use gid within the new Land Parcel Spatial Framework.
- 20m Classified Pixels preserve finer landscape features that are blurred in 25m and parcel-based summaries.
- The description and definitions of UKCEH Land Cover Classes are closely aligned with UK BAP Broad Habitats but are mapped for remote sensing; Appendix materials provide detailed relationships and guidance.

## Appendices and guidance
- Appendix 1–2: definitions and notes on UKCEH Land Cover Classes and BAP Broad Habitats; guidance on interpretation and potential confusion.
- Appendix 3: recommended RGB color mappings for displaying UKCEH Land Cover Classes.
- Appendix 4: validation confusion matrices and related statistics (provided as full detail in the document).
- Appendix 5: full list of datasets per year and their specific dataset names and holdings.

## Availability and future directions
- Datasets are organized for annual release with continued ambition to publish LCMs annually (LCM2020 and beyond discussed in Bootstrap Training context).
- Future enhancements may include expanding input data sources (e.g., additional satellite sources or radar data) to improve gap-filling and accuracy, especially in challenging regions or seasons.