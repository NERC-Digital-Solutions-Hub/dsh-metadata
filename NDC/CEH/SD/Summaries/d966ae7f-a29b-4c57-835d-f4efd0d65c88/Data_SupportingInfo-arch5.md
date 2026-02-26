# GR6J model estimates of daily river flows at 95 river catchments in Great Britain - EC-Earth large ensemble (climate model) driving data

- Dataset scope
  - GR6J modelled daily river flow time series for 95 catchments in Great Britain.
  - Driving meteorological data (precipitation and PET from temperature) from the EC-Earth SMILE large ensemble.
  - Scenarios include present-day climate, pre-industrial plus 2°C and plus 3°C global warming levels.
  - For each ensemble member, 25 realizations are generated, run for 5 years; total of 2000 years per warming level.

- Data content and structure
  - Outputs: continuous 2000-year daily river flows for each catchment, driven by EC-Earth SMILE meteorology.
  - Driving data: daily modelled precipitation and PET (from temperature).
  - File organization: one folder per warming level (PD, 2C, 3C) with a separate file per catchment in two subfolders:
    - Qsim: simulated river flows (Qsim) for each catchment
    - Driving_data: meteorological inputs (Precip, PET, Temp)
  - File naming: LE_Flow_<NRFA catchment ID>.csv (Qsim) and LE_Input_<NRFA catchment ID>.csv (driving data).
  - Data volume per file: 730,400 rows (2000 years × daily data) across five columns for Qsim and driving inputs (specific columns described below).

- Catchment selection and calibration
  - Catchments: 100 from the Low Flow Benchmark Network (LFBN) within Great Britain, plus 10 additional key East Anglia abstraction catchments.
  - Hydrological model: GR6J calibrated to 2000-year input data using Latin Hypercube Sampling (LHS).
  - Calibration process: 10,000 parameter sets evaluated against six metrics across baseline 1965–2015 using observed precipitation (CEH-GEAR) and observed temperature (CEH-CHESS); PET computed with a UK-calibrated temperature-based equation.
  - Top parameter set (per catchment) used to simulate flows with EC-Earth driving data.
  - Evaluation metrics include NSE (high and low flow focuses), logNSE, PBIAS, MAPE, Q95 APE, and MAM30 APE.

- Climate model data and bias adjustment
  - Driving data come from EC-Earth GCM v2.3 SMILE with present-day, pre-industrial, +2°C, and +3°C warming levels.
  - Bias adjustment per catchment applied to precipitation (multiplicative) and temperature (additive); a power transformation is applied to correct precipitation CV (Leander & Buishand, 2007).
  - PET recalculated from bias-adjusted temperature using UK-calibrated equation.
  - Credibility check (fidelity test): bootstrapping 10,000 monthly precipitation subsamples to compare moments (mean, SD, skewness, kurtosis) with observations; model data deemed indistinguishable if observed statistics fall within 95% of model distribution.
  - 95 of the selected catchments pass fidelity tests and are included in analyses.

- Data quality and provenance
  - The dataset is presented as a robust, physically-based hydrological projection resource with multi-thousand-year samples to explore extremes under different warming levels.
  - Data provenance includes: EC-Earth SMILE driving data, CEH-GEAR and CEH-CHESS observational baselines, and GR6J calibration results.
  - The dataset is intended to support assessment of unprecedented extreme river discharges under climate change scenarios.

- Data format details
  - Each file contains 730,400 rows of daily data across five columns.
  - Simulated river flow files (Qsim) contain: Qsim, Catch_id, Ens_member, Realisation (and an additional column not explicitly listed in the summary).
  - Driving data files (inputs) contain: Precip, PET, Temp, Catch_id, Ens_member, Realisation.
  - Structure: one folder per warming level (PD, 2C, 3C); within each, two subfolders named Qsim and Driving_data.
  - Purpose-built for downstream use and cross-catchment analyses; named consistently to link flows with their driving inputs.

- Acknowledgements and references
  - Funded as part of a PhD studentship via Natural Environment Research Council SCENARIO DTP (grant NE/S007261/1).
  - Key references detailing the methodology, calibration, bias adjustment, fidelity assessment, and related hydrological modelling work are provided.

- Usage considerations and limitations
  - The dataset provides a large ensemble-based perspective on potential hydrological responses to warming, suitable for exploring extreme droughts and discharge events.
  - The fidelity test supports statistical credibility, but users should consider residual uncertainties in bias adjustment, model structure (GR6J), and the dependence on climate model ensembles when applying results to decision-making.