# Gridded drought indices based on remote sensing data for Europe (2000-2015)

## Brief description
- Three gridded drought indicators derived from remote sensing: Vegetation Condition Index (VCI) based on NDVI, Temperature Condition Index (TCI) based on Land Surface Temperature (LST), and Vegetation Health Index (VHI) combining VCI and TCI (VHI = α VC I + (1−α) TCI; α typically 0.5).
- Spatial resolution: 0.05 degree; temporal resolution: monthly.
- Period: 2000–2015; data stored as NetCDF4 files following CEH gridded dataset conventions.
- Structure: Europe-wide two-dimensional grids; twelve monthly grids per year; one yearly file per drought indicator.
- Projection: WGS84.
- Data sources and provenance: MODIS NDVI (MOD13C2) and MODIS LST (MOD11C3) products, downloaded from NASA Reverb/ECHO.
- Purpose and use: developed within the DrIVER project to assess drought indices for monitoring and early warning (M&EW) purposes; supports real-time potential due to the near real-time nature of remote sensing data.

## Motivation
- Addresses the potential and variability of remote-sensing drought indicators in M&EW systems.
- Created to evaluate the utility of remotely sensed agricultural drought indicators for Europe within the DrIVER framework.
- Documentation and methodology support reproducibility and future integration into monitoring systems.

## Data sources
- MODIS NDVI: MOD13C2.
- MODIS LST: MOD11C3.
- Data access: NASA Reverb/ECHO portal.
- Supporting documentation available through the NERC Environmental Information Data Centre (EIDC).

## Method for deriving the drought indicators
- VCI: (NDVI − NDVI_min,i) / (NDVI_max,i − NDVI_min,i) for month i.
- TCI: (LST_max,i − LST) / (LST_max,i − LST_min,i) for month i.
- VHI: α × VCI + (1 − α) × TCI, with α typically 0.5.
- Computation follows the methodology described by Kogan (1995).

## Format and data structure
- File format: NetCDF4, following CEH conventions.
- Grid structure: two-dimensional grids covering Europe; 12 monthly grids per year.
- File organization: one yearly file per indicator (VCI, TCI, VHI).
- Coordinate reference: WGS84.

## Governance, provenance, and documentation
- Project context: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (NE/L010038/1) as part of the Belmont Forum initiative.
- Documentation: supporting documentation available; data lineage and processing described; dataset archived with related references and methodology (including key literature such as AghaKouchak et al., Kogan, and Karnieli et al.).