# Supporting Documentation for Relative surface soil moisture for the Thames Valley, United Kingdom, October 2015 to September 2021

## Overview of the data product
- Provides relative Surface Soil Moisture (rSSM) estimates for the Thames Valley, UK, from October 2015 to September 2021.
- rSSM values range from 0% (driest) to 100% (wettest) for each pixel over the time series.
- Derived from Sentinel-1 radar backscatter (σ0) using the TU-Wien Change Detection Algorithm (TWCDA).
- The dataset was created with Matlab R2021a; testable with Python and QGIS as well.

## Data product and methodology
- Core algorithm: rSSM(t) is computed by normalising σ0(Θ, t) to a reference incidence angle Θ and linearly scaling between dry and wet thresholds.
  - Formula: rSSM(t) = [σ0(Θ, t) − σ0d(Θ)] / [σ0w(Θ) − σ0d(Θ)] [percent]
  - Θ is fixed at 40 degrees; σ0d and σ0w are dry and wet backscatter thresholds, derived as described in the methodology.
- Change detection basis: backscatter changes are attributed to soil moisture changes, assuming other factors (roughness, geometry) are temporally constant.

## Pre-processing and data preparation
- Geocoding and radiometric correction performed with ESA SNAP:
  - Includes orbital corrections, thermal and border noise removal, radiometric calibration.
  - Speckle filtering with Refined Lee; terrain correction using SRTM 3Sec.
  - Data subset to the area of interest and stitched when the area is covered by multiple frames per day.
  - Local Incidence Angle (LIA) data subset and alignment with radiometrically corrected backscatter for normalization.

## Backscatter normalization (LIA normalization)
- Normalisation of σ0 to a common incidence angle to remove LIA effects:
  - Observed backscatter is adjusted to a reference angle Θ = 40° using β, a per-pixel parameter (dB/°).
  - Two methods to estimate β:
    - Direct regression slope (βd): simple linear relationship between θ and σ0°.
    - Multiple linear regression (βr): uses constants a, b, c to relate βr to mean backscatter and surface-related factors.
- Novel approach in this study: model β (both βd and βr) as monthly varying normalisation factors, enabling per-month parameterisation per Sentinel-1 orbit.

## Dynamic backscatter masking
- Removes outliers and signals unlikely to reflect soil moisture:
  - Mask thresholds per image: -5 dB (upper) and -22 dB (lower).
  - Additional masking excludes artificial (urban/suburban) and freshwater areas.

## Spatial resolution and aggregation
- Raw Sentinel-1 IW mode resolution (~5 x 20 m) is upscaled to coarser grids to reduce heterogeneity from vegetation, crop structure, roughness, etc.
- Resolutions used: 1 km, 500 m, 250 m, and 100 m.
- Upscaling performed by arithmetic mean to preserve overall moisture signal while reducing noise.

## Wet and dry threshold determination
- Wet/dry thresholds are derived statistically given the relatively short time series:
  - Use the 10th and 90th percentiles of the normalised backscatter time series to approximate 0% and 100% rSSM.
- Outlier handling and data quality:
  - rSSM values that extend beyond ±20% of the 0–100% range are clipped to 0% or 100%.
  - Values outside the ±20% buffer are set to No Data.

## Dataset metadata and structure
- Storage: single NetCDF file containing 610 variables.
- Time notation: all dates in YYYYMMDD format.
- Coordinate reference system: EPSG 4326 (WGS84).
- Variables: large metadata table listing per-timestep rSSM data and corresponding lat/lon grids (e.g., V002–V606 plus many time-indexed variables).
- Practical notes:
  - The dataset is designed for self-service analysis of relative soil moisture changes over time and space in the Thames Valley.
  - Validation and testing performed using MATLAB; tested with Python and QGIS for access and inspection.

## Data usage and potential applications
- Intended for monitoring relative soil moisture dynamics across land uses in the Thames Valley.
- Compatible with multi-scale analyses due to multiple spatial resolutions (1 km to 100 m).
- Useful for drought assessment, water management, agriculture planning, and flood risk assessment through interpretation of moisture trends.
- Reported correlation with in-situ measurements at coarse scales (≥ 0.7) for certain aggregations.

## Data quality considerations and limitations
- Time series length is limited to October 2015–September 2021; extremes may be influenced by short time windows.
- Normalisation is monthly varying, which improves accuracy but adds complexity for time-series analyses.
- Backscatter signals can still be influenced by residual surface conditions (vegetation, roughness) despite masking and normalisation.
- Wet/dry thresholds are statistical estimates rather than direct long-term extremes; No Data is returned for non-physical or unreliable values.

## References and sources
- Key references detailing the underlying methods and precedents for Sentinel-1 soil moisture retrieval and backscatter normalization, including:
  - Bauer-Marschallinger et al. on normalized backscatter models and global soil moisture monitoring.
  - Maslanka et al. (2022) on relative surface soil moisture retrieval with Sentinel-1 using different normalization factors.
  - Wagner et al. foundational change detection and soil moisture retrieval methodologies.
  - Related works on ENVISAT ASAR, ASCAT, and ENVISAT/ERS-based soil moisture approaches.
  - Land cover datasets and validation studies informing masking and accuracy assessments.