# Potential evapotranspiration derived from the UK Climate Projections 2018 Regional Climate Model ensemble 1980-2080 (Hydro-PE UKCP18 RCM) Supporting information

## Overview
- Datasets of gridded daily total potential evapotranspiration (PET) and PET with interception correction (PETI) at 12 km resolution for the UK, covering 1980–2080 under RCP8.5.
- PET derived via Penman-Monteith for well-watered grass; PETI includes interception correction on days with precipitation.
- Designed to support hydrological modelling and to align with MORECS v2.0 historic PET calculations where applicable.

## Data products (variables)
- PET: daily total potential evapotranspiration (kg m-2 d-1; equivalent to mm d-1).
- PETI: daily PET with interception correction (kg m-2 d-1).
- Both computed for each ensemble member in the UKCP18 RCM output.

## Input data and sources
- UKCP18 Regional Projections on a 12 km grid over the UK, 1980–2080, v20190731; RCP8.5 perturbation ensemble.
- Core variables (daily mean):
  - Specific humidity at 1.5 m (qa)
  - Sea level pressure (psl)
  - Net surface shortwave flux (rss; Sn)
  - Net surface longwave flux (rls; Ln)
  - Wind speed at 10 m (sfcWind; u10)
  - Air temperature at 1.5 m (tas)
- PETI uses precipitation rate (pr) in addition to the above.
- Ancillary data: surface altitude, atmospheric CO2 concentrations, land-sea mask.
- Calculations account for surface altitude adjustments to surface pressure (p* in Pa) from sea level pressure.

## Methods and calculations
- PET: computed with the Penman-Monteith equation for a well-watered grass surface; uses daily mean inputs and derived quantities (saturation humidity, air density, total net radiation, aerodynamic resistance, stomatal resistance, etc.).
- CO2 effects: stomatal resistance increases with rising CO2 to simulate stomatal closure.
- PETI: interception correction on days with non-zero precipitation; water intercepted by canopy reduces PET relative to PET, following MORECS v2.0 methods; short-term enhanced interception adjustments during spring–autumn with multiple daily precipitation events.
- Parameterisation aligns with MORECS v2.0 documentation to maintain consistency with historical PET data.

## Land-sea mask handling
- Calculations apply only to land grid boxes. For sea-grid boxes that contain land fractions, PET and PETI are filled by copying from the nearest comparable land grid box to enable hydrological modelling at higher resolutions.

## File format, structure and naming
- Format: netCDF conforming to CF Metadata Conventions v1.8 and ACDD v1-3.
- Temporal structure: daily mean values; time range 1980-12-01 to 2080-11-30 with a 360-day calendar (12 months × 30 days).
- Spatial structure: 12 km British National Grid (BNG; EPSG:27700); WGS84 (EPSG:4326) coordinates provided for reference.
- File organization: decadal files; one file per ensemble member and per variable (PET or PETI) per decade.
- Naming convention (example):
  hydro-pe_ukcp18_rcm_rcp85_[ENS]_[VARN]_uk_12km_daily_[Y1]1201[Y2]1130.nc
  - ENS: ensemble member (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15)
  - VARN: pet or peti
  - Y1–Y2: start and end years of the file (e.g., 1980–1990)

## Spatial and temporal specifics
- Spatial: 12 km grid aligned to the British National Grid (BNG); projection EPSG:27700; WGS84 coordinates also provided.
- Time: daily means from 1980-12-01 to 2080-11-30; calendar is 360-day (12 × 30) to match the underlying climate model’s calendar.

## Data quality, caveats and notes
- ArcGIS reading caveat: projected-coordinate CF files may offset display by 10–100 m due to datum assumptions; adjust layers as needed.
- Temporal calendar: 360-day year; comparisons with Gregorian/365-day datasets require calendar conversion.
- Calculations are ensemble-meanized per member; reflect uncertainty in CO2 trajectories within RCP8.5.

## Usage and applications
- Intended for hydrological modelling and as input to hydrological tools requiring PET/PETI.
- PET alignments with MORECS v2.0 documentation ensure historical consistency and comparability.
- Provides a provenance-rich, 12 km UK-wide PET dataset across a long future horizon (1980–2080).

## Data governance and provenance
- Version: v20190731; ensemble-based perturbations capturing uncertainty in future emissions.
- Acknowledgements: supported by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.

## References and further information
- Methodological and data references for PM equation, MORECS v2.0, UKCP18 data, and related parameters and datasets are provided in the supporting references section of the document.