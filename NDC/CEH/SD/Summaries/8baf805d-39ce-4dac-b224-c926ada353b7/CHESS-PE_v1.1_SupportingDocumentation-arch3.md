# The Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2015) [CHESS-PE]

- Overview
  - Provides two daily potential evapotranspiration (PET) estimates on a 1 km grid over Great Britain for 1961–2015.
  - Derived from CHESS-met meteorological variables and CEH-GEAR precipitation; two estimates cover the same time and space.

- Data products
  - PET: Penman-Monteith potential evapotranspiration for a well-watered grass surface (mm/day).
  - PETI: PET with interception correction (mm/day); accounts for rainfall interception by canopy, with interception drying during the day and rainfall-added transpiration when rainfall occurs.

- Input data
  - PET inputs (ta, qa, downward longwave and shortwave radiation, p*) from CHESS-met.
  - PETI inputs include all PET inputs plus CEH-GEAR precipitation, scaled to appropriate units.

- PET and PETI concepts
  - PET: Atmospheric evaporative demand under a standard surface assumption (well-watered grass), representing an upper limit to evaporation.
  - PETI: Adjusts PET to reflect canopy interception of rainfall, using an interception store with exponential dry-down to modify daily evaporation.

- Calculation details
  - PET, E_P, calculated via the Penman-Monteith equation.
  - Key parameters include latent heat (λ), Δ (slope of saturated humidity deficit), γ (psychrometric constant), r_s (stomatal resistance), r_a (aerodynamic resistance), A (available energy), c_p (air specific heat), ρ_a (air density), t_d (day length in seconds).
  - Assumes a constant stomatal resistance of 70 s m^-1 for PET calculations on a well-watered grass surface.
  - PETI uses the same core equation and adds an interception component E_I on wet days, with an exponential dry-down to yield PETI.
  - Full derivation and parameters are detailed in Robinson et al. (in review); references include Allen et al. (1998) for FAO standard.

- File format and access
  - Data distributed in netCDF format (CF-compliant) following CEH gridded dataset conventions.
  - Data stored as monthly files; one file per variable (PET and PETI).

- Practical considerations for monitoring frameworks
  - Data provenance: clearly documented meteorological inputs and the Pet/Mont equation basis support traceability for policy evaluation.
  - Metadata and openness: CF-compliant format; publication in scientific references; potential data sharing is aligned with openness goals described for monitoring frameworks.
  - Data governance: methodology relies on standardized inputs (CHESS-met, CEH-GEAR) and explicit assumptions (well-watered grass surface, fixed stomatal resistance) to ensure consistency across assessments.
  - Applicability: suitable for hydrological and ecological policy evaluation and scenario modelling where atmospheric evaporative demand is a key driver.

- Limitations and considerations for policy use
  - PET assumes a well-watered grass surface; real-world surfaces may differ, influencing applicability to certain policy contexts.
  - PETI accounts for canopy interception on wet days; model sensitivity to interception parameters should be considered.
  - Data coverage limited to 1961–2015 and to Great Britain at 1 km resolution; users should assess temporal and spatial relevance for current monitoring needs.
  - Interoperability depends on the availability of metadata and alignment with project-specific data governance requirements.

- References
  - Allen, R. G., Pereira, L. S., Raes, D., and Smith, M. (FAO Guidelines 1998)
  - Keller, V. D. J., et al. CEH-GEAR (2015)
  - Monteith, J. L. (1965)
  - Robinson, E. L., et al. CHESS-met (2015)
  - Robinson, E. L., et al. (in review, 2016)
  - Tanguy, M., et al. CEH-GEAR dataset (2016)