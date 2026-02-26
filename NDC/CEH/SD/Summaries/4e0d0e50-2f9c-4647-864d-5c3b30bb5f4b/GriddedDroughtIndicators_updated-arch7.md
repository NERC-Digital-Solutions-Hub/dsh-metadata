# Gridded drought indices based on remote sensing data for Europe (2000-2015)

## Overview
- Dataset comprises three gridded drought indicators for Europe.
- Spatial resolution: 0.05 degree; temporal resolution: monthly.
- Time period: 2000–2015.
- Indicators: Vegetation Condition Index (VCI) from NDVI, Temperature Condition Index (TCI) from LST, and Vegetation Health Index (VHI) combining VCI and TCI.
- Data format: NetCDF4, following CEH gridded dataset conventions; projected to WGS84.
- Data packaged as two-dimensional grids with twelve monthly grids per year; one yearly file per indicator.

## Indicators and computation
- VCI: based on NDVI with (NDVI - NDVI_min,i) / (NDVI_max,i - NDVI_min,i) for each month i.
- TCI: based on LST with (LST_max,i - LST) / (LST_max,i - LST_min,i) for each month i.
- VHI: VHI = α × VCI + (1 − α) × TCI, where α typically equals 0.5.
- NDVI and LST inputs come from MODIS products:
  - NDVI: MOD13C2
  - LST: MOD11C3
- Monthly grids are combined to create annual files for each indicator.

## Data sources
- MODIS NDVI (MOD13C2) and MODIS LST (MOD11C3) products.
- Data accessed via NASA Reverb/Echo.
- Supporting documentation published with the DrIVER project outputs.

## Processing method and conventions
- Derived using the methodology described by Kogan (1995).
- Indices are computed per month using monthly statistics across the analysis period.
- Data stored as two-dimensional grids per year and per indicator, aligned to CEH conventions.

## Usage and GIS applications
- Suitable for map-based drought visualization and European-scale drought monitoring.
- Enables time-series analysis of drought indicators and spatial pattern exploration.
- Can support monitoring and early warning (M&EW) workflows when integrated with additional impact data.
- Raw inputs (NDVI, LST) are suitable for GIS workflows after appropriate format conversions.

## Practical considerations for GIS specialists
- Large, multi-year NetCDF4 files may require chunked loading or subsetting for performance.
- Ensure data are properly projected (WGS84) and resampled as needed for compatibility with other layers.
- Maintain awareness of data resolution, temporal coverage (2000–2015), and potential data quality issues inherent in remote sensing products.
- Consider data standardization and documentation to facilitate sharing and interoperability.

## Acknowledgments and references
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.
- References include Kogan (1995, 1997) and related literature on drought indicators and remote sensing methodologies.