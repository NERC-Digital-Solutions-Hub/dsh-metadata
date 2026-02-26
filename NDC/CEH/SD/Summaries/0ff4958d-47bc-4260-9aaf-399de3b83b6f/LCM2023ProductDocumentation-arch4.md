# The UKCEH Land Cover Map for 2023

- The LCM2023 product comprises seven geospatial datasets: three per region (Great Britain and Northern Ireland) plus a single 1 km summary raster product for GB+NI. Specifically:
  - 10 m Classified Pixels (GB)
  - 10 m Classified Pixels (NI)
  - 25 m Rasterised Land Parcel Product (GB)
  - 25 m Rasterised Land Parcel Product (NI)
  - Land Parcel Product (GB)
  - Land Parcel Product (NI)
  - 1 km summary rasters (GB and NI)
- Aims: provide annual UK land cover maps with clear documentation on data production, validation, and accuracy to support informed use in policy, planning, and environmental monitoring.

## Data content and structure

- 10 m Classified Pixels
  - Two-band raster: Band 1 = most likely UKCEH Land Cover Class; Band 2 = class membership probability (confidence).
  - No generalisation with the UKCEH Land Parcel Spatial Framework to preserve fine landscape detail.
  - Overall accuracy validated at 83% for full thematic detail.
- Land Parcel datasets
  - Land Parcels are derived by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
  - Parcel attributes include unique id (gid), history, modal class, confidence, standard deviation, aggregate class, and count of pixels.
- 25 m Rasterised Land Parcel datasets
  - Rasterised representation of parcels with three bands: dominant land cover (mode), mean confidence (_conf), and pixel purity (_purity).
- 1 km summary rasters
  - Summary products derived from 25 m rasters: dominant class per 1 km pixel and percentage cover per class (21 class bands; plus 10 class aggregates).
  - Percentage values are integer-rounded; coastal areas may sum to less than 100 due to mapping extents.
- Coordinate systems and extents
  - GB: British National Grid (EPSG 27700); NI: TM75 Irish Grid (EPSG 29903).
  - GB extent: 0–700000 E, 0–1300000 N; NI extent: truncated Irish Grid to specified bounds.

## How the data are produced

- Seasonal Composite Images
  - Sentinel-2-based seasonal composites (January–March, April–June, July–September, October–December) at 10 m; 10 spectral bands used to capture phenology.
  - Occasional cloud gaps tolerated; algorithm handles partial spectral information.
- Context Rasters
  - 10 m context layers to reduce spectral confusion (GB: terrain, proximity to buildings/roads, water, foreshore, woodland, saltmarsh; NI: terrain, urban mask, distance-to-coast/road/freshwater, foreshore, etc.).
- Classification Scenes and Bootstrap Training
  - GB: 32 Classification Scenes; NI: single 49-band Scene (40 Sentinel-2 bands + NI context bands).
  - Bootstrap Training automatically harvests training data from historic LCM maps (LCM2020–LCM2022) with >80% probability and consistent class across three years.
  - Random Forest classifier trained on balanced samples (10,000 per bag) to avoid dominance by common classes.
  - Software integrates Weka with PostGIS and GDAL; open-source components.
- Validation and transparency
  - Formal validation against 33,107 reference points across all 21 classes; overall accuracy 83%.
- Data relationships and class mapping
  - 21 UKCEH Land Cover Classes tied to UK BAP Broad Habitats, with occasional one-to-one or split mappings; Appendix notes provide interpretation guidance (e.g., Urban vs Suburban, Saltwater vs Freshwater distinctions).

## Use and interpretation guidance

- The dataset is designed for change detection and trend analysis via annual layers, with random errors expected to flicker over time while real changes persist.
- The 10 m classified pixels preserve detailed landscape features; 25 m parcel rasters provide a generalized yet consistent unit for time-series analysis and change detection.
- When using coastal and mixed habitats, refer to the Appendix for cautions on spectral confusion and training data limitations, especially for Bare/rock surfaces, bog, heath, and mosaic habitats.
- The 1 km percentage products should be interpreted with rounding in mind; coastal areas may show slight under-representation due to mapping extents.

## Validation, accuracy, and limitations

- Overall accuracy: 83% (full thematic detail).
- Validation dataset drawn from GB countryside surveys, open data inventories, Rural Payments data, and bespoke validation points.
- Known issues: a small number of land parcel vector polygons are missing; corresponding nodata areas exist in the 25 m rasterised land parcel dataset. Impact is negligible for 1 km products; 10 m pixels are unaffected.
- Some class-specific producer’s accuracies vary (e.g., specific vegetation and water classes show higher/lower accuracies due to spectral and training data constraints).

## Data governance, access, and citing

- Each LCM2023 dataset has a DOI and recommended citation, with a consolidated reference to Marston et al. for production methodology.
- See Table 5 in the document for DOIs and citations per data product.
- Disclaimer: annual updates use slightly different methods; year-to-year differences may reflect methodological changes in addition to real land-cover change.

## Appendices and interpretive context (highlights)

- Appendix 1: Notes on UKCEH Land Cover Classes (descriptions and guidance for interpreting spectral classes versus BAP Broad Habitats).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and how they relate to the UKCEH classes.
- Appendix 3–4: Full dataset listings and detailed correspondence matrices (class-by-class confusion and accuracy metrics from validation).
- Appendix 5–6: Recommended color recipes for displaying UKCEH Land Cover Classes, including color-blind friendly options; accompanying QGIS symbology files are provided.