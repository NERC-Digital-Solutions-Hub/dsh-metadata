# The UKCEH Land Cover Map for 2021

## Overview and aims
- UKCEH LCM2021 is the ninth UK land cover map, produced annually to support monitoring of state and change in the countryside.
- Product consists of six geospatial holdings across Great Britain and Northern Ireland: three core datasets plus derived products, described below.
- Purpose is to describe data production, validation, and accuracy to help users make informed decisions about current and future applications.
- 21 UKCEH Land Cover Classes are aligned with Biodiversity Action Plan (BAP) Broad Habitats definitions, with careful notes to reduce ambiguity between classifications.

## Product suite and datasets
- Core geospatial holdings (GB and NI):
  - 10 m Classified Pixel datasets
  - Land Parcel datasets
  - 25 m Rasterised Land Parcel datasets
- Derived products and additional outputs:
  - 1 km dominant and percentage-cover products for both classes and aggregates
  - Seasonal Composite Images and Context Rasters used for classification
- Data extents and coordinate systems:
  - Great Britain: EPSG: 27700 (British National Grid)
  - Northern Ireland: EPSG: 29903 (TM75 Irish Grid)
- Appendix 3 lists dataset names for GB and NI across 10 m, Land Parcel, and 25 m rasters.

## How LCM2021 is produced
- Classification approach:
  - Bootstrap Training: uses historic LCM2018–LCM2020 land parcels (filtered for >80% purity and consistent class) as training data to sample pixels from Classification Scenes.
  - Random Forest classifier trained with balanced bootstrap samples to prevent bias toward common classes.
- Data inputs:
  - Classification Scenes created from four Seasonal Composite Images ( Sentinel-2 ) plus 10 Context Raster layers to reduce spectral confusion.
  - Seasonal data: four-season Sentinel-2 reflectance per scene, with some gaps due to cloud that are tolerated by the classifier.
  - Context Raster layers include terrain (Height, Aspect, Slope) and proximity masks (distance to buildings/roads/sea/freshwater), foreshore and tidal masks, and woodland mask (GB) plus NI equivalents.
- Classification Scenes:
  - GB is divided into 32 tiles; NI uses a single 49-band scene for Northern Ireland.
  - Each Scene is trained and classified independently; results are mosaicked into national outputs.
- UKCEH Land Parcel Spatial Framework:
  - Parcels have a minimum area of ~0.5 hectares (MMU).
  - Parcels are used to organise 10 m pixels and support change detection across time.

## Validation and accuracy
- Validation dataset: 35,182 points covering all 21 classes, compiled from GB countryside surveys, National Forest Inventory data, Rural Payments data, and bespoke validation points.
- Overall accuracy: 82.6% with 95% CI of 82.19%–82.99%.
- Appendix 4 provides detailed confusion matrices, producer’s accuracy, user’s accuracy, and per-class statistics.

## The 10 m Classified Pixel datasets
- Description:
  - Generated from multiple Classification Scenes; each pixel has a class ID and a confidence/probability value.
  - First band: UKCEH Land Cover Class ID; second band: probability/confidence.
- Key considerations:
  - Not generalised by the UKCEH Land Parcel Spatial Framework, preserving fine landscape features (including sub-0.5 ha patches).
  - Recommended for specialist users who understand the implications of not generalising to the parcel framework.
- Validation basis:
  - Validation is performed against the 25 m Land Parcel dataset, not directly against the 10 m pixel dataset.

## The Land Parcel datasets
- Description:
  - Created by intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to produce parcel-level attributes.
- Attributes (example):
  - gid (unique parcel ID)
  - _hist (history of land cover frequencies within parcel)
  - _mode (dominant land cover within parcel)
  - _purity (percentage of parcel pixels matching the modal class)
  - _conf (mean classification confidence)
  - _stdev (stdev of _conf)
  - _agg (aggregate class mapping to UKCEH/BAP)
  - _n (number of 10 m pixels intersecting the parcel)
- MMU and interpretation:
  - Land parcels are generally >0.5 ha; parcels typically dominated by a single land cover type.
  - Parcel-based organization supports change detection over time and reduces classification noise.

## The 25 m Pixel Rasterised Land Parcel datasets
- Description:
  - Rasterised version of Land Parcel outputs at 25 m resolution.
  - Three-band rasters carry per-parcel: dominant land cover (_mode), mean confidence (_conf), and parcel purity (_purity).
