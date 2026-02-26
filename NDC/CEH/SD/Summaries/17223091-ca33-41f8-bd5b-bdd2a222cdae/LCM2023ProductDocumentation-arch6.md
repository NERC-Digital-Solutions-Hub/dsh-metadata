# The UKCEH Land Cover Map for 2023

- Purpose and scope
  - User guide for LCM2023, UKCEH’s annual land cover map.
  - Produces seven geospatial datasets (GB and NI): three products per region (10 m Classified Pixels, Land Parcel attributes, 25 m Rasterised Land Parcels) plus a 1 km summary raster for both GB and NI.
  - Includes data production, validation, and accuracy guidance to help informed use and future work.

- Data products at a glance
  - 10 m Classified Pixel datasets (GB and NI)
    - Derived from aggregated Classification Scenes; each pixel has two bands: class (UKCEH Land Cover Class) and a confidence/probability for that classification.
    - Not generalised by the Land Parcel Spatial Framework to preserve fine features and small patches.
  - Land Parcel datasets (GB and NI)
    - Created by intersecting the 10 m classified pixels with the UKCEH Land Parcel Spatial Framework (minimum parcel size ~0.5 ha).
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterised version of parcels with three bands per parcel: dominant land cover (_mode), mean confidence (_conf), and parcel purity (_purity).
  - 1 km Summary rasters (GB and NI)
    - Summary of 25 m rasters to give dominant class, aggregate dominant, and percentage cover per class/aggregate across 1 km squares.

- Seasonal and contextual data
  - Seasonal Composite Images
    - Sentinel-2 data (resampled to 10 m) across four seasons; used to derive classification scenes.
    - Some cloud-related gaps may occur, but the classifier tolerates incomplete spectral information.
  - Context Rasters
    - 10 m GB context rasters (e.g., height, aspect, slope, distance to buildings/roads/tidal water/freshwater, foreshore and woodland masks).
    - 10 m NI context rasters (urban mask, coast/freshwater/road distances, foreshore and tidal water masks).

- Classification framework
  - Classification Scenes
    - GB classified in 32 tiles; NI uses a single scene covering the NI land mass.
    - Each scene is trained and classified independently using a 49-band input (Seasonal + Context rasters).
  - Bootstrap Training
    - Automatic training approach that uses historic LCM data (e.g., LCM2020–2022) to sample current imagery without fresh field data.
    - Pixels selected with >80% probability and consistent class across three years to create training data.
    - Addresses data sparsity and aims to maintain temporal continuity across maps.

- Random Forest methodology
  - Random Forest classifier trained on Bootstrap Training samples; balanced sampling to ensure rare classes are learned effectively.
  - Software stack includes Weka, PostGIS, and GDAL, all open source.

- UKCEH Land Parcel Spatial Framework
  - Parceled structure standardises land units (minimum ~0.5 ha) to reduce noise and enable change detection over time.
  - System updated since LCM2015; gids differ from LCM2015 for parcel comparison purposes.
  - Parcels help stabilise class signals and support spatial analyses.

- Validation and accuracy
  - Validation dataset: 33,107 reference points across all 21 classes.
  - Overall accuracy: 83% (full thematic detail).

- Known issues and caveats
  - Some vector land parcel polygons may be missing, causing nodata pockets in the 25 m rasterised parcel dataset (negligible effect on 1 km outputs; 10 m pixels are unaffected).
  - Differences between maps may reflect method changes over time as methods continue to evolve.

- Access, citation, and references
  - Each LCM2023 dataset has a DOI; citations provided for the 10 m classified pixels, land parcels, 25 m rasterised parcels, vector parcels, and 1 km rasters.
  - Related methodological references include Marston et al. (2023/2024) and Morton et al. (2011), with Marston et al. (2024) detailing 2023 data products.
  - Use is guided by appendices detailing UKCEH Land Cover Classes, their relation to UK BAP Broad Habitats, and display colour schemes (including color-blind friendly palettes).

- Display and practical use
  - Appendix 5/6 provide recommended colour schemes for mapping UKCEH Land Cover Classes (standard and color-blind friendly) with accompanying QGIS symbology files.
  - Outputs suitable for dashboards, reports, and self-serve data exploration to support environmental monitoring, policy informing, and change detection.

- Temporal considerations
  - Annual production aims to improve temporal consistency and support change detection; observed differences may reflect both real changes and methodological updates.
  - The 10 m pixel data retains fine spatial detail; the parcel framework enhances comparability over time.