# The UKCEH Land Cover Map for 2023

- A multi-dataset land cover product from UKCEH, consisting of annual maps across Great Britain and Northern Ireland (GB/NI).
- 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; created from Sentinel-2 Seasonal Composite Images plus Context Rasters.
- Automatic classification using Bootstrap Training and Random Forest; aims for temporal consistency to support change detection.

## Product Suite ( LC M2023)

- 10 m Classified Pixel datasets
  - Separate GB and NI products; mosaic of Classification Scenes.
  - Each pixel has two bands: most likely UKCEH Land Cover Class and the associated class membership probability (confidence).
  - 10 m pixels are not generalised by the Land Parcel Spatial Framework to preserve fine landscape detail.
- 25 m Rasterised Land Parcel datasets
  - GB and NI versions; rasterised to 25 m with three bands: dominant land cover (_mode), confidence (_conf), and purity (_purity).
  - Ties the 10 m results to the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
- Land Parcel (vector) datasets
  - Attributes including parcel-level statistics and cross-referencing fields (e.g., gid, _hist, _mode, _conf, _purity).
- 1 km raster products (GB + NI)
  - Summary rasters derived from 25 m data: dominant cover (1 band), dominant aggregates (1 band), and percentage cover (21 bands for classes; 10 for aggregates).
  - Percentage values are integers and can sum to slightly more/less than 100 due to rounding; coastal areas may sum to less than 100.
- Dataset metadata and DOIs
  - Each dataset has a DOI; user guidance and citations provided in the published documentation.

## Data Production & Classification

- Classification approach
  - Land cover is mapped by classifying Classification Scenes composed of Sentinel-2 Seasonal Composite Images plus Context Layers to reduce spectral confusion.
  - Bootstrap Training: uses historical LCM data (LCM2020–2022) to automatically generate training data from pixels with high probability and consistent class across three years.
  - Random Forest classifier trained on bootstrapped data; balanced sampling (10,000 samples per class per bag).
- Seasonal Composite Images
  - Four seasons: Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec; Sentinel-2 bands 2,3,4,5,6,7,8,8A,11,12; 10 m resolution; gaps treated as nulls.
  - Aims to provide temporal signal for vegetation differentiation and to tolerate occasional cloud gaps.
- Context Rasters (10 m)
  - UKGB: height, aspect, slope, distance to buildings, roads, tidal water, freshwater, foreshore mask, woodland mask, saltmarsh mask.
  - NI: height, aspect, slope, urban mask, distance to coast, distance to freshwater, distance to road, foreshore mask, tidal water mask.
- UKCEH Land Parcel Spatial Framework
  - Framework of land parcels (~0.5 ha MMU) used to aggregate 10 m pixels for a cleaner, time-consistent product.
  - Note: gid identifiers differ from LCM2015; cross-year parcel-based comparisons may require spatial overlap rather than parcel IDs.
- Software & validation
  - Classification system uses bespoke UKCEH tooling integrating WEKA, PostGIS, and GDAL (open-source components).

## Validation & Accuracy

- Formal validation
  - 33,107 validation points spanning all 21 classes; data sources include GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points.
  - Overall accuracy: 83% for LCM2023 at full thematic detail.
- Class-level accuracy
  - Appendix 4 provides detailed confusion matrices, producer’s and user’s accuracy per class (varying across classes; e.g., higher accuracy for arable, urban, freshwater, etc., and notable confusion among some grassland and peat/bog-related classes).
- Known data issues
  - A small number of polygons missing in vector land parcel products; some nodata areas in corresponding 25 m rasters (negligible impact on 1 km products).
  - 10 m classified pixels remain unaffected by these issues.

## Data Access, Citation & Usage

- Citations and DOIs
  - Each LCM2023 dataset has a DOI; Marston et al. (2024) provide production-method context for related years.
  - Users should cite the specific dataset DOIs (10 m classified pixels GB/NI, 25 m rasterised land parcels GB/NI, land parcels GB/NI, 1 km summary rasters GB/NI).
- Usage notes for data leaders
  - Annual production supports change detection; random classification errors are expected to flicker over time, while real changes persist.
  - The 10 m pixel data preserve detailed features; 25 m parcels provide a stable, comparable basis for time-series analysis.
  - Map display guidance is provided (Appendices 5 and 6) with color recipes and color-blind friendly alternatives; a QGIS symbology file is supplied.

## Methods, Standards & Relationships

- UKCEH Land Cover Classes and BAP Broad Habitats
  - 21 UKCEH Land Cover Classes linked to BAP Broad Habitats (note some deviations due to historical definitions and field-detection origins).
  - Appendices describe mapping relationships, spectrum-based distinctions, and known spectral confusions (e.g., arable vs. improved grassland, bog vs. heath vs. acid grassland).
- Appendices provide practical notes for interpretation
  - Class definitions, training data considerations, and guidance on edge cases (e.g., freshwater vs. saltwater near coasts, peat-related vegetation, arable-grassland transitions).
  - Detailed coverage of Dios, spatial frameworks, and training data sources.
- Seasonal, context, and parcel considerations
  - Seasonal imagery improves discrimination among vegetation types.
  - Context rasters help differentiate spectrally similar classes by geography and terrain context.
  - Land parcels standardize outputs for change detection and cross-time comparisons.

## Endnotes and Disclaimers

- Method evolution
  - Acknowledgement that recent LCM maps use evolving methods; differences between maps may reflect changes in methods as well as real land cover change.
- Change detection readiness
  - Annual maps provide opportunities to separate real change from classification drift; spatial and temporal analysis should account for potential method-induced variation.