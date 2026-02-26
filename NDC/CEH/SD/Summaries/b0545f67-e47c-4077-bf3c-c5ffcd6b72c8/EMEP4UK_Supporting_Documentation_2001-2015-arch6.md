# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2001 - 2015)

## Overview
- Provides daily averaged atmospheric composition and fluxes for the UK for 2001–2015, focusing on main nitrogen, sulfur, particulate organic matter, and ozone.
- Generated with the EMEP4UK rv4.17 atmospheric chemistry transport model (ACTM) and the Weather Research and Forecasting (WRF) model v3.7.1.

## Modeling and domain
- Domain: EU domain at 0.5° × 0.5° with a nested UK domain at ~5 × 6 km (0.05° × 0.055°). Only UK-domain results are included.
- Meteorology: WRF 3.7.1 with data assimilation of NCEP/NCAR GFS reanalysis (1° × 1°, every 6 hours).
- Emissions and chemistry: UK emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC) from 2015 NAEI, rescaled to 2001–2015; non-UK emissions from EMEP CEIP (0.5°) with UK total used for 2001–2015; emissions for 2001–2014 rescaled accordingly. Shipping emissions for 2011 from FMI with NMVOC and PM adjustments applied.

## Emissions data
- UK 2015 NAEI-based emissions scaled to each year 2001–2015.
- Non-UK emissions from CEIP EMEP, with year-specific UK total scaling for 2001–2015 (v2015 for 2001–2013, v2016 for 2014, v2017 for 2015).
- FMI shipping emissions used for 2011; adjustments to NMVOC and PM fractions applied as NMVOC = 0.029 × NOx, PM2.5 = 0.95 × PM, PMcoarse = 0.05 × PM.

## Data content and units
- Daily averaged outputs include surface concentrations and deposition/fluxes for nitrogen, sulfur, particulate matter and ozone; definitions include PM2.5 ( aerodynamic diameter < 2.5 μm), PMcoarse (2.5–10 μm), and PM10 (PM2.5 + PMcoarse).
- NetCDF variable names cover a wide range of species and processes (e.g., DDEP_HNO3_m2Conif, DDEP_NO2_m2Conif, WDEP_PM10ONS_m2Conif, HMIX, SURF_MAXO3, SURF_ppb_CO, etc.).
- Recorded values include dry and wet deposition fluxes, near-surface concentrations, mixing height, and various deposition/concentration terms for coniferous, deciduous, desert/sand, semi-natural, water, and grid-averaged surfaces.

## Data format and access
- Data provided in NetCDF format; an example is given for WDEP_PM25ONS (structure details provided in the document).

## Quality assurance and caveats
- QA/QC performed for 2001–2015; QA/QC reports available on request.
- Use of the dataset is at your own risk; no warranty or guarantee of error freedom or fitness for a particular purpose.

## References and notes
- Jalkanen et al. (2016); Simpson et al. (2012); Vieno et al. (2016a, 2016b); Skamarock et al. (2019); NCEP FNL/NWS data references.
- Documentation and methodology underpinning the EMEP4UK model and UK-SCAPE daily data are cited accordingly.