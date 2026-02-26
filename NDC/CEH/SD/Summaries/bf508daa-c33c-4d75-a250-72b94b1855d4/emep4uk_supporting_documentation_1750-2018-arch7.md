# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 1750 - 2018

## Overview
- Provides annual total atmospheric deposition for cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen over the UK from 1750 to 2018.
- Based on EMEP4UK model rv4.36 (ACTM) with WRF v4.2.2 meteorology; domain includes EU at 27×27 km2 with nested UK at 3×3 km2.
- Uses 2018 meteorology for all runs; emissions data from UK and CEIP sources; projections adopt UK-specific SSPs.
- Model outputs are in NetCDF format and include both dry and wet deposition components as well as rainfall.

## Data content and structure
- 30 NetCDF files, named EMEP4UK_met2018_emisYYYY.nc, where YYYY is the year of emissions.
- Temporal coverage: output for one year every decade from 1750 to 1990; every 5 years between 2005 and 2010; and 2018.
- Spatial coverage: UK results (though the domain extends to EU grid); grid defined by a specific projection string.
- Grid and variables:
  - Grid area in km2 (Area_Grid_km2).
  - Dry deposition for oxidised sulphur (DDEP_SOX_m2Grid) and oxidised nitrogen (DDEP_OXN_m2Grid); dry deposition for reduced nitrogen (DDEP_RDN_m2Grid).
  - Dry deposition for heavy metals: cadmium (DDEP_CD_m2Grid), copper (DDEP_CU_m2Grid), nickel (DDEP_NI_m2Grid), lead (DDEP_PB_m2Grid), zinc (DDEP_ZN_m2Grid).
  - Wet deposition for oxidised sulphur (WDEP_SOX), oxidised nitrogen (WDEP_OXN), reduced nitrogen (WDEP_RDN), cadmium (WDEP_CD), copper (WDEP_CU), nickel (WDEP_NI), lead (WDEP_PB), zinc (WDEP_ZN).
  - Rainfall (WDEP_PREC).
- Units and naming:
  - Depositions are area-weighted with units as specified in NetCDF attributes (e.g., mgS/m2, mgN/m2, mg/m2, and rainfall in mm).
  - NetCDF variable names follow the documented conventions (e.g., DDEP_* for dry deposition, WDEP_* for wet deposition).
- Temporal reference: model outputs are keyed to the middle of the meteorological year (e.g., 2018-07-02 12:00:00).

## Methodology and data provenance
- Modeling chain:
  - EMEP4UK rv4.36 ACTM, derived from EMEP MSC-W rv4.36.
  - 3D meteorology from WRF v4.2.2 with Newtonian nudging of NCEP/NCAR GFS reanalysis data at 1° resolution every 6 hours.
  - UK emissions from NAEI 2019 (rescaled to 2018); non-UK emissions from CEIP; UK historical emissions 1750-1960 from literature; UK 1970-2018 from NAEI.
  - Projections for 2040, 2070, 2100 use UK SSP-based scenarios.
- Implementation:
  - Compiled with Intel Fortran; runs on the UKCEH POLAR cluster.
  - Outputs postprocessed to extract target deposition variables; no additional postprocessing beyond documented extraction.

## Spatial and GIS considerations
- Spatial domain includes the UK at 3×3 km2 resolution within a European 27×27 km2 grid.
- Projection details are provided via a Proj.4 string for the NetCDF data; grid is defined in long/lat coordinates with the specified equal-area-like projection and WGS84 ellipsoid.
- Suitable for map-based visualizations and spatial analyses after conversion to GIS-friendly formats (e.g., GeoTIFF or vectorized rasters) and/or reprojecting to common CRS.
- Grid area (Area_Grid_km2) enables area-weighted analyses and aggregation to coarser resolutions as needed.

## Data quality and usage notes
- QA/QC performed for 2018; visual QA for other years; full QA/QC reports available on request.
- Use of dataset is at user’s risk; no warranty or guarantee of error-free content or fitness for a particular purpose.
- Data represent model-based estimates of atmospheric deposition, not direct measurements; consider using alongside observations for validation if available.

## Practical considerations for GIS Specialists
- Ideal for creating time-sliced deposition maps, trend visuals, and impact assessments at UK scales.
- Requires converting NetCDF to GIS-compatible formats and possibly reprojecting to a uniform CRS; retain or compute area weights using Area_Grid_km2.
- Temporal availability varies by year (decadal 1750–1990, select 2005–2010, and 2018); plan analyses accordingly for consistent time series.
- Data cover multiple species/components (heavy metals, oxidised/reduced nitrogen, sulphur) and both dry/wet deposition, plus rainfall for context.

## References and related materials
- Bibliography includes NAEI England/Scotland/Wales/Northern Ireland inventories and related model evaluations and emissions studies (e.g., Garland et al. 2022; Tomlinson et al. 2023; Vieno et al. 2016; Ge et al. 2021; Skamarock et al. 2019).