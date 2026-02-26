# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 1750 - 2018

## Overview
- Provides annual total atmospheric deposition (dry and wet) of cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen over the UK from 1750 to 2018.
- Generated with the EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM), derived from EMEP MSC-W rv4.36, using the WRF model v4.2.2 for meteorology.
- UK domain is nested within a 27 × 27 km2 EU domain, with a UK grid resolution of 3 × 3 km2.
- Meteorology for all runs is 2018 data assimilated from NCEP/NCAR GFS reanalysis every 6 hours.

## Modelling framework and inputs
- Emissions inputs for UK: NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, and non-methane VOCs from the 2019 National Atmospheric Emission Inventory (NAEI), rescaled to 2018.
- Non-UK emissions: EU CEIP data at 0.1° × 0.1° resolution; UK total used for 2018.
- Historical heavy metal emissions (1750–1960): literature-based.
- Contemporary emissions (1970–2018): from UK emissions inventory (NAEI, 2021; e.g., Garland et al., 2022).
- Projections (2040, 2070, 2100): UK-specific scenarios using SSPs.

## Data content and structure
- 30 NetCDF files named EMEP4UK_met2018_emisYYYY.nc, with YYYY representing the year of emissions.
- Temporal output: one year every decade from 1750 to 1990; every 5 years for 2005–2010; and the year 2018.
- Spatial grid: longitude-latitude grid defined in the NetCDF with a specified proj4 string; includes a grid area variable (Area_Grid_km2).
- Recorded variables (area-weighted deposition and rainfall): 
  - Dry deposition of oxidised sulphur (DDEP_SOX_m2Grid)
  - Dry deposition of oxidised nitrogen (DDEP_OXN_m2Grid)
  - Dry deposition of reduced nitrogen (DDEP_RDN_m2Grid)
  - Dry deposition of cadmium (DDEP_CD_m2Grid)
  - Dry deposition of copper (DDEP_CU_m2Grid)
  - Dry deposition of nickel (DDEP_NI_m2Grid)
  - Dry deposition of lead (DDEP_PB_m2Grid)
  - Dry deposition of zinc (DDEP_ZN_m2Grid)
  - Wet deposition of oxidised sulphur (WDEP_SOX)
  - Wet deposition of oxidised nitrogen (WDEP_OXN)
  - Wet deposition of reduced nitrogen (WDEP_RDN)
  - Wet deposition of cadmium (WDEP_CD)
  - Wet deposition of copper (WDEP_CU)
  - Wet deposition of nickel (WDEP_NI)
  - Wet deposition of lead (WDEP_PB)
  - Wet deposition of zinc (WDEP_ZN)
  - Rainfall (WDEP_PREC)
- Postprocessing: extraction of target variables; history attribute documents processing steps.

## Quality control and caveats
- Full QA/QC performed for 2018; visual QA/QC for other historical and future runs.
- QA/QC reports available on request; not included in this document.
- Use of dataset is at the user’s own risk; no warranty that content is error-free or fit for a particular purpose.

## Practical notes for analysts
- Enables long-term assessment of atmospheric deposition trends for heavy metals, nitrogen, and sulphur over the UK, with clear linkages to emissions inventories and SSP-based projections.
- Useful for correlating deposition with ecological and health impact studies, policy evaluation, and model-data intercomparison exercises.
- Data provenance and metadata are maintained to support traceability and potential dataset discovery or reuse.

## References
- Garland et al. (2022) NAEI, Air Pollutant Inventories for England, Scotland, Wales, and Northern Ireland: 2005-2020, Report ED11787
- Ge et al. (2021). Evaluation of global EMEP MSC-W (rv4.34) WRF (v3.9.1.1) model performance, Geosci. Model Dev.
- Gu et al. (2021). Abating ammonia vs NOx for PM2.5 mitigation, Science
- Jalkanen et al. (2016). Ship traffic exhaust inventory, Atmos. Chem. Phys.
- NCEP/NCAR and UCAR/NCAR data references
- Simpson et al. (2012); Vieno et al. (2016a, 2016b); Tomlinson et al. (2023); Vieno et al. (2016a, 2016b)