# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose: Present three new UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019) using 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; maps are produced automatically to enable annual updates and rapid assessment of land cover change.
- Coverage and classification goal: UK-wide maps with similar class structure to LCM2015; designed for change detection and comparability across time.

## Overview of Data and Production Approach

- Bootstrap Training: Automatic, history-based training using Bootstrap Training from LCM2015 to sample spectral training observations; future maps plan to bootstrap from majority signals across recent years.
- Random Forest classification: Supervised RF with balanced training (10,000 samples per class); implemented with custom software integrating WEKA, PostGIS, and GDAL.
- Training data and validation: Validation against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke validation points (22,325 points total); reported accuracies around 78–79% across the three years.
- Classification framework: Production uses 20m Sentinel-2 Seasonal Composite Images (TOA reflectance) plus 20m Context Rasters to form Classification Scenes; 4-season data (winter, spring, summer, autumn) with some cloud gaps.
- Classification Scenes and geography: GB uses 74 overlapping 100x100 km GB scenes; NI uses a single 43-band scene per year; scenes trained/classified independently with manual precedence to select best results.
- UKCEH Land Parcel Spatial Framework: Parcel-based structure with ~0.5 ha MMU; fixed 21 UKCEH Land Cover Classes; gid identifiers exist but differ from LCM2015; framework supports fixed time-series comparison by parcel overlap.

## Data Products and Dataset Structure

- 20m Classified Pixels: New 20m RF-based classifications per pixel with two bands: class (band 1) and membership probability (band 2, 0–100); preserves fine landscape detail (not generalised by parcels).
- Land Parcels: Parcel-level attributes linking 20m pixels to a spatial framework; key fields include hist (per-class pixel counts), mode (dominant class), purity, conf (mean class membership probability), stdev, and n (pixel count); gid ties parcels across years within the 2017–2019 framework.
- 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) derived from the Land Parcels; introduces smoother parcel-level summaries.
- 1km Raster Products: 
  - 1km Percent Cover: 21-band raster of per-class cover percentage.
  - 1km Percent Aggregate Cover: 10-band raster of aggregate cover by UKCEH Aggregate Classes.
  - 1km Dominant Cover: single-band raster of the dominant class per 1km cell.
  - 1km Dominant Aggregate Cover: single-band raster of the dominant Aggregate Class per 1km cell.
- Extents and coordinate systems: 
  - GB data in British National Grid (EPSG:27700); NI data in Irish Grid (TM75, EPSG:29903).
  - Datasets exist for Great Britain and Northern Ireland with 21 classes per dataset.
- Yearly dataset suite: Each year (2017–2019) includes 42 datasets (GB and NI products across all formats), with explicit documentation of minor attribute changes from LCM2015.

## Processing Details and Key Inputs

- Seasonal Composite Images: Derived from Google Earth Engine; four-season TOA reflectance data (Sentinel-2 bands 2,3,4,5,6,7,8,11,12); gaps due to cloud are represented as nulls; future work may fill gaps with alternative optical sources or SAR data.
- Context Rasters: 20m context layers to help disambiguate spectrally similar classes (e.g., terrain, urban proximity, distance to water). GB and NI have different context layers specified.
- Land Parcels Spatial Framework: Parceled aggregation of 20m classified pixels; preserves landscape features such as narrow patches; MMU ~0.5 ha; designed for time-series comparison while allowing user-defined alternative parcel structures.
- Bootstrap Training: 2015-based bootstrap set selected from parcels with purity ≥99%; training set used to generate RF classification for 2017–2019; plan to evolve bootstrap strategies and use larger majority signals (e.g., 2017–2019) for future maps.
- Software stack: Custom UKCEH RF pipeline, integrating WEKA, PostGIS, and GDAL (open-source components).

## Validation, Accuracy, and Quality Notes

- Validation approach: Cross-walk of UKCEH LCM outputs with multiple independent data sources and bespoke validation points; results indicate robust performance for an automated national-scale map.
- Reported accuracy (UK scale): 
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation caveats: The same validation dataset was used across all three products; fidelity depends on conversion between validation classes and UKCEH classes; pixel-level accuracy is approximate and can vary by class due to spectral similarity and training data limitations.
- Confusion and appendix materials: Confusion matrices and detailed per-class producer's and user’s accuracies are provided in appendices; documentation notes class-definition nuances and cross-year comparability considerations.

## Practical Considerations for Analysts

- Comparability across years: gid identifiers differ between LCM2015 and LCM2017–2019; cross-year parcel-based comparisons rely on spatial overlap where possible; parcel-level gid continuity is available within 2017–2019, but not guaranteed with earlier maps.
- Data granularity and usage: 
  - 20m Classified Pixels preserve fine spatial detail (good for local-scale analyses and detecting small patches).
  - 25m Rasterised Land Parcels provide a compact parcel-based summary suitable for larger-scale analyses.
  - 1km Raster products enable broader landscape-level summaries and trend analyses.
- Limitations and future directions: 
  - Automatic classification trade-off with no manual corrections; some spectral confusion (e.g., arable vs improved grassland, peatland signals) remains.
  - Gaps due to cloud acknowledged; potential for gap-filling using Sentinel-1 SAR or other data to improve year-round classification.
  - Ongoing pursuit of higher-resolution or alternative training data to improve class separability, particularly for upland and peatland habitats.

## Appendices and References (high-level)

- Appendices cover UKCEH Land Cover Class definitions, BAP Broad Habitats mappings, sample color recipes for visualization, and detailed validation tables and confusion matrices for the three years.
- Foundational references include Breiman (Random Forest), Jackson (BAP definitions), Morton et al. (LCM2007/LCM2015 lineage), and Carrasco et al. (multisensor evaluations).