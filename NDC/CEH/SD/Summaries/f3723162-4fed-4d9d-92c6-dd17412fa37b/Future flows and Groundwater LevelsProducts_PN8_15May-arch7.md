# Future flows and Groundwater Levels - SC090016

## Overview
- Aims to provide nationally consistent, map-based data products and time-series to assess climate change impacts on river flows and groundwater across Great Britain.
- Based on HadRM3-PPE ensemble (UKCP09), delivering 11-member ensembles, spanning 1951–2098.
- Produces both time-series and spatial map products suitable for GIS analysis and policy support.
- Access and licensing via CEH, BGS, and related portals; non-commercial use is free, commercial use may incur fees.

## Data products and datasets
- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded climate time series (precipitation and potential evapotranspiration).
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater level time series for 282 river sites and 24 boreholes.
- 11-member ensemble of daily catchment-averaged precipitation and PET for the same 282 river sites and 24 boreholes.
- National maps of changes in river flow statistics (mean monthly flows and low-flow statistics) for most large GB rivers.
- Regional maps of groundwater level and river flow statistics for one region.
- Briefing notes for decision-makers on how to use results.

## Data formats, scope, and resolution
- Spatial coverage: England, Wales, Scotland; GB-wide applicability.
- Climate time series: 1951–2098; 11 ensemble members; 1-km grid resolution (APr inputs for hydrology models).
- Temperature: downscaled to 5-km; bias-corrected; not publicly released as a standalone product.
- Available precipitation (APr): 1-km daily time series; bias-corrected and downscaled from HadRM3-PPE.
- Potential Evapotranspiration (PET): 5-km downscaled, then 1-km; monthly FAO56 Penman–Monteith estimates.
- Data storage:
  - FF-HadRM3-PPE-APr: 55 NetCDF files (11 ensemble members × 5 time periods) totaling ~18.5 GB.
  - FF-HadRM3-PPE-PE: 55 NetCDF files (monthly PET) totaling ~1.25 GB.
  - FF-HydMod-CatID: CSV files per site with 11 ensemble members; 1951–2098.
  - Lumped catchment APr/PE: CSV per dataset for 11 ensemble members.
  - National maps: PNGs of 2050s river flow changes (per statistic) for ~1,000 catchments, mapped to river reaches.
  - Regional groundwater: MABSWEC ASCII grids (.asc) for six 30-year slices; March, June, September, December means.
- Access and acknowledgement:
  - DOIs and gateway URLs provided; licensing terms apply; CEH Gateway and NRFA/BGS hosting.

## Section-by-section data details (GIS-relevant)
- FF-HadRM3-PPE: high-resolution climate inputs (1-km) for hydrology modelling; enables spatially explicit runoff and groundwater analyses.
- APr (Available Precipitation): daily inputs at 1-km for hydrological and groundwater models; essential for GIS-based catchment analyses.
- PET: auxiliary driver for hydrological modelling; provided at 1-km resolution.
- FF-HydMod-CatID: site-based ensemble river flow and groundwater level time series; useful for raster-to-point analysis and time-series GIS work.
- National river flow maps: GB-wide, suitable for large-scale impact mapping and policy-oriented visuals.
- Regional groundwater maps: regional context for aquifer-specific planning and risk assessment.
- Regional and national data formats: NetCDF (climate), CSV (catchment/time series), PNG (maps), ASC (gridded groundwater changes).

## Modelling approaches and caveats
- Climate inputs are bias-corrected and downscaled from HadRM3-PPE; not physically based, so some discrepancies with real climate remain.
- 11 ensemble members capture climate variability; results are not exact historical weather sequences but represent plausible futures.
- CERF-based river flow changes use change-factor methodology to downscale future climate signals to catchments and river reaches.
- CLASSIC/ZOOM models require model-specific inputs; climate data are provided for lumped-catchment use, not for all distributed models.

## Access, licensing, and references
- Data available through CEH Gateway, National River Flow Archive, and British Geological Survey sites.
- Licensing: non-commercial use free; commercial use may incur fees; licensing terms must be agreed prior to download.
- Citations required when using datasets (DOIs provided for FF-HadRM3-PPE and FF-Hydrology).

## Practical GIS applications
- Compare 2050s river flow changes across multiple ensemble realizations to assess risk hotspots.
- Create GIS layers showing mean monthly flow changes and high/low-flow percentile shifts for planning.
- Integrate time-series data (river flow, groundwater levels) with local observations for validation and scenario analysis.
- Use regional groundwater maps to support regional aquifer management and impact assessments.
- Develop decision-support briefing maps and reports for policymakers and stakeholders.