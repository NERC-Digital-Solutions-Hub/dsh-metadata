# The UKCEH Land Cover Map for 2021

- The user guide for the UKCEH Land Cover Map for 2021 (LCM2021) describes the product, data production, validation, and accuracy to help users apply the data effectively.
- LCM2021 is the ninth UK land cover map, providing 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats (BAP). It supports annual monitoring and change detection, with an emphasis on temporal consistency and comparable change signals across years.
- The dataset suite is designed to support broad use cases from policy to environmental monitoring, including potential co-ownership of data products and collaboration within the data community.

## Data Products and Structure

- LCM2021 comprises six geospatial datasets distributed across Great Britain (GB) and Northern Ireland (NI):
  - 10 m Classified Pixel datasets (GB and NI)
  - Land Parcel datasets (GB and NI)
  - 25 m Rasterised Land Parcel datasets (GB and NI)
  - 1 km Summary Raster datasets (GB and NI)
- Key technical details:
  - 10 m Classified Pixels: two-band product per region (GB/NI) with the first band = most likely UKCEH Land Cover Class, second band = classification confidence.
  - 25 m Rasterised Land Parcels: three-band raster per land parcel (dominant land cover class [mode], conf, purity).
  - 1 km Summary Rasters: per 1 km pixel products summarising dominant class and percentage cover for both classes and aggregates (with rounding that can cause minor summation differences near 100%).
  - Coordinate systems: GB uses British National Grid (EPSG 27700); NI uses Irish Grid (EPSG 29903). Pixel resolutions: GB NI include 10 m and 25 m products; 1 km summaries cover both GB and NI.
- Dataset naming/branding and official nomenclature are detailed in Appendix 3.

## Data Production and Methodology

- Seasonal Composite Images:
  - Generated from Google Earth Engine using Sentinel-2 surface reflectance data resampled to 10 m.
  - Four seasonal composites (January–March, April–June, July–September, October–December) using 10 Sentinel-2 bands (2, 3, 4, 5, 6, 7, 8, 8A, 11, 12).
  - Some seasonal data gaps due to cloud cover; the classifier is designed to tolerate partially complete spectral information.
- Context Rasters:
  - 10 m Context Rasters are used to reduce spectral confusion. GB uses terrain-derived (height, aspect, slope), proximity to features (buildings, roads, sea, freshwater), a foreshore mask, tidal mask, and a woodland mask.
  - NI uses height, aspect, slope plus urban mask, distance to coast, distance to freshwater, distance to road, foreshore, and tidal masks.
- Classification Scenes:
  - GB is partitioned into 32 Classification Scenes (tiles ~100 x 100 km) from a modified OS grid; each scene is trained and classified independently to balance regional phenology and processing efficiency.
  - NI uses a single 49-band Classification Scene (40-band Sentinel-2 Seasonal Composite plus NI context rasters).
- Bootstrap Training and Random Forest:
  - Bootstrap Training uses automatic training data derived from historic LCM maps (LCM2018–LCM2020). Training parcels must have >80% purity and the same class across three years.
  - A Random Forest classifier is trained with 10,000 samples per class (with replacement) to balance class representation and mitigate dominance by common classes.
  - The production pipeline blends Bootstrap Training with RF classification in a bespoke software stack (WEKA-based, PostGIS, GDAL).
- UKCEH Land Parcel Spatial Framework:
  - A long-running framework with ~0.5 ha minimum mapping unit (MMU) used to convert 10 m pixels into land parcels for cleaner product interpretation and change detection.
  - Parcel identifiers (gid) differ from LCM2015, which may affect cross-year parcel-based comparisons.
- Validation and Data Quality:
  - Formal validation used 35,182 reference points spanning all 21 classes, yielding an overall accuracy of 82.6% (95% CI: 82.19%–82.99%).
  - Validation data come from GB countryside surveys, National Forest Inventory data, Rural Payments Agency data, and bespoke validation points.

## Data Details and Product Descriptions

- 10 m Classified Pixel datasets:
  - Generated from classified Classification Scenes; the primary band contains the most likely UKCEH Land Cover Class, with a second band indicating confidence.
  - Not generalized to Land Parcel Spatial Framework, preserving fine-scale features below the MMU; recommended for specialist users who understand the implications for downstream analysis.
- Land Parcel datasets:
  - Intersection of 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to produce parcel-level attributes (described in Table 3).
  - Includes parcel-level statistics such as mode, confidence, purity, and aggregation details.
- 25 m Rasterised Land Parcel datasets:
  - Rasterised representation of land parcels at 25 m resolution, carrying three per-parcel attributes (mode, conf, purity).
- 1 km Summary rasters:
  - Coarser-scale products summarising dominant class and percentage cover per 1 km pixel for both 21 classes and 10-class aggregates.
  - Useful for broad-scale mapping, trend analysis, and cross-walking with coarser-resolution data.
- Seasonal, Context, and Classification Scene design:
  - Seasonal composites provide temporal signals for improved discrimination of vegetation types.
  - Context rasters provide auxiliary information to reduce spectral confusion between spectrally similar classes.
  - Scene tiling reduces processing complexity and improves local classifier performance.

## Relationship to BAP Broad Habitats and Class Definitions

- LCM2021 uses 21 UKCEH Land Cover Classes aligned, where feasible, with Biodiversity Action Plan (BAP) Broad Habitats. Some mappings are not exact matches to BAP, and certain BAP terms are italicised to indicate cross-referencing between classifications.
- Appendix 1 and Appendix 2 provide detailed notes on the mapping between UKCEH Land Cover Classes and BAP Broad Habitats, including handling of specific edge cases (e.g., Bracken, Heather, Bog, Fen, Marsh, Swamp, Saltmarsh, and Urban vs Suburban distinctions).

## Data Use, Access, and Limitations

- Annual production aims to maximize temporal consistency and change detection capabilities, enabling differentiation between random classification errors and real land-cover change.
- The 10 m Classified Pixel data preserves fine landscape features but has not undergone the same formal validation as the 25 m Land Parcel dataset; users should be aware of this when interpreting results.
- Parcel identifiers differ from earlier LCM versions, complicating cross-year parcel-based comparisons without spatial overlap-based analysis.
- The report emphasizes the ongoing development of methods and potential re-application of improvements across the full catalogue if new methods yield significant accuracy gains.

## Display and Accessibility

- Appendix 5 and Appendix 6 provide recommended color schemes for displaying UKCEH Land Cover Classes, including color-blind friendly options, and accompanying QGIS symbology files to facilitate map production and visual interpretation.

## Validation, References, and Further Details

- Validation reference framework includes GB countryside survey data, National Forest Inventory data, Rural Payment Agency data, and bespoke validation points.
- Document references include foundational works on Random Forests, ensemble learning, and prior LCM methodologies. Appendices provide in-depth notes on class definitions, spectral confusion, and recommended usage.

- The guide notes that UKCEH intends to continue evolving methods, ensuring annual maps maximize temporal consistency, comparability, and the utility for change detection and environmental objectives.