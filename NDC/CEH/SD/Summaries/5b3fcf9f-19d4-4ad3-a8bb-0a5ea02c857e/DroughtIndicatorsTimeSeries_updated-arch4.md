# Drought indicator time series for European NUTS regions based on remote sensing data (2000-2015)

## Brief Description
- Dataset of remotely sensed drought indicator time series for European NUTS regions (level 0, 1, 2, and 3).
- Three indicators derived from remote sensing: Vegetation Condition Index (VCI) from NDVI, Temperature Condition Index (TCI) from Land Surface Temperature, and Vegetation Health Index (VHI) = α·VCI + (1−α)·TCI (α ≈ 0.5).
- Data extracted from CEH’s gridded drought indicators product and masked by land use land cover (LULC) into four classes (forest, crop, shrub, grass) plus an aggregate (all classes).
- Stored in CSV format; time series cover 2000–2015.

## Data Context and Motivation
- Developed within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Aims to support monitoring and early warning (M&EW) by leveraging near real-time, globally covered, and cost-effective remote sensing data.
- Validation and application focus: drought indices related to impacts data available at the European NUTS level; LULC differentiation enables assessing different vegetation responses.

## Data Sources and Methodology
- Primary data: gridded drought indices product for Europe (2000–2015); LULC map from MODIS MCD12C1 (0.05°) for 2012.
- Calculation approach:
  - VCI: (NDVI − NDVI_min,i) / (NDVI_max,i − NDVI_min,i) for each month i over the analysis period.
  - TCI: (LST_max,i − LST) / (LST_max,i − LST_min,i) for each month i.
  - VHI: α·VCI + (1−α)·TCI, with α typically 0.5.
- Spatial-temporal structuring:
  - Regions: European NUTS (2013 version).
  - LULC differentiation yields 15 time series per NUTS region (5 per indicator: 4 land cover classes + 1 all-classes).
  - Time steps produced only if ≥50% of non-masked pixels have valid values.

## Data Format and Structure
- Format: CSV files.
- Organization: data stored in folders (structure described in the source documentation).

## Data Quality and Processing Rules
- Handling of No Data:
  - “--” indicates no valid pixels in the non-masked area.
  - “nan” indicates some valid pixels but less than 50% coverage.
- Time steps with insufficient data (less than 50% valid) are discarded to ensure representativeness.

## Access, Usage, and Applications
- Useful for cross-regional drought monitoring, validation of drought indicators against impacts data, and assessing vegetation responses by land cover type.
- Supports European-scale early warning and research into remote-sensing drought indicators.

## Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

## References
- AghaKouchak et al. 2015. Remote sensing of drought: progress, challenges and opportunities.
- Bachmair et al. 2016. Drought indicators revisited: the need for a wider consideration of environment and society.
- Bachmair et al. 2018. How well do meteorological indicators represent agricultural and forest drought across Europe?
- Kogan 1995, 1997. Drought detection methodologies.
- Tanguy et al. 2016. Gridded drought indices based on remote sensing data for Europe (2000–2015).