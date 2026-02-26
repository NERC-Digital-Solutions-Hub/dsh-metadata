# Supporting Documentation for Relative surface soil moisture for the Thames Valley, United Kingdom, October 2015 to September 2021

## Overview
- Provides relative Surface Soil Moisture (rSSM) estimates for Thames Valley, Oct 2015–Sep 2021.
- Based on the TU-Wien Change Detection Algorithm (TWCDA) applied to Sentinel-1 radar backscatter (σ0).
- rSSM values range from 0% (driest) to 100% (wettest); dataset created with MATLAB R2021a; testable with Python and QGIS.

## Dataset creation
- Changes in backscatter are attributed to soil moisture, assuming surface roughness and geometry are temporally constant.
- Uses backscatter σ0(Θ,t) at time t and incidence angle Θ, normalized to a reference angle Θ (40°) and linearly scaled between dry and wet references.
- Key equation: rSSM(t) = [σ0(Θ,t) − σ0_d(Θ)] / [σ0_w(Θ) − σ0_d(Θ)] (in percent).
- Derivation of dry and wet thresholds described in the methodology.

## Pre-processing the raw Sentinel-1 data
- Geocoding and radiometric correction performed with ESA SNAP; includes orbital corrections, thermal and border noise removals, radiometric calibration.
- Speckle filtering via Refined Lee; terrain correction using SRTM 3Sec data.
- Data subset to area of interest; stitching of frames to create a single radar file per scan day; Local Incidence Angle (LIA) data also subset for normalization.

## Backscatter Normalisation
- σ0 is normalized to a common incidence angle to remove LIA dependencies, ensuring changes reflect ground conditions (soil moisture).
- Two LIA normalization approaches: direct regression slope (β_d) and multiple regression slope (β_r).
- This study introduces a monthly varying normalization parameter, computing β_d and β_r for individual months using orbit data.
- Normalization equation: σ0(Θ,t) = σ0(θ,t) − β(θ − Θ) [dB].

## Dynamic Backscatter Masking
- Excludes very high/low backscatter values that are unlikely to reflect soil moisture signals.
- Masks applied with thresholds of −5 dB and −22 dB; additionally masks ‘Artificial’ (urban) and ‘Freshwater’ areas.

## Spatial Averaging
- IW mode resolution of Sentinel-1 (5 × 20 m) can be problematic for heterogeneous landscapes.
- Backscatter data upscaled by arithmetic mean to coarser resolutions: 1 km, 500 m, 250 m, and 100 m.
- Coarser resolutions show high correlations (≥ 0.7) with in-situ measurements, aiding evaluation across land uses and natural flood management (NFM) contexts.

## Wet and Dry Threshold
- Wet and dry thresholds (σ0_w(Θ) and σ0_d(Θ)) are statistically derived when long time series are limited.
- Uses 10th and 90th percentiles of the normalized backscatter time series, linked to approximate 0% and 100% rSSM.
- Outliers: rSSM values outside ±20% of the 0–100% range are set to 0% or 100%; values beyond the 20% buffer are set to No Data.

## Dataset Metadata
- Stored in a single NetCDF file with 610 variables.
- Dates are in YYYYMMDD format; CRS is EPSG 4326.
- Variables include lat, lon, and rSSM values for each timestep (one variable per date), organized as V002–V606 (and beyond for all timestamps).

## Data accessibility and governance
- Primary dataset reference: Maslanka et al., 2022 (IEEE Transactions on Geoscience and Remote Sensing) describing the retrieval and validation framework.
- Open data practices and metadata quality are integral to the dataset, consistent with monitoring framework practices for data provenance, traceability, and reproducibility.

## References
- (Key sources detailing the normalised backscatter model, prior sentinel-1 soil moisture work, preprocessing workflows, and related methodologies cited in the document.)