# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 2040, 2070 and 2100 for SSP scenarios 1-5

## Overview
- Dataset of annual total atmospheric deposition for cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen over the UK.
- Time period: 2040, 2070, 2100; SSP scenarios 1–5.
- Based on EMEP4UK model rv4.36 and WRF model v4.2.2; UK-centric outputs from a EU-scale domain.
- Domain: 27 × 27 km² resolution for EU with a nested UK domain at 3 × 3 km².

## Data content and structure
- Files: 15 NetCDF files named EMEP4UK_met2018_emisSSP#-YYYY.nc (SSP1–5; years 2040, 2070, 2100).
- Variables (example names and units):
  - Dry and wet deposition for oxidised and reduced nitrogen (DDEP_OXN_m2Grid, DDEP_RDN_m2Grid, WDEP_OXN, WDEP_RDN, etc.).
  - Dry deposition of heavy metals (DDEP_CD_m2Grid, DDEP_CU_m2Grid, DDEP_NI_m2Grid, DDEP_PB_m2Grid, DDEP_ZN_m2Grid).
  - Dry deposition of oxidised sulphur (DDEP_SOX_m2Grid) and wet deposition of oxidised sulphur (WDEP_SOX).
  - Wet deposition of nitrogen species (WDEP_NOX, WDEP_RDN) and rainfall (WDEP_PREC, mm).
  - Grid area (Area_Grid_km2).
- Temporal and spatial structure:
  - Time dimension: middle of each meteorological year; units are days since 1900-01-01.
  - Spatial grid: lon/lat defined by specified CRS; UK outputs extracted from larger EU domain.
- Metadata:
  - Postprocessing noted in NetCDF global 'history' attribute.
  - Current date fields: WDEP_PREC: current_date_first/last (example shown as 2019-01-01).

## Methods and provenance
- Models used:
  - EMEP4UK rv4.36 chemical transport model (derived from EMEP MSC-W rv4.36).
  - Weather inputs from WRF v4.2.2 with 1°×1° NCEP/NCAR GFS reanalysis nudging every 6 hours; 2018 meteorology used for all runs.
- Emissions and drivers:
  - UK NOx, NH3, SO2, PM2.5, PMcoarse, CO, and NMVOCs from 2019 National Atmospheric Emission Inventory (NAEI), rescaled to 2018.
  - Non-UK emissions from CEIP 0.1° resolution; UK total used for 2018.
  - Historical heavy metal emissions (1750–1960) from literature; contemporary emissions (1970–2018) from UK emissions inventory (NAEI 2021).
  - Projections for 2040/2070/2100 applied using UK-specific SSP versions.
- Compilation and computing:
  - FORTRAN Intel compiler (19.1.3.304) on UKCEH POLAR cluster.

## Data quality and QA/QC
- Full QA/QC conducted for 2018 (not included in this dataset); visual comparisons for historical and future runs.
- QA/QC reports are available on request (not included in the document).
- Use of content is at user’s own risk; no warranty that content is error-free or fit for a specific purpose.
- Related QA/QC references and evaluations are provided in associated literature and data reports.

## Access, usage, and governance
- Dataset is designed to support governance of large, multi-scenario atmospheric deposition data for UK applications.
- Metadata and postprocessing are documented via the NetCDF 'history' attribute; the primary data files are NetCDF with a clear naming convention.
- QA/QC reports and external validation literature provide context for data quality; some reports available on request.
- Users should consider potential limitations due to model assumptions, domain boundaries, and scenario-specific uncertainties when integrating into governance or discovery workflows.

## File organization and metadata considerations for Data Stewards
- File naming convention encodes SSP scenario and year, enabling straightforward discovery and filtering.
- NetCDF structure includes standard variables (time, lon, lat) and deposition metrics with explicit units.
- Projection and grid details are specified; documentation notes the postprocessing step (target variable extraction) and the contributing model versions.
- Provenance information (model versions, compilation environment, data sources) is essential for traceability and should be preserved in data catalogs and governance records.

## Limitations and caveats
- Only targeted variables and years included; extents beyond 2040, 2070, 2100 or SSP1–5 not covered.
- 2018 QA/QC is not embedded in the dataset; users should consult the referenced QA/QC reports for detailed validation.
- Dataset includes a comprehensive modeling chain with multiple sources; intercomparisons and uncertainties should be considered in downstream analyses.

## References
- Garland et al. (2022) NAEI emissions for England, Scotland, Wales, and Northern Ireland: 2005–2020.
- Ge et al. (2021); Geosci. Model Dev. on EMEP MSCW and WRF evaluations.
- Gu et al. (2021); Science article on ammonia vs NOx mitigation.
- Jalkanen et al. (2016); ship traffic emissions.
- Tomlinson et al. (2023); UK metal/air pollutant emissions at 1 km resolution, 1750–2100.
- Vieno et al. (2016a, 2016b); UK PM2.5 sensitivity studies and the 2014 PM episode.
- Simpson et al. (2012); EMEP MSC-W model description.
- Skamarock et al. (2019); WRF Model Description.