# The Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2015) [CHESS-PE]

- Overview
  - Provides two daily potential evapotranspiration (PET) estimates on a 1 km resolution grid over Great Britain for 1961–2015.
  - Outputs two variables with the same time and space coverage: PET and PETI.

- Datasets and Variables
  - PET: Penman–Monteith PET for a well-watered grass surface (mm/day).
  - PETI: PET with interception correction (mm/day); accounts for rainfall interception by the canopy, adding interception dynamics to PET on wet days and allowing interception to dry down over time.

- Input Data and Provenance
  - PET inputs: CHESS-met meteorological variables – air temperature (ta), specific humidity (qa), downward longwave (Ld) and shortwave (Sd) radiation, surface air pressure (p*).
  - PETI inputs: all PET inputs plus CHESS-met precipitation from CEH-GEAR (UK rainfall estimates).
  - Assumes a grass surface with a constant stomatal resistance (rs) of 70 s m⁻¹ for PET calculation.

- Calculation and Methodology
  - PET is computed using the Penman–Monteith equation (FAO-standard context) for a well-watered grass surface.
  - PETI uses the same PET as the transpiration component and adds interception interception EI on wet days, modeled with an interception store (S0) and capacity (Stot) and an exponential dry-down for the total interception effect.
  - Full calculation details and parameter choices are described in Robinson et al. (in review).

- File Format and Access
  - Data are distributed as CF-compliant netCDF files following CEH gridded dataset conventions.
  - Monthly files are provided for each variable, enabling organized time-series access.

- Spatial and Temporal Coverage
  - Geography: Great Britain (1 km grid).
  - Temporal: 1961–2015, daily values, with monthly netCDF organization.

- Uses and Applications
  - Designed for hydrological and land-surface modelling, enabling analysis of atmospheric evaporative demand and its variation over time.
  - Useful for model validation, data assimilation, and studies requiring high-resolution PET/PETI inputs on a national scale.

- Notes and References
  - Outputs rely on CHESS-met meteorology and CEH-GEAR precipitation data; full methodological details available in Robinson et al. (in review) and associated references (e.g., Allen et al.; Keller et al.; Monteith).
  - Key references: FAO guidelines (for PET standard), CHESS-met dataset details, CEH-GEAR precipitation, and related methodology papers.