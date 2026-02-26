# The UKCEH Land Cover Map for 2023

- A user guide describing the LCM2023 product: seven datasets across GB and Northern Ireland (GB/NI) plus a 1 km summary raster product.
- Datasets include: three products for GB and NI each (10 m Classified Pixels, Land Parcels, 25 m Rasterised Land Parcels) and a 1 km summary raster product covering GB and NI.
- Purpose: explain data production, validation, and data accuracy to help users apply LCM2023 data effectively.

## Key Data Products and Structure

- 10 m Classified Pixels (GB and NI)
  - Generated from classification scenes; RF classifier provides a most-likely land cover class and a second band with the associated probability (confidence).
  - Preserves fine detail by not generalising with the UKCEH Land Parcel Spatial Framework.
- Land Parcel Datasets
  - Land Parcel datasets result from intersecting the 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to create parcel attributes.
- 25 m Rasterised Land Parcels (GB and NI)
  - Rasterised version of land parcels to 25 m, carrying 3 bands: dominant land cover (mode), mean confidence (conf), and mean purity (purity).
- 1 km Raster Products
  - Summary rasters summarising 25 m data to 1 km: dominant class (1 band), dominant aggregate (1 band), and percentage cover by class (21 bands) and by aggregates (10 bands).
  - Percent values are integer-rounded; sums may deviate from 100% due to rounding.
- Seasonal Composite Images
  - Sentinel-2 based four-season composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) at 10 m, with some gaps due to cloud.
- Context Rasters
  - 10 m context layers used to reduce spectral confusion (terrain, proximity to buildings/roads/water, coastal/forshore masks, etc., with GB and NI-specific rasters).
- Classification Scenes
  - GB classified in 32 tiles (approx. 100 x 100 km each); NI classified in a single scene; scenes are trained and classified independently.
- UK Land Parcel Spatial Framework
  - Framework for parcel generalisation and attribute generation; note that parcel identifiers differ from LCM2015 when comparing across years.

## Production and Methodology

- Classification approach
  - Classification Scenes are built from Sentinel-2 Seasonal Composite Images plus Context Rasters.
  - Bootstrap Training: automatic generation of training data from historical land maps to train the classifier, reducing need for new field data.
  - Random Forest classifier used with balanced sampling to avoid bias toward common classes.
- Data sources for training
  - Bootstrap Training pixels derived from UKCEH LCM2020–2022 with >80% probability and consistent class across three years.
  - Some classes (e.g., arable and improved grassland) use external sources (UKCEH Land Cover plus: Crops data) when necessary due to rapid changes.
- Validation
  - 33,107 validation points across all 21 classes.
  - Overall accuracy reported at 83% for LCM2023 (full thematic detail).
- Software
  - Custom UKCEH pipeline integrating Weka (RF) with PostGIS and GDAL; uses open-source components.

## Data Quality, Accuracy, and Validation

- Overall accuracy: 83% across 21 UKCEH Land Cover Classes.
- Validation data
  - Composite reference data from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points.
- Known issues during validation
  - Some minor misclassifications across inter-class boundaries (notably among peat- and shrub-related classes) and spectral/confusion challenges noted in appendices.
- Known data issues
  - A small number of polygons missing from vector land parcel products; negligible effect on 1 km products; 10 m classified pixels unaffected.

## Dataset Details and Access

- Coordinate systems
  - GB: British National Grid (EPSG: 27700)
  - NI: Irish Grid (TM75, EPSG: 29903)
- Parcel counts and extents
  - GB parcels: approximately 6,741,294
  - NI parcels: approximately 902,252
- Extents
  - GB and NI extents defined to cover land areas; 1 km products include coastal and inland zones with specific handling near coastlines.
- Data citations
  - Each LCM2023 dataset has a DOI; formal citations provided (Marston et al. 2023/2024 series; Morton et al. 2011; Smith et al. 2007; etc.).
- Data usage notes
  - Annual updates aim to improve accuracy and temporal consistency; method changes may yield differences between maps.

## UKCEH Land Cover Classes and BAP Broad Habitats

- 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, with some differences due to design intent (field-based vs. remote sensing).
- Appendices clarify mappings and notes on potential spectral confusion between certain classes (e.g., various grasslands, peat-related habitats, and bracken).

## Classification Scenes and Localisation

- GB tiles
  - 32 classification scenes to cover GB land area; enhanced treatment near Isles and peninsulas to ensure adequate training data.
- NI scene
  - A single 49-band Classification Scene for NI combining 40 Sentinel-2 bands with NI context rasters.

## Appendices and Practical Guidance

- Appendix 1 and 2
  - Details on UKCEH Land Cover Classes and BAP Broad Habitats, with notes on definitional nuances and potential misclassifications.
- Appendix 3
  - Full list of LCM2023 datasets and their DOIs.
- Appendix 4
  - Correspondence matrices and accuracy assessments (confusion matrices) for individual classes.
- Appendix 5 and 6
  - Recommended colour schemes (standard and color-blind friendly) for displaying Land Cover Classes; accompanying QGIS symbology files provided.