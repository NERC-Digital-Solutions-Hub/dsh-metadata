# Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2019) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration (PET) estimates on a 1 km resolution grid over Great Britain for 1961–2019.
- Based on CHESS-met meteorological variables and CEH-GEAR precipitation; two PET implementations:
  - PET: Penman–Monteith PET for a well-watered grass surface.
  - PETI: PET with interception correction (accounts for rainfall interception by canopy on wet days).
- This release supersedes the previous version (2020) by extending data to 2018–2019 and updating metadata.

## Data and calculation
- Input data:
  - PET: from CHESS-met variables: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*).
  - PETI: uses the same inputs plus CEH-GEAR precipitation (scaled to appropriate units).
- PET calculation:
  - Uses Penman–Monteith equation for a grass surface; assumes a constant stomatal resistance of 70 s m⁻¹; results in daily PET (mm/day).
- PETI calculation:
  - Uses the same PET equation plus a modeled interception store that captures rainfall interception; includes exponential dry-down of interception with parameters S0 (initial store) and Stot (total capacity).
  - On wet days, interception adds to PET according to the interception dynamics.
- Data characteristics:
  - Daily PET and PETI values on a 1 km grid; both variables cover identical time and space extents.
  - Monthly CF-compliant netCDF files; CEH gridded dataset conventions.

## Data format and access
- File format: netCDF, CF-compliant, following CEH conventions.
- File structure: monthly files; one netCDF file per variable (PET or PETI) per month.
- Data availability: hosted by the Environmental Information Data Centre (EIDC); downloadable from the CEH catalogue website.

## Data governance, provenance, and metadata
- Grounded in foundational methods and datasets:
  - Core references include Robinson et al. (2017, 2020), FAO guidelines, and related CEH-GEAR and CHESS datasets.
  - Formal metadata updated alongside the 2018–2019 extension.
- Documentation enables traceability of inputs, calculation steps, and assumptions (e.g., grass surface type, stomatal resistance).

## Known issues and caveats
- ArcGIS coordinate-reading issue:
  - CF-compliant files with projected coordinate systems may misalign due to the datum assumption (WGS 1984) in ArcGIS.
  - Offset can be 10–100 meters; can be corrected using ArcGIS tools per user documentation.
- Users should verify coordinate alignment when integrating with other GIS layers.

## Usage considerations and applications
- Suitable for hydrological and ecological modelling requiring atmospheric evaporative demand estimates.
- PETI is particularly relevant for models that account for canopy interception and rainfall partitioning.
- Provides a consistent, high-resolution dataset for long-term analyses (1961–2019, extended to 2018–19).

## Versioning and updates
- CHESS-PE (1961–2019) with 2018–19 extension; metadata refreshed accordingly.
- Represents the most up-to-date PET and PETI products within this dataset lineage.

## References
- Allen et al. (1998). FAO guidelines for crop evapotranspiration.
- Keller et al. (2015). CEH-GEAR precipitation dataset.
- Monteith (1965). Penman–Monteith framework.
- Robinson et al. (2017, 2020). CHESS-met and CHESS-PE datasets; related hydrological analyses.
- Tanguy et al. (2021). CEH-GEAR gridded rainfall estimates.