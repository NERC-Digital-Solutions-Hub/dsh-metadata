# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose: A user guide for three new UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019) describing content, production, validation, and guidance for informed use. The maps share 21 UKCEH Land Cover Classes linked to Biodiversity Action Plan (BAP) Broad Habitats and are produced automatically to enable near-real-time annual updates.

## Key datasets and content

- Land Cover Classes: 21 UKCEH Land Cover Classes (based on BAP Broad Habitats; not exactly the same as BAP, but closely aligned for change detection).
- Datasets in each release:
  - 20m Classified Pixels: new, RF-classified per-pixel results with a second band showing per-pixel class membership probability (0–100). Preserves fine details and not generalised by parcel framework.
  - Land Parcels: attributes derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha). Includes gid, hist, mode, purity, conf, stdev, n (with naming changes from LCM2015).
  - 25m Rasterised Land Parcels: rasterised version (3 bands: mode, conf, purity) of the Land Parcels data.
  - 1km Raster datasets (derived from 25m parcels):
    - 1km Percent Cover (21-band 8-bit raster)
    - 1km Percent Aggregate Cover (10-band 8-bit raster)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- Spatial extents and formats:
  - Great Britain (GB) and Northern Ireland (NI) versions for each dataset.
  - Pixel sizes: Classified Pixels 20m; Raster Parcels 25m; 1km rasters derived from 25m data.
  - Coordinate systems: GB = British National Grid (EPSG:27700); NI = Irish Grid (EPSG:29903).
- Dataset structure (Figure/Appendix references in doc):
  - 42 total datasets across years (20m, Land Parcels, 25m, and 1km products for GB and NI).

## Production approach and methodology

- Bootstrap Training: Fully automatic training using a bootstrap approach that samples training data from historic maps to train a Random Forest classifier. For 2017–2019, bootstrap training uses UKCEH LCM2015 as the seed, selecting parcels with purity ≥ 99% to bootstrap the training set; future maps plan to use majority signals across multiple years.
- Random Forest classification: Balanced sampling (10,000 samples per class) to train the RF classifier; production uses bespoke UKCEH software integrated with WEKA, PostGIS, and GDAL.
- Seasonal Composite Imagery: Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season) derived for winter, spring, summer, autumn; 9 bands used. Some cloud gaps exist; algorithm tolerates partial data and future work may incorporate other sources (e.g., Sentinel-1 SAR) to fill gaps.
- Context Raster approach: 20m Context Rasters provide terrain, proximity to urban features, and other contextual cues to reduce spectral confusion.
- Classification Scenes and tiling: GB classified using overlapping 100x100 km tiles (74 GB Classification Scenes); NI uses a single 43-band scene per year (36 spectral + 7 context bands).
- Land Parcel Spatial Framework: Framework originally for LCM2007, updated for LCM2017–2019; parcels remain ~0.5 ha MMU but gid values no longer cross-match with LCM2015. Framework aims to fix a stable unit for change detection and future refinements may propose finer parcel structures with smaller MMU as data resolution increases.

## Data inputs and validation

- Satellite data: Sentinel-2 Seasonal Composite Images (TOA used for these maps; SR not yet providing improvements for this thematic level).
- Context data: NEXTMap terrain (height, aspect, slope) and OS open data (distance to buildings, roads, coast, freshwater) plus coastal/foreshore masks and urban/woodland binary masks (specific to GB and NI).
- Validation: UK-scale validation against GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (22,325 points total). Reported overall accuracies:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation caveats: Validation data are not absolute truth and were mapped to UKCEH classes; currency of validation varies year-to-year. Full correspondence tables in Appendix 4.

## Data interpretation and usage notes

- Class alignment: 21 UKCEH Land Cover Classes are used; ties to UK BAP Broad Habitats explained in Appendices 1 and 2. Users should be aware of potential ambiguities between remotely sensed classes and field-based habitat terms.
- Confidence and uncertainty: The 20m Classified Pixels provide a per-pixel probability (Band 2) to indicate classification confidence; users should use this alongside the purity/confidence metrics in Land Parcels for per-parcel interpretation.
- Comparison across years: The gid (Land Parcel ID) for LCM2017–LCM2019 differs from LCM2015 due to the framework changes; cross-year comparisons should use spatial overlap or the updated gid as the linking reference.
- Change detection and scale: The MMU and parcel-based aggregation are designed to enable robust change detection; local-scale comparisons should consider the 0.5 ha MMU and differences between 20m detail vs 25m and 1km generalized products.
- Visualization and color coding: Appendix 3 provides an RGB color recipe for display of the 21 classes; helpful for map production and quick interpretation.

## Appendices and supporting details

- Appendix 1: Notes on UKCEH Land Cover Classes (class-level interpretations and potential spectral confusions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and their relationship to UKCEH classes.
- Appendix 3: Recommended RGB color mappings for display of UKCEH Land Cover Classes.
- Appendix 4: Validation details, including confusion matrices, user/producer accuracies, and cross-year comparison notes.
- Appendix 5: Comprehensive list of datasets by year and dataset type (GB and NI entries).

## Practical takeaways for analysts

- Use 20m Classified Pixels for detailed, locally nuanced land cover information with explicit per-pixel confidence.
- Use Land Parcels and 25m Rasterised Parcels to work with stable, parcel-based units suitable for time-series analysis and change detection.
- Leverage 1km raster products (Percent Cover, Percent Aggregate Cover, Dominant/Forecasted) for broad-scale analyses and integration with other 1km products.
- Be mindful of cross-year parcel ID differences when comparing LCM2017–LCM2019 to LCM2015; use spatial overlap or updated gid for longitudinal analyses.
- Consider validation caveats and use Appendix 4 confusion matrices to understand class-specific performance and potential misclassification hotspots.