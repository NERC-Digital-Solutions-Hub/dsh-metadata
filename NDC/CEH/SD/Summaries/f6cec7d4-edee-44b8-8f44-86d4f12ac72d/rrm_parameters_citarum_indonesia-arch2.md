# Parameters_[model_name].csv

## Overview
- A dataset of 24 comma-separated value (CSV) files, each named Parameters_[model_name].csv.
- Each file contains one header row followed by 798 data rows and 5–18 columns (3 plus the number of model parameters for that file).
- Rows represent unique combinations of inputs (seven precipitation sources, three evapotranspiration sources) and gauging stations in 38 catchments across two Southeast Asian basins (Citarum and Ciliwung).
- Each row lists the parameter values for a specific model that maximize the modified Kling Gupta Efficiency (KGE') between observed and modeled daily mean flow, for a given input combination.

## Data contents and structure
- First three columns (text data): Precip, Evap, Catchment.
  - Precip: seven sources (AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, Yanto).
  - Evap: three sources (AgMERRA, SA-OBS, Yanto).
  - Catchment: gauging stations in Citarum or Ciliwung basins (e.g., Cikeruh-Jatiwangi; Ciliwungxxx and Citarumxxx naming conventions).
- Remaining columns: numeric model parameter values for the model identified in the file name.
- Number of extra numeric columns (parameters) varies by file (ranging from 2 to 15).
- Units of parameters vary by model and parameter; a comprehensive cross-model parameter table (174 parameters across 24 models) is provided.

## How the parameter values were generated
- For each combination, the model was exposed to 100,000 randomly sampled parameter sets.
- The saved parameter set is the one that produced the highest KGE' (between observed and modelled daily mean flow), after ignoring the first three years of modeled flow as spin-up.
- Precipitation and evapotranspiration inputs are catchment-average values derived by clipping gridded datasets with catchment boundaries; boundaries generated from HydroSHEDS DEM.

## Data sources and boundaries
- Precipitation data sources (7 total): AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, Yanto.
- Evapotranspiration data sources (3 total): AgMERRA, SA-OBS, Yanto.
- Catchments: 38 in two basins (Citarum and Ciliwung); boundary delineation uses shapefiles to extract catchment-average inputs.
- Ciliwung stations are named 'Ciliwungxxx'; other stations are in the Citarum basin and named 'Citarumxxx' or other identifiers.

## Model parameters catalog
- The dataset references 174 model parameters distributed across 24 models (e.g., FLEX-I, GR4J, HBV-96, HyMOD, IHACRES, MODHYDROLOG, MOPEX variants, NAM, New Zealand 2, PDM and its variants, SIMHYD, SMAR, Susannah Brook, TCM, Xinanjiang, etc.).
- For each parameter: units and description are provided; model-specific parameter naming may differ but links to consistent descriptions exist in referenced literature.
- Notable example parameter descriptions include interception storage, soil moisture storage capacity, baseflow and runoff time parameters, unit hydrograph bases, infiltration losses, and various reservoir/partitioning coefficients.

## Data provenance and references
- Data and parameter descriptions align with foundational hydrological modeling literature and tools (e.g., PDM, MARRMoT framework).
- References include:
  - Climate forcing datasets and precipitation datasets (e.g., Merged climate datasets, MSWEP, PERSIANN-CDR, SA-OBS, Yanto).
  - PDM and MARRMoT model descriptions and implementations.
- Specific sources cited for dataset components and model variants (numbered references [1]–[9] in the document).

## Usage notes for environmental analysts
- Enables cross-model, cross-data-source benchmarking of hydrological performance across multiple catchments.
- Supports evaluation of how different precipitation and evapotranspiration inputs influence model calibration results.
- Useful for assessing data provenance, reproducibility, and potential integration with other environmental datasets for monitoring policy performance over time.
- Highlights challenges such as large parameter spaces and the need for robust data management given varying parameter counts and units across models.