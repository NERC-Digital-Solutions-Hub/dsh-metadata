# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 2040, 2070 and 2100 for SSP scenarios 1-5

## Overview
- Provides annual total atmospheric deposition of cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen for the UK, covering 2040, 2070, and 2100 under SSP scenarios 1–5.
- Designed to support monitoring, evaluation of environmental health policies, and informing future decision-making.

## Modeling framework and data sources
- Uses EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM), derived from EMEP MSC-W rv4.36.
- Meteorology supplied by the Weather Research and Forecasting (WRF) model v4.2.2 with data assimilation of NCEP/NCAR GFS reanalysis (1°x1° every 6 hours), using 2018 meteorology for all runs.
- UK domain at 3x3 km and a larger EU domain at 27x27 km; only UK model results are reported.
- UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, NMVOCs) based on 2019 NAEI (rescaled to 2018); non-UK emissions from CEIP (0.1° resolution) with UK total used for 2018.
- Heavy metal emissions: historical (1750–1960) from literature; contemporary (1970–2018) from UK NAEI; projections (2040, 2070, 2100) use UK-specific SSPs.
- Related historical EMEP4UK dataset available via DOI; 2040/2070/2100 SSP scenarios included in output.

## Data files and structure
- 15 NetCDF files named EMEP4UK_met2018_emisSSP#-YYYY.nc (SSP# = 1–5; YYYY = 2040, 2070, 2100).
- Grid: geographic (lon/lat) with 240×240 resolution per variable; time dimension is unlimited (single record per output period).
- Primary variables (area-weighted deposition and precipitation, all in consistent units):
  - DDEP_SOX, DDEP_OXN, DDEP_RDN, DDEP_CD, DDEP_CU, DDEP_NI, DDEP_PB, DDEP_ZN (dry deposition; mg/m2 or mgS/m2 for SOx as specified)
  - WDEP_PREC (wet deposition precipitation; mm)
  - WDEP_SOX, WDEP_OXN, WDEP_RDN, WDEP_CD, WDEP_CU, WDEP_NI, WDEP_PB, WDEP_ZN (wet deposition; mg/m2)
  - Area_Grid_km2 (grid area in km2)
- Metadata and structure details documented in NetCDF global attributes (e.g., history, current_date_last).

## Quality assurance and limitations
- Full QA/QC performed for 2018; remaining historical and future runs subjected to visual comparisons; QA/QC reports available on request.
- Use of dataset is at user’s risk; no warranty of fitness for purpose.
- Key uncertainties arise from emissions inventories, model formulations, and meteorological drivers; ongoing data governance and metadata considerations apply.

## Temporal and spatial coverage
- Temporal: projections for 2040, 2070, and 2100 under SSP1–5.
- Spatial: UK-wide deposition totals (with UK domain at 3x3 km) derived from EU-wide modelling domain at 27x27 km.

## Metadata, data sharing, and governance considerations
- Post-processing is limited to target variables; data and metadata are provided within NetCDF files with standard CF-like conventions.
- Some barriers noted in monitoring contexts include metadata completeness, timely data sharing, and governance around dataset storage and updates.
- Underlying data sources (emissions inventories, meteorology reanalysis, and model configurations) are cited and traceable to specific publications and inventories.

## Relevance for monitoring frameworks
- Delivers scenario-based, policy-relevant indicators of atmospheric deposition for heavy metals and reactive nitrogen and sulfur compounds.
- Supports evaluation of emission-control policies and future planning by providing spatially explicit, hourly-to-annual atmosphere-to-deposition estimates.
- Enables cross-checks with ambient concentration and deposition measurements, while highlighting data provenance and methodological transparency.
- Highlights data governance considerations critical for monitoring programmes, including metadata quality and openness of underlying datasets.

## References
- Garland et al. (2022); Ge et al. (2021); Gu et al. (2021); Jalkanen et al. (2016); NCEP/NCAR (2000); Simpson et al. (2012); Vieno et al. (2016a,b); Tomlinson et al. (2023); Skamarock et al. (2019).