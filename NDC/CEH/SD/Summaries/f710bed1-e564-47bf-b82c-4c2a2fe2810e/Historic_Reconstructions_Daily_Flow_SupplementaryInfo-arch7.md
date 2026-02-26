# Historic Reconstructions of Daily River Flow for 303 UK Catchments

## Overview
- Provides consistent daily river flow timeseries for 303 UK catchments from 1891 to 2015, with uncertainty estimates.
- Based on GR4J lumped hydrological model calibrated with newly rescued rainfall data and temperature-derived PET data.
- Outputs include a single best-run flow timeseries with uncertainty bands and an ensemble of 500 model realizations.

## Spatial and Temporal Coverage
- 303 UK catchments; includes 115 within the UK Benchmark Network and several catchments of managerial interest.
- Some catchments are near-natural while others are influenced by human activity (abstraction, regulation).
- Two reconstructions are calibrated to naturalised flows (Thames at Kingston, Lee at Feildes Weir).
- Daily flows spanning 1891-01-01 to 2015-11-30 (m3/s).

## Data Content and Formats
- Two data forms:
  - Single_Run: top-ranked ensemble flow with uncertainty bands (Min_500, Max_500).
  - Ensemble_500: daily flows for 500 ensemble realizations (Realisation_1_Flow to Realisation_500_Flow).
- Files are CSV; catchments identified by NRFA IDs (with naturalised cases appended by trailing 0, e.g., 390010).
- Metadata:
  - HD_FlowSingle_Metadata.csv: 305 rows, 23 columns, including catchment info, GR4J parameters (X1–X4) for the top member, and calibration/evaluation metrics (NSE, NSElog, MAPE, absPBIAS, MAM30, Q95) and evaluation years.
  - HD_FlowEnsemble_<catchmentID>_Metadata.csv: 500 rows, 22 columns per ensemble member, including parameter values and performance metrics; uncertainty width and containment ratio not provided at the single-ensemble level.

## Input Data and Modelling
- Inputs: daily rainfall and PET data for each catchment.
- PET data: derived from reconstructed monthly temperatures using McGuinness-Bordne equation (temperature-based) to align with UK CHESS dataset.
- Rainfall: reconstructed daily rainfall, extended 1891-1958 with digitised gauge records.
- Hydrological model: GR4J v1.0.2 with four parameters (X1–X4) representing production store, inter-catchment exchange, routing store, and unit hydrograph lag.
- Calibration: 1982-2014 (water years) with 500,000 parameter sets via Bayesian Latin Hypercube Sampling; multi-objective evaluation using six metrics.

## Uncertainty and Evaluation
- Ensemble of 500 model realizations used to quantify parameter uncertainty.
- For each catchment, performance metrics are provided for calibration and, where available, evaluation periods.
- Uncertainty measures include:
  - Width of the ensemble range (relative width) over the full period.
  - Containment ratio: percentage of days observations fall within the ensemble min–max.
- Some catchments show limited match to observed flows; users should consult metadata for reliability and context.

## Guidance for GIS Use
- Suitable for map-based analyses of historical flows and drought context; enables spatial comparisons and drought indicators (e.g., Standardised Streamflow Index when combined with other data).
- Use ensemble data for probabilistic mapping of flows and uncertainty; Single_Run provides a deterministic baseline.
- Be mindful that GR4J does not explicitly account for human influences; consult naturalised reconstructions where available for near-natural baselines.
- Catchment selection should reference NRFA IDs; review per-catchment performance via the metadata before applying analyses.

## Data Access and Documentation
- Data timeframe and file structure:
  - Single_Run contains 305 catchments × 1 top member file plus 1 metadata file.
  - Ensemble_500 contains 305 catchments × 500 ensemble member files plus 305 metadata files.
- File naming conventions:
  - SingleRun: HD_FlowSingle_<catchmentID>_18910101_20151130.csv
  - Ensemble: HD_FlowEnsemble_<catchmentID>_18910101_20151130.csv
- Documentation and references available within the dataset, including:
  - Context of historical drought projects (Historic Droughts and IMPETUS), and related methodological papers.

## Acknowledgements
- Products of the Historic Droughts and IMPETUS projects under the NERC UK Droughts and Water Scarcity Programme.