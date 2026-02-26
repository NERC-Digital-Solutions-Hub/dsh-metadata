# Supporting information

- The Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2019) [CHESS-PE] provides two estimates of daily potential evapotranspiration on a 1 km resolution grid over Great Britain.
- The release extends the data to include 2018-19 and updates netCDF metadata; supersedes the previous version (Robinson et al., 2020).

## Dataset scope and purpose (Data Steward perspective)
- Two PET products for the same time and space domain:
  - PET: Penman-Monteith potential evapotranspiration for a well-watered grass surface (mm/day).
  - PETI: PET with interception correction (mm/day), accounting for canopy interception on rainfall days.
- Designed to support hydrological and ecological modeling by providing atmospheric evaporative demand at high spatial resolution.

## Data sources and inputs
- PET inputs: CHESS-met meteorological variables — air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*).
- PETI inputs: All of the above plus CHESS-met precipitation from CEH-GEAR (scaled to appropriate units).

## Variables and interpretation
- PET: Upper limit of evaporation under grass-surface assumptions (well-watered), using the Penman-Monteith equation.
- PETI: PET adjusted for canopy interception effects; includes interception storage and its dry-down dynamics; on wet days, potential interception is calculated with a zero stomatal resistance to represent canopy evaporation.

## Calculation methodology
- PET (E_P): Computed via the Penman-Monteith equation with a constant stomatal resistance (70 s m⁻¹) and standard atmospheric parameters.
- PETI (E_PI): Uses the same equation for potential transpiration (E_P) plus an interception term (E_I) that accounts for rainfall interception and its exponential decline over time.
- The approach follows FAO/Allen et al. guidelines (well-watered grass reference surface).

## File format and data organization
- Data delivered as CF-compliant netCDF files following CEH gridded dataset conventions.
- Monthly data files, with one file per variable (PET and PETI).

## Data availability and governance
- Hosted and stored by the Environmental Information Data Centre (EIDC).
- Accessible via the CEH catalogue: https://catalogue.ceh.ac.uk/documents/8651771d-aa6d-4d0f-8bcd-b3be1f733852
- This dataset is designed for long-term discoverability and reuse, with updated metadata to reflect the extended temporal coverage (1961-2019, including 2018-19).

## Known issues and considerations
- Reading CF-compliant files with projected coordinate systems in ArcGIS can offset layer positioning due to datum assumptions (WGS 1984). For CHESS-PE, adjust layers using ArcGIS tools to correct for datum difference.

## References and context
- FAO/Allen et al. (1998) on crop evapotranspiration guidelines.
- CEH-GEAR precipitation dataset (Keller et al., 2015; Tanguy et al., 2021).
- CHESS-met meteorology data (Robinson et al., 2023).
- CHESS-PE dataset documentation (Robinson et al., 2023); related methodological and validation studies (Robinson et al., 2017).