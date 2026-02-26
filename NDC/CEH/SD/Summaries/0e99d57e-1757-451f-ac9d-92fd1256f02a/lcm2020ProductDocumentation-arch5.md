# The UKCEH Land Cover Map for 2020

- LCM2020 is the eighth UKCEH land cover map, produced annually and designed to support monitoring of state and change in the UK countryside. It includes six geospatial datasets (three per region): Great Britain and Northern Ireland each have a 10 m Classified Pixels dataset, a Land Parcel dataset, and a 25 m Rasterised Land Parcel dataset (plus related raster products in Appendix 5).

## Data products and metadata

- Datasets (per Appendix 5):
  - 10 m Classified Pixels (GB and NI)
  - Land Parcel Product (GB and NI)
  - 25 m Rasterised Land Parcel Product (GB and NI)
- Extent and resolution:
  - GB: 10 m and 25 m pixel datasets; NI: 10 m and 25 m equivalents
  - Coordinate references: GB EPSG: 27700; NI EPSG: 29903
- Band structure:
  - 10 m Classified Pixels: two bands; first band = UKCEH Land Cover Class; second band = class probability/confidence
  - 25 m Rasterised Land Parcel: three bands per parcel (dominant class, mean confidence, parcel purity)
- Data framework:
  - UKCEH Land Parcel Spatial Framework with ~0.5 ha minimum mapping unit (MMU)
  - Context rasters and Seasonal Composite Images used to support classification
- Documentation and provenance:
  - Official dataset names and metadata provided in Appendix 5
  - Distinctions explained between 10 m pixels (high detail) and parcel-based generalisations

## Data production and methodology

- Classification approach:
  - Automatic, using Bootstrap Training with a Random Forest classifier
  - Bootstrap Training uses historic LCM data (2017–2019) to sample current imagery, enabling annual updates without new field data
  - Training sets derived from LCM2017–2019 with >99% purity across three years; GB training objects ≈ 941k; NI ≈ 214k
  - 10 m Classified Pixels: each pixel assigned to the most likely UKCEH Land Cover Class with a confidence probability
- Seasonal imagery and context:
  - Seasonal Composite Images derived from Sentinel-2 (4 seasons), combined with 10 m Context Rasters (terrain, proximity to features)
  - Context Rasters used to resolve spectral confusions (e.g., height, aspect, slope, distances to buildings/roads/seawater/freshwater, coastal/foreshore masks)
- Classification Scenes:
  - GB classified using 74 overlapping 100 x 100 km Classification Scenes (with overlap to balance training data)
  - NI classified using a single 36-band Classification Scene per year
- Data processing tools:
  - Bespoke UKCEH software integrating Weka (machine learning), PostGIS, and GDAL (open source)

## Land parcels, rasterisation, and data structure

- Land Parcel Spatial Framework:
  - Parcellation designed to reduce noise and enable change detection over time
  - Parcels are real-world units (fields, parks, etc.) and generally dominated by a single land cover type
  - Changes since LCM2015 mean that parcel identifiers (gid) do not match exactly; users comparing years by parcel ID may need spatial overlap instead
- 10 m Classified Pixels vs 25 m Rasterised Parcels:
  - 10 m pixels retain fine landscape details not generalised by the parcel framework
  - 25 m rasters provide parcel-based summaries with three attributes: dominant class, mean confidence, parcel purity
- Validation data and accuracy:
  - Appendix 4 provides a formal validation with an overall accuracy of 79.2% for LCM2020
  - Validation sources include GB countryside surveys (2019/2020), open National Forest Inventory data, IACS, and bespoke validation points (n ≈ 34,715)
- Data quality notes:
  - Automatic classification means some class-level confusions persist; saline/coastal water distinctions rely on context rasters
  - No manual corrections are performed post-classification to maintain annual timing; problems are noted for future methodological improvements
- Temporal and interoperability considerations:
  - Annual production helps distinguish real change from random errors (flicker in time series)
  - As methods evolve, significant accuracy gains may trigger re-application across the full catalogue

## Accuracy, validation, and caveats

- Overall validation result:
  - 79.2% accuracy at full thematic detail (Appendix 4)
- Class-level and producer/user accuracy:
  - The document provides a detailed matrices breakdown; overall producer’s and user’s accuracies vary by class
  - Some classes show higher accuracy (e.g., Arable, Improved Grassland) and others lower (e.g., Heather Grassland, Neutral Grassland)
- Important caveats for data stewards:
  - The 10 m Classified Pixels are not generalised by the UKCEH Land Parcel Spatial Framework, so use is more appropriate for specialist analyses requiring fine detail
  - Mapping of certain complex upland and peatland habitats remains challenging due to spectral similarity and MMU constraints
  - While Saltwater and Freshwater distinctions rely on context rasters, coastal classification can still involve some confusion in tidal areas

## Governance, access, and use considerations for Data Stewards

- Update cadence and maintenance:
  - LCM2020 is designed for annual updates; improvements may be applied across the entire catalogue in future releases
- Data provenance and lineage:
  - Bootstrap Training relies on historic, wall-to-wall maps to generate training data, enabling scalable, repeatable model updates
- Metadata and interoperability:
  - Clear documentation of dataset names, extents, coordinate systems, band structure, and data processing steps (Appendix 5 and main text)
  - Be aware of gid changes when comparing across years; prefer spatial overlap methods for cross-year parcel-based comparisons
- Relations to biodiversity classifications:
  - UKCEH Land Cover Classes are linked to UK BAP Broad Habitats but are not identical; careful interpretation is required when cross-walking to BAP categories
  - Appendices provide detailed crosswalks and recommended color mappings for display
- Recommendations for data users:
  - Use 10 m classified pixels for fine-scale landscapes and when detailed patch information is required
  - Use parcel-based outputs for change detection, aggregation, and management planning at the parcel level
  - Consult validation results and class-specific accuracy when designing analyses or reporting uncertainties

## Appendices and supplementary notes

- Appendix 1 and 2: UKCEH Land Cover Classes and UK BAP Broad Habitats crosswalks; notes on class definitions and potential confusions
- Appendix 3: Recommended color recipe for displaying UKCEH Land Cover Classes
- Appendix 4: Detailed correspondence matrices and accuracy statistics by class (User’s and Producer’s accuracies)
- Appendix 5: Full list of datasets and official dataset names for GB and NI (including 10 m classified, land parcel, and 25 m raster products)