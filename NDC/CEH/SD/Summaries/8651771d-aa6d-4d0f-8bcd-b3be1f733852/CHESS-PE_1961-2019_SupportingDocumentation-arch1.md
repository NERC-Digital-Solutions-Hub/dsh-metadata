# The Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2019) [CHESS-PE]

- Provides two estimates of daily potential evapotranspiration on a 1 km resolution grid over Great Britain
- Covers 1961-2019, extended to include 2018-19; updates netCDF metadata for all years
- Supersedes the previous CHESS-PE version (Robinson et al., 2020)

## What the dataset includes

- PET (mm/day): Penman–Monteith potential evapotranspiration for a well-watered grass surface
- PETI (mm/day): PET with interception correction, combining interception and transpiration, accounting for canopy interception after rainfall
- Identical spatial extent and temporal coverage for both PET and PETI
- Data derived from CHESS-met meteorology (Ta, qa, downward longwave and shortwave radiation, p*) and CEH-GEAR precipitation for PETI

## Data sources and inputs

- PET: calculated from CHESS-met variables including:
  - Air temperature (Ta)
  - Specific humidity (qa)
  - Downward longwave radiation (Ld) and shortwave radiation (Sd)
  - Surface air pressure (p*)
- PETI: uses all above plus CHESS-met precipitation (CEH-GEAR precipitation scaled to appropriate units)
- CHESS-met provides the meteorological basis; CEH-GEAR provides rainfall input for interception correction

## How PET and PETI are calculated

- PET (E_P): computed with the Penman–Monteith equation for a well-watered grass surface (r_s = 70 s m^-1)
- PETI (E_PI): uses the same Penman–Monteith calculation for potential transpiration, plus interception terms:
  - On wet days, an interception store is computed with E_I, assuming zero stomatal resistance to estimate interception
  - PETI combines interception loss and transpiration with an exponential dry-down of the interception store:
    - E_PI = E_P with interception-adjusted terms; S0 is the initial interception store; S_tot is the interception capacity

- The dataset follows FAO standards for crop evapotranspiration (well-watered grass reference) and represents atmospheric evaporative demand

## Data format and organization

- File format: netCDF (CF-compliant) following CEH gridded dataset conventions
- Organization: monthly files; one file per variable
- Metadata: updated in this release for all years

## Data availability and practical use

- Hosted by the Environmental Information Data Centre
- Download link: https://catalogue.ceh.ac.uk/documents/8651771d-aa6d-4d0f-8bcd-b3be1f733852
- Intended for hydrological modelling, climate-water demand assessments, and other applications requiring high-resolution estimates of atmospheric evaporative demand over Great Britain

## Known issues

- ArcGIS reading of CF-compliant files with projected coordinate systems can offset layers by 10–100 m due to datum assumptions (WGS 1984 vs. the dataset’s reference datum)
- Users may need to adjust layer positions using standard ArcGIS tools; refer to ArcGIS documentation for handling datum differences

## References and background

- FAO Guidelines for computing crop water requirements (Allen et al., 1998)
- CEH-GEAR: gridded rainfall estimates for the UK (Keller et al., 2015; Tanguy et al., 2021)
- Penman–Monteith methodology (Monteith, 1965)
- CHESS-met meteorology dataset (Robinson et al., 2023)
- CHESS-PE dataset descriptions and validations (Robinson et al., 2023)