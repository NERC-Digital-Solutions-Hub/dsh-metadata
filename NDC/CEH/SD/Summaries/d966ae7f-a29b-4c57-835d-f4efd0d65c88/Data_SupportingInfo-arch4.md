# GR6J model estimates of daily river flows at 95 river catchments in Great Britain - EC-Earth large ensemble (climate model) driving data

- What the dataset contains
  - GR6J modelled daily river flow time series for 95 river catchments in Great Britain.
  - Driving meteorological data (precipitation and potential evapotranspiration, PET, from temperature) from the EC-Earth Single Model Initial Condition Large Ensemble (SMILE) climate model.
  - Large ensemble configurations: present day, pre-industrial plus 2°C, and plus 3°C global warming levels.
  - For each ensemble member: 25 realizations via stochastic initial-condition perturbations, run for 5 years.
  - Total of 2000 years of driving data per warming level (16 ensemble members × 25 realizations × 5 years).
  - The top-performing GR6J parameter set for each catchment drives the hydrological model to produce continuous 2000-year daily river flow series.
  - Data are provided as CSV files, with one file per catchment and per warming level.

- Why this dataset matters
  - Addresses hydrological drought risk with multi-thousand-year simulations, enabling exploration of extremes under different warming scenarios.
  - Uses a physically-based large-ensemble approach (SMILE) to generate diverse weather sequences with spatial consistency.
  - Includes bias-adjusted climate driving data and a fidelity test to ensure the ensemble resembles observed statistics sufficiently for each catchment.

- Catchment selection
  - 100 catchments from the Low Flow Benchmark Network (LFBN) within Great Britain.
  - 10 additional catchments selected to represent key public water supply abstractions in East Anglia.
  - Catchments are mapped (LFBN catchments in black; southeast England additions in red).

- Model calibration
  - GR6J hydrological model calibrated using pooled 2000-year driving data.
  - Calibration method: Latin Hypercube Sampling (LHS) with 10,000 parameter sets across six performance metrics (high, mean, and low flow focused).
  - Baseline evaluation uses observed precipitation (CEH-GEAR) and observed temperature (CEH-CHESS) for 1965–2015; PET computed with a UK-calibrated temperature-based equation.
  - Top-performing parameter set (lowest summed rank across metrics) used to simulate flows driven by EC-Earth driving data.

- Climate model data and bias adjustment
  - EC-Earth GCM v2.3 provides present-day and +2°C, +3°C warming scenarios (relative to pre-industrial).
  - Precipitation bias-adjusted with multiplicative factors; temperature bias-adjusted additively; a variance-correcting power transformation applied per catchment (following Leander & Buishand, 2007).
  - PET derived from bias-adjusted temperature with the UK-calibrated equation.
  - Fidelity testing: for each catchment, 10,000 monthly-precipitation bootstrap samples compare statistics (mean, std, skewness, kurtosis) with observations; 95 catchments pass the test and are included.

- Data format and structure
  - Top parameter set used to generate a 2000-year daily river-flow time series for each catchment.
  - Files are CSVs, organized by warming level (PD, 2C, 3C) with 95 catchment files per level.
  - Directory structure:
    - LE_Flow_<NRFA catchment ID>.csv (simulated river flows)
    - LE_Input_<NRFA catchment ID>.csv (driving meteorological data)
  - Each catchment file contains 730,400 rows (2000 years of daily data).
  - Simulated river flow file columns: Qsim, Catch_id, Ens_member, Realisation.
  - Meteorological input file columns: Precip, PET, Temp, Catch_id, Ens_member, Realisation.
  - Files are grouped by warming level, with separate folders for driving data and flows.

- Acknowledgements
  - PhD studentship supported by the Natural Environment Research Council via the SCENARIO Doctoral Training Partnership (grant NE/S007261/1).

- References
  - Key works detailing eFLaG, UK drought modelling, calibration methods, bias adjustment, and related methodology (Hannaford et al. 2022; Harrigan et al. 2018; Robinson et al. 2020; Smith et al. 2019; Tanguy et al. 2018; Thompson et al. 2017; van der Wiel et al. 2019).