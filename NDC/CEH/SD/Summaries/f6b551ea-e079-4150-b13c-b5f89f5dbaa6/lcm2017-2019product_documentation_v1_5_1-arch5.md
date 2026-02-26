# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- Release accompanying three UKCEH land cover maps: LCM2017, LCM2018 and LCM2019, each using 21 UKCEH Land Cover Classes based on BAP Broad Habitats.
- Data produced automatically using Bootstrap Training plus Random Forest; aim to enable rapid, nationwide mapping and future annual updates.
- Includes a new 20m Classified Pixels dataset and a structured dataset suite duplicated for Great Britain and Northern Ireland, totaling 42 datasets across years.
- Emphasizes careful interpretation; maps are automatically generated with no manual corrections in this release, though visual checks and formal validation were performed.
- Licensing, provenance, and description of data structure are provided to support governance and reuse.

## Data and Production Approach
- Bootstrap Training
  - Uses historic UKCEH LCMs (LCM2015 derived from 1990–2007 data) to bootstrap training data for 2017–2019.
  - Selection of training parcels uses a 99% purity threshold from LCM2015; majority signal guides the next map update.
  - Plans to base future bootstraps on multi-year majority signals (e.g., 2017–2019; 2018–2020).
- Random Forest classification
  - Balanced sampling: from each training bag, 10,000 samples per class.
  - Production software integrates Weka, PostGIS, and GDAL (open source).
- Satellite and contextual inputs
  - Classification Scenes built from Sentinel-2 Seasonal Composite Images (TOA reflectance) produced via Google Earth Engine.
  - Seasonal data: winter, spring, summer, autumn; seasonal gaps handled by the classifier (occasional nulls).
  - Context Rasters (20m) provide terrain, proximity, and other contextual cues to reduce spectral confusion.
  - In GB, 100x100 km classification tiles yield 46-band scenes (36-band Seasonal Composites + 10 Context layers); NI uses a single 43-band scene.
  - Future work may incorporate Sentinel-1 SAR or alternative sources to fill potential seasonal gaps.
- UKCEH Land Parcel Spatial Framework
  - Fixed framework with ~0.5 ha minimum mapping unit; parcels are used to summarize 20m classified pixels and provide stable comparison units over time.
  - Parcel identifiers (gid) are consistent within this release but do not match LCM2015 parcel IDs for cross-year comparisons.
  - The framework supports both the current parcel-based outputs and user-defined alternative summarizations.

## Datasets and Products
- 20m Classified Pixels
  - New addition: RF-derived classification results at 20m with two bands: band 1 = nominated land cover class; band 2 = membership probability (0–100) for the nominated class.
  - Preserves fine landscape detail (e.g., narrow features) not generalised by parcels.
- Land Parcels
  - Attributes include: gid (parcel ID), _hist (histogram of class counts within parcel), _mode (dominant class), _purity (percent modal class), _conf (mean class membership probability), _stdev, _n (number of pixels).
  - Note: some attribute names differ from LCM2015 to align with production software; parcel IDs (gid) do not match LCM2015 for direct cross-year comparison.
- 25m Rasterised Land Parcels
  - Three-band raster: band 1 = modal class (_mode); band 2 = parcel-averaged confidence (_conf); band 3 = parcel purity (_purity).
  - Provides a generalized representation of parcel-level results.
- 1km Rasters
  - 1km Percent Cover: 21-band raster (percentage cover by each UKCEH Land Cover Class per 1km grid cell).
  - 1km Percent Aggregate Cover: 10-band raster (percentage by UKCEH Aggregate Classes per 1km).
  - 1km Dominant Cover: single-band raster of dominant class per 1km cell.
  - 1km Dominant Aggregate Cover: single-band raster of dominant aggregate class per 1km cell.
- Spatial and Coordinate Details
  - Great Britain: GB National Grid (EPSG: 27700); Northern Ireland: Irish Grid (EPSG: 29903).
  - Pixel sizes and extents are defined per dataset; outputs are provided in GB and NI variants for each year (2017, 2018, 2019).

## Classification Scenes and Input Details
- Seasonal Composite Images
  - Generated from Sentinel-2 data using Google Earth Engine; TOA reflectance used for production.
  - Bands correspond to 9 Sentinel-2 bands across multiple resolutions; 4-season composites with gaps represented as nulls.
- Context Rasters
  - GB: height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, woodland mask.
  - NI: height, aspect, slope, urban mask, distance to coast, freshwater, road.
- UK Land Parcel Spatial Framework
  - Uses fixed parcel geometries to provide stable units for time-series analysis and change detection.
  - Maintains approximately 0.5 ha MMU; designed to capture discrete real-world units (fields, parks, urban areas, etc.).
  - Supports both parcel-based outputs and user-defined summaries.

## Validation and Quality
- Validation
  - UK-scale validation using 22,325 points from GB Countryside Survey 2019, National Forest Inventory, IACS, and bespoke LCM validation points.
- Accuracy
  - Overall accuracy around 79% across 21 classes:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data are not perfect truth; variability in currency and class mapping exists. Full correspondence tables are provided in Appendix 4.
- Class-level performance
  - Producer and user accuracies vary by class; outputs include detailed confusion matrices and accuracy statistics for each year (provided in Appendices).

## Governance, Standards, and Future Plans
- Data governance and interoperability
  - Clear documentation of data lineage, coordinate systems, and class mappings to support reuse and cross-year comparisons within the Land Parcel Spatial Framework.
  - Acknowledges cross-year challenges due to gid changes and framework evolution; provides guidance for users on comparing LCM2017–2019.
- Future directions
  - Annual map releases to capture land-cover change (planning to continue beyond 2019).
  - Exploration of expanding data inputs (e.g., SAR, alternative optical sources) to improve gap-filling and thematic detail.
  - Potential refinement of the Land Parcel Spatial Framework as data inputs become higher resolution or new mapping approaches emerge.

## Appendices and References (Highlights)
- Appendix 1–2: UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats; notes on class definitions, ambiguities, and mappings to UK BAP.
- Appendix 3: Recommended RGB color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Validation details and confusion matrices for LCM2017, LCM2018, and LCM2019 (including per-class producer and user accuracies).
- Appendix 5: Full dataset list per year (20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, 1km products; GB and NI variants).

This document provides the methodology, data structures, validation, and governance context needed for Data Stewards to manage, share, and reuse the UKCEH Land Cover Maps 2017–2019 datasets effectively.