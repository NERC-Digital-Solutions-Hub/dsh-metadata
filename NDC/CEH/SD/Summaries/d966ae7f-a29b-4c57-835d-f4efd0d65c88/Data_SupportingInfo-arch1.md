# GR6J model estimates of daily river flows at 95 river catchments in Great Britain - EC-Earth large ensemble (climate model) driving data

## Overview
- A dataset of GR6J-modelled daily river flow time series for 95 Great Britain catchments, driven by EC-Earth SMILE climate-model data.
- Driving data covers present-day climate and two warming scenarios: +2°C and +3°C relative to pre-industrial.
- For each ensemble member, 25 realizations were generated across 5 years, yielding 2000 years of data per warming level (16 ensemble members × 25 realizations × 5 years).
- The best-performing GR6J parameter set is used per catchment to drive the 2000-year flows.

## Catchment selection
- Initially 100 catchments from the Low Flow Benchmark Network (LFBN) within GB plus 10 additional East Anglia public water supply catchments.
- Fidelity test applied; 95 catchments passed and are included in the analyses.

## Model calibration
- GR6J calibration via Latin Hypercube Sampling (LHS) using 10,000 parameter sets across six performance metrics for high, mean, and low flows.
- Baseline period 1965–2015 with:
  - Precipitation from CEH-GEAR (daily)
  - Temperature from CEH-CHESS
  - PET calculated using UK-calibrated temperature-based equation (Tanguy et al., 2018)
- Model evaluation used observed NRFA river flows; the top-scoring parameter set per catchment was selected for simulations.

## Climate model data and bias correction
- Large ensemble from EC-Earth GCM v2.3 with present-day, 2°C, and 3°C warming scenarios (relative to pre-industrial).
- Bias adjustment applied:
  - Precipitation: monthly multiplicative correction to match observed means
  - Temperature: additive correction
  - A power transformation adjusts precipitation CV (Leander & Buishand, 2007)
- Credibility checked with a fidelity test (Thompson et al., 2017): 10,000 monthly-precipitation bootstrap samples per catchment; model statistics deemed indistinguishable from observations if observed values fall within the 2.5–97.5 percentile range.
- 95 catchments passed the fidelity test and were included.

## Data format and content
- Output: 730,400 rows per catchment representing 2000 years of daily data.
- Two main data files per catchment, within each warming level folder (PD, 2C, 3C):
  - Simulated river flows: LE_Flow_<NRFA catchment ID>.csv
  - Meteorological input: LE_Input_<NRFA catchment ID>.csv
- Directory structure:
  - One folder per warming level (PD, 2C, 3C)
  - Within each, a Qsim folder for flows and a Driving_data folder for meteorological inputs
- File contents:
  - Simulated flows: Qsim (m3/s), Catch_id, Ens_member, Realisation
  - Meteorological inputs: Precip (mm/day), PET (mm/day), Temp (°C), Catch_id, Ens_member, Realisation
- Each file contains data for a single catchment; 95 catchments in total.

## Acknowledgements and references
- Funded by Natural Environment Research Council via the SCENARIO Doctoral Training Partnership (grant NE/S007261/1) as part of a PhD project.
- Key references provided for methodology and data sources (e.g., Hannaford et al. 2022; Smith et al. 2019; Tanguy et al. 2018; Leander & Buishand 2007; Thompson et al. 2017; van der Wiel et al. 2019).