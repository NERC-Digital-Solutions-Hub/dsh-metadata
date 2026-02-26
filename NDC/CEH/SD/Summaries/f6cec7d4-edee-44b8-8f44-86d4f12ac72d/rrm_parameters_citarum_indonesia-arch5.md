# Parameters_[model_name].csv

## Data overview

- A set of 24 comma-separated value files (CSV), each named Parameters_[model_name].csv.
- Each file contains one header row followed by 798 data rows and 5–18 columns (3 text columns plus the number of model parameter columns for that model).
- Rows represent a unique combination of: precipitation data source (seven options), evapotranspiration data source (three options), and gauging station in the Citarum or Ciliwung basin (38 total; 5 in Ciliwung labeled with Ciliwungxxx).
- Data describe the parameter values for running a specific model in a specific catchment with given input data.
- The parameter values in each row were selected from 100,000 randomly sampled parameter sets; the saved row corresponds to the highest Kling Gupta Efficiency (KGE') between observed and modeled daily mean flow (spin-up period of the first three years ignored).
- Precipitation and evapotranspiration inputs are catchment-average values derived by clipping gridded datasets to a shapefile boundary; boundaries generated from HydroSHEDS DEM.
- The first three columns (Precip, Evap, Catchment) are text data; remaining columns are numeric model parameters (the number of parameters varies by model).

## Content and structure

- 174 model parameters distributed across the 24 models (parameters vary in name and interpretation by model).
- Models represented include FLEX-I, GR4J, HBV-96, HyMOD, IHACRES, MODHYDROLOG, MOPEX, NAM, New Zealand 2, PDM variants (including exponential and 1-res versions), SIMHYD, SMAR, Susannah Brook, TCM, Xinanjiang, and others.
- Each model file contains the parameter columns specific to that model; the parameter columns and their order differ by file.
- Parameter units and descriptions are provided in a comprehensive table, with cross-references to foundational model literature (e.g., Moore 2007; Knoben et al. 2019) and related model variant documentation.

## Provenance and context

- Authors: Gianni Vesuviano et al.; funding from the Natural Environment Research Council (NE/S002790/1 and NE/S00310X/1).
- Date of upload: 2022-08-31 (Version 1).
- Data sources for inputs reference seven precipitation datasets (e.g., AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, Yanto) and three evap datasets.
- Catchments: 38 basins across Citarum and Ciliwung; five gauging stations in Ciliwung and the rest in Citarum.
- Input data are catchment-averaged values produced by clipping gridded datasets to catchment boundaries; boundary delineation based on HydroSHEDS-derived shapefiles.

## Parameter and model descriptions

- The dataset includes descriptions for 174 model parameters spread across the 24 models.
- Parameter naming does not always match the referenced literature exactly; descriptions map parameters to their model roles.
- For full parameter semantics, consult the described mappings and the cited references [8] (PDM variants) and [9] (MARRMoT framework).
- Examples of parameter groups span interception storage, soil moisture storage, various runoff reservoirs and unit hydrographs, evapotranspiration/principal controls, baseflow concepts, routing time bases, and many model-specific coefficients and thresholds.

## Documentation, reuse, and governance

- Data are designed to support hydrological modeling in the specified Southeast Asian basins using multiple input data sources.
- To interpret the parameter values, users should reference the model-specific parameter descriptions and the broader model literature cited.
- All files share the same three text columns; numeric parameter columns vary by model, requiring careful schema handling and metadata alignment.
- The dataset version is Version 1 (as of 2022-08-31); the documentation notes 174 parameters across 24 models with explicit notes on units variability and cross-model mappings.
- Licensing and access conditions are not specified in the provided text; users should verify licensing terms and data access restrictions before reuse.