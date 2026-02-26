# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 2040, 2070 and 2100 for SSP scenarios 1-5

## Overview
- Provides annual total atmospheric deposition over the UK for cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen for years 2040, 2070, and 2100 under SSP scenarios 1–5.
- Generated with EMEP4UK model rv4.36 and Weather Research and Forecasting (WRF) model v4.2.2.
- UK-focused outputs derived from a 27 × 27 km EU domain with a nested 3 × 3 km UK domain.
- Meteorology is 2018 data assimilated from NCEP/NCAR GFS via WRF; calculations use 1° × 1° NCEP reanalysis input every 6 hours.
- Anthropogenic emissions for the UK (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, non-methane VOC) from the 2019 NAEI, rescaled to 2018; non-UK emissions from CEIP at 0.1° resolution.
- Historical heavy metal emissions (1750–1960) from literature; contemporary emissions (1970–2018) from UK NAEI 2021; projections apply UK SSPs.
- Historical EMEP4UK data available (doi provided); this dataset contains annual model outputs described below.

## Data content and structure
- Data format: 15 NetCDF files named EMEP4UK_met2018_emisSSP#-YYYY.nc, where SSP# = 1–5 and YYYY = 2040, 2070, 2100.
- Temporal reference: output timestamp corresponds to the middle of the meteorological year; 2018 meteorology used across runs.
- Spatial grid: geographic (longitude-latitude) grid defined by the provided projection; UK domain within the EMEP4UK global framework.
- Variables and units (grid-mean, area-weighted where indicated):
  - Dry and wet deposition: DDEP_SOX_m2Grid, DDEP_OXN_m2Grid, DDEP_RDN_m2Grid, DDEP_CD_m2Grid, DDEP_CU_m2Grid, DDEP_NI_m2Grid, DDEP_PB_m2Grid, DDEP_ZN_m2Grid (mgS/m2 or mgN/m2 or mg/m2 as appropriate)
  - Wet deposition: WDEP_SOX, WDEP_OXN, WDEP_RDN, WDEP_CD, WDEP_CU, WDEP_NI, WDEP_PB, WDEP_ZN (mg/m2)
  - Rainfall: WDEP_PREC (mm)
  - Grid area: Area_Grid_km2 (km2)
- Data structure example: NetCDF with dimensions time, lat, lon; time is unlimited; variables include WDEP_PREC(time, lat, lon) and others as listed; coordinate metadata included (lon, lat, time with standard naming).

## Methodology and data sources
- Atmospheric chemistry transport model: EMEP4UK rv4.36 (derived from EMEP MSC-W rv4.36).
- Meteorology: WRF v4.2.2 with Newtonian nudging using NCEP/NCAR GFS reanalysis at 1° × 1° resolution, every 6 hours; 2018 meteorology used for all runs.
- Emissions:
  - UK: NAEI 2019 estimates, rescaled to 2018 totals.
  - Non-UK: CEIP 0.1° × 0.1° emissions data.
- Emissions for heavy metals: historical (1750–1960) from literature; contemporary (1970–2018) from UK NAEI/Garland et al.; projections via UK SSPs for 2040, 2070, 2100.

## Quality assurance and limitations
- QA/QC: full QA/QC performed for 2018 (not included in this dataset); visual comparisons for remaining historical and future runs; QA/QC reports available on request.
- Usage caveats: content usage is at the user’s risk; no warranty or guarantee of error-free results or fitness for a specific purpose.

## Provenance, processing, and technical notes
- Model compilation: FORTRAN with Intel compiler (version 19.1.3.304).
- Computational platform: UKCEH POLAR cluster (CentOS Linux 7.x).
- Postprocessing: only extraction of target variables; otherwise data remains in model output form.
- Related literature and references provided for model description, emissions data, and evaluation (citations include Garland et al. 2022; Ge et al. 2021; Gu et al. 2021; Jalkanen et al. 2016; and others).