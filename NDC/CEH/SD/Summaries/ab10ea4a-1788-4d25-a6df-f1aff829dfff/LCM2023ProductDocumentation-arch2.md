# The UKCEH Land Cover Map for 2023

- Summary purpose: The LCM2023 is UKCEH’s annual land cover map produced to monitor environmental state and change using a consistent, auditable data format. It integrates satellite-derived classifications with contextual landscape information to enable scrutiny of environmental health and policy performance over time.

## Product suite and data structure

- Three geospatial datasets per region (Great Britain and Northern Ireland) plus a 1 km summary product for GB+NI:
  - 10 m Classified Pixel dataset
  - Land Parcel Spatial Framework datasets (vector land parcels)
  - 25 m Rasterised Land Parcel dataset
- A 1 km summary raster product covering both GB and NI (dominant class, and percentage cover for classes and aggregates).
- Appendix 3 lists official dataset names and DOIs; all datasets have formal citations (Table 5).
- Classification outputs align with 21 UKCEH Land Cover Classes, linked to Biodiversity Action Plan (BAP) Broad Habitats.

## How LCM2023 is produced

- Data sources and inputs:
  - Seasonal Composite Images derived from Sentinel-2, resampled to 10 m; four seasons provide temporal signals.
  - Context Raster layers (terrain, urban proximity, distance to roads/water, land/water masks, etc.) to reduce spectral confusion.
- Landscape segmentation and classification:
  - UKCEH Land Parcel Spatial Framework creates land parcels (~0.5 ha MMU) to reduce noise and support change detection.
  - Bootstrap Training: uses historic LCM pixel maps (LCM2020–2022) with high-confidence labels to generate training data for the current map.
  - Random Forest classifier outputs 10 m Classified Pixels (two bands: most likely UKCEH Class and associated confidence).
  - For GB, classification Scenes are tile-based (32 scenes); for NI, a single Scene is used.
- Validation and accuracy:
  - Formal validation uses 33,107 reference points across 21 classes.
  - Overall accuracy is 83%.
- Data processing tools:
  - Custom UKCEH software integrating Weka (RF), PostGIS, and GDAL; open-source components listed.

## Land cover classes and BAP relationship

- 21 UKCEH Land Cover Classes defined, most tied to UK BAP Broad Habitats (some differences noted for historical comparability).
- Appendices explain mappings and terminology, including how BAP Broad Habitats relate to UKCEH classes and the handling of ambiguous cases.
- Classification notes address spectral confusion and edge cases (e.g., Bracken vs Acid Grassland, Bog vs peatland, Saltwater vs Freshwater).

## Context, classification and data details

- Context rasters:
  - GB: height, aspect, slope; distance to buildings/roads; distance to tidal water; distance to freshwater; foreshore, woodland, and saltmarsh masks.
  - NI: height, aspect, slope; urban mask; distances to coast/road/freshwater; foreshore and tidal water masks.
- Seasonal and spectral inputs:
  - 10 bands from Sentinel-2 four-season composites (bands including coastal aerosol to shortwave infrared) to capture phenology.
  - Some cloud-related gaps are handled by the classifier without manual gap filling.
- Output types:
  - 10 m Classified Pixels (GB/NI)
  - 25 m Rasterised Land Parcels (GB/NI)
  - Land Parcel attributes (per parcel) including history, mode, confidence, purity, etc.
  - 1 km summary rasters (GB+NI)
- Spatial framework and MMU:
  - Land Parcels designed to be dominant land cover units, facilitating time-series comparison and change detection.

## Validation, accuracy and known issues

- Validation: 33,107 reference points across all classes; overall accuracy 83%.
- Known issues:
  - A small number of polygons are missing from the vector Land Parcel products (affects 25 m raster parcels only; 10 m classified pixels unaffected).
  - Changes in methods year-to-year mean some differences are due to methodology, not only actual land cover change.
  - Bootstrap Training limitations for some rotations (e.g., arable vs improved grassland) acknowledged; alternative data sources (e.g., UKCEH Land Cover plus Crops data) used where appropriate.
- Temporal context:
  - Annual production aims to maximize temporal consistency and change detection capabilities; real changes should persist across years, while random errors flicker.

## Access, citations and user guidance

- Citing and DOIs:
  - Each dataset has a DOI; specific DOIs and recommended citations are provided (Table 5) for 10 m classified pixels, 25 m rasterised land parcels, land parcel products, and 1 km summary rasters.
- Outputs and display:
  - Appendix 5 and Appendix 6 provide recommended colour recipes (standard and color-blind friendly) for displaying UKCEH Land Cover Classes.
  - QGIS symbol files (lcm_raster.qml and lcm_raster_cb_friendly.qml) accompany data products for straightforward visualization.
- Usage notes:
  - Suppliers should cite the appropriate dataset DOIs; users are advised that annual method updates may cause small differences beyond real change.
  - Related literature (Marston et al. 2023/2024; earlier LCM reports) provides methodological context.

## Implications for Analysts Monitoring the Environment

- Consistent, auditable time-series data across GB and NI support monitoring of environmental health and policy performance.
- High-resolution (10 m) outputs preserve fine landscape features and fragmentation, enabling detailed change detection at landscape scales; 25 m parcels provide a robust framework for temporal comparisons.
- Availability of both pixel-level and aggregated parcel data facilitates diverse analyses, from habitat mapping to land-use change and ecosystem service assessment.
- The integration of Bootstrap Training and RF classification with standardized context layers aligns with standardized approaches used by monitoring organisations.
- Known issues and ongoing method evolution are clearly documented, enabling users to account for potential methodological differences in longitudinal analyses.