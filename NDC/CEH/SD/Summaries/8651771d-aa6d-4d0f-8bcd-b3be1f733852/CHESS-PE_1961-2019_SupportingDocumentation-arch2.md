# Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2019) [CHESS-PE]

## Overview
- CHESS-PE provides two daily potential evapotranspiration (PET) estimates on a 1 km resolution grid for Great Britain, covering 1961–2019.
- Derived from CHESS-met meteorological variables and CEH-GEAR precipitation; supersedes the 2020 CHESS-PE release and extends years to 2018–2019 with updated metadata.

## What is included
- PET (mm/day): Penman-Monteith PET assuming a well-watered grass surface (FAO standard).
- PETI (mm/day): PET with interception correction, accounting for rainfall interception by the canopy and subsequent transpiration when the interception store dries during the day.

## Data sources and inputs
- PET inputs: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), and surface air pressure (p*), from CHESS-met.
- PETI inputs: all PET inputs plus CHESS-met precipitation (CEH-GEAR precipitation) scaled to appropriate units.

## Calculation and methodology
- PET: computed via the Penman-Monteith equation for a well-watered grass surface; assumes stomatal resistance of 70 s m⁻¹.
- PETI: uses the same PET calculation plus interception terms. Interception is modelled with an initial store S0 and capacity Stot, and uses an exponential dry-down to transition from interception to transpiration. On wet days, interception is computed with zero stomatal resistance; total PETI combines interception E_I with transpiration E_P.
- All calculations follow established references (e.g., FAO guidelines; Robinson et al. 2017).

## Format, access and availability
- Data format: netCDF, CF-compliant, CEH gridded dataset conventions.
- Structure: monthly files; one file per variable (PET and PETI).
- Availability: hosted by the Environmental Information Data Centre (EIDC); download details provided by CEH catalog.

## Version history
- CHESS-PE is a revised release that extends the dataset to 2018–2019 and updates metadata; supersedes the previous CHESS-PE version (Robinson et al., 2020).

## Known issues
- ArcGIS CF-reading limitations with projected coordinate systems: the geographic datum is assumed to be WGS84, causing an offset (~10–100 m). Layers can be realigned using ArcGIS tools per documentation.

## Data handling and quality
- Data are verified, quality-assured, and transformed from the underlying CHESS-met and CEH-GEAR sources.
- Datasets are stored and uploaded to the appropriate data portals to support broad accessibility and reuse.

## References
- FAO guidelines for crop evapotranspiration (Allen et al., 1998)
- CEH-GEAR precipitation dataset (Keller et al., 2015; Tanguy et al., 2021)
- Penman-Monteith methodology (Monteith, 1965)
- CHESS-meteorology and CHESS-PE development and usage (Robinson et al., 2017, 2018, 2020, 2023)