# Potential evapotranspiration derived from the UK Climate Projections 2018 Regional Climate Model ensemble 1980-2080 (Hydro-PE UKCP18 RCM) Supporting information

- Purpose and scope
  - Gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) on a 12 km UK grid for 1980-2080 under RCP8.5.
  - Dataset derived from UKCP18 Regional Projections (RCM) v20190731 and designed for hydrological modelling; PETI aligned with MORECS v2.0 observations where appropriate.

- Data content and variables
  - Two variables: PET (kg m-2 d-1; equivalent to mm d-1) and PETI (kg m-2 d-1).
  - PET calculated with Penman-Monteith for a well-watered grass surface.
  - PETI adds interception correction on days with precipitation; on days with zero precipitation PETI = PET.

- Input data and calculation framework
  - Input: UKCP18 RCM regional projections on a 12 km grid (1980-2080), v20190731; perturbed parameter ensemble under RCP8.5.
  - Variables used (daily means): specific humidity at 1.5 m, sea-level pressure, net shortwave and longwave radiation, 10 m wind, air temperature at 1.5 m.
  - PETI uses daily precipitation and other ancillary data from the climate model simulations (e.g., surface altitude, CO2 concentrations, land-sea mask).
  - Calculations performed for each ensemble member; CO2-driven stomatal resistance adjustments implemented (Kruijt 2008) to reflect plant response to higher CO2.

- Penman-Monteith methodology and consistency
  - PET computed as a function of humidity, radiation, wind, temperature, and derived atmospheric properties (air density, saturation humidity, resistances).
  - Parameter choices and formulations aligned with MORECS v2.0 documentation to ensure consistency with historical PET.

- Interception correction details
  - PETI on days with precipitation uses interception water (CI) and canopy evaporation (E_I) to adjust PET; CI increases in spring/summer/autumn to reflect multiple daily events.
  - Interception-based adjustment follows MORECS v2.0 methodology; precipitation is treated as rainfall in this context.

- Land-sea mask handling and grid filling
  - Calculations conducted only for grid boxes modelled as land; sea boxes with land fractions are filled by copying PET/PETI from the nearest land grid box to support hydrological modelling need for higher-resolution downstream processes.

- File format, structure, and naming
  - Format: NetCDF adhering to CF Metadata Conventions v1.8 and ACDD v1-3.
  - Organization: decadal files, one per variable per ensemble member.
  - File naming convention: hydro-pe_ukcp18_rcm_rcp85_<ENS>_<VARN>_uk_12km_daily_<Y1>1201<Y2>1130.nc
  - Ensemble member identifiers: two-digit codes (e.g., 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, or 15).
  - Variables: pet or peti; VARN notes indicate the two variables present.

- Spatial information
  - Grid: 12 km resolution on the British National Grid (BNG); projection EPSG:27700.
  - Coordinates provided in both BNG (eastings/northings) and WGS84 (lat/lon) for compatibility.

- Temporal information
  - Time coverage: daily mean values from 1980-12-01 to 2080-11-30.
  - Calendar: artificial 360-day year (12 months × 30 days); seasonal statistics facilitated by calendar alignment.
  - Caution: 360-day calendar may require care when comparing with datasets using Gregorian or 365-day calendars.

- Data quality, limitations, and caveats
  - ArcGIS reading caveat: CF-compliant files with non-standard projected coordinate systems can offset display by ~10–100 m; adjustment may be needed for proper alignment.
  - Domain limitation: only land grid boxes are computed; sea boxes filled by interpolation from nearby land boxes rather than re-computing from sea meteorology.

- Provenance, governance, and reuse
  - Provenance: derived from UKCP18 RCM ensemble (HadGEM3-GC3.05) with CO2-driven vegetation adjustments; aligned to MORECS v2.0 for historical consistency.
  - Governance and files are organized to support reproducibility, with explicit references to processing steps and underlying sources.
  - Acknowledgement: supported by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.

- References and documentation
  - Key references include UKCP18 data sources, MORECS v2.0, HadGEM3-GC3.05 ensemble studies, and related science reports and methodological papers.
  - Detailed methodological and data lineage documentation provided to support appropriate data usage and interpretation.

- Acknowledgements
  - Recognised support from NERC and the Hydro-JULES programme.