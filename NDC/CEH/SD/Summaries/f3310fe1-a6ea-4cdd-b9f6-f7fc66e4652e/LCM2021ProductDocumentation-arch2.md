# The UKCEH Land Cover Map for 2021

- The document is the user guide for UKCEH Land Cover Map 2021 (LCM2021), detailing data production, validation, accuracy, and how to use the six datasets covering Great Britain and Northern Ireland.
- LCM2021 aims to support informed decision-making about environmental state and change with a consistent, annually updated land cover product.

## What LCM2021 consists of

- Six geospatial datasets total (three per region: Great Britain and Northern Ireland):
  - 10 m Classified Pixel datasets (pixel-level land cover classification with confidence)
  - Land Parcel datasets (derived from the 10 m data intersected with the UKCEH Land Parcel Spatial Framework)
  - 25 m Rasterised Land Parcel datasets (per-parcel land cover summarized to 25 m pixels)
- Additional derived products:
  - 1 km raster products (dominant class and percentage cover for both 21 classes and 10 aggregate classes)
  - Seasonal Composite Images ( Sentinel-2 based, four-season composites)
  - Context Rasters (10 m, used to reduce spectral confusion)

## Data production and workflow

- Seasonal Composite Images:
  - Derived from Sentinel-2 data (resampled to 10 m; four seasons: Q1–Q3; includes bands 2,3,4,5,6,7,8,8A,11,12)
  - Occasional cloud gaps are handled; the classifier tolerates partially complete spectral information.
- Context Rasters:
  - 10 m layers capturing terrain and proximity to features (e.g., height, aspect, slope, distance to buildings, roads, sea, freshwater, foreshore and water masks, woodland).
- Classification Scenes:
  - GB uses a grid of 100 x 100 km tiles, yielding 32 Classification Scenes to cover GB; NI uses a single 49-band Scene.
- Bootstrap Training:
  - Automatic training using historic LCM data (LCM2018–LCM2020), selecting parcels with >80% purity classified the same way across years.
  - Enables training without fresh field data; supports annual updates.
- Random Forest classification:
  - Balanced sampling with 10,000 samples per class per bag; 2D outputs yield the most likely UKCEH Land Cover Class and a probability/confidence band.
- Land Parcel Spatial Framework:
  - Provides fixed, discrete land parcels (~0.5 ha minimum) to reduce classification noise and support change detection.
  - 10 m pixels are not generalised to parcel framework to preserve fine features; parcel-level validation was used for accuracy assessment.
- Dataset extents and coordinate systems:
  - GB: British National Grid (EPSG 27700)
  - NI: Irish TM75 grid (EPSG 29903)

## Datasets and key attributes

- 10 m Classified Pixel datasets:
  - Two-band output: most likely UKCEH Land Cover Class (band 1) and the associated class probability/confidence (band 2)
  - High detail preserved (not generalised to parcels)
  - Recommended for specialist users aware of potential noise and the impact of non-parcels
- Land Parcel datasets (GB and NI):
  - Attributes include gid, _hist (frequency distribution of classes within parcel), _mode (dominant class), _conf (mean confidence), _stdev, _agg (aggregate class), and _n (pixel count)
- 25 m Rasterised Land Parcel datasets:
  - Three-band rasters per parcel: dominant land cover class (_mode), mean confidence (_conf), and purity (_purity)
- 1 km raster products:
  - Dominant cover at 1 km (for 21 classes and for 10 aggregate classes)
  - Percentage cover at 1 km (for 21 classes and for 10 aggregates)
  - Note: percentage values are integers and sum to approximately 100, with coastline adjustments; minor rounding can occur
- Documentation and metadata:
  - Official dataset names, extents, and pixel resolutions are provided in Appendix 3
  - Appendix 4 includes comprehensive correspondence matrices and accuracy details per class
  - Appendix 5–6 provide color recipes for displaying the classes (color and color-blind friendly versions)

## Validation and accuracy

- Validation dataset:
  - 35,182 validation points across all 21 classes
  - Data sources include GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points
- Overall accuracy:
  - 82.6% with 95% confidence interval 82.19%–82.99% for full thematic detail
- Class-level considerations:
  - Some classes show higher confusion (e.g., various grassland types, bog, fen, bracken, saltwater vs freshwater)
  - Saltwater and freshwater distinctions rely partly on Context Rasters; some coastal areas may have confusion with non-vegetated surfaces
  - Small patches below the minimum mapping unit (MMU) may be underrepresented in parcel rasters but detectable in 10 m pixels
- Producer’s vs User’s accuracy:
  - Appendix 4 provides detailed producer’s and user’s accuracy per class and local-level confusion patterns

## How to use LCM2021 for environmental monitoring

- Multi-scale applicability:
  - 10 m Classified Pixels: detailed, landscape-level features; best for fine-scale monitoring and specialist analyses
  - 25 m Rasterised Land Parcels: stable parcel-based units suitable for change detection and aggregated metrics over time
  - 1 km products: suitable for broad-scale analyses and regional assessments
- Change detection and time-series:
  - Annual production facilitates separating random classification errors from real land-cover change (errors tend to flicker year-to-year)
  - Bootstrap Training leverages multi-year data to improve consistency across years
- Relationship to biodiversity frameworks:
  - UKCEH Land Cover Classes align with, but are not identical to, UK BAP Broad Habitats; Appendix 1–2 explains mappings and nuances
- Data accessibility and reuse:
  - Data are stored and uploaded to appropriate portals; designed to enable reuse and cross-dataset analyses
  - Underlying training and validation datasets support transparent evaluation of accuracy and uncertainty

## Practical notes and caveats

- General guidance:
  - Use 10 m products for detailed mapping; use 25 m parcel products for stable, discrete-unit analyses; use 1 km products for regional summaries
  - Be mindful of MMU constraints; many small patches may not be captured in parcel rasters
- Classification nuances:
  - Some land-cover types exhibit spectral similarity and spectral confusion (e.g., certain grasslands, bog vs fen, bracken vs acid grassland)
  - Accuracy varies by class; refer to Appendix 4 for detailed accuracy matrices and user’s/producer’s accuracies
- Future improvements:
  - UKCEH aims to continuously improve methods; significant accuracy gains may trigger re-application of improvements across the entire catalogue
  - Annual production enhances temporal comparability and supports change detection objectives

## Appendices (context at a glance)

- Appendix 1: Notes on UKCEH Land Cover Classes (with distinctions from UK BAP Broad Habitats)
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and mappings to UKCEH classes)
- Appendix 3: Full list of UKCEH LCM2021 datasets (GB and NI)
- Appendix 4: Correspondence matrices and per-class accuracy details (confusion matrices, user’s/producer’s accuracy)
- Appendix 5–6: Colour recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly)
- Glossary: Key terms (Bootstrap Training, Context Raster, Classification Scene, Seasonal Composite Image, etc.) and relationships among datasets