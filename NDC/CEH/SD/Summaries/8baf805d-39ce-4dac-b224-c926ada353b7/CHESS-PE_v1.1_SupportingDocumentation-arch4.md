# Introduction The Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2015) [CHESS-PE] provides two estimates of daily potential evapotranspiration on a 1 km resolution grid over Great Britain.

- Summary of purpose and coverage
  - Provides two daily potential evapotranspiration estimates (PET and PETI) on a 1 km grid for Great Britain, spanning 1961–2015.
  - Derived from the CHESS-met meteorological dataset and CEH-GEAR precipitation data for PETI.
  - Two variables cover the same time period and spatial extent.

- Variables and definitions
  - PET (mm/day): Penman-Monteith potential evapotranspiration computed for a well-watered grass surface (FAO standard).
  - PETI (mm/day): PET with interception correction to account for rainfall interception by canopy; on wet days interception reduces transpiration, with an interception store that dries during the day.
  - Interception model: PETI splits into interception evaporation (E_I) and transpiration, with an exponential dry-down of the interception store (parameters S0 and Sot).
  - PET assumes a constant stomatal resistance of 70 s/m and uses a well-watered grass surface assumption.

- Calculation and methodology
  - PET: computed using the Penman-Monteith equation from meteorological inputs (Ta, qa, downward longwave and shortwave radiation, surface pressure).
  - PETI: uses the same Penman-Monteith framework but adds rainfall interception dynamics; wet-day interception is calculated with zero stomatal resistance, and total PETI combines interception and transpiration with the exponential dry-down formulation.
  - Key constants and parameters referenced include latent heat of vaporization, psychrometric constant, and surface/air properties; calculation follows Robinson et al. (in review) with the CHESS-met input assumptions.

- Input data and data sources
  - PET inputs: CHESS-met variables (air temperature Ta, specific humidity qa, downward longwave radiation Ld, downward shortwave radiation Sd, surface air pressure p*).
  - PETI inputs: All PET inputs plus CHESS-met precipitation from CEH-GEAR (scaled to appropriate units).
  - Coverage and units: daily values at 1 km resolution over Great Britain; PET and PETI are provided in mm/day.

- File format and data access
  - File format: netCDF, CF-compliant, following CEH gridded dataset conventions.
  - Organization: monthly files, with one file per variable.
  - Provenance and references: detailed methodology and data provenance described; full calculation details available in Robinson et al. (in review); key references include FAO guidelines and CEH data papers.

- Relevance and potential uses for Data Leaders
  - Provides standardized evaporative demand metrics for hydrological and ecological modelling, enabling consistent assessment of atmospheric demand across GB.
  - Facilitates data-driven planning and analysis for water resources, land surface modelling, and climate-risk assessment.
  - Clear data lineage: CHESS-met and CEH-GEAR inputs, with CF-compliant, well-documented netCDF outputs and monthly aggregation for manageability.
  - Supports reproducibility and quality control through detailed methodological references and established dataset conventions.

- Practical notes for implementation
  - PETI adds complexity by incorporating canopy interception dynamics; useful for models sensitive to rainfall interception effects.
  - The dataset emphasizes a standard grass surface assumption for PET, aligning with FAO guidelines, which is important for cross-study comparability.
  - Availability is tied to CHESS and CEH data streams; users should consider metadata and data discovery practices to locate the relevant monthly netCDF files.