# The UKCEH Land Cover Map 2022

- LCM2022 is an annual land cover product from UKCEH comprising seven datasets for Great Britain and Northern Ireland: three 10 m pixel datasets (two per region for classification and land parcels) plus a 25 m rasterised land parcels dataset, a 1 km summary raster, and related metadata and spatial framework.
- Purpose: describe data production, validation and accuracy to help users make informed decisions about applying UKCEH LCM data in current and future work.
- Key goal for data leaders: understand the data system, data lineage, quality, and how to manage and disseminate data assets for effective data strategy and ongoing user collaboration.

## Datasets and data structure

- 10 m Classified Pixel datasets
  - Separate for Great Britain and Northern Ireland; produced from Classification Scenes using Bootstrap Training and Random Forest.
  - Band 1: most likely UKCEH Land Cover Class; Band 2: associated classification probability (confidence).
  - 10 m pixels are not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine landscape detail; validation is conducted against the 25 m Rasterised Land Parcel dataset.
- Land Parcel datasets
  - Land Parcel products (GB and NI) created by intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to generate parcel attributes.
  - 25 m Rasterised Land Parcel datasets (GB and NI) rasterise the Land Parcel dataset to 25 m resolution with three bands: dominant land cover (mode), mean confidence (conf), and mean purity (purity) per parcel.
  - Vector land parcels (GB and NI) provided as a separate data product with parcel identifiers and attributes for integration with vector workflows.
- 1 km raster products
  - Summary rasters summarising 25 m data to 1 km resolution: dominant class (1 band) and percentage cover for classes and aggregates (multiple bands). Coefficients rounded to integers; coastal areas may sum to less than 100 due to coastal mapping extents.
- Context Rasters
  - 10 m Context Rasters used to reduce spectral confusion; GB includes terrain-derived (Height, Aspect, Slope), proximity to features (buildings, roads, tidal water, freshwater), foreshore mask, woodland mask, and saltmarsh mask.
  - NI Context Rasters include Height, Aspect, Slope, urban mask, distance to coast, distance to freshwater, distance to road, foreshore mask, and tidal water mask.
- Seasonal Composite Images
  - Sentinel-2 based Seasonal Composite Images (four seasons: Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) at 10 m, with multiple spectral bands; occasional cloud gaps represented as null data. Used to create Classification Scenes.
- Classification Scenes
  - Great Britain: 32 Classification Scenes (tiles) covering the GB land surface; trained and classified independently; occasional overlap between tiles.
  - Northern Ireland: single 49-band Classification Scene (40-band Sentinel-2 Seasonal Composite plus 9 context rasters) for full NI coverage.
- The UKCEH Land Parcel Spatial Framework
  - Framework used to generalise land parcel geometries to ~0.5 ha minimum mapping unit (MMU); enables parcel-based change detection and consistent comparison over time.
  - IDs (gid) can differ from LCM2015; designed for efficient processing and time-series comparison within the current framework.
- Bootstrap Training
  - Automated training process using historic LCM data (LCM2019–LCM2021) to source training observations for classifier training without new field data.
  - Pixels with >80% probability and consistent class across three years sampled to form Bootstrap Training sets.
- Random Forest classification
  - RF classifier trained with balanced samples from Bootstrap Training to avoid dominance by common classes.
  - Software stack: bespoke UKCEH workflow integrating WEKA, PostGIS, and GDAL (open source).
  - Output: 10 m Classified Pixel dataset; additional per-pixel confidence values accompany class predictions.
- Data accessibility and citations
  - Each LCM2022 dataset has a DOI and should be cited accordingly (see Table of DOIs in the full document). Related literature includes Marston et al. (2023/2024) for production methods and validation.

## Data quality, validation, and accuracy

- Validation: 33,107 reference points spanning all 21 UKCEH Land Cover Classes, derived from GB countryside survey data, National Forest Inventory, Rural Payments data, and bespoke validation points.
- Overall accuracy: 86.1% at full thematic detail (LCM2022 validation).
- Validation approach:Pixel-to-polygon comparison against 25 m rasterised parcels; includes producer’s and user’s accuracy metrics by class (detailed in Appendix 4).
- Known issues and caveats
  - A small number of polygons missing from vector land parcel datasets; minimal impact on 1 km summary rasters; 10 m classified pixels datasets are unaffected.
  - Annual production can lead to differences from prior maps due to methodological changes; continuous improvements may yield re-application across the catalogue to maximise temporal consistency.

## Use, access, and governance

- Data governance and lineage
  - Annual LCM production aims to differentiate real land-cover change from method-induced differences; rich time series support change detection and monitoring.
  - Bootstrap Training and RF classification provide a scalable approach to updating maps with increasing temporal consistency, though some areas (e.g., arable vs. improved grassland) may require alternative training data when detected changes occur.
- Formats and reference systems
  - 10 m Classified Pixels: 2-band raster (class ID, confidence); GB uses British National Grid (EPSG: 27700); NI uses Irish grid (EPSG: 29903).
  - 25 m Rasterised Land Parcels: 3-band rasters (mode, conf, purity); same respective CRS as above.
  - Vector Land Parcels: parcel-level attributes aligned with Land Parcel Spatial Framework; fps differences noted between LCM2015 and present frameworks.
  - 1 km Summary Rasters: GB and NI combined; percentage covers and dominant classes per 1 km pixel.
- Dois and citations
  - Each data product has an assigned DOI; users are encouraged to cite the corresponding dataset and Marston et al. for production context.
- Accessibility
  - Data products are designed for integration into policy, planning, and environmental monitoring workflows; detailed metadata and colour recipes provided (Appendices 5–6) for mapping and visualization.

## Related classifications and interpretation

- UKCEH Land Cover Classes and their relationship to Biodiversity Action Plan (BAP) Broad Habitats
  - The 21 UKCEH Land Cover Classes are closely related to BAP Broad Habitats but are not identical; BAP terms are italicised when used explicitly to avoid ambiguity.
  - Appendices detail mappings and nuances, including cases where one UK BAP Broad Habitat maps to multiple UKCEH classes (and vice versa), and notes on spectral confusion challenges (e.g., bog, fen, acid grassland, heather).
- Practical guidance
  - The product set provides both detailed (21-class) and generalized (aggregate) views to support different user needs.
  - Colour recipes and a QGIS symbology file are provided to support consistent visualization and to accommodate color-blind friendly palettes.

## End notes and disclaimers

- The document emphasizes the evolving nature of annual LCM methods; small methodological shifts can cause differences between successive maps, in addition to real land-cover change.
- Users should consult the DOIs and referenced methodological papers for deeper details on production, validation, and usage guidelines.
- Appendices offer deeper technical context on class definitions, BAP alignment, and dataset specifications for advanced data users.