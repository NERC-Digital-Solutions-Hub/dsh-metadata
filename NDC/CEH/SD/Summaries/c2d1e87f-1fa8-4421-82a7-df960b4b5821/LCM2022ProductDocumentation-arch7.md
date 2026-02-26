# The UKCEH Land Cover Map for 2022

## Purpose and scope
- User guide for UKCEH Land Cover Map 2022 (LCM2022).
- Product comprises seven datasets: three datasets for Great Britain (GB) and three for Northern Ireland (NI):
  - 10 m classified pixel dataset
  - land parcel dataset (vector attributes)
  - 25 m pixel rasterised land parcels dataset
- A separate 1 km summary raster product covers GB+NI.
- Aim: describe data production, validation, and accuracy to help users apply LCM2022 data with informed decisions.

## Data content and structure
- Land Cover Classes: 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats; relationships to BAP and aggregate classes documented in appendices.
- Datasets and formats
  - 10 m Classified Pixels (GB and NI)
    - 2 bands: class identifier (UKCEH Land Cover Class) and confidence/probability of the classification.
    - Not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine landscape detail.
  - Land Parcel dataset (vector, GB and NI)
    - Derived by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework to create parcel-level attributes.
  - 25 m Rasterised Land Parcels (GB and NI)
    - Raster produced by rasterising the Land Parcel dataset; 3 bands: dominant land cover class (_mode), confidence (_conf), and purity (_purity).
  - 1 km Summary Rasters (GB+NI)
    - Summaries of 25 m rasters: dominant class per 1 km pixel; and percentage cover per class and aggregate class (with rounding).
- Coordinate systems and extents
  - GB: British National Grid, EPSG 27700; extent (0,700000, 0,1300000).
  - NI: Irish Grid TM75, EPSG 29903; extent truncated to NI landmass.
  - Pixel sizes: GB/NI 10 m for classified pixels; 25 m for rasterised parcels.
- Classification and data mosaic
  - Classification Scenes: GB divided into 32 tiles (~100x100 km) for processing; NI uses a single Scene.
  - 49-band Classification Scene for NI (44 bands from Sentinel-2 Seasonal Composite + NI Context Rasters).

## Production methodology
- Seasonal Composite Images
  - Derived from Google Earth Engine; Sentinel-2 reflectance resampled to 10 m; four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) using 10 Sentinel-2 bands.
  - Occasional cloud-related gaps; classifier tolerates partial spectral information; full UK coverage achieved.
- Context Rasters
  - 10 m context rasters to reduce spectral confusion (differences GB vs NI):
    - GB: height, aspect, slope; distances to buildings, roads, tidal water, freshwater; foreshore and binary masks for woodland and saltmarsh.
    - NI: height, aspect, slope; urban mask; distance to coast, freshwater, roads; foreshore and binary masks.
- UKCEH Land Parcel Spatial Framework
  - MMU ~0.5 ha; parcels derived by generalising national cartography to represent discrete land units (fields, parks, woodlands, etc.).
  - 10 m pixels grouped into parcels to reduce noise and enable change detection; identifiers (gid) may not match LCM2015 when comparing parcels.
- Bootstrap Training
  - Automatic, training-data-minimised approach; uses historic LCM observations to bootstrap classifier training without new field data.
  - Bootstrap Training dataset for 2022 drawn from LCM2019–LCM2021 classified pixels; pixels kept if >80% probability and classified the same class in all three years.
  - Some classes (e.g., arable and improved grassland) may rely on external data (e.g., UKCEH Land Cover plus: Crops) for training.
- Random Forest classification
  - Balanced training using 10,000 samples per class (bags) to train RF classifier.
  - Implementation uses bespoke UKCEH software integrating WEKA, PostGIS, and GDAL (open-source tools).
- Validation and accuracy
  - Validation dataset: 33,107 reference points across all 21 classes, from GB countryside surveys, National Forest Inventory, Rural Payment Agency, and bespoke validation points.
  - Overall accuracy: 86.1% (full thematic detail) for LCM2022; detailed Appendix 4 shows producer’s and user’s accuracies per class.

## Data quality, standards, and known issues
- Validation against 25 m rasterised land parcels; 10 m classified pixels validation is not the same dataset, so some caution for users focusing solely on 10 m outputs.
- Known issues
  - Some polygons are missing from vector land parcel products, creating nodata areas in the 25 m raster parcels; negligible impact on 1 km products; 10 m pixels remain unaffected.
- Change and compatibility
  - Slight methodological differences between years; users should treat interannual changes as a combination of real change and methodological changes.
  - For cross-year parcel comparisons, parcel identifiers (gid) may not align exactly with LCM2015.

## Display, usage, and accessibility
- Colour and symbology
  - Appendix 5: recommended colour recipe for displaying UKCEH Land Cover Classes; provides R,G,B values per class and accompanying QGIS symbology file (lcm_raster.qml).
  - Appendix 6: colour-blind friendly version of the palette; QGIS symbology file (lcm_raster_cb_friendly.qml).
- Data citation
  - Each LCM2022 dataset has a DOI; Table 5 lists DOIs and recommended citations (e.g., Marston et al. 2024 for 10 m classified pixels; 2024a–g for other products).
  - Users are encouraged to cite the DOIs when publishing or redistributing LCM2022 data.
- Documentation and appendices
  - Appendix 1–2: Notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats.
  - Appendix 3: Full list of LCM2022 datasets with official dataset names and DOIs.
  - Appendix 4: Correspondence matrices for LCM2022 class accuracies (detailed producer’s and user’s accuracy per class).
  - Appendix 5–6: Display color recipes (standard and colour-blind friendly).

## Practical notes for GIS specialists
- Data integration
  - GB and NI datasets use different projected coordinate systems; ensure proper reprojection for analysis combining UK regions.
  - 10 m classified pixels preserve fine details; 25 m rasters provide parcel-based aggregation suitable for change detection and regional analyses.
- Change detection
  - Bootstrap Training and annual production help distinguish random classifier noise from real change; leverage time-series to identify persistent changes.
- Validation awareness
  - Overall accuracy is 86.1% with detailed per-class metrics; use class-specific accuracies to assess suitability for target applications.
- Usage across products
  - For area-wide summaries and change detection, the 1 km summary rasters facilitate fast overviews, while 10 m and 25 m products support detailed analyses.
- References and further reading
  - See DOIs and Marston et al. (2023–2024) for production history and methodological context.

## Quick reference: key specifications
- Data products: 10 m Classified Pixels (GB/NI), Land Parcel dataset (GB/NI), 25 m Rasterised Land Parcels (GB/NI), 1 km Summary Rasters (GB+NI).
- Classes: 21 UKCEH Land Cover Classes (UKCEH-based; linked to BAP Broad Habitats with caveats).
- Resolutions: 10 m (classified pixels; GB/NI), 25 m (rasterised parcels; GB/NI), 1 km (summary rasters; GB+NI).
- Coordinate systems: GB (EPSG 27700), NI (EPSG 29903).
- Validation: 33,107 points; overall accuracy 86.1%.
- Methodology: Seasonal Sentinel-2 composites; 10 m Context Rasters; Classification Scenes (GB tiled; NI single scene); Bootstrap Training; Random Forest classifier.
- Future-proofing: Annual production aims to improve temporal consistency and change detection; differences across years may reflect methodological changes.