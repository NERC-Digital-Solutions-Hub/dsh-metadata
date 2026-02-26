# The UKCEH Land Cover Map for 2021

## Overview
- LCM2021 is the ninth UK land cover map produced by UKCEH, aiming to support monitoring of state and change in the UK countryside.
- Product consists of six datasets: three for Great Britain (GB) and three for Northern Ireland (NI) including 10 m classified pixels, land parcels, and 25 m rasterised land parcels.
- Annual production with automatic methods; formal validation reports overall accuracy of 82.6%.

## Data structure and datasets
- 10 m Classified Pixel datasets
  - Generated from multiple Classification Scenes; Random Forest yields a most-likely land cover class per pixel.
  - Band 1: UKCEH Land Cover Class identifier; Band 2: associated class probability/confidence.
  - 10 m pixels are not generalised by the Land Parcel Spatial Framework to preserve fine, narrow features; validation was performed against the Land Parcel dataset.
- Land Parcel datasets
  - Result from intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to produce parcel attributes.
  - Key fields include gid, _hist (pixel-class frequency per parcel), _mode (dominant class), _conf (mean class-membership probability), _stdev, _agg (aggregate class), _n (number of 10 m pixels intersecting the parcel).
- 25 m Rasterised Land Parcel datasets
  - Rasterised representation of parcels at 25 m resolution; three-band raster carrying per-parcel dominant land cover (_mode), _conf, and _purity.
- 1 km raster products
  - Summary products derived from the 25 m raster: dominant cover at 1 km (21-class and 10-class aggregates) and percentage cover at 1 km (21 classes and 10 aggregates).
  - Percentage values are rounded; coastal pixels may sum to less than 100% due to partial coverage.
- 10 m Seasonal Composite Images and Context Rasters
  - Seasonal composites created from Sentinel-2 data (four seasons) with 10 m resolution; bands 2,3,4,5,6,7,8,8A,11,12 used; includes occasional null gaps.
  - Context Rasters (GB: 10 layers; NI: 9 layers) to reduce spectral confusion (e.g., height, slope, distance to roads/coast, urban masks, etc.).
- Classification Scenes
  - GB: grid of tiles (~100 x 100 km) used to select 50-band Seasonal Composite Images plus context rasters; 32 Classification Scenes cover GB.
  - NI: a single 40-band Sentinel-2 Seasonal Composite Image plus NI Context Rasters; 49-band Classification Scene.
- The UKCEH Land Parcel Spatial Framework
  - Framework with minimum parcel size ~0.5 ha (MMU); parcels represent discrete real-world units (fields, parks, urban areas, etc.) and help reduce classification noise.
  - Unique parcel identifiers (gid) do not match those from LCM2015; spatial overlap comparisons may require spatial rather than identifier matching.

## Production methodology
- Bootstrap Training
  - Automatic training process that uses historic land cover maps as training data, reducing need for new field data.
  - Training parcels filtered to >80% purity and consistent class across LCM2018–2020; used to sample pixels for RF training.
- Random Forest classification
  - RF classifier trained with balanced samples (10,000 per bag) to ensure equal representation of classes.
  - Custom UKCEH software integrates WEKA with PostGIS and GDAL; targets high-throughput, repeatable classification.

## Data processing workflow
- Seasonal Composite Images (Sentinel-2)
  - Surface reflectance resampled to 10 m; four seasonal composites created to capture phenology.
- Context Raster integration
  - Ten GB context rasters (e.g., height, aspect, slope, distance to buildings/roads/sea) and NI equivalents used to improve discrimination.
- Classification Scenes
  - GB tiles processed independently to create full GB coverage; NI processed as a single scene.
- Parcel framework and rasterization
  - Land Parcel Spatial Framework used to generate parcel attributes and to create 25 m rasterised parcels from 10 m pixel classifications.

## Relationship to UKCEH Land Cover Classes and BAP Broad Habitats
- UKCEH 21 Land Cover Classes are aligned with BAP Broad Habitats but not identical; some adaptations exist to accommodate remote sensing capabilities.
- Appendices provide mappings between UKCEH classes, BAP Broad Habitats, and derived Aggregate Classes, including notes on specific class splits and potential spectral confusion (e.g., Bracken vs Acid Grassland; Heather vs Heather Grassland; Saltwater vs Freshwater).
- Acknowledges ongoing challenges in separating certain habitats spectrally, and the role of context rasters in improving detection for several classes.

## Validation and accuracy
- Validation dataset: 35,182 points across all 21 classes, derived from GB countryside surveys, National Forest Inventory, Rural Payments data, and manual interpretation.
- Overall accuracy: 82.6% (95% CI: 82.19%–82.99%).
- Validation procedure ties to the 25 m rasterised parcel datasets; accuracy metrics include class-level user’s and producer’s accuracy figures.

## Practical considerations for GIS use
- 10 m Classified Pixels: high detail and spatial precision but come with caveats about not being validated against the 10 m product itself; suitable for specialist users aware of this limitation.
- Temporal and change-detection utility: annual updates help separate real change from random classification noise; early release of a time-series approach supports monitoring state and change.
- Data formats and coordinates
  - GB: British National Grid (EPSG 27700)
  - NI: Irish Grid (TM75, EPSG 29903)
  - Datasets come with structured attributes and metadata (e.g., gid, _hist, _mode, _conf, _purity, etc.).
- Colour schemes
  - Appendix 5 and 6 provide recommended colour recipes for displaying UKCEH Land Cover Classes, including color-blind friendly options.

## Additional notes
- Official dataset names are listed per GB and NI in the documentation.
- Appendices cover detailed class definitions, relationships to BAP Broad Habitats, and full dataset correspondence matrices and color mappings for end-user visualization.