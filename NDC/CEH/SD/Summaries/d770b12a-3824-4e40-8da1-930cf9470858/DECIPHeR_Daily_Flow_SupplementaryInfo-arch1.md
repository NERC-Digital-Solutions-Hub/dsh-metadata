# DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (19622015) using observed driving data

- Purpose: Provides an ensemble of daily river flow simulations across Great Britain to support drought and water scarcity risk analyses and impact modelling.

- Time period and scope:
  - Daily flows from 1 January 1962 to 31 December 2015.
  - 1,366 catchments/gauges across Great Britain.
  - Ensemble of 100 simulated daily flow time series per gauge.

- Modeling framework:
  - DECIPHeR: open-source, catchment-continental scale hydrological model based on Dynamic TOPMODEL concepts.
  - Forcing data: CEH GEAR rainfall and CHESS-PE potential evapotranspiration, 1961–2015; aggregated to a 5 km grid.
  - Model evaluated against observed flows from the National River Flow Archive (NRFA).

- Model evaluation and selection:
  - Evaluation over 1962–2015 using four multi-objective metrics:
    - Nash–Sutcliffe Efficiency (NSE)
    - Slope of the Flow Duration Curve (FDC)
    - Bias in Runoff Ratio (RRBIAS)
    - Low Flow Volume (LFV)
  - 10,000 parameter sets sampled via Monte Carlo across wide ranges; performance assessed with the four metrics.
  - Combined multi-objective ranking (equal weight to each metric); top 1% (100 ensemble members) designated as the behavioural ensemble.
  - Results indicate:
    - ~90% of gauges in the full ensemble achieve NSE > 0; ~72% > 0.5.
    - Regional patterns: better performance in wetter/western Scotland and NW England; poorer in drier SE England, with overestimation issues in groundwater-dominated chalk regions.
    - Biases: general overestimation of flows in SE; low-flow bias varies by region; flow variability reproduced well, though some catchments show smoother hydrographs (underestimated slope of FDC) in parts of Scotland and North Wales.

- Data contents and structure:
  - Ensemble daily flow files (one per gauge) in CSV format:
    - File name: DECIPHeR_FlowEnsemble_<gaugingstationID>_19620101-20151231.csv
    - 19,723 rows (days) + header; 102 columns:
      - catch_id, date, flow_realisation_1, flow_realisation_2, ..., flow_realisation_100
  - Ensemble metadata files (one per gauge) in CSV format:
    - File name: DECIPHeR_FlowEnsemble_<gaugingstationID>_Metadata.csv
    - 100 rows + header; 16 columns including parameter values and performance metrics:
      - realisation, catch_id, river, station, param_szm, param_lnto, param_srmax, param_srinit, param_chv, param_td, param_smax, nse, lognse, biasrr, lfv, tsfdc
  - Ensemble figure files (example visualizations):
    - File name: DECIPHeR_FlowEnsemble_<gaugingstationID>_SimFlow.png
    - Two-year period plots showing observed discharge, precipitation, and 5th–95th percentile uncertainty bounds ( GLUE-based bounds).

- Uncertainty and usage guidance:
  - The 100 members provide uncertainty bounds, but do not cover the full possible parameter space.
  - Users are encouraged to use multiple ensemble members to quantify uncertainty; top-ranked deterministic output represents only one realization.
  - Model does not currently include abstractions/reservoirs; many catchments are modified by human activity not represented in the model.
  - Metadata should be consulted to assess performance for a given catchment; additional performance metrics (e.g., logNSE) are available in metadata.
  - The time series can be used to compute user-defined performance metrics and uncertainty bounds (e.g., 5th–95th percentile ranges).

- Context and provenance:
  - Produced under the MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), NERC-funded (grant NE/L010399/1).
  - Part of a broader effort to benchmark DECIPHeR v1.0 and provide open-source, nationally scalable flow ensembles for thousands of gauges.

- Data access, licensing, and attribution:
  - Terms and conditions apply; data and license, including usage terms, available at the referenced DOI.
  - Must cite: Coxon et al. (2019) DECIPHeR v1: Dynamic fluxes and connectivity for predictions of hydrology, Geoscientific Model Development.
  - Data host and model code:
    - Open-source DECIPHeR code: https://github.com/uob-hydrology/DECIPHeR
    - Model outputs/data DOI: https://doi.org/10.5281/zenodo.2604120
  - Usage notes: consult metadata for catchment-specific performance and limitations; the dataset covers about 90% of the NRFA gauge network.

- Acknowledgements and references:
  - Acknowledges MaRIUS project and collaborators; references foundational papers and data sources (GMD 2019; TOPMODEL-related works; CEHGEAR; CHESS-PE; NRFA).