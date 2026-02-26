# The UKCEH Land Cover Map for 2021

## Purpose and scope
- User guide for the UKCEH Land Cover Map for 2021 (LCM2021), the ninth UK land cover map.
- LCM2021 comprises six datasets (three per region: Great Britain and Northern Ireland) and supports decision-making, monitoring state and change, and future policy planning.
- Reports an overall validation accuracy of 82.6% with a 95% confidence interval of 82.19%–82.99%.

## Datasets and structure
- Three geospatial datasets per region (GB and NI), plus a shared 1 km summary rasters:
  - 10 m Classified Pixel datasets: per-pixel land cover with a primary class and a confidence/probability band.
  - Land Parcel Product: vector framework with land parcel attributes; built atop the UKCEH Land Parcel Spatial Framework.
  - 25 m Rasterised Land Parcel Product: 25 m rasters derived from parcel data with three attributes (mode, conf, purity).
  - 1 km Summary Rasters: dominant class and percentage cover summaries at 1 km resolution for both GB and NI (summaries across 25 m pixels).
- Coordinate systems: GB uses British National Grid (EPSG: 27700); NI uses TM75 Irish Grid (EPSG: 29903).

## Data production and classification workflow
- Land cover classified from Classification Scenes combining Sentinel-2 Seasonal Composite Images with 10 Context Rasters to reduce spectral confusion.
- Seasonal Composite Images: four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) built from Sentinel-2 bands; occasional cloud gaps are handled by the classifier.
- Bootstrap Training: an automatic training process that uses historic LCMs (LCM2018–LCM2020) as training data, selecting parcels with >80% purity and consistent class across years to train a Random Forest classifier.
- Random Forest: ensemble classifier trained with balanced sampling (10,000 samples per class per bag) to produce the 10 m Classified Pixel product.
- Context Rasters: 10 GB context layers (GB) and 10 context layers (NI) to disambiguate spectrally similar classes.

## UK Land Parcel Spatial Framework and MMU
- UK Land Parcel Spatial Framework provides fixed units (parcels) with a minimum mapping unit (MMU) of ~0.5 ha to support change detection and cross-year comparisons.
- 10 m Classified Pixels are kept at native resolution to preserve fine features; Land Parcel products aggregate information to parcels to support stable, comparable metrics over time.
- Parcel identifiers (gid) differ from LCM2015 due to framework updates; cross-year parcel ID comparisons require spatial rather than parcel-ID-based matching.

## Data products and attributes

- 10 m Classified Pixel dataset
  - Band 1: UKCEH Land Cover Class identifier.
  - Band 2: classification probability/confidence (mean class membership probability).
  - Not generalised to the Land Parcel Spatial Framework to preserve fine-scale detail; intended for specialist users aware of potential implications for change detection and validation.

- 25 m Rasterised Land Parcel dataset
  - Three-band raster carrying per-parcel attributes:
    - Band 1: per-parcel dominant land cover (mode).
    - Band 2: mean parcel confidence (_conf).
    - Band 3: parcel purity (_purity).

- Land Parcel Product (vector)
  - Includes meta-attributes such as _gid (unique parcel ID), _hist (distribution of class counts within parcel), _mode, _purity, _conf, _stdev, _agg (aggregate class), _n (number of contributing 10 m pixels).

- 1 km Summary Rasters
  - Dominant class at 1 km for both individual classes and aggregates (1-band each).
  - Percentage cover at 1 km for both classes (21 bands) and aggregates (10 bands).
  - Note: percentages are integer values; sums may slightly deviate from 100 due to rounding; coastal pixels may show sums less than 100 due to mapping extents.

## Seasonal and contextual data
- Seasonal Composite Images (4 seasons) driven by Sentinel-2 bands (10 spectral bands, with selected red-edge and SWIR bands included).
- Context Rasters (GB and NI differences noted) include terrain attributes (height, aspect, slope) and proximity/land-use masks (distance to buildings/roads/coast/freshwater, urban mask, foreshore, tidal water, woodland, etc.).

## Validation and accuracy
- Validation dataset: 35,182 reference points covering all 21 LCM classes, derived fromGB countryside surveys, National Forest Inventory, Rural Payments data, and bespoke validation points.
- Overall accuracy: 82.6% with 95% CI 82.19%–82.99%.
- Appendix 4 provides detailed correspondence matrices and producer/user accuracy metrics by class.

## Class relationships and habitat context
- UKCEH Land Cover Classes are closely related to UK Biodiversity Action Plan (BAP) Broad Habitats, but not identical; careful interpretation is needed where BAP and UKCEH classes diverge.
- Appendices 1–2 provide mapping notes between UKCEH classes and BAP Broad Habitats, including nuances and examples (e.g., distinctions among Broadleaved/Coniferous Woodlands, Arable, Various Grasslands, Bracken, Heather, Fen/Marsh/Swamp, Saltwater/Freshwater, Urban/Suburban, coastal habitats).
- The documentation notes potential spectral confusion between similar habitats (e.g., various grasslands, bog, heather, fen, and rocky/urban surfaces) and how contextual layers help mitigate some classification errors.

## Display, accessibility, and supporting materials
- Appendix 5 and Appendix 6 provide recommended colour schemes for displaying UKCEH Land Cover Classes (including color-blind friendly options) and accompanying QGIS symbol files:
  - lcm_raster.qml (standard color recipe)
  - lcm_raster_cb_friendly.qml (color-blind friendly)
- A QGIS symbology file accompanies each data product to facilitate visualization.

## Methodological transparency and reproducibility
- Method stack emphasizes open-source tools:
  - Random Forest classifier (Breiman, 2001) with balanced bootstrap training.
  - Bespoke UKCEH workflow integrating WEKA, PostGIS, and GDAL.
- The approach is designed to allow annual updates, improve temporal consistency, support change detection, and differentiate real change from random classification errors as the time series matures.

## Notes on data lineage and limitations
- The Land Parcel Spatial Framework changed since LCM2015; parcel IDs (gid) no longer align across LCM versions for cross-year comparisons by ID alone.
- Validation is against the 25 m rasterised parcel datasets; users should be aware that 10 m Classified Pixel data were not part of the formal validation process.
- Some coastal and small patches may be underrepresented due to the MMU and spectral ambiguities; ongoing improvements and training data updates are anticipated.