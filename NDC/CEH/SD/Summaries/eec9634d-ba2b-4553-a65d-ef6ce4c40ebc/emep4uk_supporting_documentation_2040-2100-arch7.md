# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 2040, 2070 and 2100 for SSP scenarios 1-5

## Overview
- Dataset of annual total atmospheric deposition for cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen over the UK.
- Targets 2040, 2070, and 2100 under SSP scenarios 1–5.
- Generated with EMEP4UK rv4.36 (an atmospheric chemistry transport model) and WRF v4.2.2 for meteorology.

## What’s included
- 15 NetCDF files named EMEP4UK_met2018_emisSSP#-YYYY.nc (SSP# = 1–5; YYYY = 2040, 2070, 2100).
- Variables include:
  - DDEP_*: area-weighted dry deposition for various species (e.g., DDEP_SOX_m2Grid, DDEP_OXN_m2Grid, DDEP_RDN_m2Grid, DDEP_CD_m2Grid, DDEP_CU_m2Grid, DDEP_NI_m2Grid, DDEP_PB_m2Grid, DDEP_ZN_m2Grid).
  - WDEP_*: wet deposition for the same species (e.g., WDEP_PREC for rainfall; WDEP_SOX, WDEP_OXN, WDEP_RDN, WDEP_CD, WDEP_CU, WDEP_NI, WDEP_PB, WDEP_ZN).
  - Area_Grid_km2: grid area (km2) for the target region.
- NetCDF data are reported on a geographic longitude–latitude grid with a 3x3 km UK nested domain within a 27x27 km European domain.

## Spatial and temporal coverage
- Spatial domain: UK within the EU model grid; UK nested domain is 3x3 km2 resolution (EU domain is 27x27 km2).
- Temporal coverage: annual deposition values for 2040, 2070, and 2100 (for SSPs 1–5).
- Time variable represents the middle of the meteorological year; example timestamp shown is mid-2018 for model setup references.

## Data structure and variable details
- Grid definition: geographic projection with WGS84 coordinates (Proj4 string provided in documentation).
- Sample NetCDF structure includes:
  - time (unlimited), lon, lat dimensions.
  - WDEP_PREC(time, lat, lon) and similarly named WDEP_* and DDEP_* variables (units in the NetCDF attributes, e.g., mg/m2 for dry/wet depositions, mm for rainfall).
- Only post-processing applied to extract the listed target variables; history and QA/QC metadata stored in NetCDF attributes.

## File naming and access
- File naming convention: EMEP4UK_met2018_emisSSP#-YYYY.nc
  - SSP#: scenario number (1–5)
  - YYYY: year (2040, 2070, or 2100)
- Data produced using:
  - EMEP4UK rv4.36 model
  - WRF model v4.2.2
  - Emissions data from NAEI (UK) and CEIP (non-UK), with historical emissions (1750–1960) from literature and contemporary emissions (1970–2018) from NAEI (as of 2021)
- Post-processing: minimal; only extraction of target variables; metadata records processing steps in the NetCDF global 'history' attribute.

## Quality assurance and caveats
- Full QA/QC conducted for the year 2018 (not included in this dataset but described in related documentation); remaining historical and future runs verified visually.
- QA/QC reports available on request.
- Usage disclaimer: content is provided at your own risk; no warranty on accuracy or fitness for purpose.

## How to use this data in GIS
- Preparation
  - Read NetCDF files with standard GIS/remote-sensing tools that support NetCDF (e.g., QGIS, ArcGIS, Python xarray).
  - Reproject to your preferred coordinate reference system if needed; data are provided in a geographic (lon/lat) grid.
  - If necessary, convert units (e.g., mg/m2 for dry/wet deposition; mm for rainfall) to match your analysis scale.
- Spatial analysis
  - Map annual total deposition by SSP and year to assess spatial patterns of heavy metals and nitrogen/sulphur deposition across the UK.
  - Combine deposition components (e.g., sum DDEP_* and WDEP_* for total deposition per species) as required for your analysis.
  - Use Area_Grid_km2 for area-weighted analyses or resampling to align with administrative boundaries or other GIS layers.
- Temporal analysis
  - Compare deposition across SSPs and years (2040 vs 2070 vs 2100) to evaluate projected changes under different socio-economic pathways.
  - Create time-series visuals or dashboards to show projected deposition trends.
- Integration and visualization
  - Overlay with environmental or policy layers (e.g., land use, population density, protected areas) to assess potential impacts.
  - Produce map products for stakeholders (policy colleagues, clients, public) that clearly communicate spatial distribution and projected changes.

## References and notes
- References for model components and emissions data are provided in the documentation bibliography (including works by Garland et al., Ge et al., Gu et al., Jalkanen et al., Tomlinson et al., Vieno et al., and Simpson et al.).
- Historical EMEP4UK data (earlier releases) are available via the provided DOI link in the documentation.
- The dataset focuses on UK-specific projections under SSP scenarios, with support from UK emissions inventories and CEIP global emissions data.