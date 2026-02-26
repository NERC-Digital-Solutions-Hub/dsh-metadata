# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 1750 - 2018

## Overview
- Provides annual total atmospheric deposition (dry and wet) of cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen over the UK from 1750 to 2018.
- Generated with EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM), derived from EMEP MSC-W rv4.36; meteorology from the WRF model v4.2.2.
- Model domain covers the EU at 27 × 27 km2 with a nested UK domain at 3 × 3 km2; results presented for the UK domain only.
- Meteorology assimilation uses Newtonian nudging of NCEP/NCAR GFS reanalysis at 1° × 1° every 6 hours; 2018 meteorology used for all runs.
- UK emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC) based on 2019 NAEI, rescaled to 2018; non-UK emissions from CEIP; historical UK heavy metal emissions (1750–1960) from literature; 1970–2018 from UK NAEI 2021; future projections (2040, 2070, 2100) use UK-specific SSPs.
- The dataset comprises annual total outputs from these models for the specified period.

## Experimental design / sampling regime
- ACTM domain and resolution as described; UK-focused results from the nested UK domain.
- 3D meteorology from WRF with data assimilation of reanalysis meteorology (NCEP/NCAR GFS) at 1° × 1°, updated every 6 hours.
- Temporal coverage spans 1750–2018 with specified sampling between decades/years.
- Outputs include dry and wet deposition for multiple metals and nitrogen species.

## Data files and naming
- There are 30 NetCDF files named EMEP4UK_met2018_emisYYYY.nc, where YYYY is the year of emissions used.
- Coverage pattern: one year per decade from 1750–1990; five-year intervals for 2005–2010; and the year 2018.
- The timestamp for model output corresponds to the middle of the meteorological year (2018-07-02 12:00:00 for the 2018 run).
- Grid specification is geographic (lon, lat) defined by a specified proj4 string (eqc + WGS84, etc.).
- Post-processing performed to extract target variables; details recorded in the NetCDF global attribute history.

## Nature and units of recorded values
- Grid area: km2 (Area_Grid_km2).
- Dry deposition (area-weighted) for oxidised sulphur: DDEP_SOX_m2Grid.
- Dry deposition (area-weighted) for oxidised nitrogen: DDEP_OXN_m2Grid.
- Dry deposition (area-weighted) for reduced nitrogen: DDEP_RDN_m2Grid.
- Dry deposition (area-weighted) for heavy metals: Cd, Cu, Ni, Pb, Zn (DDEP_*_m2Grid for each).
- Wet deposition (area-weighted): WDEP_SOX, WDEP_OXN, WDEP_RDN, WDEP_CD, WDEP_CU, WDEP_NI, WDEP_PB, WDEP_ZN (all in mg/m2).
- Rainfall: WDEP_PREC (mm).
- Species included: Cd, Cu, Ni, Pb, Zn, oxidised sulphur (SOx), oxidised nitrogen (OXN), reduced nitrogen (RDN).

## Data structure (NetCDF details)
- Outputs are organized on a geographic grid with dimensions including lon and lat; time is UNLIMITED (currently one time step per file).
- Example variable groupings include WDEP_PREC, WDEP_SOX, WDEP_OXN, WDEP_RDN, DDEP_SOX, DDEP_OXN, DDEP_RDN, DDEP_CD, DDEP_CU, DDEP_NI, DDEP_PB, DDEP_ZN, and Area_Grid_km2.
- The exact dimensional structure is documented within each NetCDF file; the provided example illustrates typical NetCDF formatting and variable naming conventions.

## Quality control and limitations
- A full QA/QC process was conducted for the 2018 year; visual QA conducted for other historical and future runs.
- QA/QC reports are available on request but are not included in the document.
- Content usage is at the user’s risk; no warranty or guarantee of error-free content.

## Access and use (data support perspective)
- Data are provided in standard NetCDF format with clearly named deposition variables, enabling integration into dashboards, pivot analyses, or reports for self-service exploration.
- Post-processing extracts the key deposition variables, with provenance recorded in the NetCDF history field to assist reproducibility.
- Suitable for trend analysis, cross-dataset comparisons, and policy-relevant assessments of UK atmospheric deposition over long timescales.

## Bibliography / references
- Garland, L. et al. (2022). NAEI, Air Pollutant Inventories for England, Scotland, Wales, and Northern Ireland: 2005-2020, Report ED11787.
- Ge, Y. et al. (2021). Evaluation of global EMEP MSCW (rv4.34) WRF (v3.9.1.1) model surface concentrations and wet deposition of reactive N and S. Geosci. Model Dev., 14, 7021-7046.
- Gu, B. et al. (2021). Abating ammonia is more cost-effective than nitrogen oxides for mitigating PM2.5 air pollution. Science, 374, 758-762.
- Jalkanen, J.P. et al. (2016). Inventory of ship traffic exhaust emissions in European seas. Atmos. Chem. Phys., 16, 71-84.
- NCEP FNL Operational Model Global Tropospheric Analyses (2000). UCAR/NCAR Research Data Archive.
- Simpson, D. et al. (2012). The EMEP MSC-W chemical transport model technical description. Atmos. Chem. Phys., 12, 7825-7865.
- Skamarock, W.C. et al. (2019). A Description of the Advanced Research WRF Model Version 4. UCAR/NCAR.
- Tomlinson, S.J. et al. (2023). Estimates of anthropogenic emissions of metals and air pollutants in the UK at 1km resolution, 1750-2100. NERC EDS EIDC.
- Vieno, M. et al. (2016a, 2016b). UK PM2.5 mitigation sensitivity studies and the 2014 UK PM episode. Atmos. Chem. Phys.; Environ. Res. Lett.