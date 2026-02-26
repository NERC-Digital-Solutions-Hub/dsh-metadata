# Supporting documentation for 'DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (1962-2015) using observed driving data'

## Overview
- Open-access dataset providing an ensemble of 100 simulated daily river-flow time series for 1,366 GB catchments (1962–2015) using the DECIPHeR model.
- Forcing data from CEH GEAR and CHESS-PE; model code is open source (GitHub) with a Zenodo DOI for the specific run.
- Metadata and performance metrics included to enable assessment and interpretation of results.

## Data Access, Citation and Conditions of Use
- Terms, license and reuse conditions apply; access via DOI: 10.5285/d770b12a-3824-4e40-8da1-930cf9470858.
- Required citation: Coxon et al. (2019) DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (1962–2015) using observed driving data. NERC Environmental Information Data Centre. DOI: 10.5285/d770b12a-3824-4e40-8da1-930cf9470858.
- Data provenance, license and terms are specified through the access DOI.

## Dataset Description
- Ensemble: 100 daily river-flow time series per catchment (GB, 1,366 catchments), 1962-01-01 to 2015-12-31, in m3/s.
- Model: DECIPHeR open-source hydrological framework; forcing from CEH GEAR (rainfall) and CHESS-PE (PET), aggregated to 5 km.
- Evaluation: Multi-objective scoring across 4 metrics (NSE, slope of flow duration curve, bias in runoff ratio, low-flow volume) using a ranking approach; top 1% (100 members) per catchment selected as behavioural ensemble.
- Metadata: For each ensemble member, contains model parameters and performance metrics to enable interrogation of results.
- Caveat: While many gauges are well reproduced, some gauges have poor observed-flow simulation; users should consult per-catchment metadata.

## Context and Provenance
- Produced under the MARIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), UK NERC-funded (2014–2018).
- Purpose: create ensembles of daily flow to drive impact models across scales and periods; supports risk-based drought and water-scarcity studies.
- Code availability: DECIPHeR open-source on GitHub; specific model run materials accessible via Zenodo DOI.

## Methods (Key Points)
- Input data: 55-year daily precipitation and potential evapotranspiration, plus observed discharge for evaluation.
- Forcing datasets: CEH-GEAR and CHESS-PE; aggregated to 5 km grid.
- Evaluation framework: Monte Carlo sampling of 10,000 parameter sets; wide parameter ranges to cover diverse hydroclimates; parameters adapted across catchments.
- Multi-objective ranking: equal weighting of NSE, flow-variability slope, runoff ratio bias, and low-flow bias; top 100 ensembles selected per catchment.

## Data Format and Structure
- Flow data files: DECIPHeR_FlowEnsemble_<gaugingstationID>_19620101-20151231.csv for each gauge; 19,723 rows, 102 columns (catch_id, date, flow_realisation_1 … flow_realisation_100).
- Metadata files: DECIPHeR_FlowEnsemble_<gaugingstationID>_Metadata.csv; 100 rows (one per ensemble member) and 16 columns (parameters and performance: nse, lognse, biasrr, lfv, tsfdc, plus model parameters such as param_szm, param_lnto, param_srmax, param_srinit, param_chv, param_td, param_smax).
- Ensemble figure files: DECIPHeR_FlowEnsemble_<gaugingstationID>_SimFlow.png showing observed discharge, precipitation, and 5th–95th percentile bounds for selected two-year periods.

## Guidance for Use and Limitations
- Coverage: ~90% of NRFA gauge network; national-scale applicability with diverse hydrological behavior.
- Limitations: DECIPHeR currently does not include abstractions or reservoir effects; performance varies by region (better in wetter NW, poorer in SE chalk-based areas); potential overestimation of flows in SE; sometimes underestimation of low flows in parts of Midlands and NE Scotland.
- Uncertainty: 100 simulations provided to quantify parameter and model uncertainty; these do not exhaust all uncertainty sources; users should derive their own uncertainty bounds as needed.
- Best practices: consult per-catchment metadata before using flows for a specific catchment; use multiple ensemble members to capture uncertainty rather than relying on a single top-ranked run.
- Reuse: data can be used to drive impact models, evaluate hydrological scenarios, or perform independent performance assessments; users may compute additional metrics or custom uncertainty analyses.

## Acknowledgements and References
- Acknowledges NERC/MARIUS support and individuals for assistance.
- Key references include Beven and Freer (Dynamic TOPMODEL), Coxon et al. (DECIPHeR v1), and related data sources (CEH-GEAR, CHESS-PE).
- Model code and supporting materials are available in open repositories (GitHub; Zenodo DOI).