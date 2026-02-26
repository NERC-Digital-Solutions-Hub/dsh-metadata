# Gridded drought indices based on remote sensing data for Europe (2000-2015)

## Brief description of the dataset
- Three gridded drought indicators for Europe at 0.05 degree spatial resolution, monthly from 2000 to 2015.
- Indicators: Vegetation Condition Index (VCI) from NDVI, Temperature Condition Index (TCI) from Land Surface Temperature, and Vegetation Health Index (VHI) combining VCI and TCI.
- VHI calculated as VHI = alpha * VCI + (1 - alpha) * TCI, with alpha commonly set to 0.5.
- Data stored in NetCDF4 format following CEH gridded dataset conventions; projections in WGS84.
- Dataset derived to support drought assessment within a monitoring and early warning (M&EW) framework.

## Motivation
- Produced under the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices in relation to impacts data for M&EW.
- Highlights the potential of remote sensing for M&EW due to near real-time availability, global coverage, and relatively low cost.
- Acknowledges variability in the use of remote-sensing drought indicators across European operational systems and the need to evaluate their applicability.

## Data sources
- MODIS NDVI product: MOD13C2.
- MODIS LST product: MOD11C3.
- Data sourced from NASA Reverb (reverb.echo.nasa.gov).

## Method for deriving the drought indicator grids
- VCI computed from NDVI relative to monthly historical min and max for that month.
- TCI computed from LST relative to monthly historical min and max for that month.
- VHI derived as a weighted combination of VCI and TCI (commonly alpha = 0.5).

## Format of the dataset
- NetCDF4 files following CEH conventions.
- Two-dimensional grids covering Europe, with 12 monthly grids per year.
- One yearly file per drought indicator (VCI, TCI, VHI).

## Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

## References
- Foundational methods and context include works by AghaKouchak et al. (remote sensing of drought), Karnieli et al. (VHI considerations), and Kogan (drought indicators and methodologies).