# Supporting documentation for air pollution removed by vegetation in the UK 2015

- Purpose of the dataset
  - Provides 2015 UK annual average surface concentration and annual total deposition for a selection of pollutants, as simulated by an atmospheric chemistry transport model (ACTM).

- Modelling framework and domain
  - Models used: EMEP4UK (rv4.10 and rv4.17) derived from EMEP MSC-W; atmospheric chemistry transported outputs from hourly to annual scales.
  - Meteorology: Weather Research and Forecasting (WRF) model v3.7.1 with data assimilation of NCEP/NCAR GFS reanalysis at 1° every 6 hours.
  - Domain and resolution: EU domain at 0.5°×0.5° with a nested UK domain at ~0.055°×0.055° (about 5×6 km2); UK results are reported.
  - Emissions data: UK emissions (NOx, NH3, SO2, PM2.5, PMcoarse, CO, NMVOC) from NAEI (year 2014 for rv4.10, 2015 for rv4.17); non-UK emissions from CEIP (0.5° grid; v2016 for 2014, v2017 for 2015); shipping emissions from FMI with NMVOC and PM adjustments.

- Experimental design and scenarios
  - Six experiments (Table 1):
    - 1) UKBASE: UK current vegetation; Land-cover LCM2007; soil NO emissions ~vegetation.
    - 2) NoVEG: UK no vegetation; same model settings as 1.
    - 3) UrbanBASE: Urban current vegetation; Land-cover LCM2015; soil NO emissions prescribed.
    - 4) NoUrbanVEG: No urban vegetation; land-cover NoUrbanVEG; prescribed soil NO.
    - 5) 25OGSC: Urban vegetation with 25% greenspace opening; land-cover 25GLC; prescribed soil NO.
    - 6) 50OGSC: Urban vegetation with 50% greenspace opening; land-cover 50GLC; prescribed soil NO.
  - Common model configuration: WRF v3.7.1, EMEP v4.10 (for scenarios 1–2) or v4.17 (scenarios 3–6).

- Data products and file naming
  - NetCDF outputs corresponding to each scenario:
    - current_vegetation_land.nc
    - no_vegetation_land.nc
    - urban_current_vegetation_prescri.nc
    - no_urban_vegetation_prescr.nc
    - 25OGSC_open_greenspace_prescri.nc
    - 50OGSC_open_greenspace_prescri.nc
  - Time coverage: 2015 year (results ending 01/01/2016).

- Model outputs and variables
  - Types: surface concentrations and deposition fluxes.
  - Depositions (area-weighted):
    - DDEP_NH3_m2Grid (dry deposition of ammonia)
    - DDEP_NO2_m2Grid (dry deposition of nitrogen dioxide)
    - DDEP_O3_m2Grid (dry deposition of ozone)
    - DDEP_PM10ONS_m2Grid (PM10 without wind-blown dust)
    - DDEP_PM25ONS_m2Grid (PM2.5 without wind-blown dust)
  - Near-surface concentrations:
    - SURF_ppb_O3 (ozone)
    - SURF_ug_NH3 (ammonia)
    - SURF_ug_NO2 (nitrogen dioxide)
    - SURF_ug_PM10ONS (PM10)
    - SURF_ug_PM25ONS (PM2.5)
    - SURF_ug_DUST_WB_C (wind-blown coarse dust)
    - SURF_ug_DUST_WB_F (wind-blown fine dust)
  - Other referenced species include SO2, NO2, and related deposition/concentration metrics; time stamp is end of model runs (01/01/2015 to 01/01/2016).

- Data quality and validation
  - Validation against observations:
    - AURN monitoring network used to verify hourly EMEP4UK outputs.
    - UK Met Office AWS used to verify WRF outputs.
    - Simple linear regression used to compare model vs. observations for base runs and experiments.
  - QA/QC note: No further QA/QC beyond the described validation; content is provided with a caveat of risk and no warranty of fitness for a particular use.

- Metadata, structure, and accessibility
  - NetCDF data structures described with variable names and units; example provided for DDEP_NH3_m2Grid metadata.
  - Emphasis on clear naming conventions, units, and time stamping to facilitate reuse and cross-study comparisons.
  - Public sharing of underlying data is implied through documentation, but the QA note indicates users proceed at their own risk.

- References and background
  - Jalkanen et al. 2016; Jones et al. 2019; Nemitz et al. 2020; Saha et al. 2011; Simpson et al. 2012; Skamarock et al. 2019; Vieno et al. 2016.
  - Supporting documentation related to air pollution removed by vegetation in the UK 2015 (as cited in references).