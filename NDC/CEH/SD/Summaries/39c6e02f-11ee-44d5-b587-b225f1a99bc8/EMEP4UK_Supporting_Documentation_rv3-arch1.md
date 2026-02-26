# Experimental design/Sampling regime

- Purpose and scope
  - EMEP4UK is an atmospheric chemistry transport model (ACTM) coupled with the Weather Research and Forecasting model (WRF) to simulate hourly to annual average atmospheric composition and deposition of pollutants; daily averaged data are provided.

- Emissions and domain
  - Two emission types: anthropogenic and natural.
  - UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, primary PM10, CO, NMVOCs) from the National Atmospheric Emission Inventory (NAEI) at 1 km x 1 km, aggregated to 5 km x 5 km for the UK domain.
  - European domain emissions from EMEP CEIP at 50 km x 50 km resolution.
  - International shipping emissions (ENTEC) aggregated to 5 km x 5 km within the British Isles domain.
  - Forest fires included; biogenic emissions (isoprene, monoterpenes) calculated in-model per grid-cell and at every time-step based on near-surface air temperature.

- Model environment and compilation
  - Models used: WRF and EMEP4UK, compiled with the Intel FORTRAN compiler (2013_sp1.3.174).
  - Computations run on the CEH computer cluster NEMSIS.

- Variables and units
  - Surface concentration variables recorded in NetCDF files, including:
    - Nitric oxide (NO), NO2, PM10, PM2.5, NH3, HNO3, SO2, NH4, TNO3, SO4, Particulate Organic Matter (POM_F), Ozone (O3).
  - Units: micrograms per cubic meter (µg/m3) for most species; O3 in ppbv.
  - NetCDF variable names for some key species: SURF_ug_NO, SURF_ug_NO2, SURF_ug_PM10, SURF_ug_PM2.5, SURF_ug_NH3, SURF_ug_HNO3, SURF_ug_SO2, SURF_ug_NH4_F, SURF_ug_TNO3, SURF_ug_SO4, SURF_ug_PART_OM_F, SURF_ppb_O3.

- Data quality control
  - Observational verification using:
    - AURN monitoring network for hourly model output comparison.
    - UK Met Office AWS data for WRF output verification.
  - Method: simple linear regression between observations and model values.
  - Note: No further QA/QC beyond this; content is provided at user’s risk (no warranty of fitness).

- NetCDF data structure details
  - Example: EMEP4UK_UK_webrun_emep_4.3_2001_day.nc
  - Dimensions:
    - time (days of data), i (x-coordinate), j (y-coordinate)
  - Variables:
    - time: units "days since 1900-01-01 0:0:0"
    - i: GeoX coordinate (units: km)
    - j: GeoY coordinate (units: km)
    - SURF_ug_SO2 (time, j, i): surface SO2 concentration
    - grid_mapping: Polar_Stereographic with associated parameters
  - Metadata indicators include current_date_first and current_date_last for the data period.
  - Dataset carries a cautionary note about potential data limitations and is accompanied by garbled documentation in places.

- Versioning, scope, and data availability notes
  - Forest-fire data present only for 2002–2012.
  - Emissions for 2013–2014 identical to 2012 values.
  - WRF model versions vary by period: 2001–2012 uses WRF 3.1.1; 2013–2014 uses WRF 3.6.1 with humidity nudging removed from reanalysis.
  - Reference: Final report available via the provided Defra link (retrieved 2016-04-20).