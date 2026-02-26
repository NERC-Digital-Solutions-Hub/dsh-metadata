# The UKCEH Land Cover Map for 2021

## Aim and scope
- User guide for the UKCEH Land Cover Map 2021 (LCM2021), which includes six geospatial datasets (three for Great Britain and three for Northern Ireland): 10 m Classified Pixels, Land Parcel Spatial Framework attributes, and 25 m Rasterised Land Parcels.
- Purpose is to describe data production, validation, and data accuracy to help users make informed decisions about applying LCM2021 data.

## Data holdings and structure
- Datasets (for GB and NI):
  - 10 m Classified Pixel datasets: pixel-level land cover classification with a first band (most likely UKCEH Land Cover Class) and a second band (classification confidence).
  - Land Parcel datasets: attributes derived by intersecting 10 m pixels with UKCEH Land Parcel Spatial Framework.
  - 25 m Rasterised Land Parcel datasets: 3-band rasters (dominant land cover, mean probability/confidence, and purity).
  - 1 km raster products: dominant class and percentage cover products for both 21 UKCEH Land Cover Classes and 10 Aggregates.
- Coordinate systems:
  - Great Britain: British National Grid (EPSG 27700).
  - Northern Ireland: Irish Grid TM75 (EPSG 29903).
- Extents and counts:
  - GB Land Parcels: ~6,741,288; NI Land Parcels: ~902,248.
  - Pixel resolutions: 10 m and 25 m; 1 km products derived from 25 m data.
- Official dataset names are listed in Appendix 3.

## Production methodology
- Seasonal Composite Images:
  - Derived from Google Earth Engine using Sentinel-2 data resampled to 10 m.
  - Four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) using 10 spectral bands.
  - Occasional data gaps due to cloud cover; classification algorithm tolerates partial data.
- Context Rasters:
  - 10 m context layers to reduce spectral confusion (e.g., terrain, proximity to features, water, coast).
  - GB context rasters include height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore and tidal masks, woodland mask.
  - NI context rasters include height, aspect, slope, urban mask, and distances to coast, freshwater, and roads, plus foreshore/ tidal masks.
- Classification Scenes:
  - GB classified in 32 tiles (modified OS 100 x 100 km grid) to create 50-band Classification Scenes; each tile trained and classified independently.
  - NI uses a single 49-band Classification Scene combining the 40-band Sentinel-2 Seasonal Composite with NI context rasters.
- Bootstrap Training:
  - Automatic training dataset that uses historic land cover maps (LCM2018–LCM2020) to sample current imagery.
  - Training parcels must have >80% purity and consistent class across three years.
  - Provides large, wall-to-wall training data to support robust Random Forest classification.
- Random Forest classification:
  - Balanced sampling for training to ensure all classes are represented (10,000 samples per bag; multiple bags per class).
  - Output: 10 m Classified Pixel dataset (two-band product: class id and associated probability).
- UKCEH Land Parcel Spatial Framework:
  - Fixed MMU of ~0.5 ha; parcels derived by generalising national cartography to represent discrete land units (fields, woodlands, urban areas, etc.).
  - 10 m pixel classification is aggregated to land parcels to reduce noise; 25 m rasters provide a per-parcel raster representation.
  - Note: Parcel identifiers (gid) in LCM2021 do not match LCM2015 identifiers; cross-year parcel ID mapping is not straightforward.

## Data products in detail
- 10 m Classified Pixels:
  - Primary output is a mosaic of national cover with a probability/confidence band per pixel.
  - Not generalised by the Land Parcel Spatial Framework to preserve fine features (e.g., narrow patches); validation against the 25 m parcel dataset is not direct.
- Land Parcel datasets:
  - Attributes include gid, _hist (parcel-level history of class composition), _mode (most frequent class), _conf (mean confidence), _stdev, _agg (aggregate class), _n (number of 10 m pixels in the parcel).
- 25 m Rasterised Land Parcel datasets:
  - Three-band rasters: dominant land cover (mode), conf (mean probability/ confidence), and purity (how dominant the modal class is within the parcel).
- 1 km raster products:
  - Dominant class and aggregated dominant class (1 band each) plus percentage cover for 21 classes and 10 aggregates (with rounding leading to small sum discrepancies around 100%).
  - Coastal areas may have sums that are less than 100% due to map resolution and MMU considerations.
  
## Validation and accuracy
- Validation dataset: 35,182 reference points across all 21 classes, using GB countryside surveys, National Forest Inventory data, Rural Payments Agency data, and bespoke validation points.
- Overall accuracy: 82.6% (95% CI: 82.19% – 82.99%) when validated against the 25 m rasterised Land Parcel products.
- Appendix 4 provides detailed per-class confusion matrices, user’s and producer’s accuracies, and overall accuracy metrics.
- Important caveats:
  - Validation is against the 25 m parcel dataset; the 10 m pixel classifications have not been validated directly at the 10 m scale against parcel geometries.
  - Some spectral confusions are noted (e.g., across related habitat types); context rasters help mitigate but do not eliminate confusion.
  - Saltwater vs Freshwater and coastal classifications rely heavily on context rasters; occasional coastal misclassifications can occur, especially near tide states.

## Data governance, quality, and usage notes
- Annual production with evolving methods; potential re-application of methods across the entire catalogue if improved accuracy is achieved.
- Validation shows a robust accuracy level suitable for monitoring state and change in the UK countryside, supporting change detection and environmental objectives.
- Users should be aware of:
  - The MMU and parcel framework implications; 10 m pixels and parcel-level outputs serve different use cases.
  - The Bootstrap Training approach relies on historic maps; newer maps help bootstrap training but may introduce temporal biases if rapid changes occur.
  - Transferability and cross-year comparisons may be affected by changes in parcel IDs (LCM2015 mapping caveat).
- Appendix resources provide mappings between UKCEH land cover classes and Biodiversity Action Plan (BAP) Broad Habitats, plus guidance on interpretation and display (color schemes) and detailed dataset inventories.

## Data access and references
- Official dataset names and full metadata are listed in Appendix 3.
- Data are supported by methodological notes on Bootstrap Training, Random Forest classification, seasonal composites, and context rasters, with references to foundational works and prior LCM products.
- Appendices 1–6 provide extensive supporting information for class definitions, BAP broad habitats, dataset lists, validation matrices, and display color recipes.