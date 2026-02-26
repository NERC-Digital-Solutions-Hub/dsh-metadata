# Supporting documentation for air pollution removed by vegetation in the UK 2015

- Purpose: Provides 2015 UK annual average surface concentration and annual total deposition for selected pollutants, calculated by an atmospheric chemistry transport model (EMEP4UK).
- Scope: UK-domain model outputs (0.055° x 0.055° nested domain within a 0.5° x 0.5° EU-wide domain) covering hourly to annual averages and deposition for multiple pollutants.

## Experimental design and data sources

- Models and setup:
  - EMEP4UK model versions rv4.10 and rv4.17, derived from EMEP MSC-W.
  - Weather forcing: WRF v3.7.1 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1° x 1° every 6 hours.
  - Domain: EU-wide 0.5° x 0.5° with a UK nest (~5 x 6 km2).
  - Emissions:
    - UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOCs) from NAEI (2014 for rv4.10, 2015 for rv4.17).
    - Non-UK emissions from CEIP (0.5° x 0.5°, v2016 for 2014 and v2017 for 2015).
    - Shipping emissions from FMI (2011) with NMVOC and PM adjustments applied.
- Timeframe: Annual results for 2015; end-of-model-run timestamp corresponds to 2015-01-01 to 2016-01-01.

## Experiments and scenarios

- Six scenarios (Table 1):
  1) UKBASE: current vegetation, LCM2007, soil NO emissions land-cover dependent (RV4.10).
  2) NoVEG: no vegetation, LCM2007, soil NO emissions land-cover dependent.
  3) UrbanBASE: urban current vegetation, rv4.17, LCM2015, prescribed soil NO emissions.
  4) NoUrbanVEG: no urban vegetation, rv4.17, LCM2015, prescribed soil NO emissions.
  5) 25OGSC: urban vegetation with 25% open greenspace conversion, rv4.17, LCM 25GLC, prescribed soil NO emissions.
  6) 50OGSC: urban vegetation with 50% open greenspace conversion, rv4.17, LCM 50GLC, prescribed soil NO emissions.
- File naming corresponds to each scenario:
  - current_vegetation_land.nc
  - no_vegetation_land.nc
  - urban_current_vegetation_prescri.nc
  - no_urban_vegetation_prescr.nc
  - 25OGSC_open_greenspace_prescri.nc
  - 50OGSC_open_greenspace_prescri.nc

## Data products: contents and units

- Primary outputs:
  - Surface concentrations and near-surface pollutant levels (various species).
  - Deposition: dry deposition of NH3, NO2, O3; PM10 and PM2.5 (without wind-blown dust).
  - Time reference: end-of-model-run timestamps for each file correspond to 2015-01-01.
- Key NetCDF variable definitions (examples):
  - DDEP_NH3_m2Grid: dry deposition of ammonia (area-weighted, mg N m^-2).
  - DDEP_NO2_m2Grid: dry deposition of nitrogen dioxide (area-weighted, mg N m^-2).
  - DDEP_O3_m2Grid: dry deposition of ozone (area-weighted, mg m^-2).
  - DDEP_PM10ONS_m2Grid: dry deposition of PM10 (area-weighted, mg m^-2).
  - DDEP_PM25ONS_m2Grid: dry deposition of PM2.5 (area-weighted, mg m^-2).
  - SURF_ppb_O3: near-surface ozone concentration (ppb).
  - SURF_ug_PM10ONS: near-surface PM10 concentration (µg m^-3).
  - SURF_ug_PM25ONS: near-surface PM2.5 concentration (µg m^-3).
  - SURF_ug_NH3: near-surface ammonia (µg m^-3).
- Units and definitions:
  - PM2.5: aerodynamic diameter < 2.5 µm; PMcoarse: 2.5–10 µm.
  - PM2.5 ONS and PM10 ONS definitions include specific components (e.g., sea salt, mineral dust, secondary organic aerosols) as detailed in the document.
- Documentation and metadata:
  - NetCDF variable names are provided in the dataset metadata.
  - Example metadata for 2015 output for DDEP_NH3_m2Grid includes number of records and last updated date.

## Model validation and quality control

- Validation:
  - Model outputs are compared to observed data from the AURN monitoring network (hourly outputs) and UK Met Office AWS for WRF outputs using simple linear regression.
- QA/QC note:
  - No additional QA/QC beyond these comparisons; use of content is at user’s risk.
  - The document explicitly states no warranty that content is error-free or fit for any particular use.

## Technical and access details

- Model compiler and computing environment:
  - FORTRAN Intel compiler 2013_sp1.3.174.
  - Computations performed on the UKCEH NEMSIS computing cluster.
- Data format and structure:
  - Outputs are provided as NetCDF files with 2015 data for the specified scenarios.
- References:
  - Key literature related to EMEP4UK, WRF/NWP assimilation, and vegetation-related air quality analyses are cited (e.g., Jones et al., Nemitz et al., Saha et al., Simpson et al., Skamarock et al., Vieno et al.).