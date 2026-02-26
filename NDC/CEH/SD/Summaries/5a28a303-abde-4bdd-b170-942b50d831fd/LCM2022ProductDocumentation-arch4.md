# The UKCEH Land Cover Map for 2022

## Overview
- The tenth UKCEH land cover map (LCM2022), produced annually, maps 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
- Products combine Sentinel-2 Seasonal Composite Images with Context Rasters, classified automatically using Bootstrap Training and a Random Forest classifier.
- Aims to maximise temporal consistency, support change detection, and differentiate real change from classification noise. Formal validation reports an overall accuracy of 86.1%.

## Product Suite
- Three geospatial datasets for Great Britain (GB) and Northern Ireland (NI):
  - 10 m Classified Pixel dataset
  - Land Parcel Spatial Framework-based Land Parcel dataset
  - 25 m Rasterised Land Parcel dataset
- An additional 1 km summary raster product for GB and NI, aggregating the 25 m data.
- Appendix 3 lists official dataset names and accompanying DOIs for citation.

## Data Production
- Seasonal Composite Images: Sentinel-2 based, resampled to 10 m with four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec); multiband data used to produce Classification Scenes.
- Context Rasters (10 m): Used to reduce spectral confusion; GB includes terrain (Height, Aspect, Slope), distances to buildings/ roads/ tidal water/ freshwater, foreshore mask, woodland mask, and saltmarsh mask; NI includes similar terrain and additional urban mask and proximity layers.
- Classification Scenes:
  - GB: 32 tiles (~100 x 100 km) classified independently; some enlarged tiles in areas with extensive sea (Orkney, Shetland, Cornwall).
  - NI: single 49-band Classification Scene (40 Sentinel-2 bands + NI context rasters).
- Bootstrap Training: Automatic training data drawn from historic LCMs (2019–2021) filtered to pixels with >80% probability and consistent class across three years; used to bootstrap successive maps.
- Random Forest: Balanced sampling (10,000 samples per bag) to yield the 10 m Classified Pixel product; software integrates Weka, PostGIS, and GDAL; uses bespoke UKCEH tools.
- UK Land Parcel Spatial Framework: Parcellation with minimum map unit ~0.5 ha (MMU); parcels aggregate 10 m pixels to reduce noise and enable change detection.
- Data lineage notes: Bootstrapping enables continual improvement while preserving wall-to-wall coverage; annual products enable change detection and temporal comparability.

## Validation and Quality
- Validation uses 33,107 reference points across all 21 classes, combining countryside survey data, National Forest Inventory data, Rural Payments data, and expert validation points.
- Overall accuracy: 86.1%.
- Known issues: a small number of polygons missing from the vector Land Parcel products (affecting 25 m rasterised parcels; negligible for 1 km products; 10 m classified pixels unaffected).
- Data should be cited with DOIs per dataset; methodological references include Marston et al. 2023–2024 and earlier LCM publications.

## Dataset Details
- 10 m Classified Pixel datasets (GB and NI):
  - Two bands: first band = most likely UKCEH Land Cover Class; second band = class membership probability (confidence).
  - GB: 2 bands; NI: 2 bands.
  - GB uses 32 Classification Scenes; NI uses a single Scene.
- Land Parcel datasets (GB and NI):
  - Attributes include unique parcel IDs (gid), historical overlap metrics, mode, purity, confidence, standard deviation, aggregate class, and parcel counts; ogc_fid also present for production workflow.
- 25 m Rasterised Land Parcel datasets (GB and NI):
  - Three bands: per-parcel land cover mode, mean confidence, and purity.
- 1 km Summary Rasters (GB and NI):
  - Dominant class rasters and percentage cover rasters (21 class bands; 10 aggregate-class bands).
  - Percentage values are integers; sums may not exactly equal 100 due to rounding, especially near coastlines.
- Coordinate systems:
  - GB: British National Grid (EPSG 27700)
  - NI: Irish Grid TM75 (EPSG 29903)
- Pixel resolutions:
  - 10 m for classified pixels and context rasters
  - 25 m for rasterised land parcels
  - 1 km summary rasters derived from 25 m data

## Classification Components and Methods
- Seasonal Spectral Data: 10-band Sentinel-2-based data (bands 2,3,4,5,6,7,8,8A,11,12) plus context information.
- Context Rasters: 10 m layers to resolve spectral confusion (terrain, proximity to features, coastal masks).
- Bootstrap Training: Uses historical LCM data to generate large, reliable training sets; helps stabilize learning across years.
- Random Forest: Balanced, large-sample classifier to derive Land Cover Class membership probabilities.

## Relationship to BAP and Class Definitions
- UKCEH Land Cover Classes map to BAP Broad Habitats, but are not identical; some BAP classes are split or merged to form the 21 UKCEH classes.
- Appendices provide detailed mapping notes, including nuanced distinctions (e.g., Urban vs Suburban, Heather vs Heather grassland).
- Bootstrapped training data reflect historical definitions, with caveats for classes with high spectral similarity (e.g., peat-related classes, bog, fen, and certain grassland types).

## Data Access, Citation, and Display
- Each LCM2022 dataset has an assigned DOI; users should cite the DOIs and Marston et al. (2023–2024) as applicable.
- Display and visualization guidance include recommended color schemes for the 21 classes, plus color-blind friendly palettes and QGIS symbology files provided with the data.

## Known Issues and Limitations
- Minor missing polygons in vector Land Parcel products; negligible impact on 1 km products; 10 m classified pixels remain unaffected.
- 1 km percentage sums may not exactly equal 100 due to rounding; coastal pixels may sum to less than 100.
- Differences in parcel identifiers between LCM2015 and LCM2022 mean direct parcel-id comparisons across years may require spatial overlap rather than identifier matching.

## Practical Considerations for Data Leaders
- LCM2022 provides an annually updated, high-accuracy land cover dataset suitable for change monitoring, policy support, and environmental objective tracking.
- Key governance considerations:
  - Track methodological changes year-to-year (annual updates may introduce differences beyond real change).
  - Use DOIs for precise dataset citations and ensure metadata alignment with organizational data catalogs.
  - Leverage 10 m detail for fine-scale insights, and 1 km/25 m parcel summaries for large-area analyses and longitudinal comparisons.
  - Be aware of BAP-related classification nuances when aligning with legacy analyses or reporting requirements.
  - Acknowledge potential limitations in contentious classes (bog, fen, peat-associated habitats) where spectral separation is challenging and training data may be sparse.