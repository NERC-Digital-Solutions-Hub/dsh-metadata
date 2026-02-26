# The UKCEH Land Cover Maps for 2017, 2018 and 2019

## Purpose and scope
- User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018 and LCM2019.
- Map outputs: 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; aligned with LCM2015.
- Production approach: fully automatic classification using Bootstrap Training and Random Forest (RF); uses Sentinel-2 Seasonal Composite Images (TOA reflectance) and context rasters.
- Goal: enable rapid, annual UK-wide land cover mapping with validated quality and documented production decisions.

## Key concepts and terminology
- Bootstrap Training: automatic selection of training observations from historic maps (primarily LCM2015) to train RF classifiers.
- Classification Scene: multi-layer input for RF consisting of Seasonal Composite Images plus Context Rasters.
- Seasonal Composite Image: four-season, 20m Sentinel-2 reflectance data to capture phenology.
- Context Rasters: 20m layers (e.g., height, aspect, slope, distances to features) to reduce spectral confusion.
- UKCEH Land Parcel Spatial Framework: polygon-based framework (0.5 ha MMU) used to summarise 20m pixels into land parcels; gid provides parcel identifiers.

## Production approach and workflow
- Sentinel-2 data: TOA reflectance chosen over surface reflectance (SR) after evaluation; full SR benefits to be reviewed in future.
- GB Classification Scenes: 100x100 km tiles; 74 overlapping scenes classified independently to ensure coverage and balance.
- Northern Ireland: single 43-band Classification Scene per year, determined by the NI land mass.
- Bootstrap Training data: derived from LCM2015 parcels with ≥99% purity; supports 2020–2021 bootstrap plans.
- RF classifier: trained with balanced samples (10,000 per class) across scenes; uses Weka, PostGIS, and GDAL tools.

## Data products and datasets
- 20m Classified Pixels: new addition; RF classification results with class membership probability (band 2); preserves fine detail without parcel-based generalisation.
- Land Parcels: 20m classified pixels summarised within the UKCEH Land Parcel Spatial Framework; includes attributes such as _hist, _mode, _purity, _conf, _stdev, _n.
- 25m Rasterised Land Parcels: rasterised parcels (25m) with three bands: _mode, _conf, _purity.
- 1km Raster Datasets: derived by aggregating 25m parcels to 1km grids:
  - 1km Percent Cover: 21-band raster (percentage by class).
  - 1km Percent Aggregate Cover: 10-band raster (percentage by UKCEH Aggregate Classes).
  - 1km Dominant Cover: single-band raster (dominant class).
  - 1km Dominant Aggregate Cover: single-band raster (dominant aggregate class).
- Dataset extents and formats:
  - Great Britain: GB National Grid (EPSG: 27700).
  - Northern Ireland: NI Irish Grid (EPSG: 29903).
  - Pixel sizes and band counts as described above.
- Total datasets: 42 datasets per year (GB and NI versions for each product, across three years).

## Dataset structure and examples
- 20m Classified Pixels: two bands; band 1 = most likely class, band 2 = confidence (0–100).
- Land Parcels: parcel-based attributes linking 20m pixels to discrete land parcels; descriptive fields updated for consistency with production software.
- 25m Rasterised Land Parcels: three-band rasters reflecting per-parcel modal class, confidence, and purity.
- 1km products: aggregated summaries to provide broader-scale overviews and generalisation effects (e.g., comparison between 1km Dominant Cover and 25m parcels).

## Data quality, validation, and caveats
- Validation: UK-scale validation against GB Countryside Survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (n ≈ 22,325).
- Reported accuracy (overall correspondence with UKCEH classes):
  - LCM2017: ~78.6%
  - LCM2018: ~79.6%
  - LCM2019: ~79.4%
- Validation notes: same validation dataset used across three products; accuracy indicators reflect currency relative to each product; some conversions between validation outcomes and UKCEH classes were required.
- Quality considerations: intentional lack of manual corrections to enable annual production cadence; classification errors are expected to be spatially random; upland peatland and some habitat classes present known detection challenges.
- Class definitions and relationships: 21 UKCEH Land Cover Classes mapped from BAP Broad Habitats; textual notes clarify parents/derivations and potential spectral confusion; emphasis on maintaining comparability over time.

## Relationships to broader data and standards
- UKCEH Land Cover Classes linked to BAP Broad Habitats with careful handling of terminology and caps for defined classes.
- Acknowledges limitations of satellite-based detection for some habitat distinctions (e.g., Bracken vs Acid Grassland; upland peatland vegetation).

## Appendices and references
- Appendix 1: Notes on UKCEH Land Cover Classes (class-specific considerations and potential confusions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions aligned with Jackson 2000).
- Appendix 3: Recommended RGB colour recipe for displaying UKCEH Land Cover Classes.
- Appendix 4: Validation appendix with confusion matrices and accuracy statistics (per class, per year).
- Appendix 5: Full list of datasets per LCM2017, LCM2018 and LCM2019 (dataset names, extents, and availability notes).

## Access, updates, and future plans
- Annual release intention: moving toward yearly LCM updates using Bootstrap Training and RF with automated processing.
- Data availability: multi-year datasets (GB and NI) covering 20m, 25m, and 1km products; described in Appendix 5 for catalog access.
- Planned enhancements: exploration of additional data sources and methods (e.g., Sentinel-1, SR vs TOA, alternative optical sources) to improve future classifications and gap-filling for incomplete seasons.