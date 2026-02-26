# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and Overview
- User guide accompanying the release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Outputs represent 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed to be consistent with LCM2015 for comparability.
- All three maps produced automatically using Bootstrap Training with a Random Forest (RF) classifier; no manual corrections were made this time.
- Visual checks and formal validation were performed; maps are judged to be of similar quality to LCM2015.
- Aim is rapid, annual production and ongoing methodological evolution.

## Data Structure and Datasets
- Dataset package for each year includes:
  - 20m Classified Pixels (new) for GB and NI.
  - Land Parcels (GB and NI) created by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
  - 25m Rasterised Land Parcels (GB and NI).
  - 1km Dominant Cover (GB and NI).
  - 1km Percent Cover (GB and NI).
  - 1km Percent Aggregate Cover (GB and NI).
- Class and data relationships:
  - 21 UKCEH Land Cover Classes (GB/NI), matching the 21 classes used since LCM2000/2007 mix of UCHEH and BAP concepts.
  - 10 UKCEH Aggregate Classes.
  - 8-bit rasters; multiple bands per dataset (e.g., 21-band percent cover, 10-band percent aggregate cover, etc.).
- New 20m Classified Pixels dataset preserves fine landscape detail (not generalised by land parcel boundaries).

## Production Method
- Bootstrap Training:
  - Automatically samples training observations from historic UKCEH maps (primarily LCM2015) to bootstrap training data for subsequent maps.
  - Uses majority signal from 2017–2019 bootstrap sources to train RF classifiers.
- Random Forest classification:
  - RF classifier trained on balanced samples (equalizing class representation) to improve detection of rarer classes.
  - Production software integrates Weka, PostGIS, and GDAL (open source tools).
- Sentinel-2 Seasonal Composite Images:
  - Classification Scenes built from median Sentinel-2 TOA reflectance per season (winter, spring, summer, autumn) at 20m resolution.
  - Seasonal composites combined with 20m Context Rasters to form Classification Scenes.
- Context Rasters:
  - 20m context layers (e.g., height, aspect, slope, distance to roads/buildings/coast, Foreshore, tidal water, urban/woodland masks) to reduce spectral confusion.
- Classification Scenes:
  - Great Britain: 100x100 km tiles used to create 36-band Seasonal Composite Images; 74 overlapping GB scenes classified independently and then reconciled.
  - Northern Ireland: single 43-band classification scene per year determined by the NI landmass boundary.
- UKCEH Land Parcel Spatial Framework:
  - Fixed framework (same parcels as LCM2015) used to summarise 20m Classified Pixels into Land Parcels (minimum mapping unit ~0.5 ha).
  - GID identifiers are unique but do not match LCM2015 parcel IDs; parcel-level comparisons require spatial overlap rather than ID matching.
- Validation approach:
  - UK-scale validation using GB countryside survey 2019 data, National Forest Inventory data, IACS, and bespoke validation points (22,325 points).
  - Reported overall accuracies: LCM2017 ~78.6%, LCM2018 ~79.6%, LCM2019 ~79.4%.
  - Validation data are not perfect ground truth; conversions between classes and differing purposes introduce uncertainty.

## Validation and Accuracy
- Validation dataset: 22,325 points across GB/NI; cross-checked with LCM parcels.
- Reported accuracy:
  - LCM2017: 78.6% overall.
  - LCM2018: 79.6% overall.
  - LCM2019: 79.4% overall.
- Notes:
  - The same validation dataset was used for all three products; currency relative to each product varies.
  - Some validation observations may be misclassified due to differences between UKCEH classes and validation sources; results are indicators of performance, not absolute truth.
  - Full correspondence tables and Appendix 4 provide detailed validation results.

## Bootstrap Training, Land Parcels, and Parcel Identifiers
- Bootstrap Training origins:
  - Based on UKCEH LCM2015 bootstrap observations; LCM2015 itself drew from 1990–2007 data plus manual observations.
  - For 2017–2019, bootstrap samples drawn from high-purity parcels (purity ≥ 99%) in LCM2015.
- Land Parcel framework:
  - Framework unchanged in geometry from LCM2015, but storage/indexing reorganised for faster processing.
  - gid values do not match LCM2015 parcels; comparisons between 2017–2019 and 2015 must use spatial overlap or the new gid, not cross-year IDs.

## Classification Scenes and Coverage
- GB:
  - 100x100 km tiles used to extract 36-band Seasonal Composite Images; 74 GB Classification Scenes classified independently with overlap to ensure training diversity.
- NI:
  - Single 43-band classification scene per year (36 spectral bands + 7 context layers) based on minimum bounding rectangle of NI land mass.
- Data extents and pixel details:
  - 20m Classified Pixels preserve detailed heterogeneity; 25m Land Parcels summarise within the Land Parcel Spatial Framework.
  - 1km rasters summarise parcel data into three products: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band).

## Appendices and Class Definitions (Key Points)
- Appendix 1: Notes on UKCEH Land Cover Classes (definitions and detection considerations).
  - Examples include Broadleaved/Coniferous Woodland; Arable and Horticulture; Various Grassland types; Wetlands (Fen, Marsh, Swamp, Bog); Coastal and Littoral classes; Built-up Areas (Urban vs Suburban); Saltmarsh; and Inshore Sublittoral Sediment.
  - Highlights spectral confusions and the role of Context Rasters in improving discrimination.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions aligned with field-based habitat concepts).
- Appendix 3: RGB color recipe for displaying UKCEH Land Cover Classes (useful for visualization).
- Appendix 4: Validations and confusion matrices (LCM2017, LCM2018, LCM2019) including producer’s and user’s accuracies by class; overall accuracy around ~79%.
- Appendix 5: Full list of datasets per year and per product (e.g., 20m Classified Pixels GB/NI, Land Parcels GB/NI, 25m Rasterised Land Parcels GB/NI, etc.).

## Technical Details
- Coordinate Systems:
  - Great Britain: British National Grid (EPSG: 27700).
  - Northern Ireland: Irish Grid (TM75, EPSG: 29903).
- Dataset characteristics:
  - 21 classes; 21-band (or higher) products with detailed per-pixel and per-parcel attributes.
  - 20m Classified Pixels include per-pixel class and confidence (band 2: probability scaled to 0–100).
  - 25m Land Parcels include parcel-level histograms, modal class, confidence, purity, and related attributes.
  - 1km products provide per-1km grid summaries: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band).

## Future Plans and Accessibility
- Going forward: plan to release a new LCM annually (LCM2020 planned; subsequent years planned similarly).
- Potential enhancements under consideration:
  - Increasing satellite data inputs (e.g., expanding use of alternative optical sources, exploring Sentinel-1 radar data, gap-filling for seasonal completeness).
  - Possible refinement of the UKCEH Land Parcel Spatial Framework to adapt to higher-resolution data and different MMU considerations.
- Accessibility:
  - Datasets are structured in year-specific packages with GB and NI components; the gid-based parcel identifiers enable longitudinal analyses, with caveats about cross-year ID matching.