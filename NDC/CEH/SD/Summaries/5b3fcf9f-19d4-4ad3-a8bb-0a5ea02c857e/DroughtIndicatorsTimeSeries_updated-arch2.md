Drought indicator time series for European NUTS regions based on remote sensing data (2000-2015)

## Overview
- A dataset of remotely sensed drought indicators time series for Europe from 2000 to 2015.
- Derived from CEH gridded drought indicators using NDVI-based Vegetation Condition Index (VCI), Land Surface Temperature-based Temperature Condition Index (TCI), and their combination (Vegetation Health Index, VHI).
- Extracted for European NUTS regions (levels 0, 1, 2, 3) and masked by a simplified land-use land-cover (LULC) map.
- For each NUTS region, produces multiple time series across land-cover classes and an overall series; stored in CSV format.

## Data sources and indicators
- LULC map from MODIS MCD12C1 (0.05°) for 2012; simplified into four classes: forest, crop, shrub, grass (plus an all-classes series).
- NDVI (for VCI) and LST (for TCI) derived from remote sensing data.
- VCI calculation: normalized to monthly NDVI values using monthly min/max.
- TCI calculation: normalized to monthly LST values using monthly min/max.
- VHI = α·VCI + (1 − α)·TCI with α = 0.5 (equal contribution of VCI and TCI).
- NUTS geocoding based on the 2013 version of NUTS.

## Data processing and time series construction
- For each NUTS region, 15 time series are produced: 5 per drought indicator (one for each of the 4 land-cover classes plus a region-wide series without land-cover differentiation).
- Time steps are included only if at least 50% of non-masked pixels are valid.
- NoData values: “--” indicates no valid pixels; “nan” indicates some valid pixels but less than 50% coverage; those steps are discarded.

## Format and structure
- Data stored in CSV format.
- Organized in folders to reflect the dataset structure.

## Motivation and use
- Created within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices against impacts data for monitoring and early warning (M&EW).
- Remote sensing offers near real-time coverage and cost-effective monitoring; the dataset supports validation with impact data and enables land-cover differentiated analyses.

## Data quality and access considerations for the Analyst
- Employs standardised calculation methods with data verification and quality assurance.
- Data are cleaned, transformed, and prepared for inclusion in appropriate portals; underlying data can be accessed to support outputs.
- Encourages combining these drought indicators with other relevant datasets to enhance monitoring value and to enable data sharing.

## Acknowledgments and references
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative; project DrIVER.
- Key references include work by Kogan (VCI/TCI), Tanguy et al. (gridded drought indices for Europe), and Bachmair et al. (drought indicators and their use in monitoring).