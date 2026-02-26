# The UKCEH Land Cover Map for 2023

## Aim
- Provide a consistent, time-aware view of environmental condition to support monitoring of environmental health and policy performance.
- Deliver annual UK land cover maps to differentiate real change from classification noise, enabling change detection and long-term trend analysis.

## What the document covers
- User guide for LCM2023, detailing data production, validation, accuracy, and guidance for appropriate use.
- Describes seven datasets (three for Great Britain and three for Northern Ireland, plus a 1 km summary raster product), production methods (bootstrap training, Random Forest), and the relationship to Biodiversity Action Plan (BAP) Broad Habitats.

## Datasets and products
- 10 m Classified Pixel datasets (GB and NI): high-detail, two-band product (land cover class, then associated confidence). Not generalised by the Land Parcel Spatial Framework to preserve fine features.
- Land Parcel Spatial Framework and Land Parcel datasets: link 10 m pixels to discrete land parcels (~0.5 ha minimum) to reduce noise and support change detection.
- 25 m Rasterised Land Parcel datasets (GB and NI): rasterised version of land parcels with three bands per parcel (dominant class, confidence, purity).
- 1 km summary rasters (GB and NI): summarised dominant class, aggregated class data, and percentage cover per 1 km pixel (with rounding adjustments; coastal areas may sum to less than 100).
- Official dataset names and DOIs are provided for all products (see Appendix 3).

## Data inputs and structure
- Seasonal Sentinel-2 Composites: four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) at 10 m, using bands 2, 3, 4, 5, 6, 7, 8, 8A, 11, 12; occasional data gaps are accommodated.
- Context Rasters (10 m): additional layers to reduce spectral confusion (e.g., terrain, proximity to buildings, roads, water, foreshore, woodland, saltmarsh).
  - GB context rasters: height, aspect, slope; distances to buildings, roads, tidal water, freshwater; foreshore and binary masks for woodland and saltmarsh.
  - NI context rasters: height, aspect, slope; urban mask; distance to coast, freshwater, roads; foreshore and tidal/water masks.
- Classification Scenes:
  - GB: 32 tiles (based on modified OS 100 km grid) classified independently.
  - NI: single 49-band Classification Scene (40-band Sentinel-2 plus Northern Ireland Context Rasters).
- Land Parcel Spatial Framework: provides parcel-based structure for mapping and change detection; MMU ~0.5 ha; parcel identifiers (gid) used during production.

## Methods and training
- Bootstrap Training: automatically samples training data from historical land maps (LCM2020–2022) to train the classifier, reducing need for costly field data.
  - Training pixels drawn from pixels with >80% probability and consistent class across three years.
  - Large bootstrap training set supports robust learning; helps handle gradual land cover transitions.
- Random Forest classification: ensemble method used to assign land cover to pixels; 10,000 samples per bag with replacement to balance class representation.
- Production software: bespoke software integrating Weka, PostGIS, and GDAL (open source).

## Validation and accuracy
- Validation: 33,107 reference points across all 21 classes; data sources include countryside surveys, National Forest Inventory, Rural Payments Agency data, and bespoke validation points.
- Overall accuracy: 83% for LCM2023 (full thematic detail).
- Appendix 4 provides detailed confusion matrices, producer’s and user’s accuracy per class.

## Known issues and caveats
- Some vector land parcel polygons are missing, causing nodata areas in the 25 m rasterised land parcels; effect is negligible for 1 km summary products.
- 10 m Classified Pixel dataset accuracy was validated against the 25 m rasterised dataset, not directly against the 10 m pixel map.

## Classification details and outputs
- 10 m Classified Pixels: minimal generalisation to preserve fine landscape features; first band = most likely UKCEH Land Cover Class; second band = class probability/confidence.
- 25 m Rasterised Land Parcels: three-band rasters per parcel (dominant class, conf, purity); per-parcel statistics and attributes available.
- 1 km rasters: dominant class maps and percentage cover for both individual UKCEH classes and aggregated classes; percentage values summed to 100% with rounding, coastal areas may be under 100%.
- Coordinate systems and extents:
  - GB: British National Grid (EPSG: 27700)
  - NI: Irish Grid TM75 (EPSG: 29903)
  - Extents and parcel counts provided per dataset (GB and NI).

## UKCEH Land Cover Classes and BAP Broad Habitats
- 21 UKCEH Land Cover Classes aligned to Biodiversity Action Plan (BAP) Broad Habitats, with some differences due to measurement approach (remote sensing vs field-based definitions).
- Appendices explain detailed mappings and nuances, including where classes diverge and how to interpret them (e.g., coniferous vs broadleaved, bracken, heather, bog, fen, etc.).

## Seasonal, contextual and mapping considerations
- Seasonal imagery provides phenological information enabling better discrimination of vegetation types.
- Context rasters help disambiguate spectrally similar classes (e.g., urban vs non-urban surfaces, water bodies, and coastal features).
- Annual production aims to maximise temporal consistency and support change detection, while acknowledging that method updates can introduce differences between maps.

## Usage guidance for environment analysts
- Use 10 m Classified Pixels for detailed mapping and change detection at fine scales; use Land Parcel products for stable, parcel-based comparisons over time.
- Use 1 km rasters for broad-scale monitoring and integration with other national datasets.
- Refer to the BAP relationships to align with habitat-based policy contexts, while noting the differences between UKCEH classes and BAP Broad Habitats.
- Consider known issues (parcel vector gaps) and interpretation caveats when analyzing areas with fine-scale features or near coasts.
- Cite the LCM2023 datasets with the provided DOIs and follow the recommended references for production methods.