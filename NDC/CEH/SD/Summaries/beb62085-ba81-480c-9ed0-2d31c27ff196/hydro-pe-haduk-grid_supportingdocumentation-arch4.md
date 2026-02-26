# (Hydro-PE HadUK-Grid) Supporting information

## Overview
- Describes gridded potential evapotranspiration (PET) and PET with interception correction (PETI) at 1 km resolution across the UK for 1969–2022.
- PET and PETI derived from the HadUK-Grid meteorological dataset, with PET calculated via Penman-Monteith for a well-watered grass surface; PETI includes canopy interception corrections on days with precipitation.
- Latest version adds 2022 data; includes fixes for previously identified missing data and minor bugs.
- Outputs are intended for hydrological modelling and are designed to be consistent with MORECS v2.0.

## Data and variables
- Spatial and temporal coverage:
  - 1 km grid aligned to the British National Grid (BNG), EPSG:27700; also provides lat/long in WGS84 (EPSG:4326).
  - Daily mean values from 1969-01-01 to 2022-12-31.
- Core variables:
  - PET: daily total potential evapotranspiration (kg m⁻² d⁻¹).
  - PETI: PET with interception correction (kg m⁻² d⁻¹).
- Input data and sources:
  - HadUK-Grid dataset v1.x (v1.0.3.0 for 1969–2020; v1.1.0.0 for 2021; v1.2.0 for 2022).
  - Required inputs for PET: monthly mean vapour pressure, sea level pressure, sunshine hours, daily wind speed at 10 m, daily max/min temperatures; image-specific daily or monthly data interpolated to daily.
  - For PETI: all PET inputs plus daily precipitation; ancillary data include surface altitude and Ångström coefficients.
- Time handling:
  - Monthly data are quadratic-interpolated to daily, with monthly timestamps assumed to be the 15th of each month.
  - Daily interpolation is designed to maintain continuity when new years are added to the HadUK-Grid base.

## Calculation approach
- PET calculation:
  - Penman-Monteith equation parameterised for a well-watered grass surface.
  - Daily mean temperature derived from tasmax and tasmin; other variables interpolated to daily values.
  - Several inputs (e.g., net radiation, aerodynamic resistance, surface temperature) derived from HadUK-Grid variables and MORECS v2.0 methodologies for consistency.
- PETI calculation:
  - On days with precipitation, canopy interception (CI) is estimated and intercepted water evaporates more quickly than transpiration.
  - PETI accounts for interception rate and canopy drying dynamics; on days with no precipitation, PETI equals PET.
- Interception correction details:
  - CI depends on precipitation and leaf area index; enhanced in spring/summer/autumn to reflect multiple daily events.
  - Water evaporation rate from interception (EI) is computed under open-water assumptions and used to adjust PETI until canopy dries, after which PETI reverts toward PET.

## Interpolation and data integrity
- Quadratic interpolation to daily values introduces occasional unphysical negatives (pv, sun) or zero wind speeds; safeguards:
  - pv and sun set to 0 when negative; sfcWind set to the minimum non-zero daily value.
- Continuity across data updates:
  - To avoid re-computing earlier days when new years are added, the last year of existing daily data is combined with the new monthly data and interpolated separately, preserving history while ensuring contiguity with new data (end-of-old-timeseries extrapolated, then new data continues).

## File format and data discovery
- File format:
  - NetCDF files, CF Metadata Conventions v1.8 and ACDD v1-3.
  - Data stored as monthly files per variable; daily values are exposed through the dataset.
- Spatial and temporal metadata:
  - 1 km grid aligned to the British National Grid (EPSG:27700); WGS84 lat/long included.
  - Daily mean values from 1969-01-01 to 2022-12-31; monthly variables timestamped mid-month for interpolation.
- Data access notes:
  - ArcGIS reading caveat: projected coordinate systems may offset display by 10–100 m due to datum assumptions (WGS84) when reading non-WGS84 projections; adjust layers as needed.

## Data governance and lifecycle
- Versioning and updates:
  - Hydro-PE HadUK-Grid updates append new years; interpolation is performed on the extended series to maintain consistency with older data.
  - Documentation notes that 1969–2020 data are consistent across v1.0.3.0, v1.1.0.0, and v1.2.0; 2021 and 2022 have specific updates and fixes.
- Quality and limitations:
  - Some minor bugs in PETI previously caused a few NaNs or incorrect values; corrections implemented with minor impact.
  - Data gaps mitigated by interpolation; users should be aware of early-time extrapolation at the ends of the series.
- Applicability:
  - Primarily intended for hydrological modelling and analysis requiring UK-wide PET/PETI estimates at 1 km resolution; designed to be compatible with MORECS-based parameterisations.

## Acknowledgements and references
- Supported by Natural Environment Research Council grants as part of the Hydro-JULES programme.
- Key references include MORECS v2.0 methodology, HadUK-Grid development, and related radiation and evaporation literature.