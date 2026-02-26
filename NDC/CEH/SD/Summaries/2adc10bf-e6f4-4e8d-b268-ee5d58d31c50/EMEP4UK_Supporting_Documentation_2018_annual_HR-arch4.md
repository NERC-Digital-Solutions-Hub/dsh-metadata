# High resolution European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface resistance based atmospheric deposition for the UK for 2018.
- Generated with EMEP4UK model version rv4.36 (an atmospheric chemistry transport model) and WRF model version 4.1.1 for meteorology.
- Model domain covers the EU at 27×27 km2 with a nested UK domain at 1×1 km2; only UK domain results are included.
- Outputs include dry deposition and related surface concentrations for oxidised and reduced nitrogen and sulphur species.

## Experimental design and input data
- ACTM: EMEP4UK rv4.36, derived from EMEP MSC-W rv4.36; simulates hourly to annual atmospheric composition and deposition.
- Meteorology: 3D WRF v4.1.1 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1°×1° resolution every 6 hours.
- Emissions: UK emissions (NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, NMVOC) from NAEI 2019, rescaled to 2018; non-UK emissions from CEIP 0.1° data (UK total used for 2018).
- Output scope: annual total model data for 2018.

## Model details and provenance
- Model compiler and environment: FORTRAN Intel compiler 19.1.3.304; calculations run on the UKCEH POLAR cluster.
- Model lineage: WRF and EMEP4UK are peer-reviewed models with extensive use in the scientific community.
- Documentation and references: extensive bibliography provided for model descriptions and related emissions/attribution studies.

## Data products and units
- Types of data: surface concentration and deposition values for various species and deposition pathways (e.g., dry deposition of oxidised sulphur and nitrogen, reduced nitrogen, etc.).
- Example variables and units: 
  - Area grid, in km2 (Area_Grid_km2).
  - Dry deposition of oxidised sulphur (DDEP_SOX_m2Grid, etc.) in mgS/m2.
  - Dry deposition of oxidised nitrogen (DDEP_OXN_m2Grid, etc.) in mgN/m2.
  - Dry deposition of reduced nitrogen (DDEP_RDN_m2Grid, etc.) in mgN/m2.
- NetCDF data structure and variable naming follow explicit conventions (e.g., DDEP_* variables) with detailed per-pathway naming for different land-cover targets (coniferous forest, semi-natural, water, deciduous forest, crops).
- Guidance notes indicate how data are projected and what metadata are provided in the NetCDF files.

## Data structure and access
- Data format: NetCDF files (example provided for 2018 output, DDEP_SOX_m2Grid).
- Spatial grid: UK nested within EU grid; domain defined by i and j indices (i = 765, j = 1254 in the example).
- Coordinates and axes: time (unlimited), i (EMEP grid x), j (EMEP grid y), lon(j,i), lat(j,i) metadata provided.
- Projection: polar stereographic projection; proj4 string provided for use in applications.
- Software compatibility: NetCDF library required; compatible with R, Python, FORTRAN, etc.

## Quality assurance and limitations
- QA/QC: performed for 2018 with checks on input data (emissions totals vs. inventories) and model output (visual mapping, time series, and standard statistics).
- Reports: QA/QC reports available on request.
- Limitations: model content is provided with no warranty or guarantee of being error-free or fit for a specific purpose; users assume risk of use.
- Validation context: model describes and evaluates against observations as part of standard QA, but the document notes reliance on prior peer-reviewed work.

## Usage guidance and constraints
- Projection and data usage: datasets are described in a specified proj4 string; users should configure their applications accordingly.
- Data access notes: requires NetCDF libraries and appropriate computational tools (R, Python, FORTRAN) to read and process the data.
- Reproducibility: model provenance (versions, compilers, and computational environment) is provided to support reproducibility.

## References and provenance
- Key references detailing model descriptions, emissions inventories, and related methodology, including:
  - Simpson et al. 2012; Vieno et al. 2016a, 2016b (EMEP4UK rt4.36)
  - Skamarock et al. 2019 (WRF v4)
  - NAEI 2022 and CEIP emissions data
  - Ge et al. 2021; Gu et al. 2021; Jalkanen et al. 2016
  - Additional supporting documentation on model evaluation and environmental management studies