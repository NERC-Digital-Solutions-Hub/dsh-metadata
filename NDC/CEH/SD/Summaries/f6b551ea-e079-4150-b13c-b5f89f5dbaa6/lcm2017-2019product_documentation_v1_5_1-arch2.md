# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview and purpose
- Release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Maps comprise 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; classes align with LCM2015 conventions.
- Production emphasizes automatic classification (Bootstrap Training with Random Forest) to enable annual updates without manual corrections.
- Aims include providing rapidly generated, consistent UK-wide land cover data for monitoring environmental health and policy performance.

## What the datasets contain
- 20m Classified Pixels: new RF-based per-pixel classifications (20 m, 2-band rasters: class and confidence 0–100). Preserves fine detail without generalisation.
- Land Parcels: attributes derived by intersecting 20m classified pixels with the UKCEH Land Parcel Spatial Framework (0.5 ha MMU). Includes per-parcel histograms, modal class, purity, confidence, and related fields (gid and others; some field names differ from LCM2015).
- 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity) representing parcel-level summaries.
- 1km rasters (GB and NI): 
  - 1km Percent Cover (21 bands)
  - 1km Percent Aggregate Cover (10 bands)
  - 1km Dominant Cover (1 band)
  - 1km Dominant Aggregate Cover (1 band)
- Dataset extents and coordinate systems:
  - GB: Great Britain grid (EPSG:27700); NI: Irish grid (EPSG:29903).
  - Pixel/target resolutions and band structures specified in Tables 4 and Appendix 5.

## Data structure and production lineage
- Datasets mirror the LCM2015 structure with an added 20m Classified Pixels dataset to preserve landscape detail.
- UKCEH Land Parcel Spatial Framework retained, but with minor reordering and new indices; gid identifiers do not match LCM2015 when comparing parcels year-to-year.
- Land Parcels attributes refined from LCM2015 (e.g., hist and conf representations); some attribute names changed to align with production software.

## Production methodology
- Bootstrap Training: automatic generation of training data from historic UKCEH LCMs (primarily LCM2015), sampling land parcels with high purity to bootstrap classifier training for 2017–2019.
- Random Forest classification: balanced sampling (10,000 samples per class per training bag) to train the classifier and produce the 20m Classified Pixels product.
- Algorithm and tooling: bespoke UKCEH software integrating WEKA with PostGIS and GDAL; fully automated, designed to avoid manual corrections to enable annual updates.

## Imagery and contextual inputs
- Seasonal Composite Imagery: Sentinel-2 seasonal composites (TOA reflectance) created per season (winter, spring, summer, autumn) at 20m, using bands 2,3,4,5,6,7,8,11,12.
- Context Rasters (20m): include terrain (Height, Aspect, Slope), proximity masks (distance to buildings, roads, sea, freshwater), foreshore and tidal masks, and urban/woodland indicators to reduce spectral confusion.
- Classification Scenes:
  - Great Britain: 100x100 km tiles producing 46-band GB Classification Scenes; 74 overlapping scenes classified independently with visual checks for precedence.
  - Northern Ireland: single 43-band Classification Scene per year (36 spectral + 7 context bands) due to smaller area.

## Validation and accuracy
- Validation dataset: GB countryside survey 2019 data, National Forest Inventory data, IACS data, plus bespoke LCM validation points (n ≈ 22,325).
- Reported accuracies (UK scale, 21 classes):
  - LCM2017: ~78.6%
  - LCM2018: ~79.6%
  - LCM2019: ~79.4%
- Note: validation uses a cross-year set; results depend on the currency of validation points and class mappings; full correspondence tables provided in Appendix 4.

## Key considerations for users
- Class definitions and relationships:
  - 21 UKCEH Land Cover Classes derived from UK BAP Broad Habitats; not a perfect one-to-one mapping to BAP due to remote-sensing detection limits.
  - Appendix 1 and 2 provide detailed notes on class motivations, detection issues, and crosswalks between UKCEH and UK BAP Broad Habitats.
- Comparability and time-series use:
  - gid changes mean direct parcel-wise comparison with LCM2015 is not possible; parcel-based comparisons should use gid and consider the spatial framework changes.
- Gaps and future directions:
  - Automatic classification yields annual outputs but includes some classification uncertainties, especially for spectrally similar classes (e.g., various grasslands, upland vegetation).
  - Future work may include expanding data inputs (e.g., Sentinel-1 SAR) and exploring gap-filling strategies for missing seasons.
- Data quality and transparency:
  - Visual checks and formal validation were performed; about 80% correspondence at national scale is considered impressive given automatic production.
  - Appendix 4 provides full confusion matrices and producer/user accuracy by class.

## Practical guidance for analysts
- Use the 20m Classified Pixels for high-detail mapping and to build bespoke summaries; leverage Land Parcels as a structured, comparable unit for change detection.
- For broad-scale monitoring and trend analysis, employ the 1km Percent/ Dominant products to rapidly assess dominant land cover in 1 km cells.
- When linking to policy or biodiversity analyses, refer to the 21 UKCEH Land Cover Classes and be mindful of the BAP Broad Habitat mapping nuances outlined in Appendices 1–2.
- Consider annual release implications: Bootstrap Training and RF model updates support time-series consistency, but ensure cross-year comparability by understanding gid changes and frame adjustments.

## Appendices and supplementary information
- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats; guidance on interpretation and detection caveats.
- Appendix 3: Recommended RGB colour mappings for displaying classes.
- Appendix 4: Validation details, confusion matrices, and accuracy metrics by class (LCM2017–LCM2019).
- Appendix 5: Full list of datasets per year (including GB/NI distinctions and dataset naming).

## Future plans and ongoing development
- Aim to release a new LCM annually (LCM2020 planned for 2021; subsequent years to follow with 3-year majority bootstrap refinement).
- Ongoing evaluation of input data (e.g., SR vs TOA) and potential incorporation of additional imagery types (e.g., Sentinel-1 SAR) to improve classification in cloud-prone or spectrally ambiguous regions.