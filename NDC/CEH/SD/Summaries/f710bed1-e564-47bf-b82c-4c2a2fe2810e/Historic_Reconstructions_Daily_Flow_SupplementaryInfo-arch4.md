# Historic Reconstructions of Daily River Flow for 303 UK Catchments

## Overview
- Publishes consistent modelled daily river flow timeseries for 303 UK catchments from 1891 to 2015, with uncertainty estimates.
- Two data forms: a single best-performing flow timeseries with uncertainty bands, and an ensemble of 500 model realisations.
- Calibrated GR4J lumped hydrological model using newly rescued rainfall data and temperature-derived potential evapotranspiration (PET).
- Dataset produced under the UK Drought and Water Scarcity Programme (Historic Droughts and IMPETUS) to support drought analysis and decision making.
- Some catchments are near-natural while others are influenced by human activity; two reconstructions (Thames at Kingston and Lee at Feildes Weir) calibrated against naturalised flows.
- Metadata and guidance are provided to help users select suitable catchments and interpret results; data intended for use in drought indexing and long-term hydrological analyses (e.g., SSI).

## Data Content and Outputs
- Daily flow data (m3/s) for 1891-01-01 to 2015-11-30 across 303 catchments.
- Single_Run: top ensemble member flow plus daily min/max across 500 ensemble members, plus a metadata file with model parameters and performance per catchment.
  - Files: HD_FlowSingle_<catchmentID>_18910101_20151130.csv (one per catchment) and HD_FlowSingle_Metadata.csv.
  - Structure: catchID, Date, Flow_Top_Calib, Min_500, Max_500; metadata includes 23 columns (parameters, calibration/evaluation metrics, evaluation years, uncertainty width, containment ratio).
- Ensemble_500: daily flows for all 500 ensemble members plus 305 metadata files.
  - Files: HD_FlowEnsemble_<catchmentID>_18910101_20151130.csv and HD_FlowEnsemble_<catchmentID>_Metadata.csv.
  - Structure: 502 columns (catchID, Date, Realisation_1_Flow, ..., Realisation_500_Flow); metadata includes 22 columns per ensemble member (ranking, parameters, and performance metrics). Uncertainty width and containment ratio are not provided for individual realizations.
- Catchment metadata and performance guidance are included to aid interpretation, especially where model performance varies across catchments.

## Methods and Modelling
- Hydrological model: GR4J lumped catchment model (v1.0.2) with four parameters (X1–X4: production store, inter-catchment exchange, routing store, unit hydrograph time lag).
- Input data:
  - Rainfall: reconstructed daily rainfall data (1891–1958 extension) derived from digitised rain gauges.
  - PET: daily PET derived from reconstructed monthly temperatures via McGuinness-Bordne equation to align with UK CHESS dataset.
- Calibration and uncertainty:
  - Calibration period: 1982-10-01 to 2014-09-30 (32 water years).
  - 500,000 parameter sets sampled via Bayesian Latin Hypercube Sampling; each set runs the GR4J model.
  - Multi-objective evaluation using six metrics: NSE, NSE on log flows, MAPE, PBIAS, MAM30 (mean annual minimum 30-day), Q95 (flow exceeded 95th percentile).
  - Top ranking realisations retained; thresholds applied to ensure acceptable performance across catchments, though some catchments yield few or many acceptable runs.
  - Model performance varies by catchment; two naturalised reconstructions are included to improve comparability in near-natural basins.
- Evaluation and uncertainty:
  - Additional evaluation over pre-calibration observation period (varies by catchment) and metrics over total observation period.
  - Uncertainty metrics included: width of ensemble range and containment ratio (proportion of days observations fall within ensemble min/max).
  - Metadata provides evaluation years and scores to inform uncertainty interpretation.

## Data Format and Access
- File formats: CSV for all data files.
- Single_Run folder: 305 daily flow files plus one 305-row metadata file.
- Ensemble_500 folder: 305 daily flow files for 500 realizations plus 305 metadata files.
- File naming conventions align with NRFA catchment IDs; naturalised catchments append a trailing 0 to the ID (e.g., 390010, 380010).
- Guidance notes emphasize checking metadata for catchment-specific performance and recognizing that GR4J does not explicitly account for artificial human influences on flow in most catchments.

## Guidance for Data Leaders and Users
- Consult metadata before selecting catchments to ensure suitable performance for your study objectives.
- Use ensemble data to quantify parameter uncertainty; the 500-member ensemble provides a probabilistic view of flows, while the Single_Run gives a deterministic top-member result.
- Be mindful of catchments with human influences (abstractions, regulation) not explicitly modelled; that may affect applicability and interpretation.
- For reproducibility and governance:
  - Metadata includes model parameters, calibration/evaluation metrics, and evaluation years, enabling traceability and auditability.
  - Clear separation between single-run results and ensemble runs supports different risk-appetite analyses.
- Consider using the Standardised Streamflow Index (SSI) or similar drought indicators derived from these reconstructions for multi-catchment drought assessments.

## Context and Scope
- Projects: Historic Droughts (past droughts, late 19th to early 20th century) and IMPETUS (future drought forecasting; drought decision support).
- Catchment coverage: 303 across the UK, including near-natural and human-influenced basins; some used by National Hydrological Monitoring Programme.
- Output purpose: provide a consistent national daily flow dataset to support drought research, planning, and policy analysis, with quantified uncertainty for hydrological drought studies.

## Acknowledgements and References
- Funded by NERC under the UK Droughts and Water Scarcity Programme (Historic Droughts NE/L01016X/1; IMPETUS NE/L010267/1).
- Related methodological references and data sources include GR4J, CHESS meteorology, NRFA boundaries, and supporting documentation for drought indices and model evaluation.