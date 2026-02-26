# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) monthly atmospheric deposition of oxidised sulphur, oxidised nitrogen, and reduced nitrogen for 2002-2021

## Overview
- Provides monthly averaged atmospheric deposition data for oxidised sulphur (SOx), oxidised nitrogen (NOx), and reduced nitrogen (RDN) over the UK for 2002–2021.
- Based on the EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM), with meteorology from WRF v4.2.2.
- UK-specific results are extracted from the EU-domain model at 3 km × 3 km resolution within a 27 km × 27 km European domain.

## Data content and variables
- Deposition types:
  - Dry deposition: DDEP_SOX_m2Grid, DDEP_OXN_m2Grid, DDEP_RDN_m2Grid (mg S or mg N per m2).
  - Wet deposition: WDEP_SOX_m2Grid, WDEP_OXN_m2Grid, WDEP_RDN_m2Grid (mg S or mg N per m2).
- Grid information:
  - UK domain resampled on a 3 × 3 km2 grid nested within a 27 × 27 km EU domain.
  - Grid area in km2 provided (Area_Grid_km2).
- Additional fields (example in dataset structure):
  - WDEP_PREC for rainfall (mm) and related grid metadata.
- Time: monthly records, 2002–2021 (12 months per year).

## Model and data sources
- ACTM: EMEP4UK rv4.36 (based on EMEP MSC-W rv4.36) with hourly to monthly deposition outputs.
- Meteorology: WRF v4.2.2 with Newtonian nudging to NWP reanalysis (NCEP/NCAR GFS 1° × 1° every 6 hours).
- Emissions:
  - UK anthropogenic emissions (NOx, NH3, SO2, PM2.5, PMcoarse, CO, NMVOCs) from 2019 National Atmospheric Emission Inventory (NAEI); UK totals for 2002–2019 used and rescaled per year.
  - Non-UK emissions from CEIP 0.1° × 0.1° data; 2020–2021 use 2019 emissions.
- Model compilation and compute:
  - Fortran; Intel compiler (v19.1.3.304); run on UKCEH POLAR cluster.

## Data structure and technical details
- File format: NetCDF with species-specific deposition variables and grid metadata.
- Example data snippet structure:
  - DDEP_SOX_m2Grid (monthly records, Mosaic class, time range starting 2002-02-01 to 2003-01-01 in the example).
- Projection and usage:
  - Polar stereographic grid with the specified proj4 string.
  - NetCDF libraries required for R, Python, or Fortran to access data.
- Documentation and metadata:
  - QA/QC completed for 2002–2021; QA/QC reports available on request.
  - No warranty; dataset use at user’s own risk.
- Data discoverability:
  - Datasets can be accompanied by metadata to facilitate discoverability and reuse.

## Usage guidance and considerations for analysts
- Ideal for assessing deposition patterns and potential ecological impacts within the UK, or for driving policy-support analyses in environmental management.
- Useful for linking deposition fluxes (wet and dry) to ecosystem exposure, deposition loadings, and trend analyses over 2002–2021.
- Consider domain limitations:
  - UK results are nested within a European 27 × 27 km domain; higher-resolution UK results are available only within the 3 × 3 km UK grid.
  - Emission inputs for 2020–2021 rely on 2019 data, which may affect year-specific accuracy for those years.
- Data integration notes:
  - Combine deposition fluxes with ecological or hydrological models to estimate deposition-to-impact pathways.
  - When aggregating, ensure consistent units (mg S or mg N per m2) and proper handling of wet vs dry components.
- Projected coordinate and unit considerations:
  - Use the provided proj4 string and NetCDF access to align with your GIS or data analysis workflow.

## Quality and limitations
- QA/QC exists for 2002–2021; external reports can be requested.
- Guidance notes state data use at user’s risk; no formal warranty of fitness for a particular purpose.
- Potential limitations include data availability at finer local scales, reliance on emission inventories, and temporal gaps if quality checks highlight issues.

## References
- Ge, Y., Heal, M. R., et al. (2021). Evaluation of global EMEP MSCW and WRF models with measurements.
- Gu, B., Zhang, L., et al. (2021). Ammonia and NOx mitigation cost implications for PM2.5.
- Jalkanen, J.P., Johansson, L., and Kukkonen, J. (2016). Ship traffic exhaust emissions inventory.
- NCEP/NCAR reanalysis and WRF model references (various foundational sources).
- Simpson, D., Benedictow, A., et al. (2012). The EMEP MSC-W chemical transport model technical description.
- Skamarock, W.C., Klemp, J.B., et al. (2019). A Description of the Advanced Research WRF Model Version 4.
- Vieno, M., Heal, M.R., et al. (2016). UK PM2.5 emissions sensitivity and major episode analyses.