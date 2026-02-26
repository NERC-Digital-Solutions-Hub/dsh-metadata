# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- A user guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018 and LCM2019.
- Maps contain 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; aligned with prior LCM series (LCM2015, etc.).
- Production is fully automated, using Bootstrap Training plus Random Forest classifiers to enable near-annual UK-wide maps.
- Data are derived from Sentinel-2 Seasonal Composite Images (TOA reflectance) plus 20m Context Rasters, with outputs intended for rapid, consistent environmental monitoring.

## Purpose and Scope

- Documents the content, production workflow, validation, and usage guidance for LCM2017–LCM2019.
- Aims to support informed decision-making in environmental monitoring by providing consistent, yearly land cover outputs.
- Acknowledges that some users require generalized classifications (UKCEH Aggregate Classes) in addition to the 21 UKCEH Land Cover Classes.

## Data Products and Dataset Structure

- 20m Classified Pixels: new dataset added in these products. RF-classified pixels with two bands:
  - Band 1: most likely UKCEH Land Cover Class (1–21)
  - Band 2: class membership probability (0–100), indicating per-pixel classification confidence
- Land Parcels: derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework
  - Attributes include gid, hist, mode, purity, conf, stdev, n; some field names differ from LCM2015 for production consistency
  - The 0.5 ha minimum mappable unit (MMU) is preserved; parcels typically dominated by a single class
- 25m Rasterised Land Parcels: rasterised version (bands 1–3) for efficient summarisation
  - Band 1: modal land cover (_mode)
  - Band 2: parcel-averaged confidence (_conf)
  - Band 3: parcel purity (_purity)
- 1km Raster Datasets:
  - 1km Percent Cover: 21-band raster (per-class cover)
  - 1km Percent Aggregate Cover: 10-band raster (aggregate classes)
  - 1km Dominant Cover: single-band raster
  - 1km Dominant Aggregate Cover: single-band raster (dominant aggregate)
- Dataset Extents and Grids:
  - Great Britain (GB) and Northern Ireland (NI) versions for all datasets
  - Total of 42 datasets across years and geographies (GB and NI)

## Classification Methodology

- Bootstrap Training:
  - Automated training set derived from historic LCMs (Bootstrap Training) to sample current satellite imagery.
  - For LCM2017–LCM2019, training samples come from UKCEH LCM2015 parcels with purity ≥ 99%.
  - Purpose: leverage the majority signal across time to train the RF classifier for the next map cycle.
- Random Forest Classification:
  - RF classifier trained with 10,000 samples per land cover class (with replacement) to balance rare classes.
  - Software stack combines Weka, PostGIS, and GDAL; fully automated production pipeline.
- Seasonal and Spectral Inputs:
  - Sentinel-2 seasonal composites (median reflectance per season) created in Google Earth Engine.
  - Seasonal composites combined with 20m Context Rasters to form Classification Scenes.
  - Four-season TOA data used; plan to explore SAR (Sentinel-1) and other inputs to handle gaps or improve accuracy.
- Context Rasters:
  - 20m context layers to help disambiguate spectrally similar classes (e.g., terrain, proximity to buildings/roads, coastline, etc.).
  - UK-wide GB rasters include height, aspect, slope, distances to features (buildings, roads, sea, freshwater), foreshore and tidal masks, and woodland mask.
- Classification Scenes:
  - GB: 74 overlapping 100x100 km tiles, yielding 46-band GB Classification Scenes.
  - NI: single 43-band Classification Scene per year, determined by NI extent.
  - Multiple overlaps may yield slightly different results; visual checks determine final precedence.

## UKCEH Land Parcel Spatial Framework

- Based on the framework used since LCM2007, unchanged in parcel geometry but reorganised storage and indices for faster processing.
- gid remains the parcel identifier, but new products have different gid values than LCM2015 (parcel comparisons require spatial overlap rather than id matching).
- MMU remains approximately 0.5 hectares; parcels represent discrete landscape units (fields, parks, urban areas, water bodies, etc.).
- The framework is provided to enable users to summarize land cover over fixed parcels or to enable user-defined boundaries for change detection.

## Validation and Quality

- Validation approach uses GB countryside survey data (2019), National Forest Inventory data, IACS, and bespoke validation points (22,325 points total).
- Reported overall accuracy (producer’s and user’s accuracy) for the three years:
  - LCM2017: ~78.6% overall
  - LCM2018: ~79.6% overall
  - LCM2019: ~79.4% overall
- Validation notes:
  - Validation dataset uses sources with different objectives and class descriptions; some conversions were required to align with 21 UKCEH land cover classes.
  - Figures suggest roughly 80% correspondence, indicating solid performance for automated, annual updates; accuracy is expected to improve as methods mature.

## Data Use, Limitations, and Future Plans

- Purpose-built for environmental monitoring and policy evaluation over time; suitable for maps, reports, and spatial analyses that require standardized land cover classes.
- Classification errors are expected to be randomly distributed; annual updates enable detection of real land cover change against background noise.
- Limitations include lack of manual corrections to preserve automation (no region-specific manual adjustments this cycle) and potential confusion among spectrally similar classes, especially in upland and coastal contexts.
- Future directions:
  - Consider production of LCM2020 and beyond with bootstrap strategies evolving toward majority signals across longer periods.
  - Explore enhancing inputs with additional data sources (e.g., Sentinel-1 SAR, surface reflectance improvements) to improve classification in cloudy regions and improve certain classes.
  - Maintain annual releases to support time-series analyses of land cover change.

## Appendices and References (Highlights)

- Appendix 1 and 2: Notes on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats; descriptions and detection caveats for key classes.
- Appendix 3: RGB colour recipe recommended for displaying UKCEH Land Cover Classes.
- Appendix 4: Validation details, confusion matrices, and producer’s/user’s accuracy per class for LCM2017, LCM2018, and LCM2019.
- Appendix 5: Full dataset list and naming conventions for LCM2017–LCM2019 datasets.
- References: foundational works on Random Forests, bootstrap training, and prior UK land cover mapping efforts.