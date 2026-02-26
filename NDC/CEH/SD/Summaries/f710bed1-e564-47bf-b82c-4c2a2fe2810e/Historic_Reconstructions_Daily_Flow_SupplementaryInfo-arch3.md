# Historic Reconstructions of Daily River Flow for 303 UK Catchments

## Overview
- Provides consistent modeled daily river flow timeseries for 303 UK catchments from 1891 to 2015, with uncertainty estimates.
- Uses the GR4J lumped hydrological model, calibrated over 1982–2014, to produce:
  - A single best-performing flow timeseries with upper/lower uncertainty bands.
  - An ensemble flow timeseries from 500 model realizations to quantify parameter uncertainty.
- Metadata and performance information accompany the data; note that human influences on observed flows are not explicitly accounted for in the modelling.
- Part of UK drought and water scarcity research programs (Historic Droughts and IMPETUS).

## Data and Methods

### Input data
- Rainfall: reconstructed daily rainfall data from UK Met Office, extended 1891–1958 with digitised gauge records.
- Potential Evapotranspiration (PET): daily PET derived from reconstructed monthly temperatures using McGuinness-Bordne equation (to maintain consistency with UK CHESS dataset).

### Hydrological model
- GR4J v1.0.2 with four parameters (X1–X4) representing production store, inter-catchment exchange, routing store, and unit hydrograph delay.
- Snow module (CemaNeige) not used due to computational demands.

### Calibration and uncertainty
- Calibration period: 1982-10-01 to 2014-09-30.
- Uncertainty explored with 500,000 parameter sets via Bayesian Latin Hypercube Sampling.
- Multi-objective evaluation using six metrics: NSE, NSE (log), MAPE, PBIAS, MAM30, Q95.
- Ranks combined and filtered by acceptability thresholds (four tiers) before selecting top realizations.
- Top 500 model realizations included in the ensemble; top ranking realization used for the Single_Run output.
- Model performance varies by catchment; some catchments poorly reproduced; some flows influenced by human activity not explicitly modeled.

## Data Format

### Single_Run
- 305 daily flow files for top ensemble member plus 1 metadata file.
- File naming: HD_FlowSingle_<catchmentID>_18910101_20151130.csv
- Columns: catchID, Date, Flow_Top_Calib, Min_500, Max_500
- Metadata file: HD_FlowSingle_Metadata.csv (305 rows, 23 columns) with:
  - Model parameters (Param1–Param4), performance metrics for calibration (NSE_Cal, NSElog_Cal, MAPE_Cal, absPBIAS_Cal, MAM30APE_Cal, Q95APE_Cal),
  - Evaluation years (Eval_Yrs), performance over evaluation period (NSE_Eval, NSElog_Eval, MAPE_Eval, absPBIAS_Eval, MAM30APE_Eval, Q95APE_Eval),
  - UncertWidth_500 and ContRatio_500 for the ensemble context.

### Ensemble_500
- 305 daily flow files for 500 ensemble realizations plus 305 metadata files.
- File naming: HD_FlowEnsemble_<catchmentID>_18910101_20151130.csv
- Each daily file includes Realisation_1_Flow to Realisation_500_Flow.
- Metadata files (HD_FlowEnsemble_<catchmentID>_Metadata.csv) contain 500 rows with the same fields as Single metadata (columns 2–22), but exclude UncertWidth_500 and ContRatio_500 (not calculable per realization).

### Guidance notes
- Some catchments have artificial human influences (e.g., abstractions) not explicitly accounted for; performance varies by catchment.
- Users may choose the full 500-member ensemble for probabilistic analyses or the top ensemble member for a deterministic view; the full ensemble generally captures a high fraction of observations in most catchments.

## Model Evaluation and Uncertainty

- Evaluation metrics calculated over calibration and, where available, evaluation periods; summary metrics and trends provided in metadata.
- Uncertainty quantification includes:
  - Uncertainty width: average daily range across ensemble members relative to the midpoint.
  - Containment ratio: percentage of days where observations fall within the ensemble min–max range.
- Visual maps (in accompanying figures) illustrate performance across catchments for the six metrics and the ensemble uncertainty metrics.

## Context and Project Background

- Catchments: 303 across the UK, including near-natural (UK Benchmark Network) and more heavily human-influenced sites.
- Purpose: reconstruct river flows where gauged observations are unavailable or incomplete; feed into drought analysis and water resources planning.
- Projects:
  - IMPETUS: improving drought forecasting and decision-making processes; emphasized ensemble approaches to capture forecast uncertainty.
  - Historic Droughts: understanding past UK droughts (late 19th/early 20th century) to inform future drought management.
- Outputs support drought indicators (e.g., Standardised Streamflow Index) and multi-decadal drought analyses.

## Limitations and Considerations for Monitoring use

- The model does not explicitly simulate artificial human influences on flows; interpret results with this caveat.
- Performance varies by catchment; consult catchment-specific metadata to assess suitability for a given monitoring objective.
- The 500-member ensemble provides a robust basis for uncertainty characterization; the single_run output is deterministic but lacks parameter-uncertainty representation.
- Two naturalised calibrations (Thames at Kingston and Lee at Feildes Weir) are included to provide near-natural baselines.

## Data Governance and Access

- Datasets are presented in CSV format with comprehensive metadata to support transparency and reproducibility.
- Acknowledgements: Historic Droughts and IMPETUS projects under the NERC UK Droughts and Water Scarcity Programme.
- References and related methodological documentation are provided within the dataset metadata and associated literature.