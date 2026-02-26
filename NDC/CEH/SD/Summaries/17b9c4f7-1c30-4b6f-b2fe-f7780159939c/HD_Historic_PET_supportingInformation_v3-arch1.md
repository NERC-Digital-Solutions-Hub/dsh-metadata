# Historic Gridded Potential Evapotranspiration (PET) based on temperature-based equation McGuinness-Bordne calibrated for the UK (1891-2015)

## Overview
- 5 km gridded PET data using the McGuinness-Bordne temperature-based equation, calibrated for the UK (calibration period: 1961-1990).
- Temperature inputs derived from 5 km Met Office mean temperature grids (Historic Droughts project; aligned with UKCP09 methodology).
- Coverage spans 1891–2015, with daily PET grids (mm/day) and monthly PET grids (mm/month).
- Includes quality metrics grids for both daily and monthly datasets; stored in NetCDF4 and projected on the British National Grid.
- Methodology and data derivation detailed in Tanguy et al. (2018).

## Context and Projects
- Produced under the NERC Drought and Water Scarcity Programme, involving two main projects:
  - Historic Droughts: cross-disciplinary study of past UK droughts (2014–2018; £1.5m).
  - IMPETUS: focuses on improving drought forecasts (2014–2018; £1m).
- IMPETUS aimed to improve meteorological, hydrological, and water demand forecasts and combine them for drought forecasting; PET inputs were evaluated as part of this work.
- Historic Droughts Inventory: a knowledge base of past drought characteristics, drivers, impacts, and responses, including hydro-meteorological timelines and references from historical sources.

## Motivation
- PET is a critical input for hydrological models to reconstruct past streamflows and forecast future flows (e.g., Ensemble Streamflow Prediction, ESP).
- A temperature-based PET method was chosen because it uses data that are available for long historical periods; Penman-Monteith (PM) is more accurate but requires variables not readily available for the past or future.

## Data Sources
- Met Office 5 km monthly mean temperature grids:
  - Combination of UKCP09 data (1910–2011), unpublished updates (2012–2015), and rescued data (1891–1909).
  - Daily temperatures derived from monthly data via piecewise cubic Hermite interpolation (pchip).
- CHESS temperature data (Robinson et al. 2016a) used for calibration.
- CHESS PET data (Robinson et al. 2016b, 2017) used as reference (calibration with 1961–1990; evaluation with 1991–2012).

## Methodology
- Evaluated multiple PET formulations; McGuinness-Bordne was found to perform best for the UK (calibrated version described in Oudin et al., 2005).
- Calibration across 43 GB catchments using UK-specific parameters (1961–1990).
- Daily PET grids derived from the calibrated equation; monthly PET grids produced by summing daily values.
- Performance metrics computed to assess goodness-of-fit relative to CHESS-PET (Penman-Monteith) over 1991–2012.

## Data Quality and Metrics
- Metrics used: Nash-Sutcliffe Efficiency (NSE), Mean Absolute Percentage Error (MAPE), correlation coefficient, bias ratio, variability ratio (VR), Kling-Gupta Efficiency (KGE).
- Metrics computed across the evaluation period (1991–2012) for both daily and monthly grids.
- MAPE provided as mean monthly values to indicate uncertainty.
- Metrics accompany the PET grids as separate NetCDF files.

## Dataset Format and Access
- File format: NetCDF4, following CEH gridded dataset conventions.
- Daily PET: UK-wide 2D grids with 365 or 366 grids per year.
- Monthly PET: UK-wide 2D grids with 12 grids per year.
- Accompanying metric files: two daily and two monthly metric files.
- Spatial projection: British National Grid.
- Data storage and metadata suitable for discoverability and reuse.

## Acknowledgements
- Historic Droughts (NERC grant NE/L01016X/1) and IMPETUS (NERC grant NE/L010267/1).

## References (selected)
- Tanguy, M., Prudhomme, C., Smith, K., and Hannaford, J. (2018). Historical gridded reconstruction of potential evapotranspiration for the UK.
- Perry, M. and Hollis, D. (2005). The generation of monthly gridded datasets for a range of climatic variables over the UK.
- Oudin, L. et al. (2005). Which potential evapotranspiration input for a lumped rainfall-runoff model?
- Robinson, E.L. et al. (2016a, 2016b). CHESS PET and CHESS met datasets.
- Harrigan, S. et al. (2017); Kling, H. et al. (2012); Monteith, J.L. (1965). Supporting methodological context.