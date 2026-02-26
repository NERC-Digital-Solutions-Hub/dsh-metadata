# The UKCEH Land Cover Map 2021

## Overview
- UKCEH LCM2021 is the ninth UK land cover map, produced annually to monitor state and change of the countryside.
- Provides 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) for Great Britain and Northern Ireland, using a multi-source, automated workflow.
- Classification uses Seasonal Sentinel-2 composites plus 10 Context Raster layers; aims to reduce spectral confusion and enable change detection with annual updates.
- Formal validation reports overall accuracy of 82.6% (95% CI: 82.19%–82.99%).

## Data products and structure
- Three core geospatial datasets per region (Great Britain and Northern Ireland), totaling six datasets:
  - 10 m Classified Pixel datasets
  - Land Parcel Spatial Framework-based datasets (GB and NI)
  - 25 m Rasterised Land Parcel datasets
  - Additionally, 1 km raster products summarize the 25 m data (dominant class and percentage cover for both classes and aggregates)
- Seasonal Composite Images
  - Four-season Sentinel-2-based spectral composites (January–March, April–June, July–September, October–December) resampled to 10 m; 50-band scenes plus context rasters
  - Minor data gaps (clouds) are tolerated; classification can operate with partial spectral information
- Context Rasters
  - Great Britain: 10 contextual layers (e.g., height, aspect, slope; distance to buildings/roads/sea/freshwater; foreshore mask; tidal water; woodland)
  - Northern Ireland: 7 contextual layers (similar themes plus urban mask and distance to coast/roads)
- Classification Scenes and Tile System
  - GB: grid of ~100 x 100 km tiles (with some enlarged tiles for sea-dominated areas)
  - NI: single Classification Scene covering the landmass
  - 50-band Seasonal Composite Images per GB scene; 49- to 50-band setup for NI
- UKCEH Land Parcel Spatial Framework
  - Parceled representation of land units (minimum ~0.5 ha; fixed structure for change detection)
  - Parcel IDs (gid) may not match LCM2015 IDs due to framework changes
- Output formats and metadata
  - 10 m Classified Pixels: two-band raster (class ID, classification probability)
  - 25 m Rasterised Land Parcels: three-band rasters (dominant class mode, conf, purity)
  - 1 km products: dominant class (1-band) and percentage cover (21 bands for classes; 10 bands for aggregates)
  - Coordinate systems: GB (EPSG 27700); NI (EPSG 29903)
- Data availability and dataset naming
  - Official dataset names follow UKCEH LCM2021 catalog (classified pixels, land parcels, rasterised parcels, NI/GB distinctions)

## How the data were produced
- Bootstrap Training
  - Automatic training data generation using historic land-cover maps (LCM2018–LCM2020), filtered to parcels with >80% purity and consistent class across years
  - Enables large, wall-to-wall training data without new field collection
- Random Forest classification
  - Balanced sampling: 10,000 samples per class per classification scene
  - Uses a bespoke pipeline integrating Weka, PostGIS, and GDAL
- Validation
  - 35,182 validation points across all 21 classes
  - Validation data drawn from GB countryside survey, National Forest Inventory, Rural Payments Agency, and bespoke validation points
- Purpose and use-case guidance
  - 10 m Classified Pixels preserve fine-grained features (e.g., narrow patches) but are not generalised by the Land Parcel framework
  - Outputs intended for specialist users who understand potential frame-related implications

## Class relationships and interpretation
- UKCEH Land Cover Classes and UK BAP Broad Habitats
  - 21 UKCEH classes relate to BAP Broad Habitats but are not identical
  - Some distinctions are clarified in Appendices; BAP terms are italicised when referenced
  - Relationships summarized in Appendix 1–2, with notes on particular splits and cross-walking (e.g., Urban vs Suburban, Freshwater vs Saltwater)
- Use for change detection
  - Annual maps help separate random classification noise from real change (errors tend to flicker; persistent changes indicate real trends)

## Practical guidance for data users
- Output interpretation
  - 10 m Classified Pixels: primary class ID and associated confidence/probability per pixel
  - 25 m Land Parcel rasters: parcel-level summaries (mode, confidence, purity) and statistics per parcel
  - 1 km products: per-pixel class composition and dominance, with sums that may not be exactly 100 due to rounding
- Suitability
  - 10 m pixel data are best for detailed mapping needs and areas where MMU constraints of parcel data would remove detail
  - Parcel-based products provide a stable framework for temporal comparison and change detection
- Display and accessibility
  - Colour schemes and colour-blind friendly palettes are provided in appendices for mapping outputs
- Limitations and caveats
  - Some spectral confusions persist (e.g., bog vs acid grassland; bracken vs acid grassland; coastal Saltwater vs Freshwater)
  - Saltwater classification near coasts can be influenced by tidal conditions and context rasters
  - NI dataset involves a single Classification Scene; GB uses tiled processing
  - Parcel IDs differ from LCM2015 due to framework changes; cross-year parcel-based comparisons may require spatial overlap rather than ID matching

## Validation metrics at a glance
- Overall accuracy: 82.6% (95% CI: 82.19%–82.99%)
- Validation dataset: 35,182 points across 21 classes
- Producer’s and user’s accuracy matrices available in Appendix 4 (for individual class performance)

## Appendices and supplementary material
- Appendix 1–2: Notes on UKCEH Land Cover Classes and relationships to BAP Broad Habitats
- Appendix 3: Full list of LCM2021 datasets (GB and NI)
- Appendix 4: Correspondence matrices and class-level accuracy details
- Appendix 5–6: Recommended colour recipes for displaying UKCEH Land Cover Classes (including colour-blind friendly options)