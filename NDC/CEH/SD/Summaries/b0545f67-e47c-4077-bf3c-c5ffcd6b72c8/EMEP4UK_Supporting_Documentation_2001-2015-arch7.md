# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2001 - 2015)

## Overview
- Provides daily averaged atmospheric composition and fluxes for the UK, focusing on nitrogen, sulphur, particulate organic matter, and ozone for 2001–2015.
- Generated using EMEP4UK model rv4.17 (ACTM) and the Weather Research and Forecasting Model (WRF) version 3.7.1.

## Spatial and Temporal Coverage
- Spatial domain: EU domain at 0.5° × 0.5° with a nested UK domain at approximately 0.05° × 0.055° (about 5 × 6 km2). Only UK-domain results are included.
- Temporal resolution: daily averaged outputs (meteorology nudging from NCEP/NCAR GFS at 1° × 1° every 6 hours).
- Time period: 2001–2015.

## Data Sources and Modelling Chain
- Atmosphere chemistry transport model (EMEP4UK rv4.17) linked to the EMEP MSC-W framework.
- Meteorology: WRF with data assimilation (Newtonian nudging) to NCEP/NCAR GFS reanalysis.
- Emissions: UK NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC from 2015 NAEI; rescaled to 2001–2015. Non-UK emissions from CEIP 0.5° × 0.5°. UK total emissions used for rescaling 2001–2014; shipping emissions (2011) from FMI with NMVOC and PM adjustments applied.
- Computation environment: FORTRAN Intel compiler (2013_sp1.3.174) on CEH cluster NEMSIS.

## Variables and Units (Key Categories)
- Particulate matter:
  - PM2.5 (aerodynamic diameter < 2.5 µm)
  - PMcoarse (2.5–10 µm)
  - PM10 = PM2.5 + PMcoarse
  - Definitions and NetCDF variable names provided (e.g., PM2.5 and PM10-related fields)
- Deposition and concentrations:
  - Dry deposition fluxes for nitrogen, nitrogen-containing species, and other pollutants to various surfaces (coniferous forest, crops, deciduous forest, desert, water, semi-natural, grid-weighted).
  - Wet deposition fluxes for nitric acid, ammonia, nitrate, oxidised nitrogen, sulphur species, and others.
  - Surface/near-surface concentrations and related fields (e.g., O3, NO2, NO, NO3, NH3, NH4, NH4F, VOCs, PM components, sea salt, dust, organic matter).
  - Typical units include mgN/m2, mgS/m2, mgN/m2 (various subfields), ppbv, mg/m3, µg/m3, Deg C, and mixing height HMIX.
- Derived and diagnostic fields:
  - Mixing layer height (HMIX)
  - Mean daily maximum ozone (SURF_MAXO3)
  - Near-surface concentrations for a range of species (e.g., SURF_ppb_O3, SURF_ppb_NO2, SURF_ppb_CO, SURF_ppb_HCHO, SURF_ppb_HNO3)
  - Water-associated PM2.5 (SURF_PM25water)
- Example NetCDF variable references (illustrative): DDEP_HNO3_m2Conif, DDEP_NO2_m2Conif, DDEP_O3_m2Conif, WDEP_NO3_F, WDEP_PM10ONS, SURF_ppb_NO2, SURF_ug_PM25, HMIX, SURF_MAXO3.

## NetCDF Structure and Access
- Data are stored as NetCDF files with clearly labeled variables as described above.
- A concrete data-structure example is provided in the documentation (an example for WDEP_PM25ONS is shown in the text), indicating a reproducible, programmatic data layout.
- QA/QC processes have been performed for 2001–2015; detailed QA reports are available on request (not included in the document).

## Quality Assurance and Limitations
- QA/QC completed for 2001–2015; reports available on request.
- Usage of dataset is at user’s risk; no warranty of fitness for a particular purpose is provided.
- Emission data include specific adjustments (e.g., FMI shipping NMVOC and PM adjustments) due to data limitations.

## GIS and Data Integration Notes
- High-resolution UK-domain data (approximately 5 × 6 km2) are suitable for map-based visualization of pollutant distributions and fluxes.
- Daily averages enable time-series mapping and trend analysis across the 2001–2015 period.
- Users should be aware of the mixed-resolution inputs (0.5° EU domain, nested UK domain) and rescaling procedures applied to emissions data when integrating with other regional datasets.
- NetCDF variable naming requires mapping to standard GIS-friendly layers; consider creating a consistent schema for pollutant concentrations, deposition fluxes, and isopleths.

## References
- Jalkanen, J.P., Johansson, L., and Kukkonen, J. (2016). A comprehensive inventory of ship traffic exhaust emissions in the Europe sea areas in 2011. Atmos. Chem. Phys. 16, 71-84.
- Simpson, D., et al. (2012). The EMEP MSC-W chemical transport model technical description. Atmos. Chem. Phys. 12, 7825-7865.
- Skamarock, W.C., et al. (2019). A Description of the Advanced Research WRF Model Version 4. UCAR/NCAR.
- Vieno, M., et al. (2016a). The sensitivities of emissions reductions for the mitigation of UK PM2.5. Atmos. Chem. Phys. 16, 265-276.
- Vieno, M., et al. (2016b). The UK particulate matter air pollution episode of March-April 2014: more than Saharan dust. Environmental Research Letters 11, 044004.