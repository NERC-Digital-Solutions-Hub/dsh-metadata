# The UKCEH Land Cover Map for 2023

- UKCEH's eleventh land cover map (LCM2023) comprising seven datasets: three for Great Britain and Northern Ireland each (10 m classified pixels, classified land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster product covering both GB and NI.
- Purpose: a user guide describing data production, validation, and accuracy to help users apply LCM data in current and future work.
- Overall aim for users: monitor environmental state and change using a consistent, auditable data product with standardized outputs (maps, reports, charts).

## Data products and formats

- 10 m Classified Pixels (GB and NI)
  - Generated from multiple Classification Scenes; each pixel gets a most-likely UKCEH Land Cover Class (band 1) and a probability/confidence value (band 2 or additional bands for NI).
  - No generalisation with the Land Parcel Spatial Framework to preserve fine landscape detail (e.g., narrow features).
- Land Parcel datasets (GB and NI)
  - Result from intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework; used to produce parcel-level attributes.
- 25 m Rasterised Land Parcels (GB and NI)
  - Rasterised from Land Parcel data; three-band rasters carrying dominant land cover (mode), confidence (conf), and purity (purity) per parcel.
- 1 km Summary Rasters (GB and NI)
  - Summary of 25 m data to provide dominant class and percentage cover per 1 km pixel (both class and aggregate classes).
  - Percentage cover values are integers and may not sum exactly to 100 due to rounding and coastal area effects.
- Seasonal Composite Images
  - Sentinel-2 based 4-season composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with 10-band spectral information.
  - Contextual resolution and gaps handled to ensure full UK coverage.
- Context Rasters (GB and NI)
  - 10 m rasters providing spectral-context to reduce confusion (terrain, proximity to features, water, coast, urban areas, etc.).
- Classification Scenes
  - GB divided into ~100 x 100 km tiles (32 scenes); NI uses a single scene; scenes trained and classified independently to manage regional phenology.
- UK Land Parcel Spatial Framework
  - Defines parcel geometry (min ~0.5 ha), designed to stabilize comparisons over time and reduce noise; updates in identifiers may affect cross-version parcel IDs.
- Data Access and Metadata
  - Each dataset has DOIs and citations; full dataset details and validation references provided.

## Methodology

- Bootstrap Training
  - Automatic training data generated from historical LCMs (2020–2022) using pixels with >80% probability and consistent class history to bootstrap classifier training.
  - Provides a large, wall-to-wall training base to support machine learning without new field data; limitations for some crops (e.g., arable) noted.
- Random Forest Classification
  - Supervised learning using Bootstrap Training; balanced sampling to ensure rare classes are learned robustly.
  - Classification outputs two-part information: most likely class and associated confidence.
- Classification Scenes
  - GB: tiles ~100 x 100 km; NI: one scene; ensures manageable processing and accommodates regional spectral/phenological differences.
- Seasonal and Contextual Data
  - Seasonal composites via Google Earth Engine; 10 m context rasters (terrain, urban proximity, roads, water, foreshore, woodland, saltmarsh) used to reduce spectral confusion.
- Land Parcel Spatial Framework
  - Framework designed to represent discrete real-world units (fields, parks, urban areas); 0.5 ha minimum; used to generalise 10 m pixels into parcels for robust change detection.
- Validation
  - 33,107 validation points across 21 classes; overall accuracy reported at 83%.
- Known method considerations
  - Acknowledges annual method changes may yield differences beyond real land-cover change; emphasises ability to distinguish real change from methodological shifts.

## Validation and accuracy

- Overall accuracy: 83% across 21 UKCEH Land Cover Classes.
- Validation data sources: GB countryside survey, open data inventories, Rural Payments Agency data, bespoke validation points from image interpretation and fieldwork.
- Detailed validation metrics included in Appendix 4 (confusion matrices, user/producer accuracies for each class).

## Known issues and caveats

- Minor vector land parcel polygons missing in a small number of cases; 1 km summary rasters unaffected; 10 m classified pixels unaffected.
- Differences in parcel identifiers compared to LCM2015 due to framework re-ordering and indexing changes.
- Some classes (e.g., Neutral Grassland, Fen/Marsh/Swamp) exhibit inter-class confusion due to spectral similarities and definition nuances with Biodiversity Action Plan Broad Habitats.
- Saltwater vs Freshwater mapping has some coastal/estuarine confusion; coastal data prioritized for land cover rather than waterbody detail.
- Seasonality and method changes between years can introduce differences beyond real land-cover change.

## Data access, citations, and transparency

- DOIs and citations provided for all LCM2023 datasets (10 m classified pixels GB/NI, 25 m land parcels GB/NI, 1 km rasters, etc.).
- References include Marston et al. (2023-2024) documentation and foundational LCM methodological reports.
- Cited works cover Random Forests, seasonal aggregation strategies, and UK land cover history.

## Practical implications for analysts monitoring the environment

- Consistent, annual map series enables detection of real change versus method-related differences; random classification errors are unlikely to persist year to year.
- 10 m pixel data preserve fine landscape features for high-resolution monitoring, while 25 m parcel rasters and 1 km rasters support scalable analyses and cross-site comparisons.
- Bootstrap Training provides a scalable, low-data approach to training across time, with caveats for certain crop types and rapid land-use changes.
- Context rasters and seasonal composites improve discrimination among spectrally similar classes, particularly in challenging areas (coastal zones, urban interfaces, wetlands).
- Clear provenance and validation metrics support auditing, reproducibility, and policy performance monitoring.

## Appendices highlight (for context and planning)

- Appendix 1: Notes on UKCEH Land Cover Classes; guidance on class definitions and potential spectral confusion.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats; definitions and relationships to UKCEH classes; important for interpretation and cross-referencing with historical datasets.
- Appendix 3: Full list of LCM2023 datasets and citations.
- Appendix 4: Detailed correspondence matrices (confusion matrices) between classes; includes user’s and producer’s accuracy per class.
- Appendix 5 & 6: Colour recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly) with accompanying QGIS symbology files.