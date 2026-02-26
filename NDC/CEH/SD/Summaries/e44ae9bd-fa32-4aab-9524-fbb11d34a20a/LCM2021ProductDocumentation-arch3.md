# The UKCEH Land Cover Map for 2021

- UKCEH LCM2021 provides an annually produced land cover map for Great Britain and Northern Ireland, built to support monitoring the state and change of the countryside and inform environmental objectives.
- The product suite comprises six geospatial datasets (three per mass: GB and NI), plus derived 1 km products for summary analyses.
- A key goal is to enable informed decisions through improved data quality, metadata, openness, and transparency in methodology and outputs.

## Purpose and scope

- Describes data production, validation, accuracy, and guidance for applying UKCEH LCM data in current and future work.
- Produces 21 UKCEH Land Cover Classes (aligned with Biodiversity Action Plan Broad Habitats concepts, but not a one-to-one mapping).
- Aims to maximize temporal consistency, comparability, and change detection potential; annual updates help distinguish errors from real change.
- Formal validation reports an overall accuracy of 82.6%.

## Data products (LCM2021 dataset suite)

- 10 m Classified Pixel datasets (GB and NI):
  - Output: two-band mosaic per mass; Band 1 = most probable UKCEH Land Cover Class, Band 2 = class membership probability.
  - Preserves detailed features not generalized by the Land Parcel Spatial Framework.
- Land Parcel datasets (GB and NI):
  - Intersects the 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to produce parcel attributes.
- 25 m Rasterised Land Parcel datasets (GB and NI):
  - Rasterized version of parcel data; three-band rasters carrying per-parcel dominant class, mean confidence, and purity.
- 1 km raster products (derived products across GB/NI):
  - Dominant class at 1 km (two sets: by LCM2021 classes and by LCM2021 Aggregate classes).
  - Percentage cover at 1 km (21 bands for classes; 10 bands for aggregates); values are integers and may not sum exactly to 100 due to rounding.
- Georeferencing and coordinate systems:
  - GB: British National Grid (EPSG: 27700); NI: Irish Transverse Grid (TM75, EPSG: 29903).
- Extents and parcel details:
  - GB parcels: about 6.7 million; NI parcels: about 0.9 million.
  - Land Parcel Spatial Framework MMU: ~0.5 ha minimum mapping unit.

## Production methodology

- Data foundations:
  - Seasonal Composite Images derived from Sentinel-2; four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
  - Ten Context Rasters to reduce spectral confusions (e.g., height, slope, proximity to roads/buildings, coast, freshwater, foreshore, etc.).
- Classification Scenes:
  - GB: 32 Classification Scenes created from a grid tiling of roughly 100 x 100 km tiles; NI: a single Classification Scene covering NI.
  - Each Classification Scene trained and classified independently, using 50-band Seasonals plus Context rasters (total 49 bands for NI; GB setups vary by tile).
- Bootstrap Training:
  - Automatic training dataset constructed from historic LCM maps (LCM2018–LCM2020) with filtering for purity (>80%) and consistent class across years.
  - Training samples drawn from Bootstrap parcels to train a Random Forest (RF) classifier; sampling with replacement ensures balanced learning across classes.
- Random Forest classification:
  - RF classifier outputs the most probable class per 10 m pixel; a second band provides classification confidence.
  - UKCEH’s bespoke classification software integrates WEKA, PostGIS, and GDAL (open source).
- The UKCEH Land Parcel Spatial Framework:
  - A fixed framework that groups 10 m pixels into land parcels, aiding noise reduction and change detection.
  - Parcels designed to represent discrete real-world units (fields, parks, woodlands, etc.) with a 0.5 ha MMU.

## Validation and accuracy

- Validation dataset:
  - 35,182 validation points across all 21 classes, drawn from GB countryside surveys, National Forest Inventory, Rural Payments data, and manual image interpretation.
- Accuracy:
  - Overall accuracy: 82.6% (95% CI 82.19%–82.99%).
- Validation details and correspondence matrices are provided to support user assessment of class-specific performance.

## UKCEH Land Cover Classes and BAP alignment

- 21 UKCEH Land Cover Classes are linked to UK BAP Broad Habitats, though not identical.
- Appendix notes and tables describe mappings, with certain split/merge decisions (e.g., building-related classes separated into Urban and Suburban; Freshwater and Saltwater distinctions where feasible).
- The mapping preserves historical continuity for cross-compatibility with earlier UKCEH products while acknowledging changes in BAP definitions and remote-sensing capabilities.

## The UKCEH Land Parcel Spatial Framework (technical context)

- MMU and parcel design decisions (approx. 0.5 ha) balance map detail with computational efficiency and change-detection utility.
- Parcels provide a stable, fixed reference for comparing land cover over time.
- GIDs (unique parcel identifiers) differ from LCM2015 due to framework updates, which may affect direct cross-year parcel-id comparisons.

## Context and methodology details for monitoring use

- Bootstrap Training leverages wall-to-wall historical data to maximize training sample size and robustness against changes.
- Annual production enhances assessment of change vs. random mapping noise; persistent changes across years indicate real alteration.
- Classification transparency:
  - Clear documentation of data sources, processing steps, and validation statistics to support governance and decision-making.

## Use considerations and governance

- Data quality, openness, and data management:
  - Data are produced with explicit attention to metadata, provenance, and model parameters; public sharing of underlying data is a consideration in practice.
- Applicability for policy and environmental health monitoring:
  - The 21-class framework supports habitat- and land-cover-related policy indicators.
  - 1 km and parcel-level products enable scalable analysis from fine-grained to landscape-scale assessments.
- Caveats for interpretation:
  - Spectral confusion remains (e.g., grasslands, mosaics, and certain wetland types).
  - Saltwater vs Freshwater boundaries and coastal classifications can have higher uncertainty near shorelines; near-term quarries and small water bodies may be underrepresented due to MMU.
  - Some linear features (e.g., hedgerows) are difficult to map spectrally and are not explicitly classified, though they may appear as narrow features.

## Practical implications for monitoring policy and decision-making

- Enables time-series analyses to distinguish real ecological change from mapping noise, aiding monitoring of policy outcomes.
- Provides a standardized, auditable dataset with accompanying validation metrics and class definitions.
- Supports open-data approaches and transparent methodological reporting, aligned with governance expectations for environmental monitoring.
- Facilitates change detection, landscape-scale assessments, and habitat-related reporting by linking land cover classes to BAP Broad Habitats.

## Appendices and supplemental guidance (highlights)

- Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and alignment with BAP Broad Habitats.
- Appendix 3–4: Full dataset listings and confusion/accuracy matrices (Producer’s and User’s Accuracy) for class-level interpretation.
- Appendix 5–6: Color recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly) to support effective visualization in reports and dashboards.

- Overall, LCM2021 provides a robust, well-documented framework of annual land cover data with clearly described production, validation, and usage guidance, designed to inform environmental health monitoring and policy evaluation while acknowledging data limitations and governance considerations.