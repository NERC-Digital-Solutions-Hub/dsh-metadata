# Historic Gridded Potential Evapotranspiration (PET) based on temperature-based equation McGuinness-Bordne calibrated for the UK (1891-2015)

## Brief description of the dataset
- 5km gridded PET data for the UK based on a calibrated McGuinness-Bordne temperature-based equation (calibration period 1961-1990).
- Covers 1891-2015 with daily (mm/day) and monthly (mm/month) PET grids.
- Includes performance metric grids for both daily and monthly PET to indicate spatial data quality.
- Data stored in NetCDF4 format and projected on the British National Grid.
- Calibration sources and evaluation reference CHESS PET as a benchmark; methodology documented in Tanguy et al. (2018).

## Context of the dataset
- Produced under two UK NERC projects within the Drought and Water Scarcity Programme: Historic Droughts and IMPETUS.
- IMPETUS (2014-2018) aimed to improve drought forecasting and decision-making with emphasis on uncertainty in meteorological and hydrological modelling.
- Historic Droughts (2014-2018) sought to develop an interdisciplinary understanding of past UK droughts and create tools for better drought management.
- The Historic Droughts Inventory provides a common reference for multi-sector understanding of drought drivers, impacts, and responses.

## Motivation
- PET is a key climate input for hydrological models; accurate long-term PET estimation enables reconstruction of past streamflows and improved drought forecasting (ESP framework).
- A temperature-based PET method was chosen due to data availability for historical periods; Penman-Monteith is more accurate but data-intensive and less feasible for past/future periods.

## Data sources
- Met Office 5km monthly mean temperature grids (1910-2011 from UKCP09, 2012-2015 updates, and 1891-1909 rescued data); daily temps derived via pchip interpolation.
- CHESS temperature data (for calibration 1961-1990; evaluation 1991-2012) and CHESS PET (reference PET based on Penman-Monteith) used for calibration and validation.
- CHESS datasets are treated as the best available references for calibration and assessment.

## Method for deriving the PET grids
- Evaluated multiple PET formulations; McGuinness-Bordne (UK-calibrated version of Oudin et al., 2005) selected for best UK performance.
- Calibration performed using 43 catchments across Great Britain for the 1961-1990 period.
- PET grids produced as daily values, aggregated to monthly totals; methodology documented in Tanguy et al. (2017, 2018).

## Metrics to characterise quality of the data
- Evaluated against CHESS PET over 1991-2012 using:
  - Nash-Sutcliffe efficiency (NSE)
  - Mean absolute percentage error (MAPE)
  - Correlation coefficient
  - Bias ratio
  - Variability ratio (VR)
  - Kling-Gupta efficiency (KGE)
- Metrics provided for both daily and monthly PET; MAPE also presented as mean monthly values to indicate uncertainty.
- These metrics help users gauge confidence and suitability for specific study areas.

## Format of the PET dataset
- NetCDF4 format following CEH gridded dataset conventions.
- Daily grids: 365 or 366 time steps per year; two-dimensional spatial grids covering the UK.
- Monthly grids: 12 grids per year; two-dimensional spatial grids covering the UK.
- Accompanying metric files (two daily, two monthly) in NetCDF format.
- Spatial projection: British National Grid.

## Acknowledgements
- Joint outcome from Historic Droughts (NERC NE/L01016X/1) and IMPETUS (NERC NE/L010267/1).

## References (selected)
- Harrigan et al., benchmarking ESP skill in the UK (2017)
- Kling et al., upper Danube runoff under climate scenarios (2012)
- Monteith, Evaporation and environment (1965)
- Oudin et al., PET inputs for lumped models (2005)
- Perry & Hollis, UK gridded climatic datasets (2005)
- Robinson et al., CHESS PET and CHESS met datasets (2016-2017)
- Tanguy et al., Historical gridded reconstruction of PET for the UK (2018)