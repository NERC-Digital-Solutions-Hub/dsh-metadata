# Gridded drought indices based on remote sensing data for Europe (2000-2015)

## Overview
- Dataset comprises three gridded drought indicators for Europe at 0.05-degree spatial resolution with monthly temporal resolution, covering 2000–2015.
- Indicators: Vegetation Condition Index (VCI) based on NDVI; Temperature Condition Index (TCI) based on Land Surface Temperature; Vegetation Health Index (VHI), a weighted combination of VCI and TCI.
- VHI is calculated as VHI = α·VCI + (1−α)·TCI, with α typically set to 0.5.

## Data motivation and use
- Developed within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices in relation to impacts data for monitoring and early warning systems.
- Demonstrates the potential of remotely sensed drought indicators for European-scale monitoring and early warning, complementing precipitation-based indicators.

## Data sources
- MODIS NDVI data: MOD13C2.
- MODIS Land Surface Temperature (LST) data: MOD11C3.
- Sources retrieved from NASA Reverb / Echo.

## Method for deriving grids
- VCI derived from NDVI using the normalize-by-month equation: VCI = (NDVI − NDVI_min,i) / (NDVI_max,i − NDVI_min,i).
- TCI derived from LST using a similar normalization: TCI = (LST_max,i − LST) / (LST_max,i − LST_min,i).
- VHI combines VCI and TCI with α: VHI = α·VCI + (1−α)·TCI (α commonly 0.5).
- Method follows Kogan (1995) methodology.

## Data format and structure
- Data stored in NetCDF4 format following CEH gridded dataset conventions.
- European-wide two-dimensional grids with twelve monthly grids per year.
- One yearly NetCDF file per drought indicator.
- Projection in WGS84.

## Access, metadata, and acknowledgments
- Part of the DrIVER project; funded by Natural Environment Research Council (award NE/L010038/1) under the Belmont Forum initiative.
- Supporting documentation and data deposited at the NERC Environmental Information Data Centre; DOI provided in the documentation.

## References (selected)
- AghaKouchak et al., 2015; remote sensing of drought.
- Bachmair et al., 2016, 2018; drought indicators and their representation in M&EW systems.
- Karnieli et al., 2006; Kogan, 1995, 1997; development and validation of vegetation and drought indices.