- Visualization:
  - Provides a compact representation suitable for regional analyses and compatibility with coarser scales.

## 1 km raster products
- Summary products derived from the 25 m data:
  - Dominant cover at 1 km for LCM2021 classes (1-band)
  - Dominant cover at 1 km for LCM2021 Aggregate classes (1-band)
  - Percentage cover at 1 km for LCM2021 classes (21 bands)
  - Percentage cover at 1 km for LCM2021 Aggregate classes (10 bands)
- Note on sums:
  - Percentage values are integers and may not sum exactly to 100 due to rounding, especially near coast where area is mixed and some pixels fall below 1% thresholds.

## Seasonal Composite Images and context rasters
- Seasonal composites:
  - Derived from Google Earth Engine; Sentinel-2 data reprojected to 10 m; four seasons provide phenological detail.
  - Occasional null data due to cloud cover; the classifier tolerates partially complete spectral information.
- Context rasters:
  - GB: terrain (Height, Aspect, Slope), proximity to buildings/roads/sea/freshwater, foreshore mask, tidal mask, woodland mask.
  - NI: terrain (Height, Aspect, Slope), urban mask, distances to coast, freshwater, road, plus foreshore and tidal masks.
- Purpose:
  - Context rasters are designed to reduce spectral confusion (e.g., bare rocks vs. urban surfaces) and improve class separation.

## Classification scenes and workflow
- GB classification tiles:
  - 32 scenes covering GB land surface; each scene processed independently with tailored training data.
- NI classification scene:
  - Single 49-band scene for Northern Ireland.
- Data processing tools:
  - Bespoke UKCEH software integrating Weka, PostGIS, and GDAL (open source).

## The UKCEH Land Parcel Spatial Framework
- Historical lineage:
  - Originally developed for LCM2007; minor updates since LCM2015.
- Identifier changes:
  - Parcel gid values do not match LCM2015; cross-year parcel-ID-based comparisons require spatial overlap methods.
- MMU details:
  - Parcels designed to represent discrete real-world units (fields, parks, urban areas, etc.) and typically dominated by a single land cover class.

## Data governance, limits, and use considerations
- Strengths for data stewards:
  - Clear documentation of methods (Bootstrap Training, RF), validation, and dataset extents.
  - Detailed class definitions and links to BAP Broad Habitats to support interdisciplinary use.
  - Annual cycle enables change detection and temporal consistency assessment.
- Limitations and caveats:
  - 10 m Classified Pixels are not validated against the Land Parcel Spatial Framework; users should be aware of the difference when interpreting results.
  - Some classes (e.g., Saltwater vs Freshwater; Saltmarsh; Fen, Marsh and Swamp; Bog) show inter-class confusion and may be underestimated in small patches below the MMU.
  - Saltwater and coastal classifications use context rasters and may have coastal- and tide-related misclassifications during varying tidal conditions.
  - Comparison with previous years (e.g., LCM2015) may require spatial overlap methods due to changes in parcel identifiers.
- Data provenance and reproducibility:
  - Data rely on Sentinel-2, high-resolution terrain/open data context rasters, and UKCEH’s open-source toolchain; explicit references and appendices support reproducibility and interpretation.

## Appendices and display considerations
- Appendix 1 and 2: Detailed notes on UKCEH Land Cover Classes and mapping to UK BAP Broad Habitats, including nuances and potential ambiguities.
- Appendix 3: Full list of datasets per UKCEH LCM2021.
- Appendix 4: Comprehensive correspondence matrices (confusion matrices) between Land Cover Classes and observed classifications.
- Appendix 5 and 6: Colour recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly) to aid consistent visualization and interpretation.

## Practical takeaways for Data Stewards
- Document methodology:
  - Include Bootstrap Training and RF model details, Seasonal Composites, Context Rasters, MMU, and validation approach in metadata.
- Ensure data interoperability:
  - Note differences in parcel IDs across years; provide crosswalks or spatial-overlap-based comparators if longitudinal analyses are required.
- Communicate usage guidance:
  - Emphasize that 10 m pixels are high-detail but not validated against the parcel framework; provide user guidance on when to use 10 m vs 25 m vs 1 km products.
- Quality and governance:
  - Leverage 35k validation points to assess class-level accuracy; monitor per-class confusion via Appendix 4 when applying the data for decision-making.
- Update and stewardship:
  - Acknowledge annual updates; consider re-applying improvements across the catalogue if methodological enhancements achieve substantial accuracy gains.