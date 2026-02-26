# Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2017) [CHESS-PE]

## Purpose and scope
- Provides two daily potential evapotranspiration (PET) estimates on a 1 km grid over Great Britain for 1961–2017.
- Based on CHESS-met meteorological variables and CEH-GEAR precipitation; enables assessment of atmospheric evaporative demand for environmental monitoring and policy scrutiny.

## Data and inputs
- PET: Penman-Monteith PET for a well-watered grass surface (mm/day).
- PETI: PET with interception correction; accounts for rainfall interception and canopy storage, adjusting transpiration as interception stores dry.
- Input drivers:
  - CHESS-met: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*).
  - CEH-GEAR precipitation used for PETI.

## Variables and interpretation
- PET: theoretical maximum evapotranspiration under ample soil moisture.
- PETI: PET adjusted for rainfall interception and canopy interception storage dynamics.

## Calculation methodology
- PET (E_P): computed via the Penman-Monteith equation, assuming grass with a fixed stomatal resistance (70 s m⁻¹), following FAO guidelines.
- PETI (E_PI): uses the same equation for potential transpiration, plus:
  - E_I: potential interception on wet days (stomatal resistance set to zero).
  - PETI = E_PI with an exponential dry-down of the interception store (S0) to S_tot, incorporating rainfall interception dynamics.

## Release history and improvements
- This release supersedes the 2016 version (Robinson et al., 2016) due to:
  - Extension to include 2016–2017 data.
  - Updated netCDF metadata for all years.
  - Bug fixes:
    - PET: humidity deficit (qs - qa) limited to a minimum of zero; affects ~4% of data. Mean PET increases ~0.001 mm/day (0.1%), with larger differences at some times/locations.
    - PETI: previous overestimation of interception correction corrected; affects ~63% of data; overall PETI decreases by ~0.02 mm/day (1.5%), with winter reductions ~4% and summer ~1%.

## File format and data access
- File format: netCDF, CF-compliant, CEH gridded dataset conventions.
- Organization: monthly files, one file per variable.
- Data hosting: Environmental Information Data Centre.
- Access: available for download at the CEH catalogue (link provided in documentation).

## Known issues
- ArcGIS reading of CF-compliant files with projected coordinate systems may offset layers by ~10–100 m due to default WGS84 datum handling; adjust layers using ArcGIS tools as needed.

## Practical usage for environmental monitoring
- Enables consistent, standardized assessment of atmospheric evaporative demand over time and space.
- Suitable for hydrological and ecological modelling, trend analysis, and policy evaluation where PET and PETI are required inputs or diagnostic metrics.
- Ensures reproducibility through documented data provenance (CHESS-met, CEH-GEAR) and transparent version updates.

## References
- FAO guidelines on crop evapotranspiration (Allen et al., 1998).
- CEH-GEAR precipitation dataset (Keller et al., 2015; Tanguy et al., 2019).
- CHESS-met and CHESS-PE datasets and related publications (Robinson et al., 2017; Robinson et al., 2016; Robinson et al., 2020).