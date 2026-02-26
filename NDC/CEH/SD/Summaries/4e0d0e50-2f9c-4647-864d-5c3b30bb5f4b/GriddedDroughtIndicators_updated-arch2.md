# Gridded drought indices based on remote sensing data for Europe (2000-2015)

## Brief description
- A dataset of three gridded drought indicators for Europe with 0.05-degree spatial resolution and monthly temporal resolution from 2000 to 2015.
- Indicators: Vegetation Condition Index (VCI) from NDVI, Temperature Condition Index (TCI) from Land Surface Temperature, and Vegetation Health Index (VHI) combining VCI and TCI.
- VHI is computed as VHI = α·VCI + (1−α)·TCI, with α typically 0.5.
- Data stored in NetCDF4 format and aligned to CEH gridded dataset conventions; projected in WGS84.

## Data and geographic coverage
- Two-dimensional grid datasets covering Europe.
- Twelve monthly grids per year; one yearly file per drought indicator.

## Data sources
- MODIS NDVI product: MOD13C2.
- MODIS Land Surface Temperature: MOD11C3.
- Data downloaded from NASA Reverb/ECHO.

## Method for deriving drought indicators
- Based on Kogan (1995) methodology:
  - VCI = (NDVI − NDVI_min,i) / (NDVI_max,i − NDVI_min,i) for month i across the analysis period.
  - TCI = (LST_max,i − LST) / (LST_max,i − LST_min,i).
  - VHI = α·VCI + (1 − α)·TCI, with α often set to 0.5.

## Motivation and purpose
- Produced within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Aims to assess drought indices in relation to impacts data within a monitoring and early warning (M&EW) system.
- Highlights the potential of remote sensing for near real-time, globally coherent drought monitoring and its integration into M&EW frameworks; complements other indicators like SPI.

## Format and access details
- NetCDF4 format following CEH gridded dataset conventions.
- Data organized as Europe-wide grids; 12 monthly grids per year; separate yearly files per indicator.
- Projection: WGS84.

## Acknowledgments and context
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.
- Related references discuss the use and evaluation of remote-sensing drought indicators in Europe.

## Implications for analysts monitoring the environment
- Provides standardized, multi-indicator drought metrics suitable for integration with impacts data and other environmental datasets.
- Facilitates long-term monitoring and policy performance assessment across Europe (2000–2015).
- Potential enhancements include combining with additional datasets to increase utility and improving data accessibility for broader analysis.