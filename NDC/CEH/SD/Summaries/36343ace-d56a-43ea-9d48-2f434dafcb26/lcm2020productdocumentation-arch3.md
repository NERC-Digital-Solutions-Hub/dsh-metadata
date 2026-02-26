# The UKCEH Land Cover Map for 2020

## Overview and purpose
- UKCEH LCM2020 is the eighth UK land cover map produced by UKCEH, designed to monitor state and change in the UK countryside and inform policy decisions.
- It comprises six datasets across Great Britain (GB) and Northern Ireland (NI): three datasets per region.
- Outputs include 10m classified pixel data, 25m rasterised land parcels, and associated land parcel datasets, enabling annual time-series analysis and change detection.
- The product uses automated methods to maximize temporal consistency and annual production, while acknowledging ongoing methodological evolution.

## Data products and structure
- GB and NI datasets (three per region):
  - 10m Classified Pixel dataset (GB and NI)
  - Land Parcel dataset (GB and NI)
  - 25m Rasterised Land Parcel dataset (GB and NI)
- Additional NI-specific dataset:
  - 20m Classified Raster Product (NI)
- Key characteristics:
  - Classification is based on 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats (with careful handling of differences between UKCEH classes and BAP definitions).
  - Output bands:
    - 10m Classified Pixel: Band 1 = most likely UKCEH Land Cover Class; Band 2 = associated confidence.
    - 25m Rasterised Land Parcel: three bands per parcel (mode, conf, purity) to describe per-parcel land cover and certainty.
  - Spatial framework: UKCEH Land Parcel Spatial Framework (minimum mapping unit ~0.5 ha) to support parcel-level change detection; parcels are derived by generalising national cartography and intersecting with the 10m pixel classifications.

## Data sources, inputs, and processing
- Seasonal information: Seasonal Composite Images derived from Sentinel-2 (four seasons) used to capture phenology; nine Sentinel-2 bands (2, 3, 4, 5, 6, 7, 8, 11, 12) contribute to classification.
- Context layers: 10m context rasters (GB and NI) including terrain (height, aspect, slope) and proximity masks (distance to buildings, roads, coast, freshwater, etc.) to reduce spectral confusion.
- Classification Scenes: GB uses 100x100 km tiles with 36-band Sentinel-2 scenes plus context rasters (total ~46 bands); NI uses a single 43-band scene.
- Training data (Bootstrap Training): Automatic sampling from historic UKCEH maps (LCM2017–2019) with >99% purity across three years to build a large training set (GB ~941k objects; NI ~214k). This enables self-starting, iterative learning without new field data.
- Classification method: Random Forest (RF) trained on Bootstrap Training data; pixels sampled in balanced bags to ensure robust learning across all land cover classes.
- Software: Bespoke UKCEH pipeline integrating WEKA, PostGIS, and GDAL (all open source).

## Validation, accuracy, and limitations
- Validation approach: 34,715 validation points drawn from GB countryside survey data (2019–2020), National Forest Inventory data, IACS data, and bespoke validation points; interpolated to the Land Parcel datasets to assess correspondence.
- Overall accuracy: 79.2% at full thematic detail (LCM2020 validation Appendix).
- Per-class performance: Detailed confusion matrices and per-class producer’s and user’s accuracies are provided in Appendix 4, highlighting variable performance across classes (e.g., Urban, Suburban, Arable, Grasslands, Wetland types, etc.).
- Validation caveats:
  - 10m Classified Pixels are not generalized via the UKCEH Land Parcel Spatial Framework, so they preserve fine features but were not the primary basis for formal validation (validated against Land Parcel data rather than the 10m pixels themselves).
  - Some spectral confusions persist (e.g., upland peatland vegetation, bracken, certain grassland types, saltwater vs freshwater near coasts).
  - GID/parcel identifier mismatch between LCM2015 and LCM2020 means exact parcel-to-parcel comparisons across years may require spatial overlap rather than direct ID matching.

## Data governance, openness, and use in monitoring
- Open, shareable outputs: Data are presented with accompanying metadata, validation details, and classification schema; outputs are designed for dissemination via reports, charts, or dashboards.
- Data management standards: Context rasters and training data are documented; the Classification Scenes and parcel framework provide repeatable structures for time-series analysis.
- Data accessibility challenges acknowledged: Metadata quality and timely access to some datasets can be barriers; the guide describes methods to verify data quality and ensure appropriate data governance, while noting constraints around publicly sharing certain datasets and ensuring up-to-date data.
- Data provenance and reproducibility: The document details data sources, processing steps, and model parameters (RF with Bootstrap Training), enabling independent understanding and potential replication.

## Relationship to biodiversity classifications
- UKCEH Land Cover Classes (21 classes) are closely related to UK BAP Broad Habitats but not identical; BAP categories are often broader or field-detection oriented. Appendix notes clarify mapping and use of UKCEH vs BAP terminology, including interpretation guidance and potential ambiguities.
- Appendices provide detailed mapping relations, example descriptors, and colour recipes to support consistent visualization and interpretation.

## Practical considerations for monitoring frameworks
- Time-series capability: Annual LCM2020 enables differentiation between random classification errors and real land-cover change (errors tend to flicker over time; persistent changes indicate real change).
- Change detection support: The combination of high-resolution 10m data with parcel-level frames and a robust time series supports monitoring of land-cover dynamics and attribution to policy or management actions.
- Class-specific considerations: Users should be aware of potential misclassification issues in complex habitats (peatlands, fen/marsh/swamp, bracken, upland vegetation) and interpret results with context from context rasters and seasonal signals.
- Guidance on data use: The 10m pixel outputs are best for specialists aware of the effects of not using parcel generalisation; parcel-based outputs are more suitable for generalized, comparable assessments over time.

## Appendices and dataset access
- Appendix 5: Full list of LCM2020 datasets (GB NI):
  - GB: 10m Classified Pixels; GB Land Parcel Product; GB 25m Rasterised Land Parcel Product
  - NI: NI 10m Classified Pixels; NI Land Parcel Product; NI 25m Rasterised Land Parcel Product
- Dataset extents and coordinate systems:
  - GB: EPSG 27700 (OSGB36); extent 0–700000 E, 0–1300000 N
  - NI: EPSG 29903 (Irish Grid); extent 180000–400000 E, 300000–500000 N
- The datasets and official product names are documented in Appendix 5 to support data management and integration into monitoring frameworks.