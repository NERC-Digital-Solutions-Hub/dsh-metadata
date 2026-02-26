# The UKCEH Land Cover Map for 2022

## Purpose and scope
- User guide for the UKCEH Land Cover Map 2022 (LCM2022).
- Product consists of seven datasets: three for Great Britain (GB) and three for Northern Ireland (NI) plus a 1 km summary raster, covering GB+NI.
  - 10 m classified pixel dataset (GB)
  - 10 m classified pixel dataset (NI)
  - 25 m rasterised land parcel dataset (GB)
  - 25 m rasterised land parcel dataset (NI)
  - Land parcel vector datasets (GB)
  - Land parcel vector datasets (NI)
  - 1 km summary rasters (GB+NI)
- Classifies land cover into 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats, using a Bootstrap Training approach with a Random Forest classifier.
- Annual production aims to improve temporal consistency and support change detection; formal validation reports an overall accuracy of 86.1%.

## Data products and structure
- 10 m Classified Pixel datasets
  - Derived from multiple Classification Scenes; each pixel has a dominant UKCEH Land Cover Class and an accompanying probability/confidence band.
  - 10 m pixels are not generalised by the Land Parcel Spatial Framework to preserve fine features below the MMU (0.5 ha).
- Land Parcel datasets
  - Land parcels result from intersecting the 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
  - Land Parcel attributes summarize pixel-level data within discrete parcels; used to reduce noise and enable change detection.
- 25 m Rasterised Land Parcel datasets
  - Rasterised versions of the Land Parcel datasets with three bands: dominant class (_mode), mean confidence (_conf), and purity (_purity).
- 1 km raster products
  - Summary products derived from 25 m rasters:
    - Dominant cover (1 band)
    - Dominant cover for Aggregate classes (1 band)
    - Percentage cover by class (21 bands)
    - Percentage cover by Aggregate classes (10 bands)
  - Note: percentage sums may not total exactly 100 due to rounding; coastal pixels may sum to less than 100.
- Coordinate systems and extents
  - GB: British National Grid (EPSG 27700)
  - NI: TM75 Irish Grid (EPSG 29903)
  - GB extent: 0–700000 East, 0–1300000 North; NI extent truncated to NI grid
- Production details
  - GB has 32 Classification Scenes; NI uses a single 49-band Classification Scene (NG) for Northern Ireland
  - 10 m pixel products include 2 bands (GB) or 3 bands (NI); 25 m raster products have 3 bands
  - GB Land Parcel count: 6,741,294 parcels; NI: 902,252 parcels
- Data content and classes
  - 21 UKCEH Land Cover Classes defined; linked to BAP Broad Habitats with explicit mappings and notes on differences where applicable
  - Appendix 1/2 describe class definitions and BAP relationships

## Production methodology and data lineage
- Bootstrap Training
  - Automatic training process using historic LCM observations (LCM2019–LCM2021) to sample current imagery, reducing need for new field data.
  - Pixels with >80% probability and consistent class across three years are used to build training data.
  - Balances classes by drawing 10,000 samples per class per bag for Random Forest training.
- Random Forest classification
  - Classifier outputs the most likely land cover class per 10 m pixel; second band provides class membership probability/confidence.
  - Software stack combines Weka, PostGIS, and GDAL; uses open-source components.
- Seasonal and contextual information
  - Seasonal Composite Images: Sentinel-2 data, resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with spectral bands 2,3,4,5,6,7,8,8A,11,12; some null data due to cloud are tolerated by the classifier.
  - Context Rasters (10 m): GB includes height, aspect, slope, distances to buildings/roads/tidal water/freshwater, foreshore mask, woodland mask, and saltmarsh mask; NI includes height, aspect, slope, urban mask, distances to coast/road/freshwater, foreshore and tidal water masks.
- Classification Scenes
  - GB: 32 tiles (modified OS grid) to ensure manageable processing and avoid regional phenological variation; some overlap between adjacent tiles.
  - NI: single Classification Scene covering whole NI land mass (49-band scene).
- UK Land Parcel Spatial Framework
  - MMU ~0.5 ha; parcels derived by generalising national cartography to create discrete, real-world units.
  - Framework normalizes data and reduces noise; 10 m pixels are not forced to align to parcel boundaries.
- Validation and accuracy
  - Validation dataset: 33,107 points across 21 classes; compiled from field data, countryside surveys, open data inventories, and bespoke validation points.
  - Reported overall accuracy: 86.1% (LCM2022).
- Documentation and citations
  - Each LCM2022 dataset has a DOI; detailed citations provided (Table 5) and related methodological references (e.g., Marston et al., 2023/2024; Breiman 2001; Carrasco et al. 2019).

## Semantics, classification scheme, and user guidance
- UKCEH Land Cover Classes and BAP mapping
  - 21 UKCEH Land Cover Classes defined; relationship to BAP Broad Habitats described with notes on occasional one-to-one vs split mappings.
  - Appendices 1–2 explain nuanced distinctions and common spectral confusion (e.g., arable vs. improved grassland, bog vs. acid grassland vs. heath, bracken, fen/marsh/swam, coastal/seabed classes).
- Data presentation and use
  - Appendix 5/6 provide recommended color schemes and color-blind-friendly palettes for map displays; a QGIS symbology file is provided with the data products.
- Glossary and terminology
  - Key terms defined (Bootstrap Training, Context Raster, Classification Scene, Seasonal Composite Image, Land Parcel Spatial Framework) to aid proper interpretation.

## Known issues, limitations, and caveats
- Missing polygons in the vector land parcel products; corresponding nodata areas in 25 m rasterised land parcels (negligible effect on 1 km products; 10 m pixels unaffected).
- Interclass confusion remains for certain habitat types (e.g., bog, heath, acid grassland, fen/marsh/swamp) due to spectral similarity and legacy BAP definitions not originally designed for satellite sensing.
- Annual methodological changes may introduce differences between years; methods may be updated to improve accuracy, with potential implications for comparability over time.
- Bootstrap Training data for arable and improved grassland may be less reliable; alternative sources (e.g., UKCEH Land Cover plus Crops data) used for those classes in some areas.

## Governance, maintenance, and data stewardship considerations
- Temporal updates
  - LCM2022 is part of an ongoing annual series; future releases may re-apply improvements to maintain temporal consistency and enhance change detection.
- Provenance and reproducibility
  - Clear lineage from historic LCM products to Bootstrap Training sets; 10 m pixel and 25 m parcel products provide multiple layers for analyses and validation.
- Metadata and citation
  - DOIs and formal citations available for all data products; cite Marston et al. 2023/2024 as appropriate for production methods and data products.
- Compatibility and comparability
  - While designed for continuity with earlier LCM versions, some parcel identifiers differ from LCM2015; spatial overlap-based comparisons may require alternative matching approaches.
- Usage guidance
  - Users should consider the 0.5 ha MMU and the 10 m vs 25 m representations when designing analyses, especially for small habitat features and change-detection studies.

## Appendix highlights (for reference)
- Appendix 1: Notes on UKCEH Land Cover Classes with class-specific considerations and potential confusions.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats summaries and their relation to UKCEH classes.
- Appendix 3: Full list of datasets and DOIs for LCM2022 products.
- Appendix 4: Correspondence (confusion) matrices by class, including producer’s and user’s accuracies.
- Appendix 5: Recommended colour recipes for displaying UKCEH Land Cover Classes.
- Appendix 6: Colour-blind friendly colour recipes and accompanying QGIS symbology files.