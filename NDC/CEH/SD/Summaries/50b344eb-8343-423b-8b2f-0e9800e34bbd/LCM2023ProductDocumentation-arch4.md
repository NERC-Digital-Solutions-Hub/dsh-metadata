# The UKCEH Land Cover Map for 2023

- LCM2023 is the eleventh UK land cover map produced by UKCEH, enabling annual monitoring of land cover for Great Britain and Northern Ireland with a target of temporal consistency and change detection.
- Overall validation accuracy is 83% at full thematic detail across 21 UKCEH Land Cover Classes.

## What is included (dataset-suite)

- Seven datasets total, with three per region (GB and NI) plus a 1 km summary raster:
  - 10 m Classified Pixels (GB and NI): Pixel-level land cover class and a per-pixel confidence; preserves fine landscape details (not generalized to Land Parcel framework).
  - Land Parcel Dataset (GB and NI): Land Parcel Spatial Framework-based parcels, created by intersecting 10 m pixels with parcel boundaries.
  - 25 m Rasterised Land Parcels (GB and NI): Rasterized parcel data (3-band: dominant class (_mode), confidence, and purity).
  - 1 km Summary Raster Products (GB and NI): Dominant class and percent cover per class per 1 km pixel; includes both class and aggregate summaries.
- Processing components:
  - Seasonal Composite Images: Sentinel-2 data (four seasons) resampled to 10 m; used to form Classification Scenes.
  - Context Rasters: 10 m context layers to reduce spectral confusion (e.g., terrain, distance to roads, water, urban features); separate lists for GB and NI.
  - Classification Scenes: GB classified with 32 100×100 km tiles; NI classified with a single scene; scenes combine Sentinel-2 seasonal data with context rasters.

## How the data are produced (methodology)

- Bootstrap Training: Automatic training data generated from historical LCM maps (LCM2020–2022) with >80% probability and consistent class across three years; used to train the classifier and bootstrap subsequent maps.
- Random Forest Classification: Each classification uses balanced sampling (equal numbers of samples per class; 10,000 samples per bag) to derive the most likely land cover class and its probability.
- UKCEH Land Parcel Spatial Framework: Parcels have a minimum mapping unit of about 0.5 ha; designed to reduce noise and enable change detection over time; IDs between LCM2015 and LCM2023 parcels are not directly interchangeable.
- Data Processing Tools: Bespoke UKCEH software integrating Weka, PostGIS, and GDAL; uses open-source components.

## Data quality and validation

- Formal validation uses 33,107 reference points across all 21 classes.
- Overall accuracy: 83% for LCM2023 at full thematic detail.
- Validation sources include GB countryside survey, National Forest Inventory data, Rural Payments Agency data, and bespoke validation points.
- Appendix 4 provides detailed confusion matrices and class-specific producer/user accuracies.

## Data structure, metadata, and accessibility

- Coordinate systems:
  - Great Britain: British National Grid, EPSG 27700.
  - Northern Ireland: Irish Grid TM75, EPSG 29903.
- 10 m Classified Pixels:
  - Two bands: class ID (integer) and class probability/confidence.
  - Maintains detailed landscape features (e.g., narrow patches) not present in the 25 m parcel raster.
- 25 m Rasterised Land Parcels:
  - Three bands: dominant land cover class (_mode), mean confidence (_conf), and purity (_purity) per parcel.
- 1 km Summary Rasters:
  - Dominant class (1 band) and percentage cover for 21 classes (and 10 aggregate classes) per 1 km pixel; percentage values are integers with rounding, so sums may deviate from 100%.
- Seasonal and Context data:
  - Seasonal Composite Images derived from Sentinel-2 bands (10 m resolution for most bands) across four seasons.
  - Context rasters provide additional spatial information to disambiguate spectrally similar classes.
- Validation and documentation:
  - Data products have DOIs; each dataset should be cited when used.
  - Caution: annual methodological updates may cause small differences across releases.

## Known issues and caveats

- A small number of polygons are missing from the vector Land Parcel products, creating nodata areas in the 25 m rasterised parcels; negligible impact on 1 km products; 10 m classified pixels are unaffected.
- Methodological differences across annual releases may cause apparent changes that reflect processing changes as well as real land cover change.
- Bootstrap Training for some classes (e.g., crop rotations between arable and improved grassland in recent years) may rely on supplementary data (e.g., UKCEH Land Cover plus: Crops data for 2023) for training accuracy.

## Practical notes for Data Leaders

- Data governance and reuse:
  - The suite provides scalable, high-resolution (10 m) and parcel-based products with consistent annual updates to support monitoring and change detection.
  - Clear provenance via DOIs and referenced literature; regular updates aim to improve temporal comparability.
- Data discovery and interoperability:
  - Datasets are organized by region (GB and NI) with explicit coordinate systems and metadata; 1 km rasters enable broad-scale analyses.
  Metadata highlights:
  - 10 m Classified Pixels: class IDs, confidence per pixel; suitable for detailed mapping and change detection at fine scales.
  - Land Parcel datasets: enable parcel-level analysis and change tracking; MMU ~0.5 ha.
  - 25 m Parcel rasters: compact, parcel-level summaries for analyses at moderate resolution.
  - 1 km summaries: efficient for large-scale assessments and integration with other 1 km products.
- Use cases:
  - Annual monitoring of land cover change, policy and conservation planning, ecosystem service assessments, and integration with Biodiversity/Habitat frameworks where relevant (BAP Broad Habitats mappings are described in Appendices).

## Appendices (highlights)

- Appendix 1-2: Notes on UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats; definitions, mappings, and notes on potential spectral confusion.
- Appendix 3: Full list of LCM2023 datasets and DOIs for GB and NI products.
- Appendix 4: Detailed correspondence (confusion) matrices for class-specific accuracy.
- Appendix 5-6: Recommended colour recipes for displaying UKCEH Land Cover Classes (including colour-blind friendly options) and accompanying QGIS symbol files.