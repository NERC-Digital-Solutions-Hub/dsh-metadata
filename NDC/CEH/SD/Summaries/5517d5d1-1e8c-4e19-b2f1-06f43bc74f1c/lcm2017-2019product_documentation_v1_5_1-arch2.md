# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and Overview
- Presents three new UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019) detailing land cover across Great Britain and Northern Ireland.
- Land cover is mapped into 21 UKCEH Land Cover Classes, aligned with UK Biodiversity Action Plan (BAP) Broad Habitats concepts.
- Maps are produced automatically using Bootstrap Training plus Random Forest (RF) classification to enable rapid, annual output.
- Aim is to support environmental monitoring and policy evaluation with a consistent, time-series dataset, while noting the trade-off with manual corrections.

## Data Components and File Structure
- 20m Classified Pixels: new RF classification results for each year; per-pixel class with a second band indicating classification confidence (0–100).
- Land Parcels: parcel-level attributes derived by intersecting 20m classified pixels with the UKCEH Land Parcel Spatial Framework (LPF); includes histogram, mode, purity, confidence, standard deviation, and pixel counts.
- 25m Rasterised Land Parcels: three-band raster (mode, confidence, purity) summarising parcels at 25m resolution.
- 1km Raster Products:
  - 1km Percent Cover: 21-band raster (per-class percentage per 1km grid).
  - 1km Percent Aggregate Cover: 10-band raster (aggregate class percentages per 1km).
  - 1km Dominant Cover: single-band raster of the dominant class per 1km.
  - 1km Dominant Aggregate Cover: dominant aggregated class per 1km.
- Datasets are provided for Great Britain (GB) and Northern Ireland (NI) with respective coordinate systems and extents.
- Total product suite includes 42 datasets per release (for 3 years × GB and NI).

## Production Methodology
- Bootstrap Training: automatic, uses historic LCM observations (primarily from LCM2015) to bootstrap training data for new maps; intends to leverage majority signals over multi-year windows (e.g., 2017–2019) for future updates.
- Random Forest Classification: balanced training (10,000 samples per class per classification scene) to yield the 20m Classified Pixels product.
- Seasonal Composite Images: Sentinel-2 seasonal composites (TOA reflectance) representing median seasonal spectra; four-season composites (winter, spring, summer, autumn).
- Context Rasters: 20m context layers (terrain, urban proximity, roads, coast, etc.) added to reduce spectral confusion.
- Classification Scenes: GB mapped in overlapping 100x100 km tiles; NI uses a single 43-band scene per year. This tiling supports diverse phenology and processing manageability.
- Seasonal and data notes: full cloud gaps may occur; there is consideration of future gap-filling with alternative sources (e.g., Sentinel-1 SAR).
- Classification Outputs: GB scenes yield 46-band classification scenes; outputs are then aggregated to parcel and grid-based products.

## The UKCEH Land Parcel Spatial Framework
- LPF is unchanged in footprint since LCM2015, but storage indices reordered to speed processing; gid identifiers for 2017–2019 do not match LCM2015, limiting direct parcel-to-parcel year-to-year comparisons except via gid-based matching.
- Land parcels have a minimum area of ~0.5 ha (MMU) and are designed to represent discrete real-world units (fields, urban areas, etc.).
- LPF can be replaced or complemented by user-defined parcel structures; future refinements may target higher-resolution data and smaller MMU as satellite data precision increases.

## Validation and Accuracy
- UK-scale validation used 22,325 points from multiple sources (Countryside Survey, National Forest Inventory, IACS, and manual interpretation).
- Reported overall accuracy (approximate) for UK-wide 21-class maps:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation data share caveats: single validation set used across years; some class label conversions required; accuracy indicators reflect best available matching rather than absolute truth.
- Appendices provide detailed confusion matrices and class-specific producer and user accuracies.

## Data Access, Extents, and Formats
- Geographic Extents:
  - Great Britain: British National Grid (EPSG: 27700)
  - Northern Ireland: Irish Grid (EPSG: 29903)
- Pixel and Raster Specifications:
  - 20m Classified Pixels: 2-band (class, confidence) rasters
  - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity)
  - 1km Rasters: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band)
- Datasets are provided in GB and NI versions; annual releases are planned to extend to a new LCM each year (per aims).
- Appendix 5 lists full dataset names and formats per year (LCM2017, LCM2018, LCM2019).

## Class Relationships and Visualization
- UKCEH Land Cover Classes (21) are tied to BAP Broad Habitats with carefully defined relationships (Appendix 1) to aid interpretation and alignment with habitat concepts.
- A color recipe (Appendix 3) is provided for consistent visual display of classes.
- The documentation notes common confusions among classes and how context rasters and training data help mitigate misclassifications.

## Practical Considerations for Analysts
- Annual maps enable change detection but rely on automated classification with no manual post-correction in this release; users should interpret localized anomalies as potential changes or artefacts, considering data quality and validation context.
- The Bootstrap Training approach leverages historical data but implies that cross-year comparisons should use consistent identifiers (e.g., gid where possible) and be aware of LPF reindexing.
- The dataset suite supports multi-scale analysis (20m to 1km), with detailed parcel-level attributes enabling both pixel- and area-based analyses.
- Users should consult Appendices for detailed class definitions, validation results, and methodological nuances.