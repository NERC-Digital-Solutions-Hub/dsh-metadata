# Gridded drought indices based on remote sensing data for Europe (2000-2015)

## Overview
- Three gridded drought indicators for Europe at 0.05-degree spatial resolution with monthly temporal resolution (2000–2015).
- Indicators: Vegetation Condition Index (VCI) from NDVI, Temperature Condition Index (TCI) from Land Surface Temperature, and Vegetation Health Index (VHI) = α·VCI + (1−α)·TCI (α typically 0.5).
- Data stored in NetCDF4 format and projected on the WGS84 coordinate system.

## Motivation
- Developed within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices in relation to impacts data for monitoring and early warning systems.
- Highlights the potential of remote sensing for near real-time, globally covered, low-cost drought monitoring.
- Addresses variability in the use of remote sensing indicators in operational drought monitoring and aims to evaluate their utility at a European scale (found in related work Bachmair et al., 2018).

## Data Sources
- MODIS NDVI product: MOD13C2.
- MODIS LST product: MOD11C3.
- Data accessed from NASA Reverb | Echo.
- Supporting documentation and project context provided in the associated NERC data centre records.

## Method for deriving the drought indicator grids
- VCI calculation: (NDVI − NDVImin,i) / (NDVImax,i − NDVImin,i), where NDVImin,i and NDVImax,i are the monthly min/max values across the analysis period for month i.
- TCI calculation: (LSTmax,i − LST) / (LSTmax,i − LSTmin,i), using monthly bounds.
- VHI: VHI = α·VCI + (1 − α)·TCI, with α commonly set to 0.5.
- Method follows the approach described by Kogan (1995).

## Data Format and structure
- Stored in NetCDF4 format, following CEH gridded dataset conventions.
- Europe-wide two-dimensional monthly grids, with twelve grids per year for each indicator.
- One yearly NetCDF file per drought indicator (three files total).
- Data are projected in the WGS84 reference system.

## Acknowledgments
- Result of the DrIVER project; funding from the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

## References
- AghaKouchak et al. 2015; remote sensing of drought.
- Bachmair et al. 2016, 2018; drought indicators and their use in M&E.
- Karnieli et al. 2006; Kogan 1995, 1997; vegetation index and drought indicators.