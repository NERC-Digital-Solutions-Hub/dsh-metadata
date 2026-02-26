# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 1750 - 2018

- Purpose and scope
  - Provides annual total atmospheric deposition (wet and dry) for cadmium (Cd), copper (Cu), nickel (Ni), lead (Pb), zinc (Zn), sulphur (S), and nitrogen (N) over the UK from 1750 to 2018.
  - Enables long-term environmental health monitoring and policy performance assessment through consistent, time-series data.

- Modelling framework and data sources
  - EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM), derived from EMEP MSC-W rv4.36.
  - Meteorology: Weather Research and Forecasting (WRF) v4.2.2 with data assimilation of NCEP/NCAR GFS reanalysis (1°x1° every 6 hours); 2018 meteorology used for all runs.
  - Domain and resolution: EU domain at 27×27 km, nested UK domain at 3×3 km; UK results extracted.
  - Emissions inputs:
    - UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, non-methane VOC) from 2019 NAEI, rescaled to 2018.
    - Non-UK emissions from CEIP 0.1°×0.1°; UK total used for 2018.
    - Heavy metal emissions: historical 1750–1960 from literature; 1970–2018 from UK NAEI (2021); future projections (2040, 2070, 2100) via UK SSP-based scenarios.
  - Outputs: 30 NetCDF files covering years; timesteps represent the middle of the meteorological year.

- Data files, structure and contents
  - File naming: EMEP4UK_met2018_emisYYYY.nc (YYYY = year of emissions).
  - Temporal coverage: output for one year each decade from 1750–1990; every 5 years between 2005–2010; and 2018.
  - Spatial and grid details: geospatial grid defined with a specified Proj4 string; 240×240 grid cells for the domain (lon×lat).
  - Variables (dry deposition, area-weighted; wet deposition; rainfall):
    - Dry deposition (area-weighted): oxidised sulphur (SOx), oxidised nitrogen (OXN), reduced nitrogen (RDN), Cd, Cu, Ni, Pb, Zn.
      - NetCDF variable names: DDEP_SOX_m2Grid, DDEP_OXN_m2Grid, DDEP_RDN_m2Grid, DDEP_CD_m2Grid, DDEP_CU_m2Grid, DDEP_NI_m2Grid, DDEP_PB_m2Grid, DDEP_ZN_m2Grid.
    - Wet deposition: SOx, OXN, RDN, Cd, Cu, Ni, Pb, Zn.
      - NetCDF variable names: WDEP_SOX, WDEP_OXN, WDEP_RDN, WDEP_CD, WDEP_CU, WDEP_NI, WDEP_PB, WDEP_ZN.
    - Rainfall: WDEP_PREC.
    - Grid metadata: Area_Grid_km2 (grid cell area).
  - Postprocessing: only extraction of the target deposition variables; history attribute documents postprocessing steps.

- Output format and accessibility
  - Outputs are netCDF format suitable for integration into monitoring portals and scientific analyses.
  - QA/QC: full QA/QC performed for 2018; visual QA for other years; reports available on request.
  - Usage disclaimer: dataset content provided at user’s own risk; no warranty of error-free or fit for a specific purpose.
  - Data stewardship: datasets stored and accessible through appropriate data portals (as part of standard monitoring data practices).

- Temporal, spatial and analytical context
  - Temporal span enables analysis of long-term trends from 1750 to 2018 and projections under SSP scenarios for future decades.
  - Spatial focus on the UK, with higher-resolution UK domain outputs to support national-scale environmental monitoring.

- References and supporting material
  - Model and emissions methodology draw on published work (e.g., Simpson et al. 2012; Vieno et al. 2016a,b; Tomlinson et al. 2023) and the NAEI/CEIP emission datasets; related validation studies cited in the bibliography.