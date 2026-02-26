# The UKCEH Land Cover Map for 2022

## Overview and purpose
- UKCEH LCM2022 is the tenth UK land cover map, providing 21 UKCEH Land Cover Classes derived from Biodiversity Broad Habitats (BAP).
- Map produced from automatic classification of Classification Scenes that combine Sentinel-2 Seasonal Composite Images with Context Rasters; uses Bootstrap Training and a Random Forest classifier.
- Aims to support annual monitoring, improve temporal consistency, enable change detection, and help users make informed decisions on UK countryside state and change.
- Formal validation reports an overall accuracy of 86.1% at full thematic detail.

## Data products and datasets
- 10 m Classified Pixel datasets (GB and Northern Ireland)
  - Generated from multiple Classification Scenes; each pixel has a dominant UKCEH Land Cover Class and an associated confidence/probability.
  - No generalisation to Land Parcel Spatial Framework to preserve fine landscape detail; validation conducted against 25 m rasterised land parcels.
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterised from the 10 m classified pixels using the UKCEH Land Parcel Spatial Framework; three attributes per parcel: mode (dominant class), conf (mean class membership probability), and purity.
- Land Parcel Products (vector)
  - Land parcel attributes tied to the spatial framework; includes fields such as gid, hist, mode, purity, conf, agg, n, and ogc_fid; designed for change detection and parcel-based analyses.
- 1 km Summary rasters (GB and NI)
  - Derived by summarising the 25 m raster data; provide dominant class per 1 km pixel and percentage cover per class (21 class bands) and per aggregate (10 bands).
  - Percentage values are rounded; sums may not exactly equal 100 due to rounding and coastal effects.
- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec); 10 m resolution; occasional gaps due to cloud are handled by the classifier.
- Context Rasters
  - 10 m context rasters to reduce spectral confusion; GB includes terrain (height, aspect, slope), proximity to buildings/roads/tidal water/freshwater, foreshore mask, woodland mask, saltmarsh mask.
  - NI includes terrain, urban mask, distance to coast, freshwater, road, foreshore, and tidal water masks.
- Classification Scenes and tiling
  - GB classified in 32 tiles (approx. 100 x 100 km); NI uses a single 49-band scene for the landmass; some tile extents are enlarged to include sea areas.
- UKCEH Land Parcel Spatial Framework
  - Global parcel framework with ~0.5 ha minimum parcel size; maps discrete real-world units (fields, parks, urban areas, etc.); parcels help reduce noise and enable change detection.
  - Note: unique parcel identifiers (gid) do not match LCM2015 when comparing across years.
- Bootstrap Training
  - Automated training dataset created from historic LCMs (LCM2019–LCM2021) by selecting pixels with >80% probability and consistent class across three years.
  - Training data limitations: arable and improved grassland classifications may rely on alternative sources (UKCEH Land Cover plus: Crops data) due to land-use changes.

## Methods and validation
- Bootstrap Training and Random Forest
  - Classifier is trained with balanced samples (10,000 per class per bag) to mitigate dominance by common classes.
  - Software stack combines Weka, PostGIS, and GDAL; uses bespoke UKCEH tools.
- Validation and accuracy
  - Validation used 33,107 reference points across all 21 classes.
  - Overall accuracy: 86.1% (full thematic detail).
  - Appendix 4 provides per-class producer’s and user’s accuracy details.

## Data interpretation and caveats
- Known issues
  - A small number of polygons missing from vector Land Parcel products, creating nodata gaps in the 25 m parcel raster; negligible effect on 1 km products; 10 m classified pixels remain unaffected.
- Method changes and caveats
  - Subtle methodological changes across recent years mean some differences between maps reflect both real changes and classifier refinements.
- Relationship to BAP Broad Habitats
  - 21 UKCEH Land Cover Classes align closely with BAP Broad Habitats but are not identical; Appendix 1 and Appendix 2 explain mappings, including cases where splits or merges occur (e.g., Urban vs Suburban; Heather vs Heather grassland; Freshwater vs Rivers/Standing water).

## Data details and access
- Coordinate reference systems
  - GB: British National Grid (EPSG: 27700)
  - NI: Irish Grid TM75 (EPSG: 29903)
- Dataset metadata
  - Each dataset has a DOI; Table 5 lists DOIs and citations for the 10 m classified pixels, 25 m rasterised land parcels, land parcel vectors, and 1 km summary rasters.
  - See cited Marston et al. (2023–2024) for production methods and dataset-specific details.
- Display and usage
  - Appendix 5 and Appendix 6 provide recommended colour schemes for displaying UKCEH Land Cover Classes (standard and colour-blind friendly), with accompanying QGIS symbol files (lcm_raster.qml and lcm_raster_cb_friendly.qml).

## Appendices: key reference material
- Appendix 1 and Appendix 2
  - Notes on UKCEH Land Cover Classes and BAP Broad Habitat definitions; guidance on interpretation and potential spectral confusions.
- Appendix 3
  - Full list of datasets and their official names/DOIs.
- Appendix 4
  - Detailed correspondence/validation matrices including per-class accuracies.
- Appendix 5 and Appendix 6
  - Colour recipes for displaying land cover classes (standard and colour-blind friendly) with corresponding QGIS symbol files.