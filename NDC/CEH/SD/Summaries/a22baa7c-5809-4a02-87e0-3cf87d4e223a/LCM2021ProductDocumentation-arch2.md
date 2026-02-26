# The UKCEH Land Cover Map for 2021

## Purpose and scope
- LCM2021 is the ninth UK land cover map produced by UKCEH, offering 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats (BAP).
- Product suite comprises six geospatial datasets: three for Great Britain and three for Northern Ireland (GB and NI)—a 10 m classified pixel dataset, a land parcel dataset, and a 25 m pixel rasterised land parcel dataset; plus 1 km raster products summarising the 25 m data.
- Aim: enable monitoring of environmental state and change, supporting a wide range of environmental objectives with annual updates to maximize temporal consistency and change detection.

## Datasets and data structure
- Datasets (Appendix 3 lists official dataset names):
  - 10 m Classified Pixels (GB and NI)
  - Land Parcel Dataset (GB and NI)
  - 25 m Rasterised Land Parcel Dataset (GB and NI)
  - 1 km Dominant and Percentage cover products (class and aggregate classes)
- Output structure:
  - 10 m Classified Pixel dataset: two bands—band 1 = most likely UKCEH Land Cover Class; band 2 = class membership probability (classification confidence).
  - 25 m Rasterised Land Parcel dataset: three attributes per parcel—dominant land cover (_mode), confidence (_conf), and purity (_purity).
  - 1 km products summarize 25 m data to provide dominant class and percentage cover (for both classes and aggregates).
- Coordinate systems and extent:
  - GB: British National Grid (EPSG: 27700)
  - NI: TM75 Irish Grid (EPSG: 29903)
  - Outputs cover GB and NI extents with corresponding parcel counts and extents.

## Data production and validation overview
- Seasonal imagery and context:
  - Seasonal Composite Images derived from Sentinel-2 across four seasons; 10 bands used.
  - 10 Context Rasters capture terrain, proximity to features (buildings, roads, sea, freshwater), foreshore and water masks, and binary land-cover masks (e.g., woodland).
- Classification Scenes and tiles:
  - GB: 32 Classification Scenes (tiles ~100 x 100 km) used to cover the GB land surface; NI: a single Classification Scene for Northern Ireland.
  - Scenes combine Seasonal Composite Images with Context Rasters to produce 50-band inputs for classification.
- Bootstrap Training and Random Forest:
  - Bootstrap Training automatically derives training data from historic LCM maps (LCM2018–LCM2020) to train a Random Forest classifier.
  - Training data are sampled from land parcels with >80% purity across three years, ensuring balanced representation of classes during RF training (10,000 samples per bag).
  - The process aims to reduce dependence on new field data, leveraging wall-to-wall historic maps for scalable training.
- Land Parcel Spatial Framework:
  - UKCEH Land Parcel Spatial Framework provides fixed land parcels (~0.5 ha MMU) to aggregate 10 m pixels, reducing noise and enabling robust change detection.
  - Parcels are derived from generalised national cartography; unique parcel identifiers (gid) differ from LCM2015, affecting cross-year parcel ID comparisons.
- Product validation:
  - Validation employed 35,182 reference points across all 21 classes.
  - Overall accuracy: 82.6% (95% CI: 82.19% to 82.99%).
  - Validation data integrated with 25 m rasterised parcels to determine correspondence and accuracy.

## Key methods and details
- Classification method:
  - Random Forest classifier trained via Bootstrap Training data; balanced bag sampling to ensure minority classes are learned effectively.
  - Pixels classified to the most probable UKCEH Land Cover Class; probability/confidence recorded as a secondary band.
- Data sources and structure:
  - Seasonal Composite Images built from Google Earth Engine; Sentinel-2 spectral bands used for classification.
  - Context Rasters include terrain (height, aspect, slope) and proximity measures to roads, buildings, coast, freshwater, and urban features.
- Parcellation and MMU:
  - Land parcels have a minimum area of ~0.5 ha (MMU); parcels aggregate 10 m pixels to reduce noise and enable stable time-series analysis.
- Relationships to BAP:
  - UKCEH Land Cover Classes are aligned with BAP Broad Habitats but are not a direct one-to-one mapping; Appendix 1 and Appendix 2 detail mappings, notes on divergences, and cases where BAP and UKCEH classes differ.
  - Some BAP categories (e.g., standing water vs rivers) are combined into UKCEH classes (e.g., Freshwater) for satellite mapping.
- Bootstrap Training data provenance:
  - Bootstrap Training sets derived from LCM2018–LCM2020; only parcels with >80% purity and consistent class across the three years are included.

## Outputs and usage guidance
- Pixel-level data:
  - 10 m Classified Pixel dataset preserves fine landscape features (e.g., narrow patches) not generalised by the Land Parcel Framework.
  - Outputs suitable for specialists who understand potential limitations due to the lack of parcel-level generalisation in the 10 m dataset.
- Parcel-level data:
  - 25 m Rasterised Land Parcel dataset provides robust parcel-based attributes for change detection and aggregation.
  - Land Parcel attributes include modality, confidence, and purity metrics to assess classification reliability per parcel.
- 1 km summaries:
  - Seasonal and compositional summaries provided at 1 km to facilitate broader-scale analyses and coarser-resolution applications.
- Color and visualization:
  - Appendix 5 and Appendix 6 provide recommended color recipes for displaying UKCEH Land Cover Classes, including color-blind friendly options.

## Class relationships and guidance for analysts
- UKCEH Land Cover Classes (21 total) are closely related to BAP Broad Habitats but not identical; detailed mapping, notes, and cautions are provided in Appendix 1 and Appendix 2.
- Certain splits and combinations reflect practical mapping constraints:
  - Freshwater combines Standing Open Water & Canals with Rivers & Streams.
  - Built-up Areas & Gardens are split into Urban and Suburban in the UKCEH scheme.
  - Saltwater and Saline water distinctions are treated with context rasters; saltwater classification may have slightly lower accuracy in tidal areas.
- Recognised challenges:
  - Spectral confusion among grassland types, bog, heather, calcareous vs acid grasslands, and other mosaic vegetation patterns.
  - Subtle microhabitat differences (e.g., Linear Features) are not reliably classified by current algorithms; linear features are not separately classified by spectra alone.

## Practical considerations for monitoring and time-series work
- Annual production supports distinguishing real change from random classification errors (flicker effect in time series).
- Validation demonstrates robust overall accuracy but highlights class-specific performance variations (documented in Appendix 4 confusion matrices).
- Users should reference the Land Parcel Spatial Framework and note the gid changes when attempting year-to-year parcel ID comparisons with LCM2015.
- For change-detection workflows, leverage both 10 m pixel outputs for detailed mapping and 25 m parcel outputs for stable, comparable time-series analyses.

## Appendices (highlights)
- Appendix 1: Notes on UKCEH Land Cover Classes (with class-specific considerations and training caveats).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and relationships to UKCEH classes).
- Appendix 3: Full list of datasets for UKCEH LCM2021 (dataset names and national scope).
- Appendix 4: Correspondence matrices (class-by-class accuracy and producer/user accuracies at the class level).
- Appendix 5 & Appendix 6: Colour recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly).