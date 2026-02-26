# The UKCEH Land Cover Map for 2021

## Overview
- UKCEH LCM2021 is the ninth UK land cover map, produced annually using automated methods.
- Product consists of six datasets (GB and NI combined): three datasets per region
  - 10 m Classified Pixel dataset
  - Land Parcel dataset (based on UKCEH Land Parcel Spatial Framework)
  - 25 m Rasterised Land Parcel dataset
- Also provides 1 km raster products summarising the 25 m data (dominant class and percentage cover for both UKCEH classes and aggregates).
- Overall formal validation accuracy: 82.6%.

## Datasets and Data Formats
- Datasets (UKCEH LCM2021):
  - 10 m Classified Pixel dataset (GB and NI)
  - Land Parcel dataset (GB and NI)
  - 25 m Rasterised Land Parcel dataset (GB and NI)
  - 1 km Dominant cover (UKCEH classes) — 1 band
  - 1 km Dominant cover (UKCEH Aggregate classes) — 1 band
  - 1 km Percentage cover (21 bands for classes; 10 bands for aggregates)
- Coordinate systems and extents:
  - Great Britain: British National Grid (EPSG: 27700)
  - Northern Ireland: Irish Grid (TM75, EPSG: 29903)
  - GB extent: 0 to 700000 E, 0 to 1300000 N; NI extent truncated to Irish grid
- 10 m vs 25 m:
  - 10 m: classification at pixel level; not generalized by the Land Parcel Framework to preserve fine features
  - 25 m: rasterised Land Parcel products; three-band rasters: dominant class (_mode), mean confidence (_conf), and purity (_purity)
- Dataset metadata: per-Parcel attributes include gid, _hist, _mode, _purity, _conf, _stdev, _agg, _n, etc.

## Data Production and Methodology
- Land cover classes: 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats; designed for satellite mapping but aligned to BAP concepts with careful notes on differences.
- Seasonal information:
  - Seasonal Composite Images: Sentinel-2 data (resampled to 10 m) across four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) using bands 2,3,4,5,6,7,8,8A,11,12; occasional cloud gaps are handled without manual gap filling.
  - Context Rasters (10 m): terrain (Height, Aspect, Slope) and proximity masks (buildings, roads, sea, freshwater, foreshore, tidal water, woodland) to reduce spectral confusion.
- Classification Scenes:
  - Great Britain: 32 Classification Scenes arranged on a modified OS 100 x 100 km tile grid; each scene trained and classified independently.
  - Northern Ireland: single 49-band Classification Scene combining a 40-band Sentinel-2 Seasonal Composite with NI context rasters.
- Bootstrap Training:
  - Automatic training dataset built from historic LCMs (LCM2018–LCM2020), using parcels with >80% purity and consistent class across three years.
  - Training pixels are sampled with replacement to balance classes (10,000 samples per bag) and drive RF classifier performance.
  - The Bootstrap Training approach enables annual updates without new field data.
- Random Forest classification:
  - Implemented with bespoke UKCEH software integrating WEKA, PostGIS, and GDAL.
  - Outputs: 10 m classified pixels with class ID and associated confidence.

## Land Parcel Spatial Framework
- Land Parcel Framework (MMU ~0.5 ha) generalises national cartography to form discrete parcels (fields, parks, urban areas, etc.).
- Parcels help reduce classification noise and provide a stable basis for change detection.
- Parcel identifiers (gid) are not compatible with LCM2015 parcel IDs due to framework reordering and indexing changes.

## Validation and Accuracy
- Validation dataset: 35,182 reference points from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points.
- Validation method: points intersected with 25 m rasterised Land Parcel datasets to assess correspondence.
- Reported accuracy: 82.6% overall (95% CI 82.19%–82.99%).
- Appendix 4 provides detailed confusion matrices and producer/user accuracies by class.

## Data Access, Use, and Considerations for GIS Workflows
- The 10 m Classified Pixels preserve fine features not captured in the Land Parcel framework; intended for advanced users who understand that validation was performed against the 25 m parcel dataset, not the 10 m pixels.
- The 1 km products provide a scalable summary for larger-area applications.
- There is a known mismatch in parcel identifiers between LCM2021 and earlier products; spatial overlap is the recommended basis for comparison rather than gid matching.
- Rounding in 1 km percentage-cover products may produce totals slightly diverging from 100% (coastal areas may sum to less than 100%).
- Bootstrap Training supports consistent annual updates but may still exhibit class-confusion in spectrally similar habitats.
- Data are intended for map-based data products and change detection, with the annual series enabling differentiation between random errors and real changes.

## Appendices: Key References and Practical Details
- Appendix 1: Notes on UKCEH Land Cover Classes and BAP Broad Habitats (including class nuances and common confusions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and mapping considerations).
- Appendix 3: Full list of UKCEH LCM2021 datasets (naming by region and dataset type).
- Appendix 4: Correspondence matrices and accuracy details by class (confusion matrix metrics).
- Appendix 5 & 6: Recommended colour schemes for displaying UKCEH Land Cover Classes (standard and colour-blind friendly).
  - Includes class-specific RGB values for mapping with both standard and color-blind palettes.