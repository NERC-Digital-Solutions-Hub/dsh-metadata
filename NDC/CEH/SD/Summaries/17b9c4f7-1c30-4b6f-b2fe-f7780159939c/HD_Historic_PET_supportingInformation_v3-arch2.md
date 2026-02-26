# Historic Gridded Potential Evapotranspiration (PET) based on temperature-based equation McGuinness-Bordne calibrated for the UK (1891-2015)

## Brief description
- 5 km gridded PET data derived from the McGuinness-Bordne temperature-based equation, calibrated for the UK (calibration period 1961-1990).
- Daily PET grids (mm/day) and monthly PET grids (mm/month) covering 1891–2015.
- Includes performance metrics assessing spatial quality; metric grids accompany PET grids.
- Data stored in NetCDF4 format, projected on the British National Grid.
- Calibration and validation rely on CHESS temperature and CHESS PET references; data sources and methods documented in Tanguy et al. (2018).

## Context of the dataset
- Produced as part of the NERC Drought and Water Scarcity Programme, spanning two interlinked projects:
  - Historic Droughts: aims to understand past UK droughts (1960s–19th century extents) and develop cross-disciplinary tools (hydrometeorological, social, regulatory) including the Historic Droughts Inventory.
  - IMPETUS: aims to improve drought forecasting (monthly to decadal) by integrating meteorology, hydrology, and demand forecasts, and addressing uncertainty in modelling chains.
- The dataset supports drought reconstructions and forecasting by providing a long-term PET input for hydrological modelling.

## Why PET and the dataset’s role
- PET is a key climate variable for hydrological models; accurate estimation enables past streamflow reconstructions and future drought forecasts.
- Temperature-based PET was adopted due to data availability in historical periods; PM (Penman-Monteith) PET is more accurate but not consistently available for the full 1891–2015 span.

## Data sources
- Met Office 5 km monthly mean temperature grids (1910–2011 from UKCP09; 2012–2015 unpublished updates; 1891–1909 rescued data).
- CHESS temperature data (used for calibration 1961–1990; evaluation 1991–2012).
- CHESS PET data (used as reference for calibration/evaluation; based on PM equation).

## Method for deriving the PET grids
- Evaluated multiple PET formulations; selected McGuinness-Bordne (UK-calibrated version of Oudin et al., 2005).
- Calibration performed using 43 catchments across Great Britain (1961–1990).
- Daily PET grids derived and aggregated to monthly totals; validation against CHESS-PET reference.
- The UK-calibrated parameters provide the version used for the historic PET dataset.

## Metrics to characterize data quality
- Evaluated over 1991–2012 (monthly and daily) using:
  - Nash-Sutcliffe efficiency (NSE)
  - Mean absolute percentage error (MAPE)
  - Correlation coefficient
  - Bias ratio
  - Variability ratio (VR)
  - Kling-Gupta efficiency (KGE)
- Metrics enable users to assess confidence by location; MAPE provided as mean monthly values to indicate uncertainty.

## Format and contents of the PET dataset
- NetCDF4 format; adheres to CEH gridded dataset conventions.
- Daily grids: UK-wide 2D grids with 365 or 366 layers per year.
- Monthly grids: UK-wide 2D grids with 12 monthly layers per year.
- Accompanying metric files: two daily and two monthly NetCDF files detailing performance metrics.
- Projection: British National Grid.
- Acknowledges joint outputs from Historic Droughts and IMPETUS projects (funding: NE/L01016X/1 and NE/L010267/1).

## Acknowledgements
- Joint outcome from Historic Droughts (NERC grant NE/L01016X/1) and IMPETUS (NERC grant NE/L010267/1).

## Utility for analysts
- Provides a long-term, standardized PET dataset suitable for cross-time hydrological modelling and drought analysis.
- Includes quality metrics to gauge spatial reliability and an explicit uncertainty context via MAPE values.
- Data provenance and calibration details support reproducibility and methodological scrutiny.