# Drought indicator time series for European NUTS regions based on remote sensing data (2000-2015)

- Brief Description
  - A dataset of remotely sensed drought indicator time series for Europe, extracted from CEH’s gridded drought indicators product (2000-2015).
  - Indicators: Vegetation Condition Index (VCI) from NDVI, Temperature Condition Index (TCI) from LST, and Vegetation Health Index (VHI) = α·VCI + (1−α)·TCI (α typically 0.5).
  - Time series are provided for European NUTS regions (levels 0, 1, 2, 3) and are masked by a simplified land use land cover (LULC) map with four classes (forest, crop, shrub, grass) plus an “all classes” aggregate.
  - Data stored in CSV format.

- Motivation
  - Developed within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to support monitoring and early warning systems with near real-time, globally covered, cost-effective remote sensing data.
  - Aims to assess agricultural and forest drought indicators at the European scale; NUTS-region aggregation aligns with available drought impact data and allows LULC differentiation.

- Data Sources
  - Gridded drought indices derived from remote sensing data for Europe (2000-2015).
  - Land Use and Land Cover (LULC) map derived from MODIS Land Cover Type data (MCD12C1, 0.05°) for 2012.

- Method for deriving the drought indicator time series
  - VCI: (NDVI − NDVI_min,i) / (NDVI_max,i − NDVI_min,i) for month i, using monthly NDVI values.
  - TCI: (LST_max,i − LST) / (LST_max,i − LST_min,i) for month i, using monthly LST.
  - VHI: VHI = α·VCI + (1−α)·TCI, with α typically 0.5.
  - NUTS spatial references use the 2013 version.
  - LULC: simplified four-class map (forest, crop, grass, shrub) applied per NUTS region to yield 15 time series per region (5 per drought indicator: 4 land cover classes plus the aggregated whole-region series).
  - Data inclusion criteria: a time step is produced only if at least 50% of pixels in the non-masked area have valid values.
  - Data absence semantics: two No Data cases exist—'--' for no valid pixels within the non-masked area, and 'nan' when some valid pixels exist but coverage is below 50%. Time steps with <50% are discarded.

- Format & Structure of the dataset
  - Stored in CSV format.
  - Data organized in folders (structure described but not exhaustively detailed in the summary).
  - Each NUTS region has multiple time series (15 total per region: 5 per indicator across 4 land cover classes plus the all-classes series).

- Acknowledgments
  - Outcome of the DrIVER project; funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

- References
  - Key foundational sources on remote sensing drought indicators (VCI, TCI, VHI) and their application, including works by Kogan (1995, 1997) and related reviews and European-focused studies (AghaKouchak et al., Bachmair et al., Tanguy et al., etc.).