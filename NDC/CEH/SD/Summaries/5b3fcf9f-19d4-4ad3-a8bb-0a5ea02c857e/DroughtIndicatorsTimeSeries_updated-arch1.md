# Drought indicator time series for European NUTS regions based on remote sensing data (2000-2015)

## Brief Description of the dataset
- Remotely sensed drought indicators time series for Europe (2000-2015) derived from CEH’s gridded drought indicators product.
- Three indicators: Vegetation Condition Index (VCI) from NDVI, Temperature Condition Index (TCI) from Land Surface Temperature, and Vegetation Health Index (VHI) combining VCI and TCI.
- Data extracted for European NUTS regions (level 0–3), masked by a land-use land-cover (LULC) map with four classes (forest, crop, shrub, grass) plus an overall aggregate time series.
- Stored as CSV files.

## Motivation
- Part of the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices against impacts data for monitoring and early warning systems.
- Remote sensing offers near real-time, globally covering, low-cost data; aim to evaluate usefulness of agricultural drought indices for M&EW at European scale.
- NUTS-region aggregation chosen because many impact data are available at that scale; LULC differentiation included to study different vegetation responses.

## Data Sources
- Gridded drought indices derived from the CEH gridded product for Europe (2000-2015).
- LULC map from MODIS Land Cover Type (MCD12C1, 0.05°) for 2012.

## Method for deriving the drought indicator time series
- VCI calculation: (NDVI - NDVI_min,i) / (NDVI_max,i - NDVI_min,i) for each month i.
- TCI calculation: (LST_max,i - LST) / (LST_max,i - LST_min,i) for each month i.
- VHI: VHI = α * VCI + (1 - α) * TCI; α commonly set to 0.5.
- NUTS regions defined by the 2013 NUTS nomenclature.
- LULC: simplified to four classes; for each NUTS region, drought indicators extracted for each class plus a non-differentiated (all classes) series, yielding 15 time series per region (5 per indicator: 4 classes + all).
- For each time step, a value is produced only if at least 50% of the non-masked area has valid values.
- NoData handling: two types observed — “--” indicates no valid pixels; “nan” indicates some valid pixels but <50%.

## Format & Structure of the dataset
- Data stored in CSV format.
- Organized in folders (structure described but not exhaustively listed in the summary).

## Acknowledgments
- Funded as part of the DrIVER project by the Natural Environment Research Council (award NE/L010038/1) under Belmont Forum initiative; conducted under the NERC Environmental Information Data Centre.

## References
- AghaKouchak et al. 2015; remote sensing of drought.
- Bachmair et al. 2016; drought indicators in M&EW.
- Bachmair, Tanguy, Hannaford, Stahl 2018; representativeness of meteorological indicators.
- Kogan 1995, 1997; foundational drought indicators using vegetation indices and temperature.
- Tanguy et al. 2016; Gridded drought indices based on remote sensing data for Europe (2000-2015).