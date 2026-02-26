# Parameters_[model_name].csv

## Overview
- A dataset comprising 24 comma-separated CSV files named Parameters_[model_name].csv.
- Each file contains 798 data rows and 5–18 columns (plus a header row), representing best parameter values to run a specific model in a specific catchment under specific input data.
- The dataset uses seven sources of precipitation data and three sources of evapotranspiration data, across 38 catchments (38 stations) in Indonesia (Citarum and Ciliwung basins).

## Content and structure
- Each file is tied to a single model (identified in the file name) and describes a unique combination of:
  - Precipitation data source (e.g., AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, Yanto)
  - Evapotranspiration data source (e.g., AgMERRA, SA-OBS, Yanto)
  - Gauging station (catchment) in the Citarum or Ciliwung basin
- The first three columns are text data: Precip, Evap, Catchment.
- The remaining columns are numeric model parameter values for the corresponding model.
- Number of columns varies by file (2–15 numeric parameter columns beyond the first three).
- The 38 catchments include five gauging stations in the Ciliwung basin and 33 in the Citarum basin.

## Data generation and target metric
- Parameter values were not obtained by direct optimization. Instead:
  - Each scenario was run with 100,000 randomly sampled parameter sets.
  - The file saves the parameter set that produced the highest modified Kling Gupta Efficiency (KGE') between observed and modeled daily mean flow, after discarding the first three years as spin-up.
- Input precipitation and evapotranspiration data are catchment-averaged, derived by clipping gridded datasets with boundary shapefiles; boundaries are generated from HydroSHEDS 15 arc-second DEM.

## Models and parameters
- The dataset spans 24 hydrological models with a total of 174 parameters distributed across them.
- Models included (examples): FLEX-I, GR4J, HBV-96, HyMOD, IHACRES, MODHYDROLOG, MOPEX variants, NAM, New Zealand 2, PDM (and exponential variants), SIMHYD, SMAR, Susannah Brook 1–5, TCM, Xinanjiang, among others.
- Parameter columns vary by model; parameter units differ depending on model components (e.g., mm, day, dimensionless).
- A companion table provides descriptions for the 174 parameters and their units, cross-referencing standard model descriptions (e.g., PDM variants and MARRMoT references).

## Data provenance and sourcing
- Funding: Natural Environment Research Council (NERC) Understanding the impacts of hydrometeorological hazards in Southeast Asia programme (references NE/S002790/1 and NE/S00310X/1).
- Date of upload: 2022-08-31 (Version 1).
- Data sources for inputs and basins:
  - Precipitation dataset references: Ruane et al. 2015; Funk et al. 2015; Xie et al. 2010; Beck et al. 2019; Ashouri et al. 2015; van der Besselaar et al. 2017; Yanto et al. 2017.
  - Model references: Moore 2007 (PDM); Knoben et al. 2019 (MARRMoT supplement).

## Metadata, quality, and interoperability
- Text fields (Precip, Evap, Catchment) ensure traceable data grouping across files.
- Numeric parameter fields include model-specific units; not all parameter names align directly with standard references, but descriptions map them to model structures.
- The data are designed for cross-model, cross-input comparison of parameterizations in Catchments within Indonesia, enabling assessment of how input choices affect parameterization.
- Considerations for users:
  - Inconsistent naming across models and varying unit conventions require careful interpretation when aggregating or comparing parameters.
  - No explicit licensing is stated; metadata focus is on provenance, inputs, and model parameterization descriptions.

## Practical implications for Data Leaders
- Discoverability and reuse: 24 clearly named files with consistent three-column identifiers (Precip, Evap, Catchment) facilitate cross-model analyses.
- Governance and quality: Clear documentation of spin-up, random-parameter approach, and KGE' objective supports reproducibility and auditability.
- Data completeness and gaps: Complex metadata with model-specific parameters and units necessitates robust metadata management and domain expertise to ensure correct interpretation.
- Collaboration potential: Rich, multi-model parameter sets across multiple basins support comparative studies, benchmarking, and broader data ecosystem development in hydrological modeling.

## References and additional information
- Data sources and model descriptions cited in the accompanying references, including foundational papers for PDM and MARRMoT.
- Detailed model parameter descriptions and units are provided in the accompanying table, with cross-references to the cited literature.