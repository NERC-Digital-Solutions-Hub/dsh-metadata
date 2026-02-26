# Supporting documentation for 'DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (1962-2015) using observed driving data'

- Scope and purpose
  - Provides the dataset and methodology used to generate an ensemble of daily river flow timeseries for 1,366 catchments across Great Britain from 1962 to 2015.
  - Based on the DECIPHeR hydrological model; open-source framework designed for national-scale flow simulations and uncertainty assessment.

- Data access and use
  - Terms, licence and conditions of use available via a dedicated data DOI.
  - Users must cite the dataset and associated paper: Coxon et al. (2019) in Geoscientific Model Development or the provided DOI.
  - Data publicly accessible through the specified DOI; datasets are provided to enable scrutiny and reuse.

- Dataset description
  - Ensemble content: 100 simulated daily river flow time series for each of 1,366 GB catchments (1962-2015).
  - Forcing data: daily rainfall and potential evapotranspiration from CEH GEAR and CHESS-PE, 1961-2015; aggregated to a 5 km grid.
  - Model and evaluation: DECIPHeR evaluated using a multi-objective approach over 1962-2015 with four metrics (NSE, slope of flow duration curve, bias in runoff ratio, low flow volume).
  - Metadata: includes model parameters and performance for all 100 ensemble members to support interpretation and reuse.

- Context and purpose
  - Part of the MARIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity); aims to support drought and water scarcity impact modeling across scales.
  - DECIPHeR code is open source (GitHub) and the specific model run data are provided for benchmarking and broad applications.

- Methods (highlights)
  - Input data: 55-year period 1961-2015 for precipitation, potential evapotranspiration, and discharge; 1961 used as warmup.
  - Model framework: DECIPHeR based on Dynamic TOPMODEL concepts; parameters explored with Monte Carlo sampling of 10,000 sets per catchment.
  - Ensemble selection: top 1% (n = 100) of simulations ranked by equal-weighted multi-objective score combining NSE, flow duration slope, runoff ratio bias, and low-flow bias.
  - Evaluation outcomes: detailed per-catchment performance summarized in metadata; overall performance varies geographically.

- Data format and contents
  - Daily flow data: CSV files for each catchment, time span 1962-01-01 to 2015-12-31.
  - File pairs per gauge: 
    - DECIPHeR_FlowEnsemble_<gaugingstationID>_19620101-20151231.csv containing flow_realisation_1 to flow_realisation_100.
    - DECIPHeR_FlowEnsemble_<gaugingstationID>_Metadata.csv containing 100 rows (one per ensemble member) with parameters and performance metrics (nse, lognse, biasrr, lfv, tsfdc, plus model parameters).
  - Data structure: 19723 data rows per file (plus header) and 102 columns in flow files; 100 rows plus header and 16 columns in metadata files.
  - Ensemble visualization: DECIPHeR_FlowEnsemble_<gaugingstationID>_SimFlow.png plots showing observed discharge, precipitation, and 5th-95th percentile uncertainty (GLUE-based bounds) for selected two-year periods.

- Model performance and limitations
  - Overall: around 90% of gauges have NSE > 0; about 72% exceed NSE > 0.5 for the top-ranked ensemble.
  - Spatial patterns: better performance in wetter, western Scotland/Northwest England; poorer in drier southern and eastern England, particularly in groundwater-dominated chalk regions.
  - Specific biases: tendency to overestimate flows in the Southeast, under-representation of low flows in parts of the Midlands and Northeast Scotland, and underestimation of flow variability (smoother hydrographs) in Scotland and North Wales.
  - Limitations: model does not currently explicit include abstractions or reservoirs; performance varies by catchment; users should consult per-catchment metadata for suitability.

- Guidance for use
  - Coverage: ~90% of the National River Flow Archive gauge network; suitability varies by catchment due to unmodeled processes.
  - Uncertainty: 100 simulations provide uncertainty bounds; these do not cover the full parameter space; users are encouraged to use many simulations to characterize uncertainty.
  - Practical use: time series can be used to compute custom performance metrics; do not rely on a single deterministic output.
  - Data management: metadata and ensemble outputs enable interrogation of model performance and support principled data use.

- Context for analysts monitoring the environment
  - Enables consistent, comparable river-flow representations across GB for monitoring environmental health and policy performance over time.
  - Datasets and performance metadata support transparent assessment of model outputs, enabling integration with other environmental indicators and impact models.
  - Open-source nature and thorough documentation facilitate reproducibility and method standardization across monitoring programs.

- Acknowledgements and references
  - Acknowledges the MaRIUS project and NERC support; thanks specific contributors.
  - Key references listed for DECIPHeR framework, input datasets, and evaluation methods.