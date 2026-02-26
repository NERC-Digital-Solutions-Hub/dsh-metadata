# The UKCEH Land Cover Map 2023

## Purpose and scope
- UKCEH Land Cover Map 2023 (LCM2023) is the eleventh UK land cover map, providing seven datasets (three for Great Britain and three for Northern Ireland) plus a unified 1 km summary raster.
- Land cover is represented by 21 UKCEH Land Cover Classes, derived from Biodiversity Action Plan (BAP) Broad Habitats, using automated classification of Classification Scenes created from Sentinel-2 seasonal composites and contextual rasters.
- Classification uses Bootstrap Training with a Random Forest (RF) to enable yearly production and improve temporal consistency and change detection. Formal validation reports an overall accuracy of 83%.

## Key concepts and terminology
- Bootstrap Training: automatic generation of training sets from historical land maps to train RF classifiers without new field data.
- Classification Scene: multi-layer raster combining Seasonal Composite Images and Context Rasters used for classification.
- Seasonal Composite Image: four-season, multi-band Sentinel-2 reflectance data used for temporal information.
- Context Rasters: 10 m layers (and NI equivalents) to reduce spectral confusion (e.g., terrain, distance to features, coastal masks).
- UKCEH Land Parcel Spatial Framework: vector framework delimiting land parcels (~0.5 ha MMU) to aggregate 10 m pixels and support change detection.

## Datasets and product suite
- 10 m Classified Pixel datasets (GB and NI): per-pixel land cover class with a second band indicating classification confidence. Not generalised by the Land Parcel Framework to preserve fine detail (e.g., narrow features).
- 25 m Rasterised Land Parcel datasets (GB and NI): parcels with three attributes: _mode (dominant class), _conf (mean confidence), _purity (modal class purity).
- Land Parcel datasets (vector): Land Parcel Spatial Framework used to structure classification outputs.
- 1 km Raster products: summary rasters providing dominant class, class percentage cover (21 bands), and aggregate percentage cover (10 bands); rounding can cause sums to deviate from 100%.
- Seasonal Composite Images: four 3-month periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) from Sentinel-2, with occasional null data during cloud gaps; 12 Sentinel-2 bands used (bands 2–12 with specific resolutions).
- Context Rasters: GB uses 10m terrain (height, aspect, slope), proximity masks (buildings, roads, tidal water, freshwater), foreshore and water-related masks; NI uses a subset including an urban mask and distance to coast/road/freshwater.
- Classification Scenes: GB classified in 32 tiles (~100 x 100 km each); NI uses a single scene; NI input comprises 49 bands (40-band Sentinel-2 plus context rasters).
- Pixel and parcel formats: 10 m classified pixels (2 bands), 25 m rasterised land parcels (3 bands), and vector land parcels with their own attributes.
- 1 km summary rasters: GB and NI combined for cross-regional analyses.

## Production workflow and methodology
- Data inputs: Sentinel-2 Seasonal Composite Images plus Context Rasters; classification scenes assembled per national tile grid.
- Bootstrap Training: historic LCM maps (LCM2020–LCM2022) provide training observations; pixels with >80% probability and consistent across three years are used to bootstrap new maps; class balance is achieved by drawing 10,000 samples per class.
- Random Forest classification: supervised RF model trained on Bootstrap Training pixels to produce 10 m classified pixel outputs.
- Software stack: bespoke UKCEH pipeline integrates WEKA, PostGIS, and GDAL with open-source components.
- Output validation: compared against a validation set of 33,107 points across 21 classes; overall accuracy 83%.

## Validation and accuracy
- Formal validation total: 83% overall accuracy at full thematic detail (Appendix 4 provides confusion matrices and per-class metrics).
- Validation dataset composition includes GB countryside surveys, National Forest Inventory data, Rural Payments data, and bespoke validation points.

## Data accessibility, routing, and citation
- Each LCM2023 dataset has its own DOI; data are archived at NERC EDS Environmental Information Data Centre.
- Citations and DOIs are provided for all products (10 m classified pixels GB/NI, 25 m land parcels GB/NI, 1 km rasters, and related datasets).
- The document notes that minor methodological changes between years can yield year-to-year differences beyond real land-cover change (disclaimer).

## Known issues and limitations
- Some vector land parcel polygons are missing, causing nodata gaps in corresponding 25 m parcel rasters; impact on 1 km products is negligible; 10 m classified pixels are unaffected.
- Parcel identifiers (gid) do not align with LCM2015; cross-year parcel-ID comparisons may require spatial overlap rather than ID matching.
- Spectral confusion remains between certain land-cover types (e.g., various grassland types, bog, fen, heather); Appendix 4 (confusion matrices) documents observed misclassifications.
- Saltwater vs freshwater discrimination near coasts can be challenging; coastal pixels are lower priority and may show reduced accuracy in Saltwater.
- The “seasonal gaps” in some Seasonal Composite Images are tolerated by the classifier, but gaps persist in some tiles.

## Appendices and supplementary materials
- Appendix 1: Notes on UKCEH Land Cover Classes with respect to BAP Broad Habitats.
- Appendix 2: Summary of Biodiversity Action Plan Broad Habitats definitions.
- Appendix 3: Full list of LCM2023 datasets with DOIs.
- Appendix 4: Detailed correspondence (confusion) matrices between classified classes.
- Appendix 5: Recommended colour recipe for displaying UKCEH Land Cover Classes (including a QGIS .qml file).
- Appendix 6: Colour-blind friendly color recipe and corresponding .qml file.

## Practical guidance for analysts
- Use 10 m Classified Pixel data for high-resolution mapping, with caution about avoiding reliance on exact parcel IDs for longitudinal analyses.
- Use 25 m Land Parcel data for generalized change detection within the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
- Leverage the 1 km summary rasters for broad-scale assessments and cross-region comparisons, mindful of rounding effects.
- Consider contextual rasters and seasonal composites to resolve spectral confusion, especially in heterogeneous landscapes.
- When comparing maps across years, rely on the Bootstrap Training framework and the annual time-series to distinguish real changes from methodological differences.
- Cite DOIs provided for each dataset when using or publishing analyses based on LCM2023.