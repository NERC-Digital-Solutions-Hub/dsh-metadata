# Parameters_[model_name].csv

- A dataset consisting of 24 comma-separated CSV files, each containing the best parameter values to run a specific hydrological model in a particular catchment, given selected input data.
- Each file has:
  - 1 header row
  - 798 data rows
  - 3 text columns (Precip, Evap, Catchment)
  - 5–18 numeric model-parameter columns (vary by model), totaling 174 distinct parameters across all models
- The same structure and order of the first three columns is consistent across all files, while the number and identity of subsequent columns depend on the model.

- Purpose and context:
  - The parameter sets are derived from evaluating 100,000 randomly sampled parameter combinations for each model/catchment/climate-input combination.
  - The file stores the parameter set that yielded the highest modified Kling Gupta Efficiency (KGE') between observed and modeled daily mean flow, ignoring the first three years as spin-up.

- Climate input data and catchments:
  - Precipitation data sources: AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, Yanto
  - Evapotranspiration data sources: AgMERRA, SA-OBS, Yanto
  - Catchments: 38 in total, including the Citarum and Ciliwung basins; catchments are defined upstream of gauging stations
  - Precipitation/evaporation inputs are catchment-averaged by clipping gridded datasets with catchment boundaries derived from HydroSHEDS-based shapefiles

- Data composition details:
  - The first three columns are textual descriptors: Precip, Evap, Catchment
  - The remaining columns are numeric parameters specific to the identified model in the file name
  - The total number of columns varies by model (from as few as 2 extra parameter columns to as many as 15)
  - Units for parameters vary by model and parameter; some example parameters and their typical roles include interception storage, soil moisture storage, baseflow and runoff reservoir times, and routing coefficients

- Model families included:
  - FLEX-I, GR4J, HBV-96, HYCYMODEL, HyMOD (and HyMOD exponential variants), IHACRES, MODHYDROLOG, MOPEX (1, 3, 4), NAM, New Zealand 2, PDM variants (including exponential and 1-res variants), SIMHYD, SMAR, Susannah Brook 1-5, TCM, Xinanjiang, among others

- Parameter descriptions and references:
  - A total of 174 model parameters are described across the 24 models
  - Parameter naming may differ from sources, but descriptions map to corresponding model structures
  - For detailed parameter relationships, refer to the cited sources [8] and [9] (PDM variants and MARRMoT framework)

- Provenance and funding:
  - Authors: Gianni Vesuviano (UK Centre for Ecology & Hydrology); Simon Mathias, Rahmawati Rahayu, Sim Reaney (Durham University)
  - Funded by the Natural Environment Research Council (NE/S002790/1 and NE/S00310X/1) for understanding hydrometeorological hazards in Southeast Asia

- Data integrity and usage notes for GIS work:
  - Rows represent unique combinations of precipitation input, evapotranspiration input, and catchment
  - The parameter values were not found via direct optimization but were selected from 100,000 random samples per case to maximize KGE'
  - The dataset enables GIS-based exploration of model parameters and their spatial distribution across multiple catchments and input data scenarios
  - Be mindful of varying parameter units across models when integrating or visualizing parameter maps

- Practical considerations for GIS workflows:
  - Ensure consistent catchment geometries and boundary clipping when linking climate inputs to spatial features
  - When comparing models or performing cross-model analyses, account for differences in parameter naming and units
  - Use the 798-row structure to generate sensitivity analyses or to map parameter ranges by model and catchment
  - Leverage the first three textual columns to join parameter data with GIS attributes (e.g., catchment identifiers, model names)

- Access and references:
  - Climate data sources and model references are enumerated in the accompanying documentation
  - References include foundational works on the climate forcing datasets, precipitation products, and hydrological model descriptions
  - Date of upload: 2022-08-31 (Version 1)