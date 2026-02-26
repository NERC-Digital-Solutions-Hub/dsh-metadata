# Supporting documentation for 'DECIPHeR model estimates of daily flow for 1366 gauged catchments in Great Britain (19622015) using observed driving data'

## 1. Data access, citation and conditions of use
- Access to data, licence, and terms of use are provided via a DOI link.
- Users must cite the associated publication: Coxon et al. 2019 (NERC Environmental Information Data Centre) when using the data.
- The dataset is provided to enable reuse under specific terms; check the DOI for details.

## 2. Summary Description of the Dataset
- An ensemble of 100 simulated daily river-flow time series for 1,366 catchments across Great Britain from 1962-01-01 to 2015-12-31.
- Simulations produced with the open-source DECIPHeR hydrological modelling framework.
- Forcing data come from CEH GEAR (rainfall) and CHESS-PE (potential evapotranspiration) spanning 1961-2015; data aggregated to a 5 km grid.
- Model performance evaluated with a four-metric multi-objective approach; metadata from all 100 ensemble members included.
- Top-ranked simulations (based on joint ranking) are highlighted; users should consult metadata as performance varies across gauges.
- A related Geoscientific Model Development paper (Coxon et al., 2019) describes the framework and performance.

## 3. Context of the dataset
- Produced under the MARIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), a UK NERC-funded initiative (2014-2018).
- Aims to support risk-based drought and water scarcity assessments across ecosystems, agriculture, economy, and energy.
- DECIPHeR is open source; code available on GitHub and Zenodo; dataset designed to drive various impact models nationally across the UK.

## 4. Methods
### 4.1 Input data
- Daily precipitation, potential evapotranspiration, and discharge data for 1961-2015 used to run and evaluate DECIPHeR.
- Forcing data: CEHGEAR (1 km) and CHESS-PE (1 km), aggregated to 5 km.
- Model evaluation uses observed daily flow data from the National River Flow Archive (NRFA).

### 4.2 Model Evaluation
- Monte Carlo approach with 10,000 parameter sets drawn from uniform priors, applied across each catchment.
- Parameters tuned to reflect Dynamic TOPMODEL-based hydrology; ranges documented in the study.
- Four evaluation metrics: NSE, slope of Flow Duration Curve, bias in Runoff Ratio, and Low Flow Volume.
- A multi-objective ranking assigns equal weight to all metrics; the top 1% (100) simulations constitute the behavioural ensemble.
- Performance insights: ~90% of gauges have NSE > 0; ~72% have NSE > 0.5; better performance in wetter NW regions; poorer in SE groundwater-dominated (chalk) regions with overestimation biases; low-flow and variability captured with varying success across regions.
- Additional metric: logNSE (NSE on log-transformed flows) included in metadata but not used in ranking.

### 4.3 Data Format
- Two CSV files per gauge: one with daily flows for all 100 ensemble members, and one with metadata for all members.
- File naming example: DECIPHeR_FlowEnsemble_<gaugingstationID>_19620101-20151231.csv
- Ensemble daily flow file structure: 19723 rows x 102 columns (catch_id, date, flow_realisation_1 … flow_realisation_100).
- Ensemble metadata file structure: 100 rows x 16 columns (parameter values for each ensemble member plus performance metrics such as nse, lognse, bias metrics, tsfdc).

### 4.4 Ensemble Figure Files
- Visualizations per gauge showing observed discharge, precipitation, and uncertainty bounds (5th–95th percentile) for selected two-year periods.
- Uncertainty bounds derived from likelihood-weighted distribution of top 1% simulations using GLUE.
- Notes that observed discharge may be missing in some periods.

## 5. Guidance notes
- Coverage: ~90% of the NRFA gauge network; model excludes abstractions, reservoir operations, and other human alterations (future work planned to include these processes).
- Use of uncertainty: 100 simulations provided to quantify uncertainty; users are advised to utilize multiple simulations or derive uncertainty bounds rather than relying on a single top-ranked run.
- Metadata-driven interpretation: users should consult metadata to understand performance for their chosen catchment and interpret results accordingly.
- Potential applications: datasets support a wide range of impact assessments and uncertainty analyses across scales.

## 6. Acknowledgements
- Funded by NERC UK Droughts and Water Scarcity Programme: MaRIUS (NE/L010399/1).
- Acknowledgement of contributions from individuals who assisted with dataset availability.

## 7. References
- Key references detailing DECIPHeR, dynamic TOPMODEL, evaluation metrics, and supporting input datasets (Beven & Freer; Coxon et al. 2019; Keller et al. 2015; Tanguy et al. 2016; Robinson et al. 2016; Yadav et al. 2007; Yilmaz et al. 2008; etc.).