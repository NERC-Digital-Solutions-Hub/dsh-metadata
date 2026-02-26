# The UKCEH Land Cover Map for 2022

- The user guide for the UKCEH Land Cover Map for 2022 (LCM2022) describing its purpose, data production, validation, data accuracy, and how to use the datasets effectively.
- LCM2022 is the tenth in a series mapping UK land cover using automatic classification of Sentinel-2 seasonal composites plus contextual information, produced annually to support change detection and environmental objectives.
- Overall validation accuracy is 86.1% at full thematic detail.

## Data products and dataset structure

- 10 m Classified Pixel datasets (GB and NI)
  - Derived from Classification Scenes classified with a Random Forest (RF) and Bootstrap Training.
  - Each pixel has two bands: first band = most likely UKCEH Land Cover Class; second band = confidence/probability for that class.
  - No generalisation with the Land Parcel Spatial Framework to preserve fine landscape details (e.g., narrow patches below MMU).
- Land Parcel datasets
  - Created by intersecting the 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to generate land parcel attributes.
  - Include per-parcel statistics such as hist, mode, purity, conf, n, and an aggregated class (agg).
- 25 m Rasterised Land Parcel datasets
  - Rasterised version of the Land Parcel data at 25 m resolution.
  - Three bands: band 1 = dominant land cover (mode); band 2 = conf; band 3 = purity.
- 1 km raster products
  - Summary rasters produced by aggregating 25 m data to 1 km cells for GB and NI.
  - Products include dominant class (1 band) and percentages for both class and aggregate classes (21 and 10 bands respectively).
  - Percentage totals are rounded; sums may deviate from 100% due to rounding and coastal partial coverage.
- Seasonal Composite Images and Context Rasters
  - Seasonal Composites: Sentinel-2 bands resampled to 10 m; four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with optional nulls for cloud gaps.
  - Context Rasters (GB: 10 rasters; NI: 9 rasters) provide terrain, proximity, and land-cover context (e.g., height, slope, distance to buildings/roads/coast, foreshore masks, etc.).
- Classification Scenes
  - GB uses 32 Classification Scenes (tiles ~100 x 100 km) for full GB coverage; NI uses a single Classification Scene covering the Northern Ireland land mass.
  - Each GB scene is trained and classified independently; NI scene is a single, broader 49-band classification scene (40-band Sentinel-2 Seasonal Composite + NI Context Rasters).
- Spatial framework and extents
  - UK Land Parcel Spatial Framework used to define discrete land parcels (minimum ~0.5 ha) and to structure outputs for change detection.
  - GB and NI coordinate systems differ: GB = British National Grid (EPSG:27700); NI = Irish grid TM75 (EPSG:29903).

## How the data are produced

- Bootstrap Training
  - An automatic training approach that uses historic LCM observations (LCM2019–LCM2021) with >80% probability and consistent class across years to sample training data.
  - Enables training without fresh field data; mitigates the need for labour-intensive pre-processing.
- Random Forest classification
  - RF classifier trained on Bootstrap Training samples; 10,000 samples per bootstrap bag with replacement to balance class representation.
  - Produces the 10 m Classified Pixel product and associated class probabilities.
- Seasonal and contextual inputs
  - Classification Scenes combine Sentinel-2 Seasonal Composite Images (spectral information across four seasons) with Context Rasters to reduce spectral confusion.
- The UKCEH Land Parcel Spatial Framework
  - Parcels are created by generalising national cartography; parcels are designed to represent discrete land units and are used to reduce noise and enable time-series comparisons.

## Data quality, accuracy, and known issues

- Validation
  - 33,107 validation points across 21 LCM classes; overall accuracy 86.1% (full thematic detail).
- Known issues
  - Some polygons are missing from the vector Land Parcel products, causing nodata areas in the 25 m raster parcel dataset (negligible effect on 1 km products; 10 m classified pixels unaffected).
- Method changes
  - Some methodological differences across yearly LCMs can cause small changes beyond real land-cover change; outputs may differ slightly year to year due to method evolution.

## UKCEH Land Cover Classes and BAP relationships

- LCM2022 maps 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats, with careful notes to maintain consistency with earlier products.
- The document explains relationships and occasional distinctions between UKCEH Land Cover Classes and UK BAP Broad Habitats, including when certain classes are split or combined (e.g., Urban vs Suburban; Heather vs Heather grassland; Freshwater vs Rivers/Standing water).
- Appendices provide definitions and mappings to aid interpretation and cross-walking with BAP Broad Habitats.

## Data usage, access, and citation

- DOIs and citations
  - Each LCM2022 dataset has its own DOI and citation (e.g., 10 m Classified Pixels GB/NI, 25 m Rasterised Land Parcels GB/NI, Land Parcels GB/NI, 1 km Summary Rasters GB/NI).
  - Marston et al. (2023) and Marston et al. (2024a–g) provide production method overviews and dataset-specific details.
- User guidance
  - The guide emphasizes using the outputs for “self-serve” data exploration, mapping, and change detection, with notes on data layers, confidence, and how to interpret the class probabilities.
- Data presentation and accessibility
  - Appendix 5 and 6 provide recommended color recipes (including color-blind friendly options) for displaying UKCEH Land Cover Classes in GIS environments (e.g., QGIS).

## Practical considerations for data support and integration

- Temporal context
  - Annual production is intended to help separate real land-cover change from classification noise; random errors are expected to flicker over time.
- Data integration
  - The 10 m pixel data are not generalised to Land Parcels to preserve fine features, while parcel-based analysis benefits from the fixed parcel framework for robust change detection.
- Usage caveats
  - If exact parcel identifiers are needed when comparing with LCM2015, direct id matching may not be straightforward due to changes in the Land Parcel Spatial Framework.
- Glossaries and appendices
  - Appendices provide detailed habitat definitions and mappings to help users interpret the 21 land-cover classes and their BAP broad habitat equivalents.