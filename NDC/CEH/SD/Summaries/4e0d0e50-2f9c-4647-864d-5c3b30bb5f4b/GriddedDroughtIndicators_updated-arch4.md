# Gridded drought indices based on remote sensing data for Europe (2000-2015)

## Brief description
- Three gridded drought indicators based on remote sensing data for Europe.
- Spatial resolution: 0.05 degree; temporal resolution: monthly; period: 2000–2015.
- Indicators: Vegetation Condition Index (VCI) from NDVI (MODIS NDVI product MOD13C2), Temperature Condition Index (TCI) from Land Surface Temperature (MODIS LST product MOD11C3), and Vegetation Health Index (VHI), a combination of VCI and TCI.
- Data stored in NetCDF4 format, following CEH gridded dataset conventions.
- Grid structure: two-dimensional grids covering Europe, twelve monthly grids per yearly file; one yearly file per indicator.
- Projection: WGS84.

## Motivation
- Developed under the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to support monitoring and early warning systems.
- Remote sensing offers near real-time availability, wide coverage, and relatively low cost for drought indicators.
- Aimed to assess and compare remotely sensed agricultural drought indicators for European monitoring and early warning contexts.

## Data sources
- MODIS NDVI product MOD13C2 (for VCI).
- MODIS Land Surface Temperature product MOD11C3 (for TCI).
- Data downloaded from NASA Reverb/ECHO.

## Method for deriving the drought indicator grids
- VCI = (NDVI − NDVI_min,i) / (NDVI_max,i − NDVI_min,i), where NDVI_min,i and NDVI_max,i are the monthly min/max NDVI over the analysis period.
- TCI = (LST_max,i − LST) / (LST_max,i − LST_min,i), with LST_min,i and LST_max,i being the monthly min/max LST over the period.
- VHI = α·VCI + (1 − α)·TCI, with α typically set to 0.5 (equal contribution of VCI and TCI).

## Format and structure of the dataset
- Stored as NetCDF4 files, adhering to CEH gridded dataset conventions.
- Europe-wide grids with 12 monthly grids per year; one file per indicator per year.
- Data are projected in the WGS84 coordinate system.

## Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

## References
- AghaKouchak et al., 2015; Bachmair et al., 2016; Karnieli et al., 2006; Kogan, 1995, 1997; and related DrIVER project publications (Bachmair et al., 2018).