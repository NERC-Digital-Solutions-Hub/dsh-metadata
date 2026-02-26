# Parameters_[model_name].csv

## Overview
- A dataset comprising 24 comma-separated value (CSV) files, each named Parameters_[model_name].csv.
- Each file contains one header row plus 798 data rows and 5–18 data columns beyond the initial three.
- Files reflect combinations of input data: seven precipitation sources, three evapotranspiration sources, and 38 catchments, hence 798 rows per file.

## Purpose and use
- Each row represents a unique combination of:
  - Precipitation input data (e.g., AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, Yanto)
  - Evapotranspiration input data (e.g., AgMERRA, SA-OBS, Yanto)
  - Gauging station in the Citarum or Ciliwung basins
- The first three columns specify Precip, Evap, and Catchment; the remaining columns hold model parameter values for the model named in the file, which maximize the modified Kling Gupta Efficiency (KGE') between observed and modeled daily mean flow at the selected station, using the specified inputs.
- The flow period uses the maximum shared time span of the precipitation and evapotranspiration series; the first three years of modeled flow are treated as spin-up.

## Data inputs and spatial setup
- Precipitation and evapotranspiration inputs are catchment-averaged, derived by clipping gridded datasets with a shapefile boundary.
- Boundaries and catchments are based on HydroSHEDS-derived delineations.
- Gauging stations: five in the Ciliwung basin (named Ciliwungxxx) and 33 in the Citarum basin (main Citarum or tributaries).

## Data generation method
- Parameter values in each row were not obtained by optimizing the KGE' objective directly.
- Each case used 100,000 randomly sampled parameter sets; the saved row corresponds to the highest KGE' achieved.

## CSV structure details
- Columns 1–3: Precip (seven possible values), Evap (three possible values), Catchment (38 possible values).
- Additional numeric columns: model-specific parameters; the number of extra columns varies by file (range 2 to 15).
- Parameter units vary by model and parameter; column descriptions provide the mapping for each model.

## Model parameters and descriptions
- A total of 174 model parameters distributed across 24 models (e.g., FLEX-I, GR4J, HBV-96, HyMOD, IHACRES, MODHYDROLOG, MOPEX variants, NAM, New Zealand 2, PDM family, SIMHYD, SMAR, Susannah Brook, TCM, Xinanjiang, and others).
- Parameter naming and units are provided, with descriptions linking to model structure.
- Examples of parameter groups include interception storage, soil moisture storage, runoff/reservoir times, baseflow and interflow coefficients, evapotranspiration adjustments, percolation rates, and unit hydrograph bases.

## Data provenance and governance
- Funding: Natural Environment Research Council (NERC) Understanding the impacts of hydrometeorological hazards in Southeast Asia program (NE/S002790/1 and NE/S00310X/1).
- Date of upload: 2022-08-31 (Version 1).
- Data sources and references span climate forcing datasets and hydrological modelling literature, including widely used precipitation datasets (e.g., Merged climate datasets, gauge-based analyses) and model documentation (PDM variants, MOPEX toolbox references).

## Relevance for monitoring frameworks
- Demonstrates integration of multi-source climate inputs with a suite of hydrological models to produce calibrated parameter sets for catchment-scale flow modeling.
- Highlights a reproducible approach for assessing model performance (KGE') across diverse input data, essential for scrutinizing monitoring frameworks and informing future decision-making.
- Illustrates the importance of metadata richness, cross-model parameter mappings, and transparent data provenance for governance and open-data sharing.

## Key challenges and considerations for monitoring practitioners
- Metadata clarity: varying parameter names and units across models require careful interpretation and documentation.
- Data sharing and openness: while the dataset includes rich metadata, sharing of underlying inputs and results must be managed with clear governance.
- Reproducibility: random-parameter-search approach necessitates explicit reporting of seeds and methods to enable replication.
- Data harmonization: combining multiple climate datasets with different temporal and spatial characteristics requires rigorous methodological alignment.
- Scalability: the large number of model configurations and input combinations poses storage and retrieval considerations for monitoring programs.