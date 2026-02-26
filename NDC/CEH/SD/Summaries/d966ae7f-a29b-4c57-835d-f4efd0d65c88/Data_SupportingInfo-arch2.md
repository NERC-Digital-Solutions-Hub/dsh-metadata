# GR6J model estimates of daily river flows at 95 river catchments in Great Britain - EC-Earth large ensemble (climate model) driving data

## Overview
- Dataset of GR6J modelled daily river flows for 95 GB catchments, driven by EC-Earth SMILE climate model data.
- Scenarios cover present-day climate, and +2°C and +3°C global warming.
- Uses multi-thousand-year driving sequences to better characterise extreme droughts and hydrological variability.
- Top-performing parameter sets per catchment are applied to generate a continuous 2000-year time series per warming level.

## Data contents and structure
- Outputs: 95 files per warming level containing daily river flow (Qsim) for each catchment.
- Driving inputs: daily modelled precipitation (Precip) and potential evapotranspiration (PET) with corresponding temperature (Temp).
- Data organization:
  - PD (present day), 2C, 3C folders; within each, two subfolders:
    - Qsim: simulated river flows
    - Driving_data: meteorological inputs
  - File naming:
    - LE_Flow_<NRFA catchment ID>.csv (river flows)
    - LE_Input_<NRFA catchment ID>.csv (driving data)
  - Each file contains 730,400 rows (2000 years of daily data) and multiple columns:
    - River flow file: Qsim, Catch_id, Ens_member, Realisation
    - Driving data: Precip, PET, Temp, Catch_id, Ens_member, Realisation
- Time series: 2000 years for each warming level, derived from 16 EC-Earth ensemble members × 25 realizations × 5 years per member.

## Driving climate data and ensemble design
- Climate model: EC-Earth Global Climate Model v2.3 SMILE large ensemble.
- Scenarios:
  - Present-day climate (PD): corresponds to 2011–2015 observed global mean surface temperature.
  - Pre-industrial plus 2°C (2C) and plus 3°C (3C) warming relative to pre-industrial baseline.
- Ensemble construction: for each member, 25 realizations created via stochastic parameterizations; total 16 members × 25 realizations × 5 years = 2000 years per warming level.
- Bias adjustment and transformation:
  - Precipitation bias-adjusted with monthly multiplicative factors; temperature adjusted additively.
  - Precipitation subjected to a power transformation to match observed coefficient of variation.
  - PET recalculated from bias-adjusted temperature using UK calibration.
- Credibility check:
  - Fidelity test comparing modelled precipitation statistics (via bootstrapped subsamples) against observations.
  - 10,000 monthly subsamples per catchment; 95 catchments pass the fidelity test and are included.

## Catchment selection
- 100 river catchments from the Low Flow Benchmark Network (LFBN) within Great Britain (England, Scotland, Wales).
- 10 additional catchments included to reflect key public water supply abstractions in East Anglia.
- Selection described in related literature; catchments mapped in accompanying figures.

## Hydrological modelling and calibration
- Hydrological model: GR6J used to simulate river flows from pooled 2000-year inputs (precipitation and temperature).
- Calibration approach:
  - Latin Hypercube Sampling (LHS) with 10,000 parameter sets across six GR6J parameters.
  - Evaluation based on six metrics across high, mean, and low flows:
    - Nash-Sutcliffe efficiency (NSE) for high flows
    - NSE for overall window
    - logNSE for low flows
    - Absolute percent bias (PBIAS)
    - Mean absolute percent error (MAPE)
    - Q95 APE (low flows)
    - MAM30 APE (mean annual minimum, 30-day moving average)
  - Baseline period 1965–2015 using observed precipitation (CEH-GEAR) and observed temperature (CEH-CHESS); PET calibrated for the UK (Tanguy et al., 2018).
  - Top-scoring parameter set per catchment selected and used to generate the 2000-year simulations driven by EC-Earth inputs.

## Data format and accessibility
- Formats:
  - CSV files for simulated river flows (Qsim) and driving meteorology (Precip, PET, Temp).
- Metadata:
  - Each flow file includes Catch_id, Ens_member, Realisation; each input file includes Catch_id, Ens_member, Realisation.
- Purpose and provenance:
  - Dataset produced as part of a PhD studentship funded by NERC SCENARIO DTP (grant NE/S007261/1).
- Documentation and references:
  - Related methodological and dataset references provided to support reproduction and usage (eFLaG, UK drought analyses, and climate-hydrology data sources).

## Use, value, and access considerations
- Purpose aligned with environmental monitoring analysts: provides standardized, bias-adjusted, multi-scenario hydrological projections for drought risk assessment and policy evaluation.
- Data value and interoperability:
  - Large ensemble-driven, long-horizon time series facilitate analysis of extreme events and drivers under warming.
  - Fidelity testing enhances credibility for use as alternative realizations of real-world hydrology.
- Enhancing accessibility:
  - Outputs are organized and stored with clear naming conventions and per-catchment files to support reuse and cross-study comparability.
  - Emphasized importance of enabling access to underlying driving data for broader analyses.

## Acknowledgements
- Supported by Natural Environment Research Council via the SCENARIO Doctoral Training Partnership.