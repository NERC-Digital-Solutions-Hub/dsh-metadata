# The UKCEH Land Cover Map for 2020

- The LCM2020 product consists of six datasets for GB and Northern Ireland: for each region, a 10m classified-pixels dataset, a classified land parcels dataset, and a 25m pixel rasterised land parcels dataset.

- Purpose: to describe data production, validation, and accuracy to help users apply UKCEH LCM data in current and future work, with an emphasis on enabling informed decisions and change detection over time.

## Data products and structure

- 10m Classified Pixel datasets
  - Created from Classification Scenes using a Random Forest classifier.
  - Each pixel has two bands: the most probable UKCEH Land Cover Class and the associated probability (confidence).
  - Not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine landscape detail; recommended for specialist users.

- Land Parcel datasets
  - Created by intersecting the 10m classified pixels with the UKCEH Land Parcel Spatial Framework.
  - Provide parcel-level attributes for analysis and change detection.

- 25m Rasterised Land Parcel datasets
  - Rasterised representation of land parcels at 25m resolution.
  - Three bands per parcel: dominant land cover (mode), mean probability/confidence (conf), and parcel purity (purity).

- Seasonal Composite Images
  - Sentinel-2 spectral data resampled to 10m, aggregated by season (winter, spring, summer, autumn).
  - Bands 2,3,4,5,6,7,8,11,12 used; cloud gaps represented as nulls.
  - Used to form Classification Scenes with temporal and phenological information.

- Context Rasters
  - 10m context layers to reduce spectral confusion (GB: height, aspect, slope; distance-to-building, road, sea, freshwater; foreshore and tidal masks; woodland mask).
  - NI adds urban mask, distance-to-coast, distance-to-freshwater and distance-to-road.

- Classification Scenes
  - GB: 100x100 km tiles; 36-band Sentinel-2 Seasonal Composite Images plus 10 Context Rasters, creating 46-band GB Classification Scenes; 74 overlapping scenes classified independently with manual precedence for final cut.
  - NI: single 43-band Classification Scene per year, using the NI tile.

- The UK Land Parcel Spatial Framework
  - Based on generalised national cartography with a minimum mapping unit of ~0.5 ha.
  - Designed to binarise and stabilise land cover for change detection; identifiers (gids) differ from LCM2015 for compatibility reasons.

- Bootstrap Training
  - Automatic training data sampled from historical LCMs (LCM2017–2019), filtering to >99% purity across three years.
  - Resulting bootstrap training sets: ~941k GB objects and ~215k NI objects.

- Random Forest classification
  - Balanced training: 10,000 samples per class drawn with replacement from each class in each bag.
  - Implemented with a bespoke pipeline integrating Weka, PostGIS, and GDAL; open-source components.

## Class definitions and relations

- LCM2020 uses 21 UKCEH Land Cover Classes, linked to Biodiversity Action Plan (BAP) Broad Habitats but not identical to them.
- BAP Broad Habitats are italicised when referred to; UKCEH Land Cover Classes are capitalised.
- Appendix 1 and Appendix 2 detail relationships between UKCEH Classes, UK BAP Broad Habitats, and aggregation schemes.
- A generalized UKCEH Aggregate Class set (Land Parcel product) is also provided for users who do not require full thematic detail.

## Validation and accuracy

- Validation approach
  - Compared LCM2020 with countryside survey data (2019/2020), open-source National Forest Inventory data, IACS data, and bespoke validation points.
  - Total validation locations: 34,715.
- Overall accuracy
  - 79.2% at full thematic detail (Appendix 4).
- Validation metrics
  - Producer’s and user’s accuracies vary by class (detailed in Appendix 4); results show reasonable performance across many major classes but highlight some confusion among shrub/grassland, upland vegetation, and coastal/marine categories.

## Data details and access (Appendix 5)

- Datasets by region and type:
  - UKCEH LCM2020 10m Classified Raster Product (GB and NI)
  - UKCEH LCM2020 Land Parcel Product (GB and NI)
  - UKCEH LCM2020 25m Rasterised Land Parcel Product (GB and NI)
- Coordinate systems
  - Great Britain: EPSG 27700
  - Northern Ireland: EPSG 29903
- Pixel resolution
  - 10m for classified pixels
  - 25m for rasterised land parcels
- Band structure
  - 10m Classified Pixels: 2 bands (class, conf)
  - 25m Rasterised Land Parcels: 3 bands (mode, conf, purity)
  - Land Parcel attributes include fields such as _hist, _mode, _purity, _conf, _stdev, _agg, _n
- Note on validation scope
  - Validation conducted against Land Parcel datasets; 10m Classified Pixels were not separately validated against the Land Parcel framework.

## Production notes and interpretation

- Annual production: aims to maximise temporal consistency, comparability, and change detection; continuous methodological improvements considered for future re-application across the catalogue.
- Manual corrections from earlier LCMs are not performed this year to maintain annual production tempo; problems are noted for future method improvements.
- Random errors are expected to be spatially and temporally variable; with time-series, random errors are expected to flicker while real changes persist.

## Practical considerations for analysts

- The 10m Classified Pixel dataset preserves fine landscape detail but has not been validated against the parcel framework; best used by specialists aware of implications of not being parcel-generalised.
- The Land Parcel dataset enables change detection and parcel-level analysis, but gid identifiers do not match LCM2015 if cross-year comparisons are needed.
- The 21-class scheme maps to BAP Broad Habitats with some caveats; for field-like interpretations, refer to the Appendices for class definitions and potential spectral confusions.
- For coastal or upland areas, expect higher confusion among certain vegetation and habitat classes; the inclusion of context rasters mitigates some of these issues.
- Color recipes and display guidelines are provided in Appendix 3 for visualization consistency.