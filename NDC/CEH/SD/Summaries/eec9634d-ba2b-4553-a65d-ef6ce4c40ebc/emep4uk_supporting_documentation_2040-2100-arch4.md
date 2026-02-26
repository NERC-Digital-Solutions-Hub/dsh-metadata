# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 2040, 2070 and 2100 for SSP scenarios 1-5

## Purpose and scope
- Provides annual total atmospheric deposition over the UK for cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen for 2040, 2070, and 2100 under SSP scenarios 1-5.
- Uses EMEP4UK model (rv4.36) combined with WRF (v4.2.2) to simulate deposition and atmospheric composition.
- UK-focused outputs derived from a EU domain (27×27 km) with a nested UK domain (3×3 km); only UK results are included.

## Data sources and model lineage
- Atmospheric chemistry transport model: EMEP4UK rv4.36 (based on EMEP MSC-W rv4.36).
- Meteorology: Weather Research and Forecasting (WRF) Model v4.2.2 with 1°×1° NWP data assimilation (6-hour updates from NCEP/NCAR GFS reanalysis).
- Emissions:
  - UK: NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, non-methane VOC from 2019 NAEI, rescaled to 2018 totals.
  - Non-UK: CEIP 0.1°×0.1° emissions; UK total used for the year 2018.
  - Heavy metal historical emissions (1750–1960) from literature; 1970–2018 from UK emissions inventory (NAEI 2021).
  - Projections for 2040, 2070, 2100 use UK-specific SSPs.
- Related historical data: previous EMEP4UK dataset available via DOI link provided in the document.

## Data contents and structure
- Output files:
  - 15 NetCDF files named EMEP4UK_met2018_emisSSP#-YYYY.nc (SSP# = 1–5; YYYY = 2040, 2070, 2100).
  - Time dimension is unlimited; spatial grid: lon × lat with 240 × 240 points in the UK domain representation.
- Variables and units:
  - Area_Grid_km2: grid area (km²).
  - DDEP_SOX_m2Grid: dry deposition of oxidised sulphur (mgS/m²).
  - DDEP_OXN_m2Grid: dry deposition of oxidised nitrogen (mgN/m²).
  - DDEP_RDN_m2Grid: dry deposition of reduced nitrogen (mgN/m²).
  - DDEP_CD_m2Grid, DDEP_CU_m2Grid, DDEP_NI_m2Grid, DDEP_PB_m2Grid, DDEP_ZN_m2Grid: dry deposition of heavy metals (mg/m²).
  - WDEP_SOX, WDEP_OXN, WDEP_RDN, WDEP_CD, WDEP_CU, WDEP_NI, WDEP_PB, WDEP_ZN: wet deposition (mg/m²) for corresponding species.
  - WDEP_PREC: rainfall (mm).
- Temporal reference:
  - Time variable denotes middle of the meteorological year; units are days since 1900-01-01.
- Metadata and data structure:
  - NetCDF files include standard naming and metadata conventions; examples show time, lon, lat dimensions and corresponding variables.
  - A minimal postprocessing step extracts the target variables; the global NetCDF attribute 'history' documents postprocessing steps.

## Quality assurance and limitations
- QA/QC performed for the year 2018 (not included in this data release); additional QA/QC for remaining historical and future runs with visual comparisons.
- QA/QC reports available on request; no warranty or guarantee that content is error-free or fit for a specific use.
- Users should consider uncertainties inherent in model simulations, emission inventories, and SSP-based projections when conducting analyses or policy decisions.

## Accessibility, use, and governance
- The dataset enables assessment of UK deposition of heavy metals, nitrogen, and sulphur under multiple SSP scenarios through 2040–2100.
- Documentation notes that data use is at the user’s own risk; contextual background and references provided for methodological transparency.
- Related publications and datasets cited offer provenance and validation context (NAEI inventories, EMEP MSC-W evaluations, and SSP-related studies).

## Provisional notes for data leaders
- Data asset value: long-term, scenario-based deposition data enabling policy impact assessment and cross-portfolio data integration.
- Key governance considerations: ensure discoverability of the 15 NetCDF files, maintain links to the DOI for related historical data, and manage access to QA/QC reports.
- Metadata and standardization: consistent units across species and deposition types; clear naming conventions facilitate discoverability and interoperability with other atmospheric deposition datasets.
- Update and lifecycle planning: dataset reflects 2018 meteorology and 2018 UK emissions baseline with SSP-based future projections; plan for documenting future updates or expanded coverage (years beyond 2100, alternative meteorology reanalyses, or updated inventories).