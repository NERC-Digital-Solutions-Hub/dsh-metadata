# The UKCEH Land Cover Map for 2022

- UKCEH's annual land cover map (LCM2022) comprises seven geospatial datasets (GB and NI), plus a 1 km summary raster product covering both regions. It provides 21 UKCEH Land Cover Classes aligned with Biodiversity Broad Habitats (BAP) and aims to support monitoring of state and change in the UK countryside.
- Formal validation reports an overall accuracy of 86.1% at full thematic detail (21 classes) based on 33,107 reference validation points.

## What’s in the LCM2022 data product suite

- 10 m Classified Pixel datasets
  - One for Great Britain and one for Northern Ireland.
  - Each pixel has two bands: the most likely UKCEH Land Cover Class (integer) and a confidence/probability value.
  - Not generalised by the Land Parcel Spatial Framework to preserve fine-scale detail (e.g., narrow features below 0.5 ha MMU).
- 25 m Rasterised Land Parcel datasets
  - GB and NI versions; rasterised from the Land Parcel Spatial Framework.
  - Three attributes per parcel: dominant land cover (mode), confidence (conf), and purity (purity).
- Vector Land Parcel datasets
  - GB and NI versions; parcel-level attributes for change detection and time-series comparison.
- 1 km Summary Raster datasets
  - Dominant class and percentage cover per 1 km pixel, for both GB and NI (with aggregate class options).
  - Percentage values are integer-based; totals may not exactly sum to 100 due to rounding and coastal effects.
- Dataset provenance and citation
  - Each dataset has DOIs; references include Marston et al. (2023, 2024) and related production method papers.

## How LCM2022 was created (methodology)

- Land cover classes
  - 21 UKCEH Land Cover Classes derived from the UK Biodiversity Action Plan Broad Habitats (BAP) and mapped from satellite data.
  - Classes mapped using Classification Scenes built from Sentinel-2 Seasonal Composite Images plus Context Rasters to reduce spectral confusion.
- Bootstrap Training and Random Forest
  - Bootstrap Training automatically sources training data from historical LCM observations (LCM2019–LCM2021) with >80% probability and consistent class across three years.
  - Training data then used by a Random Forest classifier to produce the 10 m Classified Pixel products.
  - To ensure balanced learning, 10,000 samples per class are drawn with replacement.
  - Software stack is open source (Weka, PostGIS, GDAL) and integrated via a bespoke UKCEH toolchain.
- Seasonal and context inputs
  - Seasonal Composite Images derived from Google Earth Engine using four seasons and 10 Sentinel-2 bands.
  - Context Rasters (10 m GB; 10 m NI) provide terrain, proximity to features, and land-cover masks to improve discrimination (e.g., height, aspect, slope, distance to buildings/roads, coastal masks).
- Classification Scales and scenes
  - Great Britain: 32 Classification Scenes (tiles ~100 x 100 km) processed independently to manage regional phenology and data volume.
  - Northern Ireland: a single Classification Scene (49-band input) covering the land mass.
- Land Parcel Spatial Framework
  - The UK Land Parcel Spatial Framework (minimum parcel size ~0.5 ha) groups 10 m pixels into land parcels to support noise reduction and change detection.
  - Parcel identifiers (gid) are used in the parcel datasets, but may not match older LCM datasets due to framework re-ordering.
- Temporal context and change detection
  - Annual production enables differentiation between random classification noise and real land-cover change over time.

## Data quality, validation, and known issues

- Validation
  - 33,107 reference points across GB and NI; overall 86.1% accuracy for 21 classes.
  - Validation data drawn from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points.
- Known issues
  - Some vector land parcel polygons missing, causing nodata areas in the 25 m rasterised parcels; effect is negligible for 1 km products and 10 m pixels remain valid.
  - Validation targeted at 25 m rasterised land parcels; 10 m classified pixels are not validated against the parcel framework.
- Display data and metadata
  - Appendices provide detailed crosswalks between UKCEH LC Classes and BAP Broad Habitats, plus guidance on interpretation and display.
  - Colour recipes and QGIS/ARIA-ready symbology files are provided (including a color-blind friendly version).

## Data accessibility, usage, and governance

- Accessibility
  - All datasets are published with DOIs; intended for broad reuse and cross-regional comparison.
  - Annual updates support temporal analyses and change detection.
- Usage and interpretation
  - Complex data require careful interpretation; validation is against a 25 m parcel framework, while the 10 m pixel data preserve finer landscape detail.
  - Seasonal and Context inputs are essential to understanding the spectral information and classification decisions.
- Display and dissemination
  - Appendix 5/6 provide recommended color schemes for displaying classes (including color-blind friendly options) and accompanying QGIS symbol files.
- Citations and references
  - DOIs and citations for each data product are listed; Marston et al. (2023, 2024) provide production method context and overview of prior versions.

## Practical implications for data leaders

- Currency and comparability
  - Annual LCM2022 supports near-real-time monitoring of land-cover state and change, enabling separation of real changes from random classification errors.
  - Consistency with earlier LCM products is maintained through class definitions, with notes on cross-walks to BAP Broad Habitats.
- Data governance and interoperability
  - Clear data lineage: Sentinel-2 seasonal composites, context rasters, Bootstrap Training, RF classification, and the UK Land Parcel Spatial Framework.
  - Well-documented metadata, DOIs, and structured data formats (10 m and 25 m rasters, vector parcels) support integration into data platforms and analytical pipelines.
- Limitations and risk management
  - Some misclassification is possible in spectrally ambiguous habitats (e.g., certain grassland types, bog, fen) even with context rasters; users should leverage the 1 km summaries and time-series for robust trend analysis.
  - Differences between UKCEH LC Classes and BAP Broad Habitats exist; consulted appendices provide guidance to minimize ambiguity.
- Next steps and future improvements
  - Methods continue to evolve; significant accuracy improvements may prompt re-application across the catalogue to maximise temporal consistency and enable effective change detection.