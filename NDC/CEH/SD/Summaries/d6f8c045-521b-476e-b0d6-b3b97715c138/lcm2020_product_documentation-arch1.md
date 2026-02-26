# The UKCEH Land Cover Map for 2020

- A user guide for LCM2020, the UKCEH land cover map produced annually with six datasets (three for GB and Northern Ireland): 10m classified pixels, land parcels, and 25m rasterised land parcels per region, plus 1km summary rasters.
- Purpose: explain data production, validation, and accuracy to help users apply LCM2020 in current and future work.

## Datasets and data products

- 10m Classified Pixel datasets (GB and NI): per-pixel land cover classification with two bands — the dominant UKCEH Land Cover Class and the associated classification confidence.
- 25m Rasterised Land Parcel datasets: derived by rasterising the land parcels; carry three bands (dominant class, mean confidence, and parcel purity).
- Land Parcel datasets: attributes for each parcel, including histograms of class occurrences, mode, purity, and confidence.
- 1km raster products: summarize 25m classifications to provide dominant class and percentage cover per 1km pixel (for both GB and NI).
- 10m “Seasonal Composite Images” ( Sentinel-2 based) and 10m Context Rasters used for classification.
- Appendix 6 lists dataset names and extents; coordinate systems: GB (EPSG 27700) and NI (EPSG 29903).

## Classification framework and imagery

- UKCEH LCM2020 classes: 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, with some caveats (not identical to BAP; differences noted where relevant).
- Basis: Classification Scenes combine Sentinel-2 Seasonal Composite Images with 10 Context Rasters to reduce spectral confusion.
- Seasonal data: four-season Sentinel-2 imagery (winter, spring, summer, autumn) with nine bands used; cloud gaps exist but do not cripple full UK coverage.
- Context Rasters (GB and NI): terrain (height, aspect, slope) plus proximity to roads, buildings, coast, freshwater, urban masks, etc.

## Modelling approach and training data

- Bootstrap Training: fully automated training process that uses historical LCM outputs as training data to avoid new field campaigns.
- Training data: derived from UKCEH LCM2017–2019; parcels with >99% purity across three years used; GB training objects ≈ 941,027; NI ≈ 214,833.
- Random Forest classifier: 10,000 samples per class (with replacement) from each training bag to ensure balanced learning across classes.
- Processing pipeline: 36-band GB Classification Scenes (plus 10 context rasters) and a single 43-band NI Classification Scene; 74 GB classification tiles overlapped to cover the UK.

## Land parcel framework and data structure

- UKCEH Land Parcel Spatial Framework: based on a generalised national parcel system with ~0.5 ha minimum mapping unit (MMU).
- Parcels provide a stable structure for comparing land cover over time and for reducing classification noise.
- Parcel identifiers (gid) do not exactly match LCM2015 when comparing across years due to data reorganization.

## Validation and accuracy

- Validation: 34,715 points from GB countryside survey (2019/2020), National Forest Inventory, IACS data, and bespoke validation points; intersected with Land Parcel datasets.
- Overall accuracy: 79.2% at full thematic detail (per Appendix 5).
- Validation provides producer’s and user’s accuracy metrics across all 21 classes, with detailed confusion matrices illustrating class-level performance and typical misclassifications.

## Relationship to BAP Broad Habitats

- The 21 UKCEH Land Cover Classes map to UK BAP Broad Habitats, but not identically; BAP design goals (field detection) differ from satellite-based mapping.
- Appendices detail the mappings, including cases where single BAP classes map to multiple UKCEH classes (e.g., Freshwater vs Rivers/Canals, Dwarf Shrub/Heath splits into Heather and Heather Grassland, etc.).
- Color schemes and display guidelines (including color-blind friendly options) are provided to help interpret results.

## Practical considerations for users

- The 10m Classified Pixel dataset preserves fine landscape detail (not generalised to Land Parcel framework), suitable for advanced users who understand interpretation implications.
- Annual production aids change detection by distinguishing real changes from random classification noise (which flickers over time).
- The dataset uses a robust, automated approach but acknowledges that errors exist; ongoing methodological improvements are anticipated as the time series matures.

## Key references and appendices

- Appendices cover detailed class definitions (UKCEH vs BAP), recommended color recipes for display, and extensive validation matrices.
- Major references include foundational works on Random Forests, Bootstrap Training, and past LCM products.

## Access and metadata

- Datasets include GB and NI variants plus 1km rasters; official dataset names and metadata are listed in Table/Table-like sections and Appendix 6.
- Metadata and data provisioning emphasize discoverability, with guidance on handling confidence metrics and parcel-based comparisons.