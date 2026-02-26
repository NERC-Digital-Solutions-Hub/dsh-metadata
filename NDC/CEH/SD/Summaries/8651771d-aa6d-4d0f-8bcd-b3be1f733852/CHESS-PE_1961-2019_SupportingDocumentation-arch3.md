# The Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2019) [CHESS-PE]

- Overview
  - Provides two daily potential evapotranspiration (PET) estimates on a 1 km resolution grid over Great Britain.
  - Time extent 1961–2019; supersedes the previous version by extending years to 2018–19 and updating metadata.
  - Data are delivered as CF-compliant netCDF files, aligned with CEH gridded dataset conventions.

- Data products
  - PET: Penman–Monteith potential evapotranspiration for a well-watered grass surface (mm/day).
  - PETI: PET with interception correction; on days with rainfall, interception stores reduce transpiration, and the daily PETI accounts for interception and transpiration components.

- Calculation and methodology
  - PET (E_P): Calculated using the Penman–Monteith equation from CHESS-met inputs (air temperature, specific humidity, downward radiation, surface pressure).
  - PETI: Uses the same equation plus a model for interception, with an exponential dry-down of the interception store (S0) against total capacity (Stot). On wet days, interception is computed with zero stomatal resistance; PETI combines interception and transpiration terms.
  - Assumptions: well-watered grass surface with a constant stomatal resistance of 70 s m⁻¹ for PET; PETI adjusts for canopy interception after rainfall.

- Input data
  - PET: Derived from CHESS-met meteorological variables (Ta, qa, Ld, Sd, p*).
  - PETI: In addition to CHESS-met variables, uses CEH-GEAR precipitation (scaled to appropriate units).

- File format and structure
  - NetCDF files, CF-compliant, following CEH gridded dataset conventions.
  - Monthly files, with separate files for each variable.

- Data availability and access
  - Hosted by the Environmental Information Data Centre (EIDC).
  - Available for download via the CEH catalogue link provided in the documentation.

- Known issues and caveats
  - ArcGIS reading issues for CF-compliant files with projected coordinate systems due to datum assumptions (WGS84). This can cause an offset of about 10–100 m; layers can be adjusted using ArcGIS tools.

- Usage and applications
  - Provides evaporative demand estimates useful for hydrological modelling and environmental monitoring.
  - Supports policy evaluation and decision-making by enabling assessment of atmospheric evaporative demand across Great Britain.

- Updates and references
  - This release extends CHESS-PE to 2018–19 and updates netCDF metadata.
  - Key references include FAO guidelines (Allen et al. 1998), CEH-GEAR (Keller et al. 2015; Tanguy et al. 2021), CHESS-met (Robinson et al. 2023), CHESS-PE (Robinson et al. 2023), and Monteith (1965).