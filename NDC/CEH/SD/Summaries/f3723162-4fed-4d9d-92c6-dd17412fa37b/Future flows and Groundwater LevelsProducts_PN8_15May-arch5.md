# Future flows and Groundwater Levels - SC090016

## Overview
- Aimed to provide datasets and products for assessing climate change impacts on river flows and groundwater across Great Britain within a nationally consistent framework.
- Based on HadRM3-PPE ensemble (UKCP09) with 11 ensemble members; covers 1951–2098.
- Deliverables support cross-location comparability and inclusion of climate variability, enabling impact analyses for water availability, ecology, fisheries, and policy decisions.
- All products are available via dedicated web pages under licensing; non-commercial use is free, commercial use may be fee-based.

## Datasets and products
- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded precipitation and potential evapotranspiration time series for Great Britain.
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater level time series for 282 river sites and 24 boreholes, derived from Future Flows Climate using HydMod.
- 11-member ensemble of daily catchment-average precipitation and PET time series for 282 river sites and 24 boreholes (derived from Future Flows Climate).
- National maps of changes in river flow statistics (mean monthly flows, low-flow statistics) for most large rivers of Great Britain.
- Regional maps of changes in groundwater level and river flow statistics for one region.
- Briefing notes for decision-makers on how to use the results.

## Data formats and structure
- FF-HadRM3-PPE: climate time series, 1-km resolution; daily time series; 11 ensemble members; 1951–2098.
- APr (Available precipitation) and PE (Potential evapotranspiration): downscaled and bias-corrected daily/hourly inputs to hydrological models.
  - APr data: stored as multiple NetCDF files (55 files for APr across ensemble members and periods) due to size; 1950–2098.
  - PE data: stored as multiple NetCDF files (55 files) for ensemble members and periods; 1950–2098.
- Temperature: downscaled/bias-corrected 5-km series used for internal processing; not publicly released.
- FF-HydMod-CatID: CSV files with 11 ensemble members per site; two files if two hydrological models are used; 1951–2098.
- Lumped catchment climate averages (PDM/CERF/BGS): CSV files for APr and PE time series per catchment; available for lumped-model catchments only.
- Regional groundwater maps (MABSWEC): ASCII grid (.asc) files for mean monthly groundwater changes (Mar, Jun, Sep, Dec) across six 30-year slices (2030s–2080s) for each of 11 climate projections; also regional PNG maps via BGS site.
- Regional groundwater maps (MABSWEC) availability: PNG maps via BGS; ASCII grids via CEH/Future Flows pages.
- Briefing notes: provided with datasets in zipped packages.

## Access, licensing, and attribution
- Data are distributed via CEH Gateway, National River Flow Archive, and British Geological Survey websites; licensing is required.
- Digital Object Identifiers (DOIs) for datasets:
  - Future Flows Climate: 10.5285/bad1514f-119e-44a4-8e1e-442735bb9797
  - Future Flows Hydrology: 10.5285/f3723162-4fed-4d9d-92c6-dd17412fa37b
- Access is granted under special licensing conditions; non-commercial use is free; commercial use may incur fees to CEH/BGS licensing teams.
- Proper citation required for use:
  - Prudhomme et al., 2012 for Future Flows Climate
  - Haxton et al., 2012 for Future Flows Hydrology
- Data sources and documentation are available on project websites; NetCDF is the primary format for climate data, CSV for catchment averages, ASCII grids for regional groundwater, and PNGs for map outputs.

## Methodology and data processing highlights
- Climate data: HadRM3-PPE outputs at 25-km resolution, downscaled to 1-km with bias correction to align with observed statistics; spatial downscaling to capture sub-grid variability and elevation effects; temperature bias-corrected using a 5-km observation-based series.
- Available precipitation (APr): accounts for snow-melt and snowpack impacts using elevation-dependent snow-melt modelling; converts to 1-km APr inputs for hydrological modelling.
- Potential evapotranspiration (PET): derived from HadRM3-PPE using FAO56 Penman-Monteith method at monthly scales; 1-km PET data provided for consistency with APr inputs.
- Hydrology and groundwater: multiple models used (lumped and semi-distributed, e.g., CERF, CERF-based approaches, HydMod); ensemble approach provides 11 realizations per catchment/site.
- River flow and groundwater maps: CERF-based approach for river-flow changes; regional groundwater modelling (MABSWEC) for changes across months and time-slices.
- Temporal scope and purpose: 1951–2098 time horizon to explore climate-change impacts and variability; designed to support cross-regional comparisons and adaptation planning.

## Use cases and guidance for data stewards
- Suitable for climate impact assessments on water resources, ecology, fisheries, and water planning across Great Britain.
- Enables exploration of temporal evolution of river flows and groundwater levels without simple linear interpolation; supports uncertainty analysis via multiple ensemble realizations.
- Briefing notes provide non-technical interpretation guidance for scientists, water managers, and policymakers.
- Regional and national maps help communicate potential changes to stakeholders and decision-makers.

## Considerations and caveats
- Climate time series are not exact historical weather sequences; they are designed to reproduce climate statistics and variability patterns, not replicate specific past years.
- Bias correction and downscaling are not physically-based; users should be aware of residual discrepancies with observed climate.
- Availability of some datasets is conditional on licensing; some data components (e.g., detailed 1-km precipitation inputs) are stored in multiple files to manage dataset size and access.
- For catchments modelled with lumped vs. distributed models, data availability differs; some climate inputs are not provided for fully distributed models, though relevant information can be inferred from FF Climate data.

## Summary of key outputs (by category)
- Climate time series: 11-member 1-km gridded precipitation and PET (1951–2098).
- Hydrology: 11-member daily river flow and monthly groundwater levels at 282 river sites and 24 boreholes (1951–2098).
- Catchment averages: 11-member daily catchment-average precipitation and PET time series.
- River flow statistics maps: national-scale changes by 2050s for large British rivers.
- Regional maps: groundwater and river-flow statistics for one region.
- Groundwater regional modelling: MABSWEC region maps and ASCII grids for six 30-year slices across the 21st century.
- Briefing notes: interpretation and usage guidance for datasets.

## Contact and provenance
- Authors and project teams from CEH, BGS, Environment Agency, Defra, UKWIR, and associated collaborators; funded by UK environmental and water agencies.
- Primary dissemination through CEH Gateway, NRFA, and BGS portals with licensing terms.