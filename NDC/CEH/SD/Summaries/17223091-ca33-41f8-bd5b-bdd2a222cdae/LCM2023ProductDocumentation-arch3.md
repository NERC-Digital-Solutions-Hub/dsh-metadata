# The UKCEH Land Cover Map for 2023

- LCM2023 is the UKCEH land cover map product for 2023, produced annually using automated classification to monitor state and change of the countryside.
- It comprises seven datasets across Great Britain (GB) and Northern Ireland (NI): three datasets per region (a 10 m classified pixel dataset, a land parcel dataset, and a 25 m rasterised land parcel dataset) plus a 1 km summary raster product covering GB+NI.
- The land cover classification uses 21 UKCEH Land Cover Classes, linked to Biodiversity Action Plan (BAP) Broad Habitats, with deliberate notes on differences between UKCEH classes and BAP broad habitats to maintain consistency with earlier products.
- Overall validation accuracy for LCM2023 is 83%.

## Product Suite (datasets)

- 10 m Classified Pixel datasets (GB and NI)
- Land Parcel datasets (GB and NI)
- 25 m Rasterised Land Parcel datasets (GB and NI)
- 1 km Summary Raster data (GB and NI)
- Appendix 3 lists official dataset names and DOIs for each product.

## Dataset Descriptions and Key Details

- 10 m Classified Pixels
  - Derived from mosaics of Classification Scenes; classifier assigns each pixel to a UKCEH Land Cover Class with the highest membership probability.
  - First band: most likely UKCEH Land Cover Class; Second band: class membership probability (confidence).
  - Unlike 25 m parcel rasters, 10 m pixels are not generalised by the Land Parcel Spatial Framework to preserve fine features.
  - Validation for this dataset was not conducted against the 10 m pixels; formal validation used the 25 m raster dataset.

- Land Parcel Datasets
  - Created by intersecting the 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to generate land parcel attributes.
  - GB and NI specifics: coordinates, extent, and 8-bit raster products; parcel counts and pixel counts per parcel.
  - The Land Parcel Spatial Framework MMU is ~0.5 ha; parcels are intended to align with discrete real-world units.

- 25 m Rasterised Land Parcel Datasets
  - Rasterised version of the Land Parcel datasets (GB and NI) with a 25 m pixel size.
  - Three attributes per parcel: dominant land cover class (_mode), confidence (_conf), and purity (_purity).
  - Designed to provide a stable, comparable summary of parcels at a coarser resolution.

- 1 km Summary Rasters
  - Created by summarising the 25 m rasters to 1 km cells.
  - Products include dominant class (1 band) and percentage cover for both 21 UKCEH Land Cover Classes and 10 UKCEH Aggregate Classes (plus coastal-specific adjustments).
  - Percentages are integers; sums may slightly differ from 100 due to rounding and coastal area considerations.

## Production Methods and Data Layers

- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 reflectance data.
  - 10 m resolution; four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with 10 spectral bands used.
  - Data gaps due to clouds are accommodated; classification tolerates partially complete spectral information.

- Context Rasters
  - Used to reduce spectral confusion between spectrally similar land covers.
  - GB Context Rasters include height, aspect, slope, distances to buildings/roads/tidal water/freshwater, foreshore mask, woodland mask, saltmarsh mask.
  - NI Context Rasters include height, aspect, slope, urban mask, distance to coast, distance to freshwater, distance to road, foreshore mask, and tidal water mask.

- Classification Scenes and Tiling
  - GB: 32 Classification Scenes, each trained/classified independently on a modified OS 100 x 100 km tile grid.
  - NI: single Classification Scene (minimum bounding rectangle of NI land mass) with 49 bands (40-band Sentinel-2 Seasonal Composite plus NI Context Rasters).
  - Scenes allow regional phenological variation; overlaps between tiles can occur.

- Bootstrap Training and Random Forest
  - Bootstrap Training: an automatic training approach using historic UKCEH LCMs (2020–2022) to generate training observations without field collection.
  - Pixels retained if >80% probability and consistently classified across three years; sample galaxy feeds the Random Forest classifier.
  - Random Forest: balanced training with 10,000 samples per bag; uses Weka, PostGIS, and GDAL; produces the 10 m Classified Pixels.
  - The production suite integrates open-source tools.

## The UKCEH Land Parcel Spatial Framework

- An established framework used to aggregate 10 m pixels into land parcels (0.5 ha MMU).
- Parcels group a dominant land cover type to reduce classification noise and support change detection over time.
- Changes to the framework since LCM2015 mean parcel identifiers (gid) do not match older LCM2015 datasets, affecting cross-version parcel ID-based comparisons.

## Validation and Quality

- Validation dataset: 33,107 reference points across all 21 classes, derived from countryside surveys, open data inventories, Rural Payments data, and bespoke validation points.
- Overall accuracy: 83%.
- Appendix 4 provides detailed confusion matrices, producer’s and user’s accuracy per class, highlighting areas of inter-class confusion (e.g., bog, heath, grassland types).

## Known Issues and Considerations

- Some polygons missing from vector land parcel products, causing nodata areas in 25 m rasterised land parcels; minimal effect on 1 km products.
- 10 m classified pixels are unaffected by the missing parcels.
- Differences in methodology over successive years mean changes between maps reflect both real change and methodological updates.

## Data Access, Citation, and Documentation

- Each LCM2023 dataset has a DOI; users are encouraged to cite the corresponding DOI and dataset documentation.
- Table of DOIs and references provided for 10 m classified pixels, 25 m rasterised land parcels, land parcels, and 1 km summary rasters.
- See Marston et al. (2023–2024) for related production method overviews; references to earlier LCM reports are included.

## Appendices (Key Context)

- Appendix 1: Notes on UKCEH Land Cover Classes, including distinctions and potential misclassification nuances (e.g., conifer vs broadleaf woodland, arable vs grassland, bracken, heather, fen/marsh/swamp, bog).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and their relationship to UKCEH Land Cover Classes (with mappings and caveats).
- Appendix 3: Full list of datasets for UKCEH LCM2023 and DOIs.
- Appendix 4: Correspondence matrices showing class-to-class confusion and accuracy statistics.
- Appendix 5: Recommended colour recipe for displaying UKCEH Land Cover Classes (RGB values) for standard and Appendix 6 for color-blind friendly displays.
- Additional notes: A companion QGIS symbol file (.qml) is provided for visualization; disclaimers about methodological variations across annual maps.