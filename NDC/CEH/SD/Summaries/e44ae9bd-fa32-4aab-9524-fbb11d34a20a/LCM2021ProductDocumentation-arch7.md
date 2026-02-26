# The UKCEH Land Cover Map for 2021

## Overview
- UKCEH LCM2021 is the ninth UK land cover map, produced annually using automated methods.
- 21 UKCEH Land Cover Classes (based on Biodiversity Broad Habitats) classified from Sentinel-2 Seasonal Composite Images plus 10 Context Layers to reduce spectral confusion.
- Production method combines Bootstrap Training with a Random Forest classifier; aims for temporal consistency, change detection, and lower cost of annual updates.
- Validation reports an overall accuracy of 82.6% (95% CI 82.19%–82.99%) at full thematic detail.
- Product suite includes six geospatial datasets (GB and Northern Ireland): three each for 10 m classified pixels, land parcels, and 25 m rasterised land parcels.
- Additional outputs include 1 km raster products summarising 25 m data (dominant and percentage cover).

## Data Product Suite (GB and NI)
- 10 m Classified Pixel datasets
- Land Parcel datasets
- 25 m Rasterised Land Parcel datasets
- 1 km Dominant cover products (class and aggregate)
- 1 km Percentage cover products (class and aggregate)

## Datasets and Dataset Names
- LCM2021 comprises six geospatial datasets across Great Britain and Northern Ireland (GBNI): three per region (10 m classified pixels; land parcels; 25 m rasterised land parcels).
- Appendix 3 lists the official dataset names for GB and NI variants.
- The 1 km products summarize the 25 m raster data (dominant class and percentage cover for both classes and aggregates).

## Data Production and Methods
- Seasonal Composite Images: Derived from Google Earth Engine; Sentinel-2 surface reflectance at 10 m, four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec). Minor gaps due to cloud are tolerated; classification can handle partial spectral information.
- Context Rasters: 10 m context layers to reduce spectral confusion (GB: height, aspect, slope; distance to buildings, roads, sea, freshwater; foreshore and tidal/water masks; woodland mask). NI includes urban mask and distance-to-coast/freshwater/road plus foreshore and tidal masks.
- Classification Scenes: GB classified on a grid of tiles (~100 x 100 km) with 32 scenes; NI uses a single 49-band scene (40 band Sentinel-2 + NI context rasters).
- Bootstrap Training: Automatic training data generated from historic LCM maps (LCM2018–LCM2020). Training parcels must have >80% purity and consistent class across three years. Random Forest classifier trained with 10,000 samples per bag; balanced across classes via sampling with replacement.
- UKCEH LCM Spatial Framework: Land Parcel Spatial Framework (MMU ~0.5 ha) used to aggregate 10 m pixels into parcels; parcel IDs (gid) are used for parcel-level attributes; parcel IDs differ from LCM2015 due to framework updates.
- Validation: 35,182 reference points across 21 classes; results show overall accuracy 82.6%.

## Spatial Framework and Parcel Data
- UKCEH Land Parcel Spatial Framework: generalised land parcels representing discrete units (fields, parks, urban areas, etc.), minimum parcel area ~0.5 ha.
- Parcels facilitate noise reduction and enable change detection; 10 m pixels are intersected with parcels to produce parcel-level attributes.
- Parcel dataset attributes include:
  - gid (unique parcel identifier)
  - _hist (history of class frequencies within parcel)
  - _mode (most frequent parcel class)
  - _purity (dominant proportion of parcel’s modal class)
  - _conf (mean class membership probability within parcel)
  - _stdev (standard deviation of _conf)
  - _agg (aggregate class mapping)
  - _n (number of 10 m pixels within parcel)

## Data Schema and Bands
- 10 m Classified Pixel dataset
  - Band 1: integer UKCEH Land Cover Class identifier (most likely class)
  - Band 2: probability/confidence for the selected class
  - Note: Not generalised by the Land Parcel Spatial Framework; preserves fine-scale features; recommended for specialist users aware of limitations.
- 25 m Rasterised Land Parcel dataset
  - 3-band raster per parcel: band 1 is dominant land cover (mode), band 2 is conf, band 3 is purity.
- Land Parcel dataset (vector)
  - Parcel-level attributes as described above (gid, _hist, _mode, _purity, _conf, _stdev, _agg, _n).

## 1 km Raster Products
- Created by summarising the 25 m raster data to 1 km pixels.
- Products include:
  - Dominant cover at 1 km for LCM2021 classes (1-band)
  - Dominant cover at 1 km for LCM2021 Aggregate classes (1-band)
  - Percentage cover at 1 km for LCM2021 classes (21 bands)
  - Percentage cover at 1 km for LCM2021 Aggregate classes (10 bands)
- Note: Percentage cover values are integers and may not sum exactly to 100 due to rounding; coastal pixels may sum to less than 100 as they may contain sub-100% land cover within a 1 km square.

## Data Accuracy and Validation
- Validation dataset: 35,182 points across all 21 classes.
- Overall accuracy: 82.6% (95% CI 82.19%–82.99%).
- Appendix 4 presents per-class accuracy metrics (user’s and producer’s accuracy) and cross-tabulations with a confusion matrix for GB/NI; results indicate varying class-specific performance, with strongest distinctions for dominant classes and notable confusion among spectrally similar habitats (e.g., various grassland and peat-related classes).

## Usage and Practical Considerations for GIS Specialists
- Resolution and detail:
  - 10 m Classified Pixel dataset preserves fine landscape features; not generalised by the Land Parcel framework.
  - 25 m Rasterised Land Parcel dataset provides parcel-level attributes suitable for change detection over time.
  - The 1 km products are aggregations suitable for regional-scale mapping and quick assessments.
- Time series and change detection:
  - Bootstrap Training uses historic maps to improve consistency across years; annual updates help distinguish real change from random errors.
- Data integration and standards:
  - Datasets come in GB National Grid (EPSG 27700) and NI Irish Grid (EPSG 29903).
  - The Land Parcel Identifiers (gid) differ from LCM2015 due to framework changes; cross-year comparisons by parcel IDs may require spatial overlap rather than IDs.
- Limitations and caveats:
  - Some spectral confusions remain (e.g., certain grasslands, bog, bracken, acidic habitats).
  - 10 m pixels are not validated against the 25 m parcel framework; users should be aware of differences in validation scope.
  - Saltwater vs. Freshwater distinctions rely heavily on context rasters and may show coastal misclassifications near tidal zones.

## Access, Metadata, and References
- Appendix 3 lists official dataset names for GB and NI variants; Appendix 5 and 6 provide recommended colour recipes for display (standard and color-blind friendly).
- Appendix 1–2 provide notes on UKCEH Land Cover Classes and the Biodiversity Action Plan (BAP) Broad Habitat crosswalks.
- Key references include Breiman (Random Forests), Carrasco et al. (seasonal composites), and Morton et al. (LCM2007).