# The UKCEH Land Cover Map for 2022

- LCM2022 is the UKCEH Land Cover Map for 2022, the tenth in the series, mapping 21 UKCEH land cover classes (based on Biodiversity Broad Habitats) across Great Britain and Northern Ireland.
- It provides annual land cover data to support monitoring, change detection, and policy assessment, with validation indicating an overall accuracy of 86.1% at full thematic detail.
- The product suite includes seven geospatial datasets plus a 1 km summary raster, covering both GB and NI, with separate GB and NI components and a combined 1 km raster for GB+NI.

## Data Products and Formats

- Three main data categories, for GB and NI respectively, plus a 1 km summary product:
  - 10 m Classified Pixel datasets (GB and NI): per-pixel land cover class with a second band giving the class membership probability. No generalisation to land parcels to preserve fine-scale features.
  - Land Parcel datasets (vector): parcels derived from the UKCEH Land Parcel Spatial Framework; used to create parcel-level attributes and to support change detection.
  - 25 m Rasterised Land Parcel datasets (GB and NI): 3-band rasters per parcel (dominant class, confidence, and purity).
  - 1 km Summary rasters (GB+NI): dominant class, aggregate class summaries, and percentage cover per 1 km pixel (21 class bands for classes, 10 for aggregates).
- Coordinate systems:
  - Great Britain: British National Grid, EPSG 27700
  - Northern Ireland: Irish Grid (TM75), EPSG 29903
- Parcel framework:
  - Land Parcels have a minimum area of ~0.5 ha (MMU); parcels are designed to represent discrete real-world units (fields, parks, urban areas, etc.) and are used to reduce classification noise and enable time-series comparisons.
- Class definitions:
  - 21 UKCEH Land Cover Classes, linked to UK BAP Broad Habitats with careful cross-references and occasional re-splitting to improve accuracy in certain areas (e.g., Heather vs. Heather grassland; Urban vs. Suburban).
- Validation and references:
  - DOIs are provided for each dataset; detailed methodological references are available (e.g., Marston et al., 2024; Marston et al., 2023 for prior years).

## Data Production and Methods

- Data foundations:
  - Seasonal Composite Images: Sentinel-2 reflectance data resampled to 10 m, four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) to capture phenology, using 10 spectral bands.
  - Context Rasters (10 m): include terrain (Height, Aspect, Slope) and proximity masks (distance to buildings, roads, tidal water, freshwater; foreshore and coastal masks; woodland and saltmarsh masks).
- Classification approach:
  - Bootstrap Training: automatic training data derived from historical LCM maps (LCM2019–2021) by selecting pixels with >80% probability consistently labeled the same class across years.
  - Random Forest: balanced training across classes (10,000 samples per bag) to classify 10 m pixels into UKCEH Land Cover Classes.
  - Software: bespoke RF pipeline integrating Weka with PostGIS and GDAL (open-source tools).
- Classification Scenes and tiling:
  - Great Britain is partitioned into approximately 100 x 100 km tiles; NI uses a single Classification Scene for the island.
  - Each Classification Scene is trained and classified independently; NI uses a 49-band scene (Sentinel-2 Seasonal Composite plus NI Context Rasters).
- Outputs and validation:
  - 10 m Classified Pixels: per-pixel class with a secondary confidence band; not generalised to Land Parcel Spatial Framework.
  - Validation used 33,107 reference points from GB and NI covering all 21 classes; overall accuracy 86.1% (thematic detail).
- Data processing and methods disclaimer:
  - Annual updates may reflect real changes and method changes; users should interpret year-to-year differences with awareness of methodological evolution.

## Validation and Accuracy

- Validation dataset: 33,107 reference points drawn from GB countryside surveys, National Forest Inventory data, Rural Payments data, and bespoke validation points.
- Reported accuracy: 86.1% overall (full thematic detail) for LCM2022.
- Validation caveats:
  - Validation performed against the 25 m Rasterised Land Parcel dataset; 10 m Classified Pixels are not re-validated directly at 10 m but are aligned with the 25 m validation.
  - Some known issues exist (e.g., edge cases, spectral confusion among certain habitats); cross-tabulations and producer/user accuracy are provided in the full appendix.

## Spatial Coverage, Access, and Use

- Coverage:
  - Great Britain and Northern Ireland; annual production supports temporal monitoring and change detection.
- Data access and citation:
  - Each LCM2022 dataset has a DOI; users should cite Marston et al. (2024) for the methods overview and the specific dataset DOI for data use.
  - Data are hosted and documented via the UKCEH/Land Cover Map data centre and the NERC EDS Environmental Information Data Centre.
- Temporal context:
  - Aims to sustain temporal consistency to distinguish real land cover changes from random classification noise; annual maps help separate persistent changes from flicker errors.

## Known Issues and Considerations

- Minor data gaps:
  - Some polygons are missing from the vector Land Parcel products, causing nodata areas in the associated 25 m raster parcel data; negligible effect on 1 km summary rasters; 10 m classified pixels are unaffected.
- Parcel identifier changes:
  - The UKCEH Land Parcel Spatial Framework identifiers (gid) do not match LCM2015 identifiers; cross-year parcel-based comparisons should use spatial overlap rather than id equality.
- Classification caveats:
  - Some land cover classes (e.g., Neutral Grassland, Bog, Fen/Marsh/Swamp) exhibit inter-class confusion; context rasters and training data improvements aim to mitigate this.
- Color and presentation:
  - Appendix 5 and 6 provide recommended color recipes (including color-blind friendly options) and accompanying QGIS style files for visualization.

## Appendix Highlights (for Analysts)

- Appendix 1 & 2: Notes on UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats; guidance on interpretability and cross-walks between UKCEH classes and BAP habitats.
- Appendix 3: Full list of datasets and DOIs for LCM2022 products (10 m classified pixels, land parcels, 25 m rasterised parcels, vector parcels, and 1 km summaries).
- Appendix 4: Correspondence (confusion) matrices showing user and producer accuracies for major classes.
- Appendix 5 & 6: Colour recipes for displaying classes (standard and color-blind friendly) and associated QGIS symbology files.

## Practical Takeaways for Analysts

- LCM2022 provides a rich, multi-scale, annually updated view of UK land cover across GB and NI, enabling robust monitoring, trend analysis, and policy performance assessment.
- The workflow combines Sentinel-2 seasonal information with contextual terrain and proximity data, using Bootstrap Training and Random Forest to produce high-resolution land cover maps with quantified confidence.
- The 10 m pixel products preserve detailed landscape features, while the 25 m parcel rasters and vector parcels offer stable units for change detection and downstream analyses.
- Validation indicates solid accuracy, but users should be mindful of known class-confusion areas and the year-to-year methodological evolution when interpreting changes.
- Datasets are well-documented, citable with DOIs, and accompanied by visualization resources to support effective dissemination and analysis.