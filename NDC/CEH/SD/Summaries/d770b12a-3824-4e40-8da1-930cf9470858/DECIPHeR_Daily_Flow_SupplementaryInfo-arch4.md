# Supporting documentation for 'DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (19622015) using observed driving data'

## Overview
- Provides an ensemble of 100 simulated daily river flow time series for 1,366 catchments across Great Britain from 1962-01-01 to 2015-12-31.
- Generated with the DECIPHeR hydrological model (open source) based on Dynamic TOPMODEL concepts.
- Forcing data: daily rainfall and potential evapotranspiration from CEH GEAR and CHESS-PE, aggregated to 5 km.
- Model performance evaluated over 1962-2015 using four multi-objective metrics; top 100 ensemble members are supplied with metadata to aid interpretation.

## Data access, citation and conditions of use
- Terms and conditions apply; data and license available at the provided DOI.
- If used, cite Coxon et al. (2019) NERC Environmental Information Data Centre.
- Data and code are open source; model code available on GitHub; outputs also archived with DOI.

## Summary Description of the Dataset
- Ensemble: 100 daily-flow time series per gauge, for 1,366 GB gauges, 1962-2015.
- Outputs: daily flows in m3/s; metadata includes model parameters and performance metrics.
- Note: While flows are well reproduced at many gauges, some gauges are poorly simulated; users should consult metadata for each catchment.
- A related paper detailing the framework and performance is published in Geoscientific Model Development (Coxon et al., 2019).

## Context of the dataset
- Created under the MARIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), UK NERC-funded (2014-2018).
- Purpose: develop ensembles of daily flow for drought risk assessment across scales and periods; support impact models.
- DECIPHeR is open source and designed for national-scale UK applications; code available on GitHub and Zenodo.

## Methods
- Input data: 55-year forcing data (1961-2015) with 1961 as warm-up; daily precipitation (CEHGEAR) and potential evapotranspiration (CHESS-PE) at 5 km resolution; observed NRFA daily discharge for evaluation.
- Model evaluation: Monte Carlo approach with 10,000 parameter sets; parameters drawn from wide uniform priors to span diverse hydroclimatic conditions.
- Four evaluation metrics: Nash-Sutcliffe efficiency (NSE), slope of the flow duration curve, bias in runoff ratio, and low flow volume.
- Multi-objective ranking: each metric ranked, summed ranks, top 1% selected (100 ensembles per gauge).
- Performance notes: majority of gauges (90%) have NSE > 0; many gauges (>72%) have NSE > 0.5; better performance in wetter northern/western GB; poorer in southeast chalk areas; overestimation biases in SE; low-flow bias varies; Scotland/North Wales curves trend toward flatter hydrographs; full details in Coxon et al. (2019).
- Metadata includes an additional metric (logNSE) not used in the ranking.
- Outputs include uncertainty representations via a likelihood-weighted subset (GLUE-based) for ensemble plots.

## Data format
- Daily flow data: two CSV files per gauge (2,732 files total).
  - FlowEnsemble file: 19,723 rows, 102 columns
    - Columns include catch_id, date, and flow_realisation_1 through flow_realisation_100.
- Metadata: one CSV file per gauge (1,366 files)
  - 100 rows per file (ensemble members), 16 columns
  - Key fields: realisation, catch_id, river, station, model parameters (param_szm, param_lnto, param_srmax, param_srinit, param_chv, param_td, param_smax), NSE, logNSE, biasrr, lfv, tsfdc.
- Figure files: DECIPHeR_FlowEnsemble_<gaugingstationID>_SimFlow.png for selected 2-year periods, showing observed discharge, precipitation, and uncertainty bands (5th–95th percentile).
- Note: 90% gauge coverage of NRFA network; some gauges lack observed data in certain periods.

## Guidance notes for data leaders
- The model does not currently include abstractions or reservoirs; results should be interpreted with this limitation in mind.
- 100 ensemble simulations enable uncertainty quantification, but do not span the full parameter space; users are encouraged to use multiple simulations or derive uncertainty bounds.
- For a given catchment, consult metadata to assess performance before use; consider using several ensemble members to capture uncertainty rather than relying on the top-ranked run alone.
- Outputs can be used to compute user-defined performance metrics and uncertainty bounds, or to drive impact models across scales.

## Acknowledgements and references
- Funded under the MaRIUS project (NERC UK Droughts and Water Scarcity Programme); grant NE/L010399/1.
- Acknowledgements to contributors for data curation and dissemination.
- Core references include Beven and Freer on Dynamic TOPMODEL and Coxon et al. (2019) on DECIPHeR v1 performance.