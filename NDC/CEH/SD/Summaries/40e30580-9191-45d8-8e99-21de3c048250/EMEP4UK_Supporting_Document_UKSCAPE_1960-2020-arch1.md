# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (1960 - 2020)

## Overview
- Provides daily averaged atmospheric composition for the UK (1960–2020) focusing on main nitrogen, sulfur, particulate matter, and ozone.
- Generated with EMEP4UK model version rv5.0 and Weather Research and Forecasting (WRF) model version 4.4.2.

## Data content and coverage
- Outputs daily averaged atmospheric composition and fluxes for the UK as part of the UK-SCAPE project.
- Model domain: European Union domain at 27 × 27 km2 with a nested UK domain at 3 × 3 km2; only UK domain results are provided.
- Variables include surface concentrations for a wide range of species and metrics, such as:
  - PM2.5 (including water content and NH4+, sulfates, nitrates, organics, sea salt, mineral dust, and primary PM2.5 components)
  - PMcoarse and PM10 (PM2.5 + water content)
  - Ozone metrics (mean daily maximum)
  - Mixing layer height (HMIX)
  - Near-surface concentrations for gases and aerosols (e.g., NOx, NO, NO2, NH3, HNO3, CO, HCHO, O3, SO2, various organic and inorganic aerosols, dust components, black carbon, elemental carbon)
- Units and NetCDF variable naming: detailed mapping of surface concentrations to NetCDF variables (e.g., SURF_ug_PM25_rh50, SURF_ppb_O3, SURF_ppb_NO2, SURF_ug_DUST, etc.). PM2.5 definition combines multiple components and assumes 50% relative humidity for water content.

## Data sources and emissions
- UK anthropogenic emissions: National Atmospheric Emission Inventory (NAEI) for a specific year.
- Non-UK emissions: CEIP 0.1° × 0.1° gridded data; UK total used for 1960–2020.
- Daily averaged EMEP4UK outputs are provided, reflecting emissions and atmospheric chemistry transport modelling.

## Modelling framework and computation
- ACTM foundation: EMEP4UK rv5.0, derived from EMEP MSC-W rv5.0.
- Meteorology: 3D meteorology from WRF v4.4.2 with data assimilation (Newtonian nudging) of ERA5 reanalysis (0.25° × 0.25° every 6 hours).
- Grid and projection: data projected on a polar stereographic grid; proj4 string provided for use in applications.
- Computation and software: FORTRAN Intel compiler 19.1.3.304; calculations performed on the UKCEH POLAR cluster (CentOS 7.9).

## Data structure and access
- Data format: NetCDF files; dataset contains surface concentrations and related fluxes.
- Example provided for SURF_ug_PM25_rh50; extensive variable naming conventions described for reproducibility and interoperability.
- Guidance notes indicate compatibility with NetCDF libraries in R, Python, and FORTRAN.

## Quality, limitations, and caveats
- QA/QC conducted for 1960–2020; QA/QC reports available on request but not included in the document.
- Use of the dataset is at the user’s risk; no warranty or guarantee of error-free content or fitness for purpose.
- Documentation acknowledges potential variability in dataset details and the need to refer to metadata for specific variable definitions.

## Guidance for use
- Users should be aware of the polar stereographic grid and the specific proj4 string when integrating into applications.
- Ensure appropriate NetCDF libraries and data handling capabilities in R, Python, or FORTRAN to interpret the dataset correctly.
- Reference the provided bibliography for methodological context and validation studies related to the EMEP MSC-W and UK-SCAPE modelling.

## Bibliography
- Ge, Y. et al. (2021). Evaluation of global EMEP MSC-W and WRF models against measurements.
- Gu, B. et al. (2021). Ammonia abatement costs and PM2.5 mitigation.
- Jalkanen, J.P. et al. (2016). Ship traffic emissions inventory.
- NCEP/NOAA and ERA5-related data sources and model integrations.
- Simpson, D. et al. (2012); Vieno, M. et al. (2016a, 2016b); Skamarock, W.C. et al. (2019); Vieno et al. (2016) related to model architecture and applications.