# Parameters_[model_name].csv

## Overview
- A dataset of 24 CSV files, each named Parameters_[model_name].csv, containing best parameter values to run a specific hydrological model in a catchment.
- Intended to enable exploration of how different climate inputs affect model performance (KGE' between observed and modeled daily mean flow).

## What’s inside
- 24 CSV files total, each with:
  - 798 data rows
  - 3 text columns (Precip, Evap, Catchment)
  - 5–18 columns of numeric model parameters (vary by model)
- The 7 precipitation data sources: AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, Yanto
- The 3 evapotranspiration data sources: AgMERRA, SA-OBS, Yanto
- 38 catchments across two basins (Citarum and Ciliwung); 5 gauging stations in Ciliwung, 33 in Citarum
- Each row describes a unique combination of precipitation source, evapotranspiration source, and catchment

## Data structure and generation
- Row structure:
  - Columns 1–3: Precip, Evap, Catchment (text values)
  - Remaining columns: numeric model parameters for the model identified in the file name
- Data generation method:
  - For each combination, 100,000 parameter sets were randomly sampled
  - The saved row corresponds to the parameter set that yielded the highest KGE' (observed vs. modeled daily mean flow)
  - The KGE' calculation ignores the first three years of modeled flow as spin-up
- Input data preparation:
  - Precipitation and evap inputs are catchment-averaged, created by clipping gridded datasets with a shapefile boundary
  - Boundaries generated using HydroSHEDS 15 arc-second DEM
- Model inputs align with a fixed set of 7 precipitation sources, 3 evap sources, and 38 catchments

## Models and parameters
- 24 models represented (e.g., FLEX-I, GR4J, HBV-96, HyMOD, IHACRES, MODHYDROLOG, MOPEX variants, NAM, New Zealand 2, PDM families, SIMHYD, SMAR, Susannah Brook variants, TCM, Xinanjiang, etc.)
- A total of 174 model parameters distributed across the 24 models
- Parameter descriptions and units are provided, with cross-references to model-specific documentation (e.g., PDM variants and MARRMoT toolbox references)

## Data provenance and metadata
- Data owner authors: Gianni Vesuviano et al., UK Centre for Ecology & Hydrology; Durham University team
- Funding: Natural Environment Research Council, Southeast Asia hydrometeorological hazards program
- Upload date: 2022-08-31 (Version 1)
- Basin and station details:
  - 5 Ciliwung stations (Ciliwungxxx)
  - 33 Citarum stations (Citarumxxx or tributaries)
- Data used to derive parameter values were not optimized against KGE' beyond the random search; the best of 100k random sets is stored

## How to use and supporting data exploration
- Self-service potential:
  - Compare model performance across different climate inputs (precipitation and evap sources) and catchments
  - Explore how parameter values vary by model and data source
- Data integration:
  - Combine across the 24 model files to perform cross-model sensitivity analyses
  - Use the 7×3×38 combination space (Precip × Evap × Catchment) as a canonical index for replicability
- Data quality and governance:
  - Ensure consistent handling of units and parameter naming across models
  - Consider creating a unified data dictionary mapping model-specific parameter names to standardized terms
  - Be mindful that parameter values were selected from random search, not from direct optimization against KGE' for all cases

## Limitations and caveats
- Parameter values were chosen from random 100k samples, not derived from a uniform objective optimization per se
- The number of additional numeric parameter columns varies per file (2 to 15), and units differ by model
- Spin-up period (first three years) intentionally ignored in KGE' calculation
- Text labels for the first three columns are fixed in content; ensure consistent interpretation when merging files

## Access, references, and related materials
- Data references include classic hydrological model sources and the MARRMoT toolbox documentation
- Key climatology datasets cited for precipitation inputs: AgMERRA, CHIRPS, CPC, MSWEP, PERSIANN-CDR, SA-OBS, Yanto
- Additional model parameter descriptions and cross-model references available in the associated literature (Moore 2007; Knoben et al. 2019) and the referenced datasets
- The dataset is part of a project on understanding hydrometeorological hazards in Southeast Asia

References:
- Climate forcing datasets and precipitation datasets (listed within the dataset metadata)
- Model documentation and MARRMoT toolbox references
- Project funding and contributor affiliations as noted in the dataset record