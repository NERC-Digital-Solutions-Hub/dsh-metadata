# Supporting documentation for 'DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (19622015) using observed driving data'

## Overview
- Provides an ensemble of 100 simulated daily river flow time series for 1,366 catchments across Great Britain from 1962-01-01 to 2015-12-31.
- Uses the DECIPHeR hydrological model with forcing from CEH GEAR (rainfall) and CHESS-PE (potential evapotranspiration); forcing data aggregated to a 5 km grid.
- Model evaluation relies on four metrics (NSE, slope of the flow duration curve, bias in runoff ratio, and low-flow volume) within a multi-objective framework; top 1% (100) ensemble members are supplied.
- Metadata accompany the flows to aid interpretation of model performance per catchment and ensemble member.
- Model is part of the MaRIUS project focusing on drought and water scarcity; code is open-source.

## Data Access and Citation
- Terms, license, and data access at: https://doi.org/10.5285/d770b12a-3824-4e40-8da1-930cf9470858
- Must cite: Coxon et al. 2019 (DECIPHeR v1) and related sources as provided in the dataset documentation.

## Data Contents

- Data formats
  - Ensemble daily flow files:
    - Naming: DECIPHeR_FlowEnsemble_<gaugingstationID>_19620101-20151231.csv
    - For 1,366 gauges: 2,732 CSV files total.
    - Each file: ~19,723 rows (daily data) and 102 columns:
      - catch_id (NRFA gauge ID), date (YYYY-MM-DD), flow_realisation_1 … flow_realisation_100 (daily flow in m3/s) for the 100 ensemble members.
  - Ensemble metadata files:
    - Naming: DECIPHeR_FlowEnsemble_<gaugingstationID>_Metadata.csv
    - Each file contains 100 rows (ensemble members) and 16 columns, including:
      - realisation, catch_id, river, station
      - model parameters: param_szm, param_lnto, param_srmax, param_srinit, param_chv, param_td, param_smax
      - performance metrics: nse, lognse, biasrr, lfv, tsfdc
  - Ensemble figure files:
    - Naming: DECIPHeR_FlowEnsemble_<gaugingstationID>_SimFlow.png
    - Visuals for selected two-year periods (e.g., 1966-1968, 1990-1992, 2004-2006, 2010-2012)
    - Observed discharge (black line, left axis) and precipitation (blue bars, right axis)
    - Uncertainty bounds: 5th–95th percentile (red shading) from the likelihood-weighted top 1% simulations (GLUE framework)

- Spatial and temporal coverage
  - 1,366 GB catchments; daily flows from 1962-01-01 to 2015-12-31.
  - Gauges aligned with National River Flow Archive (NRFA) IDs.

- Forcing and inputs
  - Forcing data: CEHGEAR (daily rainfall) and CHESS-PE (daily potential evapotranspiration); both 1 km grids, aggregated to 5 km for model run.
  - Evaluation against observed NRFA daily streamflow data.

## Context and Purpose
- Project context: MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity); UK NERC-funded (2014-2018).
- Purpose: provide ensembles of daily flow time series to drive impact models across multiple scales, enabling uncertainty analysis and drought risk assessment.
- Open-source: DECIPHeR model code available on GitHub; flows produced for thousands of gauges across GB.

## Methods

- Input data and run setup
  - 55-year data window (1961-01-01 to 2015-12-31); 1961 used as model warmup (no evaluation).
  - 1 km forcing data aggregated to 5 km; evaluation against observed NRFA flows.

- Model evaluation framework
  - Monte Carlo: 10,000 parameter sets per catchment, drawn from uniform priors.
  - Parameter ranges defined for catchment-scale variability (based on Dynamic TOPMODEL concepts).
  - Multi-objective scoring across four metrics; rankings summed to produce a combined score.
  - Top 1% of simulations (n=100) per catchment selected as the behavioural ensemble.

- Interpretation guidance
  - Performance varies by region; generally better in wetter northern/western GB catchments; poorer in drier southern/eastern areas and groundwater-dominated zones (e.g., chalk regions in SE England).
  - Overestimation biases observed in the SE; potential underestimation of low flows in some Midlands and NE Scotland areas.
  - Notes on reservoir abstractions and other anthropogenic controls not included in the current model.

## Data Quality, Limitations, and Use Guidance

- Usage considerations
  - 100-member ensemble provides uncertainty bounds; not guaranteed to cover the full parameter space.
  - Users are encouraged to utilize multiple simulations to quantify uncertainty rather than rely solely on the top-ranked run.
  - Model does not currently incorporate certain processes (e.g., abstractions, reservoirs); consult metadata for catchment-specific limitations.

- Metadata usefulness
  - Metadata enables inspection of parameter sets and performance per ensemble member.
  - Users can compute custom performance metrics and uncertainty bounds beyond the provided GitueGLUE-based visuals.

- Coverage and applicability
  - Ensemble spans around 90% of the NRFA gauge network; suitable for national-scale hydrological analyses, with caveats for affected or poorly reproduced gauges.

## Acknowledgements and References
- Acknowledgements to NERC MaRIUS project; gratitude extended to contributors for data availability.
- References include key DECIPHeR and TOPMODEL-related literature (Beven, Freer, Coxon et al., etc.) as cited in the dataset documentation.