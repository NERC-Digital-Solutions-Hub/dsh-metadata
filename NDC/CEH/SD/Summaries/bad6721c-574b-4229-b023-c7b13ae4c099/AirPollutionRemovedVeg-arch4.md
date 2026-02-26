# This dataset provide a 2015 UK annual average surface concentration, and annual total deposition; for a selection of pollutants as calculated by an atmospheric chemistry transport model.

## Overview
- Provides 2015 UK annual average surface concentrations and annual total deposition for selected pollutants, calculated with the EMEP4UK atmospheric chemistry transport model (ACTM).
- Domain and resolution: EU domain at 0.5° × 0.5° with a nested UK domain at ~0.055° × 0.055° (about 5 × 6 km2); only UK-domain results are included.
- Temporal framing: Outputs cover 2015, with NetCDF time stamps corresponding to the end of model runs (01/01/2015 to 01/01/2016).
- Outputs include both concentrations and dry/wet deposition fields for multiple species (e.g., PM2.5, PM10, NO2, O3, NH3, SO2) and near-surface concentrations.

## Experimental design and data sources
- Model framework:
  - EMEP4UK model versions rv4.10 and rv4.17, derived from EMEP MSC-W.
  - Meteorology: WRF v3.7.1 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1° × 1° every 6 hours.
- Emissions inputs:
  - UK emissions (NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, NMVOC) from NAEI (2014 for rv4.10, 2015 for rv4.17).
  - Non-UK emissions from CEIP (v2016 for 2014, v2017 for 2015).
  - Shipping: FMI 2011 emissions adjusted to NMVOC and PM using specified scaling.
- Recorded outputs: Hourly to annual averages and depositions, with units defined in the NetCDF files.

## Experiments setup (six scenarios)
- 1) UKBASE: UK current vegetation; land-cover LCM2007; soil NO emissions landcover-dependent; EMEP rv4.10.
- 2) NoVEG: UK no vegetation; same model settings as 1.
- 3) UrbanBASE: Urban current vegetation; EMEP rv4.17; land-cover LCM2015; soil NO prescribed.
- 4) NoUrbanVEG: No urban vegetation; EMEP rv4.17; land-cover NoUrbanVEG; soil NO prescribed.
- 5) 25OGSC: Urban 25% open greenspace conversion; EMEP rv4.17; land-cover 25GLC; soil NO prescribed.
- 6) 50OGSC: Urban 50% open greenspace conversion; EMEP rv4.17; land-cover 50GLC; soil NO prescribed.

## Data files (NetCDF)
- current_vegetation_land.nc
- no_vegetation_land.nc
- urban_current_vegetation_prescri.nc
- no_urban_vegetation_prescr.nc
- 25OGSC_open_greenspace_prescri.nc
- 50OGSC_open_greenspace_prescri.nc

## Model hardware and software
- Code compiled with the Intel FORTRAN compiler (2013_sp1.3.174).
- Computations run on the UKCEH NEMSIS computing cluster.

## Variables, units, and data structure
- Recorded variables include:
  - PM2.5 and PM10 (aerosol concentrations and compositions).
  - Near-surface ozone, nitrogen dioxide, ammonia, and other pollutants.
  - Dry and wet deposition fluxes for multiple species (e.g., DDEP_NH3_m2Grid, DDEP_NO2_m2Grid, WDEP_NO2, WDEP_PM10ONS, etc.).
- PM definitions:
  - PM2.5: aerodynamic diameter < 2.5 µm.
  - PM10: aerodynamic diameter < 10 µm (includes PM2.5 and coarse fractions).
- NetCDF metadata:
  - Time stamps mark the end of the model runs.
  - Variable names and units are provided within the NetCDF files (e.g., DDEP_NH3_m2Grid; SURF_ppb_O3).
- Example structure snippet provided for one variable (DDEP_NH3_m2Grid) illustrating metadata like numberofrecords and current_date_last.

## Quality control and limitations
- Model validation:
  - Hourly outputs compared against AURN monitoring network (for the UK) and UK Met Office AWS (for WRF) using simple linear regression.
- QA/QC: Limited to basic regression comparisons; no extended QA/QC performed; users assume responsibility for suitability to their purposes.

## Data provenance and governance (for Data Leaders)
- Provenance:
  - Dataset integrates multiple established models and inventories (EMEP4UK ACTM, EMEP MSC-W, WRF meteorology with nudging, NAEI, CEIP, FMI shipping emissions).
  - Clear versioning across rv4.10 and rv4.17, with corresponding land-cover and vegetation scenarios.
- Reproducibility:
  - Detailed experimental configurations per scenario (model versions, land-cover, soil NO emissions, years, and vegetation settings) enable repeatability.
  - Filenames and scenario mappings anchor data to specific model runs.
- Data management and discoverability:
  - Outputs are provided as NetCDF files with explicit variable names and units, supporting discoverability and programmatic access.
  - Documentation links to foundational references for model descriptions and data sources.
- Limitations and caveats:
  - QA is limited to simple observational comparisons; no formal uncertainty quantification is provided.
  - Shipping emissions and NMVOC/PM scaling are based on specific assumptions, which should be reviewed when applying results to new use cases.

## References
- Jalkanen, J. P., Johansson, L., & Kukkonen, J. (2016). A comprehensive inventory of ship traffic exhaust emissions in the European sea areas in 2011.
- Jones, L. et al. (2019). Urban natural capital accounts: developing a novel approach to quantify air pollution removal by vegetation.
- Nemitz, E. et al. (2020). Potential and limitation of air pollution mitigation by vegetation and uncertainties of deposition-based evaluations.
- Saha, S. et al. (2011). NCEP Climate Forecast System Version 2 (CFSv2) six-hourly products.
- Simpson, D. et al. (2012). The EMEP MSC-W chemical transport model – technical description.
- Skamarock, W. C. et al. (2019). A Description of the Advanced Research WRF Version 4.
- Vieno, M. et al. (2016). The sensitivities of emissions reductions for the mitigation of UK PM2.5.