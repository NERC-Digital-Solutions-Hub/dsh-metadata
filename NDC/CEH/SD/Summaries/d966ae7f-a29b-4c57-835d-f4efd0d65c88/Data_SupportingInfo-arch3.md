# GR6J model estimates of daily river flows at 95 river catchments in Great Britain - EC-Earth large ensemble (climate model) driving data

## Overview
- A dataset of GR6J-modelled daily river flows for 95 Great Britain catchments, driven by precipitation and potential evapotranspiration from the EC-Earth SMILE climate model large ensemble.
- Large ensemble comprises present-day climate and scenarios at pre-industrial plus 2°C and 3°C global warming, enabling multi-thousand-year sequences for extreme drought analysis.
- Aimed at understanding drought risks, supporting monitoring and policy planning for environmental health and water resource management under climate change.

## Dataset scope and design
- Catchment selection: 95 GB catchments drawn from the Low Flow Benchmark Network (LFBN) plus ten additional southeast catchments; 95 pass a credibility fidelity test.
- Ensemble and time horizon: For each warming level, 16 EC-Earth ensemble members × 25 realizations × 5 years = 2000 years of driving data; continuous 2000-year input and flow time series produced by pooling all realizations.
- Driving data: Precipitation and PET derived from EC-Earth large ensemble; bias-adjusted to align with observed climate data.

## Modelling approach
- Hydrological model: GR6J used to simulate daily river flows from 2000-year meteorological inputs.
- Calibration: Latin Hypercube Sampling (LHS) with 10,000 parameter sets; six performance metrics evaluated over baseline 1965–2015 using observed data (NRFA river flows, CEH-GEAR precipitation, CHESS temperature, UK PET calibration).
- Parameter selection: Top parameter set chosen per catchment based on multi-metric ranking for simulating flows.

## Climate data and bias correction
- Climate data source: EC-Earth GCM v2.3 SMILE ensemble; scenarios include present day, 2°C, and 3°C warming relative to pre-industrial levels.
- Bias correction: 
  - Precipitation adjusted with multiplicative factors to match monthly observed means.
  - Temperature adjusted additively.
  - A power transformation applied to adjust precipitation variability (CV) by catchment.
  - PET computed from bias-adjusted temperature using a UK-calibrated equation.
- Credibility assessment: Fidelity test (per Thompson et al. 2017) comparing model-driven statistics to observations via 10,000 bootstrapped monthly precipitation samples; 95 catchments pass the test, supporting use as alternative realizations of the real world.

## Data quality and credibility
- 95 catchments subjected to fidelity testing; included in analyses if statistically indistinguishable from observations for key moments.
- Quality assurance embedded in calibration, bias adjustment, and validation steps to ensure the driving data and simulated flows are internally consistent and suitable for drought risk assessment.

## Data products and format
- Output structure:
  - 95 catchments × 3 warming levels (PD, 2C, 3C) with 2000 years of daily data per catchment.
  - Files: 730,400 rows per file; multiple columns capturing Qsim and driving meteorology.
- File organization and naming:
  - Simulated river flows: LE_Flow_<NRFA catchment ID>.csv
  - Meteorological input: LE_Input_<NRFA catchment ID>.csv
  - Separate folders for each warming level (PD, 2C, 3C); two subfolders: Qsim (flows) and Driving_data (meteorology).
- Contents:
  - Qsim files: Qsim (m3/s), Catch_id, Ens_member, Realisation
  - Driving data: Precip (mm/day), PET (mm/day), Temp (°C), Catch_id, Ens_member, Realisation

## Usage for monitoring and policy
- Enables assessment of drought risk and extreme river discharge scenarios under present-day and warmer climates, supporting water supply planning, drought mitigation, and policy evaluation.
- Provides a long, physically consistent basis for exploring drivers of extremes and for testing monitoring frameworks and decision-support tools in environmental health contexts.
- Data structure is suitable for integration into dashboards, reports, and governance processes that require transparent, reproducible projections.

## Limitations and caveats
- Based on a single-model initial-condition large ensemble (SMILE); results depend on the underlying climate model and bias-correction approach.
- While credibility tests are passed for most catchments, uncertainties remain regarding ensemble representativeness and residual biases after correction.
- The top-performing parameter set is selected per catchment, which may constrain the representation of parameter uncertainty in some analyses.

## Acknowledgements and references
- Data produced as part of a PhD project supported by NERC SCENARIO Doctoral Training Partnership; references provided for CF methods, calibration, bias correction, and fidelity testing.