# GR6J model estimates of daily river flows at 95 river catchments in Great Britain - EC-Earth large ensemble (climate model) driving data

## 1. Brief Description of the Dataset
- GR6J modelled daily river flow time series for 95 river catchments in Great Britain.
- Driving data come from the EC-Earth Single Model Initial Condition Large Ensemble (SMILE) climate model: precipitation and PET calculated from temperature.
- Ensembles cover present day, pre-industrial, plus 2°C and 3°C global warming levels.
- For each ensemble member, 25 realizations are created via initial-condition variations and run for 5 years, yielding 2000 years of driving data per warming level.
- Across ensemble members, the best-performing GR6J run per catchment is used to drive the hydrological model, producing a continuous 2000-year daily river-flow series.
- Data are delivered as CSV files: one per catchment, organized by warming level (PD, 2C, 3C) with folders for simulated flows (Qsim) and driving data (Precip, PET, Temp). Filenames follow LE_Flow_<NRFA_catchment_ID>.csv and LE_Input_<NRFA_catchment_ID>.csv.

## 2. Introduction
- Hydrological droughts threaten public water supply and have broad socioeconomic and environmental impacts.
- Large ensembles provide multi-thousand-year sequences, enabling exploration of extremes and drivers under non-stationary/climate-change conditions.
- SMILE-based projections are presented as more physically based than some statistical methods, preserving spatial and internal consistency of rare events.

## 3. Catchment selection
- 100 river catchments from the Low Flow Benchmark Network (LFBN) within Great Britain were selected.
- An additional 10 catchments were included to represent key public water-supply abstractions in East Anglia.
- A map (Figure 1) illustrates catchments, with LFBN in black and southeast catchments in red.

## 4. Model calibration
- GR6J hydrological model calibrated and validated against a 1965–2015 baseline.
- Calibration uses Latin Hypercube Sampling (LHS) to generate 10,000 parameter sets for GR6J’s six parameters; each set is evaluated with six performance metrics across high, mean, and low flow regimes, producing a total rank-based score.
- Observed baseline data: daily precipitation (CEH-GEAR) and temperature (CEH-CHESS); PET calculated using a UK-specific temperature-based equation (Tanguy et al. 2018).
- Observed river flows from NRFA are used for validation.
- The top-performing parameter set (lowest total rank score) per catchment is used to drive GR6J with EC-Earth SMILE precipitation and PET (from the ensemble) for the 2000-year simulations.
- Six evaluation metrics (and their focuses) include NSE, logNSE, PBIAS, MAPE, Q95 APE, and MAM30 APE.

## 5. Climate model data
- Based on EC-Earth GCM v2.3, run for present day, pre-industrial, +2°C, and +3°C warming scenarios.
- Bias adjustment applied per catchment:
  - Precipitation adjusted with multiplicative factors to match monthly observed means.
  Temperature adjusted additively; a power transformation is applied to correct precipitation CV to match observed variability.
  - PET recalculated from bias-adjusted temperature using the UK-calibrated equation.
- Fidelity testing (Thompson et al. 2017 style) per catchment: 10,000 bootstrap samples of monthly precipitation are compared to observations using moments (mean, SD, skewness, kurtosis). A catchment is considered statistically indistinguishable from observations if observed statistics fall within the 2.5–97.5 percentile range of the model distribution.
- 95 catchments pass the fidelity test and are included in analyses.

## 6. Data format
- Top-performing parameter set from calibration drives GR6J to produce a 2000-year continuous daily river flow series for each catchment.
- Files are CSVs with 730,400 rows (daily data across 2000 years) and five columns for flows per catchment.
- Driving data files contain modeled precipitation (mm/day), PET (mm/day), and Temperature (°C).
- Directory structure:
  - PD (present day), 2C, 3C
  - LE_Flow_<NRFA catchment ID>.csv (simulated river flows)
  - LE_Input_<NRFA catchment ID>.csv (driving data)
- Columns:
  - For Qsim: Qsim, Catch_id, Ens_member, Realisation
  - For driving: Precip, PET, Temp, Catch_id, Ens_member, Realisation

## 7. Acknowledgements
- Dataset produced as part of a PhD studentship supported by the Natural Environment Research Council via the SCENARIO Doctoral Training Partnership (grant NE/S007261/1).

## 8. References
- Hannaford et al. 2022; Harrigan et al. 2018; Robinson et al. 2020; Smith et al. 2019; Tanguy et al. 2018; Leander & Buishand 2007; Thompson et al. 2017; van der Wiel et al. 2019.