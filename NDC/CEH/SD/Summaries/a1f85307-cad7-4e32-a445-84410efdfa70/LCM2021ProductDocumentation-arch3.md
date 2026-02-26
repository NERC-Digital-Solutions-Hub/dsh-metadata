# The UKCEH Land Cover Map 2021

## Purpose
- User guide for the UKCEH Land Cover Map 2021 (LCM2021).
- Describes data production, validation, and data accuracy to help users apply LCM2021 in current and future work.
- LCM2021 comprises six datasets (three per region: Great Britain and Northern Ireland): 10 m classified pixels, classified land parcels, and 25 m rasterised land parcels; with additional 1 km summary products.

## Product overview and datasets
- 10 m Classified Pixel datasets (GB and NI): high-resolution classified pixels with a second band indicating classification probability/confidence.
- Land Parcel datasets (GB and NI): derived by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework; provide parcel-level attributes and metrics.
- 25 m Rasterised Land Parcel datasets (GB and NI): rasterized parcel products carrying per-parcel land cover, mean confidence, and purity across 25 m cells.
- 1 km raster products: summarised outputs including dominant cover (1-band) and percentage cover (21 bands for classes; 10 bands for aggregates) per 1 km pixel.
- Classification products are built to support change detection, temporal analysis, and consistent monitoring over time.

## Data production workflow
- Seasonal Composite Images: derived from Google Earth Engine using Sentinel-2 data; four seasonal median composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) across 10 spectral bands; occasional gaps due to cloud are tolerated.
- Context Rasters: 10 m context layers to reduce spectral confusion (e.g., terrain, distance to buildings/roads/seas/freshwater, foreshore and coastal masks, woodland mask for GB; analogous layers for NI).
- Classification Scenes: GB classified using 32 tiles (100 x 100 km grid) each containing 50-band Seasonal Composite Images plus 10 Context Rasters; NI uses a single 49-band scene with NI-specific context rasters.
- Bootstrap Training: automatic, non-field data-driven training using historic LCM years (LCM2018, LCM2019, LCM2020); training samples require >80% purity and consistent class across three years.
- Random Forest classification: balanced sampling (10,000 samples per class per bag) from Bootstrap Training data to derive 10 m Classified Pixel product; open-source software stack (WEKA, PostGIS, GDAL) used.
- UK Land Parcel Spatial Framework: fixed parcel structure (~0.5 ha minimum MMU) to aggregate pixels into parcels; designed to support change detection and inter-map comparability.
- Validation: formal validation against 35,182 points covering all 21 classes; overall accuracy 82.6% (95% CI 82.19–82.99%).

## Spatial framework and class relationships
- UKCEH Land Cover Classes: 21 classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, but not identical to BAP classifications.
- Appendices explain mappings and nuances between UKCEH classes and BAP Broad Habitats; some splits/merges (e.g., Urban vs Suburban, Heather vs Heather Grassland, Freshwater vs Saltwater).
- Landsurface and habitat descriptions are provided to support interpretation and cross-walk with environmental reporting.

## Data specifics and accessibility considerations
- Coordinate systems: Great Britain – British National Grid (EPSG 27700); Northern Ireland – Irish Grid TM75 (EPSG 29903).
- Extents and parcel counts: GB parcels ~6.74 million; NI parcels ~0.90 million.
- 10 m Classified Pixels retain fine landscape detail (not generalized by the Land Parcel Framework) to preserve narrow features; validation was performed on the 25 m land parcel dataset.
- Outputs include detailed metadata fields in the Land Parcel dataset (e.g., _hist, _mode, _conf, _stdev, _agg, _n) to describe class composition, confidence, and aggregation.
- 25 m rasters provide three-band outputs: dominant land cover, mean confidence, and purity per parcel.
- Accessibility: authoring and validation rely on open-source tools; production aims to support annual updates for improved temporal consistency and change detection.

## Validation, accuracy, and interpretation
- Overall accuracy: 82.6% with 95% confidence interval 82.19%–82.99%.
- Validation dataset compiled from GB countryside survey data, National Forest Inventory data, Rural Payments data, and bespoke validation points.
- The study acknowledges potential inter-class confusion (e.g., between some grassland types, bog, heather) and notes higher certainty for broader classes and more easily spectrally separable features (e.g., urban vs. natural surfaces).

## Temporal strategy and monitoring implications
- Annual production enables better differentiation between random classification errors and real changes over time.
- Bootstrap Training leverages historical maps to sustain training data volume and reduce the need for new field data.
- The approach supports change detection and long-term monitoring across the UK countryside, aligning with environmental and policy monitoring objectives.

## Appendices and documentation highlights
- Appendix 1: Notes on UKCEH Land Cover Classes (details and caveats for each class).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats – definitions and mappings to UKCEH classes.
- Appendix 3: Full list of datasets and their official names.
- Appendix 4: Detailed validation matrices (confusion matrices) and producer/user accuracy metrics.
- Appendix 5 & 6: Recommended color recipes for displaying UKCEH Land Cover Classes, including color-blind friendly options.
- General notes on data descriptions, terminology, and class naming conventions throughout.

## Implications for monitoring framework authors
- Provides a reproducible, automated workflow for annual land cover mapping with clear data lineage and validation.
- Demonstrates handling of data gaps, metadata provision, and governance considerations through the use of Bootstrap Training, context rasters, and formal validation.
- Offers detailed class definitions, crosswalks to BAP habitats, and robust documentation to facilitate integration into environmental monitoring and reporting systems.
- Highlights practical trade-offs between high-resolution detail (10 m pixels) and parcel-based analysis (0.5 ha MMU) for change detection and policy evaluation.