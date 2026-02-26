# Supporting Documentation for Relative surface soil moisture for the Thames Valley, United Kingdom, October 2015 to September 2021

## Overview
- Provides relative Surface Soil Moisture (rSSM) estimates for Thames Valley, UK, from October 2015 to September 2021.
- rSSM ranges from 0% (dryest) to 100% (wettest) across the time series.
- Derived from Sentinel-1 radar backscatter (sigma0) using the TU-Wien Change Detection Algorithm (TWCDA).
- Assumes changes in backscatter reflect soil moisture changes, with other influencing factors (roughness, geometry) treated as temporally constant.
- Methodology documented in Maslanka et al., 2022.

## Data processing and algorithm (Method Summary)
- Pre-processing:
  - Sentinel-1 data geocoded and radiometrically corrected via ESA SNAP.
  - Apply orbital corrections, thermal/border noise removals, radiometric calibration.
  - Speckle filtering (Refined Lee) and terrain correction (SRTM 3Sec).
  - Subset to area of interest; stitch frames into single radar file per scan day; align Local Incidence Angle (LIA) data.

- Backscatter normalization:
  - Normalize sigma0 to a common incidence angle using a per-pixel beta factor (dB/°).
  - Reference angle Theta = 40°.
  - Normalization: sigma0(Theta,t) = sigma0(theta,t) − beta(theta−Theta) (in dB).
  - Beta estimated via direct regression (beta_d) or a monthly-updated multiple regression (beta_r) that incorporates mean backscatter and other factors.
  - Novel approach: monthly varying normalization factors applied to Sentinel-1 orbits.

- Dynamic backscatter masking:
  - Remove extreme backscatter values using thresholds of −5 and −22 dB.
  - Mask out artificial (urban) and freshwater areas.

- Spatial averaging:
  - Original IW mode resolution is 5×20 m (effective ~20×22 m).
  - Upscale to 1 km, 500 m, 250 m, and 100 m by arithmetic mean to reduce heterogeneity while preserving soil-moisture signal.

- Wet and dry thresholds:
  - Compute per-pixel thresholds from the 10th and 90th percentiles of the normalized backscatter time series.
  - Convert thresholds to 0–100% rSSM; clamp values to 0%–100%.
  - Outliers beyond ±20% from the 0–100% range are set to 0% or 100%; values outside the 20% buffer are set to No Data.

## Dataset structure and contents
- Delivered as a single NetCDF file containing approximately 610 variables.
- Dates are in YYYYMMDD format; coordinate system is EPSG 4326.
- Data includes latitude/longitude arrays and per-timestep rSSM values.
- Time span covered: 20151002 to 20210930.
- Variable naming in the NetCDF file includes numerous V### entries (e.g., V002 for lat, V003 for time 20151002, etc.), representing the spatial and temporal dimensions of the rSSM dataset.

## Applications and validation
- Coarser spatial resolutions (e.g., 1 km, 500 m) show high correlation with in-situ measurements (≥0.7) for land-use evaluation relevant to natural flood management (NFM).
- The dataset supports analysis of soil moisture dynamics and land-use impacts within Thames Valley.

## Technical references and lineage
- Core concepts based on the TU-Wien Change Detection Algorithm (TWCDA) with foundations in:
  - Wagner et al. (1999a, 1999b)
  - Bauer-Marschallinger et al. (2019, 2021)
  - Pathe et al. (2009)
  - Maslanka et al. (2022) for sub-kilometric rSSM retrieval with Sentinel-1 normalization factors
  - Related validation and methodological works (Lindell & Long 2016; Loew et al. 2006; Sabel et al. 2010; Zakharov et al. 2020; Mattia et al. 2017, 2018)

## Data access, reproducibility, and references
- Processing implemented in Matlab R2021a; can be opened with Python or QGIS for inspection.
- Open Access Publication provides full dataset creation explanation and methodological details.
- Key references cited for the methodology and validation, including datasets and land-cover context.