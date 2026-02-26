# Parameters_[model_name].csv

- Overview
  - A dataset consisting of 24 comma-separated value (CSV) files named Parameters_[model_name].csv.
  - Each file contains one header row and 798 data rows with 3 text columns plus 0–15 numeric parameter columns, depending on the model.
  - Each row represents a unique combination of inputs: one of seven precipitation data sources, one of three evapotranspiration data sources, and one gauging station catchment in the Citarum or Ciliwung basins (totaling 7 × 3 × 38 = 798 combinations).
  - The seven precipitation datasets are: AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, and Yanto. The three evapotranspiration datasets are: AgMERRA, SA-OBS, and Yanto.
  - The dataset was created to provide the best parameter values to run a specific model for each catchment and input combination.

- Data structure and content
  - First three columns: Precip (text), Evap (text), Catchment (text) — identifying the input data and location.
  - Remaining columns: model parameters (numeric). The number of parameter columns varies by file (2 to 15 extra columns), corresponding to the parameters of the specified model.
  - Parameter values in each row were selected as the best among 100,000 randomly sampled parameter sets for that model/input combination, measured by a modified Kling Gupta Efficiency (KGE′) between observed and modeled daily mean flow, after discarding the first three years as spin-up.
  - Spin-up: The initial three years of modeled flow are ignored when evaluating KGE′.
  - Input data values are catchment-averaged, obtained by clipping the gridded datasets with catchment boundaries derived from HydroSHEDS, with upstream boundaries defined for each gauging station.

- Input data and catchments
  - Model runs span seven precipitation sources, three evapotranspiration sources, and 38 catchments.
  - Gauging stations: 33 in the Citarum basin (main stem or tributaries) and 5 named in the Ciliwung basin (Ciliwungxxx).
  - Precipitation and evapotranspiration inputs are catchment-averaged for each combination.

- Model parameter catalog
  - The dataset includes descriptions for 174 model parameters distributed across the 24 models.
  - Parameters are provided with units and descriptive meanings; mappings and full descriptions are related to four variants of the PDM and to 20 other models.
  - Model examples included in the dataset descriptions: FLEX-I, GR4J, HBV-96, HYCYMODEL, HyMOD, IHACRES, MODHYDROLOG, MOPEX variants, NAM, New Zealand 2, PDM (and exponential variants), SIMHYD, SMAR, Susannah Brook, TCM, Xinanjiang, among others.
  - Some parameter names and units vary across models; additional cross-reference details are provided in the documentation to aid interpretation.

- Data provenance and funding
  - Funding: Natural Environment Research Council (NERC) Understanding the impacts of hydrometeorological hazards in Southeast Asia programme (NE/S002790/1 and NE/S00310X/1).
  - Date of upload: 2022-08-31 (Version 1).
  - Data sources for inputs include established climate forcing datasets and precipitation/temperature records referenced in the accompanying literature.

- References and documentation
  - The dataset references foundational sources for precipitation datasets and hydrological modeling parameter frameworks, including:
    - Climate forcing datasets (Ruane et al., 2015)
    - SA-OBS, PERSIANN-CDR, MSWEP, CHIRPS, and other precipitation datasets
    - PDM model framework (Moore, 2007) and MARRMoT toolbox (Knoben et al., 2019)
  - Parameter descriptions and model mappings are detailed in the accompanying references [8] and [9] (the PDM variants and the broader MARRMoT framework).

- Usage notes and caveats
  - Parameter values are not derived from direct optimization of KGE′; rather, they reflect the best result among a large random search (100,000 parameter sets) for each model/input combination.
  - Units and parameter names vary across models; users should consult the per-model parameter descriptions to interpret columns correctly.
  - The dataset focuses on SE Asia hydrometeorological contexts (Java islands’ basins) and uses catchment-averaged inputs and boundary definitions; applicability to other regions may require reprocessing.
  - Data accessibility includes 24 separate CSV files; each file targets a specific model and includes 798 rows corresponding to all input combinations.

- Practical value for analysts
  - Enables rapid comparison of model performance across multiple input datasets and catchments using a consistent metric (KGE′) framework, with a transparent record of the parameter sets that yielded the best performance under random search.
  - Supports sensitivity analyses and benchmarking of hydrological models under varying climate forcings and catchment characteristics.
  - Provides a comprehensive parameter reference (174 parameters across 24 models) to facilitate cross-model understanding and transferability studies.