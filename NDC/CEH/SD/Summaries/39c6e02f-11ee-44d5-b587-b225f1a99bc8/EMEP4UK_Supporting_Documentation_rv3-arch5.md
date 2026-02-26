# Experimental design/Sampling regime

- The EMEP4UK model is an atmospheric chemistry transport model (ACTM) that simulates hourly to annual atmospheric composition and deposition; daily averaged data are included here, alongside the Weather Research and Forecasting model (WRF).
- Two emissions types are modelled: anthropogenic and natural, with spatial resolutions tailored by region.

## Data scope, emissions, and resolutions

- UK emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC) are from the National Atmospheric Emission Inventory (NAEI) at 1 km x 1 km, aggregated to 5 km x 5 km for the model.
- European domain emissions use EMEP CEIP data at 50 km x 50 km.
- International shipping emissions (ENTEC, 2010i) are aggregated to 5 km x 5 km within the British Isles.
- Forest fires are included; biogenic emissions (isoprene, monoterpenes when required) are computed per grid cell and time-step using near-surface temperature.
- Model output focuses on daily averaged data.

## Model compilation, environment, and data generation

- Fortran-based model compilation using the Intel FORTRAN compiler (2013_sp1.3.174).
- Computations run on the CEH computer cluster NEMSIS (Linux nemesis 2.6.32-431.29.2.el6.x86_64).
- Time coverage and data granularity cover hourly to daily to annual scales with daily averaged outputs emphasized.

## Nature and units of recorded values

- Data stored in NetCDF files; variables represent surface concentrations for pollutants including:
  - Nitric oxide (NO), NO2, PM10, PM2.5, NH3, HNO3, SO2, NH4, NO3, SO4, Particulate Organic Matter (POM) for <2.5 μm, O3, and related species.
- Units are specified per variable (e.g., SURF_ug_NO for NO in μg/m3; SURF_ppb_O3 for O3 in ppbv).
- Variable names follow standardized NetCDF conventions (e.g., SURF_ug_PM2.5, SURF_ug_SO2) with clear metadata including long_name and units.

## Quality control and validation

- Model output is validated against observations using the AURN monitoring network (hourly data) and UK Met Office AWS for WRF outputs.
- Validation method is simple linear regression analysis between observations and model values.
- No additional QA/QC beyond the described validation; dataset use is explicitly at the user’s risk with no warranty of fitness for purpose.

## Data structure and documentation

- NetCDF data structure example provided for SO2 (EMEP4UK_UK_webrun_emep_4.3_2001_day.nc) with:
  - Dimensions: time (days), j (270), i (220)
  - Coordinates: time, i (GeoX), j (GeoY)
  - Variables: SURF_ug_SO2 (dimensions: time, j, i) and associated metadata
  - Grid mapping: Polar_Stereographic with explicit projection parameters
  - Time coordinates expressed as days since 1900-01-01; metadata includes current_date_first/last and grid mapping details
- Dataset includes standard attributes describing grid, coordinates, and data mapping to geographic space.

## Supporting documentation and notes

- Supporting documentation for the EMEP4UK modelled daily atmospheric composition is included, with notes on data versions and model configurations.
- Important notes:
  - Forest fire data are included only for 2002–2012.
  - Emissions for 2013–2014 reuse 2012 values.
  - 2001–2012 use WRF version 3.1.1; 2013–2014 use WRF version 3.6.1 due to changes in specific humidity nudging.
- References and external documentation are cited (e.g., Final Report 291110, retrieved 2016-04-20).

## Data governance, availability, and responsibilities

- The dataset is prepared with clear provenance, processing steps, and variable definitions to support discoverability and reuse.
- Data are intended to be uploaded to relevant portals and catalogued within data holdings.
- Users should note the model-specific assumptions, emissions sources, and versioning changes over time when performing longitudinal analyses.