# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2002 - 2021)

## Summary
- Provides daily averaged atmospheric composition for the UK (2002–2021) focusing on main nitrogen and sulfur species, particulate matter (PM2.5, PMcoarse, PM10), organic matter, ozone, and related tracers.
- Generated with EMEP4UK model rv4.36, an atmospheric chemistry transport model (ACTM) derived from EMEP MSC-W rv4.36, driven by WRF v4.2.2 meteorology.
- Domain: EU 27 × 27 km2 with a nested UK domain at 3 × 3 km2; UK results extracted for UK-wide analysis.
- Meteorology: 3D fields from WRF with data assimilation (Newtonian nudging) using NCEP/NCAR GFS reanalysis at 1° × 1° every 6 hours.
- Emissions: UK NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC from 2019 NAEI; CEIP 0.1° × 0.1° non-UK emissions; 2020–2021 use 2019 UK emissions.
- Data format: NetCDF with detailed species, units, and grid definitions; polar stereographic projection specified; requires NetCDF-compatible libraries (R, Python, FORTRAN).
- Quality: QA/QC conducted (not included in document); content usage risk rests with user; no warranty on error-free results.
- Supporting references and provenance provided for model descriptions and related evaluations.

## Experimental design / Sampling regime
- Model: EMEP4UK rv4.36 ACTM; based on EMEP MSC-W rv4.36, simulating hourly to annual atmospheric composition and deposition.
- Meteorology: WRF v4.2.2 with Newtonian nudging of NWP reanalysis from GFS/NCEP/NCAR at 1° × 1° resolution, updated every 6 hours.
- Domain and resolution: EU domain at 27 × 27 km2 with nested UK domain at 3 × 3 km2; UK results extracted for UK-scale analyses.
- Emissions and inputs: UK emissions from 2019 NAEI, downscaled to 2002–2019; non-UK emissions from CEIP; 2020–2021 emissions set to 2019 UK totals.
- Outputs: Daily averaged atmospheric composition and fluxes for specified species.

## Nature and units of recorded values
- Fine PM (PM2.5): aerodynamic diameter < 2.5 µm.
- Coarse PM (PMcoarse): aerodynamic diameter 2.5–10 µm.
- PM10: PM2.5 + PMcoarse.
- PM2.5 definition: combines various components including sulfate, nitrate (fine and coarse), ammonium, sea salt, mineral dust, secondary organics, and primary PM2.5; plus specific coarse NO3 from coarse fraction and water at 50% RH.
- Variables (examples of NetCDF naming): SURF_ug_PM25_rh50, SURF_ug_PM10_rh50, SURF_ppb_O3, HMIX, SURF_ug_DUST, SURF_ug_ECCOARSE, SURF_ug_ECFINE, SURF_ug_NH3, SURF_ug_NO2, SURF_ug_NO, SURF_ug_NO3_F, SURF_ug_NO3_C, SURF_ug_PM_ASOA, SURF_ug_PM_BSOA, SURF_ug_PM_OM25, SURF_ug_PM_PMFINE, SURF_ug_SEASALT_F, SURF_ug_SO2, SURF_ug_SO4, etc.
- Units: micrograms per cubic meter (µg m-3) for particulates and many trace species; parts per billion by volume (ppbv) for near-surface ozone; meters for mixing height (HMIX); all NetCDF headers specify units.
- Projection: polar stereographic grid; proj4 string provided for usage within mapping/GIS tools.

## NetCDF data structure and accessibility
- Data structure: NetCDF files containing multiple species with a clear naming convention for surface and coarse/fine components; includes near-surface concentrations and related tracers.
- Example snippet: an example 2001 output for SURF_ug_PM25_rh50 is provided, illustrating the NetCDF organization and variable naming.
- Documentation: Guidance notes accompany data on projection, grid, and CRS; NetCDF compatibility with common scientific software (R, Python, FORTRAN) is stated.

## Guidance for using the data
- Projections and CRS: Data described on a polar stereographic grid; use provided proj4 string for correct CRS integration.
- Software requirements: A NetCDF library is required; compatible with R, Python, and FORTRAN environments.
- Practical usage: Suitable for model evaluation, trend analysis, and scenario assessments related to UK air quality and pollutant deposition; can be combined with emissions and meteorology datasets for attribution studies.
- Data accessibility: Quality assurance reports exist but are available on request; no embedded warranty in the dataset content.

## Quality Assurance and caveats
- QA/QC: Performed for 2002–2021; reports available on request (not included in this document).
- Limitations: Use of 2019 UK emissions for 2020–2021; model-derived outputs rather than direct measurements; content usage risk is borne by the user.
- Documentation gaps: An example data snippet in the document appears to be incomplete or placeholder; users may need to verify NetCDF structures in actual files.

## Data provenance and software environment
- Model compilation: FORTRAN Intel compiler 19.1.3.304 (20200925).
- Computing environment: UKCEH POLAR cluster (CentOS Linux 7.9.2009) used for computations.
- References for model components and validation provided in bibliography.

## Bibliography
- Ge, Y., Heal, M. R., Stevenson, D. S., Wind, P., and Vieno, M. (2021). Evaluation of global EMEP MSCW (rv4.34) WRF (v3.9.1.1) model surface concentrations and wet deposition of reactive N and S with measurements. Geosci. Model Dev., 14, 7021-7046.
- Gu, B., et al. (2021). Abating ammonia is more cost-effective than nitrogen oxides for mitigating PM2.5 air pollution. Science, 374, 758-762.
- Jalkanen, J.P., Johansson, L., and Kukkonen, J. (2016). A comprehensive inventory of ship traffic exhaust emissions in the European sea areas in 2011. Atmos. Chem. Phys., 16, 71-84.
- National Centers For Environmental Prediction / NOAA / NCAR (2000). NCEP FNL Operational Model Global Tropospheric Analyses.
- Simpson, D., et al. (2012). The EMEP MSC-W chemical transport model technical description. Atmos. Chem. Phys., 12, 7825-7865.
- Skamarock, W.C., et al. (2019). A Description of the Advanced Research WRF Model Version 4.
- Vieno, M., et al. (2016a, 2016b). The sensitivities of emissions reductions for the mitigation of UK PM2.5; The UK PM2.5 episode of March-April 2014. Atmos. Chem. Phys. / Environmental Research Letters.