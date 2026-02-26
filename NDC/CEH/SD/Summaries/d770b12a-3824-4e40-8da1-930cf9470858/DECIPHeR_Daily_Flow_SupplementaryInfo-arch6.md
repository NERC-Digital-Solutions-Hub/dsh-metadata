# Supporting documentation for 'DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (19622015) using observed driving data'

## Overview
- Provides an ensemble of 100 simulated daily river flow timeseries for 1,366 catchments across Great Britain from 1962-01-01 to 2015-12-31.
- Flows are produced with the DECIPHeR hydrological model using observed driving data (rainfall and potential evapotranspiration).
- Forcing data: CEH GEAR and CHESS-PE, aggregated to 5 km grid; evaluation against National River Flow Archive (NRFA) gauges.
- A multi-objective evaluation selects the top 1% of simulations (100 per catchment) for end-user use.

## Data Access and Licensing
- Terms and conditions apply; data, licence and use terms available at the provided DOI.
- Users must cite the dataset:
  Coxon, G.; Freer, J.; Lane, R.; Dunne, T.; Knoben, W.J.M.; Howden, N.J.K.; Quinn, N.; Wagener, T.; Woods, R. (2019). DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (1962-2015) using observed driving data. NERC Environmental Information Data Centre. https://doi.org/10.5285/d770b12a-3824-4e40-8da1-930cf9470858
- The DECIPHeR code and model framework are open source (GitHub) with the model version used described in Coxon et al. (2019).

## What the Dataset Contains
- An ensemble of 100 daily flow time series for each gauge (1,366 gauges) spanning 1962-01-01 to 2015-12-31.
- Metadata for all 100 ensemble members per gauge to aid interpretation of performance.

## Methods and Data Sources
- Input data: Daily precipitation and potential evapotranspiration (1961-2015) and discharge data for calibration/validation from CEHGEAR, CHESS-PE, aggregated to 5 km.
- Model framework: DECIPHeR, based on Dynamic TOPMODEL concepts; open-source and national-scale capable.
- Evaluation: Multi-objective scoring across four metrics to capture balance, variability, and extremes:
  - Nash-Sutcliffe Efficiency (NSE)
  - Slope of the Flow Duration Curve
  - Bias in Runoff Ratio (RR)
  - Low Flow Volume (LFV)
- 10,000 parameter sets sampled in Monte Carlo; top 1% (100 ensemble members per gauge) selected via equal-weighted ranking across the four metrics.

## Data Format and Structure
- Time series data files (CSV) for daily flows:
  - File naming: DECIPHeR_FlowEnsemble_<gaugingstationID>_19620101-20151231.csv
  - Contents: 19,723 rows (plus header), 102 columns:
    - catch_id, date, flow_realisation_1, flow_realisation_2, ..., flow_realisation_100
- Metadata files (CSV) for the 100 ensemble members:
  - File naming: DECIPHeR_FlowEnsemble_<gaugingstationID>_Metadata.csv
  - Contents: 100 rows (plus header), 16 columns per row:
    - realisation, catch_id, river, station, param_szm, param_lnto, param_srmax, param_srinit, param_chv, param_td, param_smax, nse, lognse, biasrr, lfv, tsfdc
- Figure files (optional): DECIPHeR_FlowEnsemble_<gaugingstationID>_SimFlow.png
  - Visualizes observed flow, precipitation, and 5th–95th percentile uncertainty bounds for selected two-year periods.

## Model Performance and Guidance
- Coverage: Approximately 90% of the NRFA gauge network represented; suitable for national-scale applications and impact modelling.
- General performance: Majority of gauges show NSE > 0; many exceed NSE > 0.5 in the top ensemble, though performance is regionally variable.
  - Better performance in wetter northern/western GB; poorer in drier southern/eastern GB.
  - Groundwater-dominated areas (e.g., chalk in SE) show poorer mass balance and overestimation biases.
  - Midlands low flows influenced by reservoir regulation, affecting LFV and related metrics.
  - Slope of the flow duration curve tends to be under-estimated in Scotland and North Wales (flows appear smoother).
- Uncertainty: 100-member ensemble enables uncertainty quantification; these do not span the full parameter space, and users are encouraged to use as many realizations as needed or derive uncertainty bounds from the ensemble.
- Caveats: The model currently does not include abstractions or reservoir effects; results should be interpreted with this in mind, especially for heavily modified catchments.
- Metadata includes additional evaluation (not used in ranking) such as log NSE for further assessment.

## How to Use the Data
- Self-service analysis: Use the 100 ensemble flows to explore uncertainty and to feed impact or risk-assessment models.
- Performance-aware usage: Consult the per-gauge metadata to understand model performance and suitability for a given catchment before application.
- Comparative metrics: You can compute your own performance metrics using the provided time series.
- Reproducibility: Access to open-source model code and the associated DOIs facilitates replication and extension.

## Provenance and Resources
- Part of the MaRIUS project (Managing the Risks, Impacts and Uncertainties of droughts and water Scarcity) funded by NERC.
- Related publications detailing the modelling framework and evaluation: Coxon et al. 2019; Beven & Freer; Beven 2006; and supporting datasets for CEHGEAR, CHESS-PE, and references within.

## Acknowledgements and References
- Acknowledges contributors and funding from the MaRIUS programme; cites Beven, Freer, Coxon, Keller, Tanguy, Robinson, Yadav, Yilmaz, and others as foundational sources.