# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2001 - 2015)

## Summary
- Provides daily averaged atmospheric composition and fluxes for the UK (2001–2015) focusing on nitrogen, sulphur, particulate matter, and ozone.
- Built with the EMEP4UK rv4.17 atmospheric chemistry transport model and the WRF model (v3.7.1) for meteorology.

## What the dataset includes
- Daily averaged model output for UK-scale atmospheric composition and fluxes (2001–2015) from EMEP4UK rv4.17 and WRF.
- Coverage: EU domain at 0.5° × 0.5° with a nested UK domain at ~5 km resolution (0.05° × 0.055°).
- Model inputs and drivers:
  - Meteorology from WRF with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1° × 1° every 6 hours.
  - Emissions: UK 2015 NAEI emissions (NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, NMVOC) rescaled to 2001–2015; non-UK emissions from CEIP; shipping emissions (2011) from FMI with specific NMVOC/PM scaling.
- Data products: NetCDF outputs including surface concentrations, dry and wet deposition fluxes, mixing height, ozone metrics, and near-surface concentrations for a wide range of species and deposition pathways.

## Experimental design and technical details
- ACTM and domain:
  - EMEP4UK rv4.17 (ACTM) deriving from EMEP MSC-W rv4.17.
  - WRF meteorology at high resolution for the UK domain.
- Emissions and scaling:
  - UK emissions from NAEI (2015) scaled to 2001–2015 annual totals.
  - Non-UK emissions from CEIP; shipping emissions based on FMI 2011 data with targeted scaling for NMVOC and PM components.
- Computation:
  - FORTRAN Intel compiler (2013_sp1.3.174) on the CEH NEMSIS cluster.

## Data content and structure
- Units and definitions:
  - PM classifications: PM2.5, PMcoarse, PM10 defined with specific compositions.
  - Surface concentrations and deposition fluxes for numerous species (nitrogen, sulphur, ammonium, nitrate, ozone, VOCs, PM components, etc.) across various land/biophysical categories.
  - Includes mixing height, near-surface pollutant concentrations, and various wet/dry deposition metrics.
- Data format:
  - NetCDF files containing daily averaged outputs for the UK-SCAPE timeframe.
  - Example structure provided (e.g., WDEP_PM25ONS) to illustrate NetCDF variable naming.
- Scope of variables:
  - Dry deposition to different land uses (forests, crops, water, etc.) and to different nitrogen, sulfur, and PM species.
  - Wet deposition, rainfall, and related deposition fluxes.
  - Near-surface concentrations of gases and particles, including O3, NOx, NH3, HNO3, NO2, PM components, and related aerosols.

## Quality and provenance
- Quality control:
  - QA/QC performed for 2001–2015; reports available on request.
  - Use of dataset is at user’s risk; no warranty provided.
- Documentation and references:
  - Technical descriptions and supporting literature for EMEP4UK, WRF, and emissions data (e.g., Simpson et al., Vieno et al., Jalkanen et al., NCEP FNL references).

## Practical considerations for Data Leaders
- Data lineage and reproducibility:
  - Clear model versions (EMEP4UK rv4.17 and WRF v3.7.1) and data sources (NAEI, CEIP, FMI) documented.
  - Data produced on a dedicated compute cluster with FORTRAN-based processing, enabling reproducibility for similar future runs.
- Data discovery and interoperability:
  - NetCDF format supports integration with common GIS and data analysis tools; rich set of variables facilitates cross-domain analyses (air quality, emissions scenarios, environmental modeling).
- Gaps and caveats:
  - Some emissions components (e.g., FMI shipping NMVOC and PM splits) not explicitly included and require rescaling.
  - Non-UK emissions and rescaling introduce uncertainties; regional applicability is strongest for UK-SCAPE context.
  - QA/QC reports are not embedded in the main document; request-based access is available.
  
## End notes and references
- Bibliography highlights key sources for model descriptions, emission inventories, and data assimilation, including Jalkanen et al. (ship emissions), NCEP/NCAR/FNL analyses, Simpson et al. (EMEP MSC-W), Skamarock et al. (WRF) and Vieno et al. (PM2.5 mitigation sensitivities).