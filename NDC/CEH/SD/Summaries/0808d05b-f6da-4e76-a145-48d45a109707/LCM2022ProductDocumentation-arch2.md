# The UKCEH Land Cover Map for 2022

- Purpose and outputs
  - UKCEH Land Cover Map 2022 (LCM2022) delivers seven geospatial datasets: three for Great Britain and three for Northern Ireland comprising 10 m classified pixels, a dataset of classified land parcels, and a 25 m pixel (rasterised) land parcels dataset; plus a 1 km summary raster product covering both GB and NI.
  - Provides 21 UKCEH Land Cover Classes aligned loosely with Biodiversity Action Plan (BAP) Broad Habitats, with notes on differences and occasional splits (e.g., Heather vs Heather grassland; Urban vs Suburban).
  - Formal validation reports an overall accuracy of 86.1% at full thematic detail.
  - Designed to support consistent environmental monitoring, time-series analysis, and policy evaluation, with outputs suitable for reports, maps, and dashboards.

- Data model and classification approach
  - Classification Scenes: 4-season Sentinel-2 Seasonal Composite Images combined with a set of Context Rasters to reduce spectral confusion; 32 GB classification Scenes for GB plus a single Scene for NI.
  - Bootstrap Training: automatic, field-data-light training using historic LCM observations (2019–2021) with >80% probability and cross-year consistency to train a Random Forest classifier.
  - Random Forest: ensemble classifier trained on Bootstrap Training data to produce 10 m Classified Pixel products (class with highest probability plus a confidence value).
  - Land Parcel Framework: introduces a Land Parcel Spatial Framework to aggregate 10 m pixels into land parcels (minimum ~0.5 ha), reducing noise and enabling stable change detection across time.
  - Context Rasters: 10 m layers (GB) including height, aspect, slope, distances to buildings/roads/water, foreshore, woodland, saltmarsh; NI includes urban mask and distance to coast, freshwater, roads, etc. Context rasters help resolve spectral confusion.

- Datasets and formats
  - 10 m Classified Pixels (GB and NI): two-band outputs per pixel—an integer UKCEH Land Cover Class and a second band indicating the classification probability/confidence.
  - 25 m Rasterised Land Parcels (GB and NI): three-band rasters per parcel—dominant class (mode), mean confidence (conf), and parcel purity (purity). Parcellisation uses the UKCEH Land Parcel Spatial Framework.
  - 1 km Summary Rasters (GB+NI): products summarising the 25 m data to 1 km cells, including dominant class, aggregated class percentages (21 class bands for full detail; 10 bands for aggregates). Percentages are integer values and may not sum exactly to 100 due to rounding and coastal edge effects.
  - Spatial and attribution details: GB uses British National Grid (EPSG 27700); NI uses Irish Grid TM75 (EPSG 29903); extensive metadata on extents, parcel counts, and product naming included in the dataset descriptions.
  - Seasonal Composite details: four seasonal bands per pixel (based on Sentinel-2 bands) derived from 10 m resolution with gaps handled automatically.
  - Color and accessibility resources: Appendix-based color recipes and color-blind friendly versions provided; accompanying QGIS symbol files included.

- Class definitions and BAP relationship
  - 21 UKCEH Land Cover Classes are defined from the BAP Broad Habitats framework, with explicit notes where UKCEH classes and BAP Broad Habitats diverge. Appendices provide detailed definitions and mapping guidance to improve interpretation and comparability with earlier products.

- Validation, accuracy, and caveats
  - Validation dataset: 33,107 points spanning all 21 classes, drawn from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points.
  - Overall accuracy: 86.1% at full thematic detail; producer’s and user’s accuracies are reported in the accompanying validation matrices (Appendix 4).
  - Known issues: a small number of polygons missing from the vector land parcel products, causing nodata in the 25 m rasterised land parcels; effect negligible on 1 km rasters; 10 m classified pixels are unaffected.
  - Method consistency: methods evolve year-to-year; users should anticipate minor differences in outputs due to methodological updates, not just real-world change.

- Usage and monitoring notes for analysts
  - Time-series value: annual mapping emphasizes distinguishing real land-cover change from classification noise; persistent changes across years indicate real changes.
  - Data resolution choice: 10 m classified pixels preserve fine landscape detail; 25 m rasterised parcels provide a stable, change-detection-friendly framework.
  - Compare with past products carefully: differences between UKCEH Land Cover Classes and BAP Broad Habitats; refer to appendices for precise interpretations.
  - Training data considerations: Bootstrap Training leverages historical maps; note potential limitations for rapidly changing classes (e.g., annual rotations between arable and improved grassland).
  - Access and citation: all LCM2022 datasets have DOIs; recommended citations include Marston et al. (2023/2024) and related data-center records; see Appendix 3 for dataset-specific references.

- Access, citations, and further information
  - Each dataset is DOI-enabled; detailed citations and cross-references are provided (e.g., 10 m classified pixels, land parcels, 25 m rasterised land parcels, 1 km summary rasters) with corresponding Marston et al. and Marston et al. (2024) entries.
  - Appendix 3 lists the full dataset set; Appendix 4 provides correspondence matrices; Appendices 5–6 include color recipes (and color-blind friendly versions) for map display.
  - Disclaimer: annual production may introduce method-driven changes; users should account for both real change and methodological differences when interpreting year-to-year differences.