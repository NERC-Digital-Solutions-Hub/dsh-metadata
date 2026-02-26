# Future Flows and Groundwater Levels - SC090016

## Executive summary
- The project aims to provide a nationally consistent framework of datasets and products to assess climate change impacts on water-related issues across Great Britain.
- Two main products:
  - National maps of changes in river flow statistics for most large GB rivers (2050s horizon).
  - Daily time series of river flows (1951–2098) at 282 river sites and groundwater levels at 40 boreholes, enabling analysis of climate-change impacts over time.
- Supports multiple outputs: time series, catchment-averaged series, and both national and regional change maps; designed to aid impact analyses in ecology, fisheries, and water availability.
- Outputs are available via dedicated web portals under licensing (non-commercial use free; commercial use may incur a fee). Data are citable with DOIs.

## Datasets and products
- FF-HadRM3-PPE (Future Flows Climate): 11-member ensemble of 1-km gridded climate time series (precipitation and potential evapotranspiration) for GB.
- FF-HydMod-CatID (Future Flows Hydrology): 11-member ensemble of daily river flow and monthly groundwater-level time series for 282 river sites and 24 boreholes.
- 11-member ensemble of daily catchment-average precipitation and PET time series for 282 river sites and 24 boreholes (derived from Future Flows Climate).
- National maps (snap shots) of changes in river-flow statistics for GB rivers (mean monthly flows and low-flow statistics).
- Regional maps (snap shots) of changes in groundwater levels and river-flow statistics for one region.
- Briefing notes for decision-makers on how to use results.

## Data processing and climate inputs
- HadRM3-PPE climate time series are downscaled to 1-km resolution and bias-corrected to align with observed historical statistics; 25-km HadRM3-PPE inputs are downscaled to incorporate sub-grid variability.
- Available precipitation (APr) time series are created to reflect rain/snow partitioning and snowmelt, feeding hydrological models.
- Potential evapotranspiration (PE) is computed at 5-km resolution using FAO56 Penman-Monteith and downscaled to 1-km consistency with APr.
- Temperature time series are downscaled and bias-corrected; these intermediate products are not publicly released.
- Time period covered: 1951–2098; data provided as NetCDF files; 11 ensemble members to capture climate variability.

## Access, licensing, and acknowledgement
- Data sets are associated with DOIs and are accessible through the CEH Environmental Informatics Data Centre Gateway (special licensing; non-commercial use free; commercial use potentially subject to a fee).
- Citations required when using the data (specific DOIs and acknowledgment wording provided in the document).
- Data sources and licensing terms are published on the CEH gateway and NRFA/BGS websites.

## FF Climate details and formats
- FF-HadRM3-PPE provides 11 ensemble members at 1-km resolution for 1951–2098; outputs include:
  - 1-km daily available precipitation (APr) time series (55 files total for all ensembles and periods, ~18.5 GB).
  - 1-km monthly/ daily potential evapotranspiration (PE) time series (55 files total for all ensembles and periods, ~1.25 GB).
- Temperature is downscaled/bias-corrected but not publicly released as an intermediate product.
- Data delivered as NetCDF files (standard for gridded time series).

## Hydrology and groundwater modeling
- Hydrology models (e.g., PDM, CERF, BGS) use APr and PE time series; lumped models require catchment-averaged inputs; semi-distributed models (CLASSIC, ZOOM) need highly grid-specific inputs, with climate data extractable from FF Climate as needed.
- FF-HydMod-CatID provides, for each of 282 river sites and 40 boreholes, an 11-member ensemble of daily river flows and monthly groundwater levels (1951–2098). Available as per-site CSV files (one or two files if multiple hydrological models are used).
- Additional catchment-average climate time series (APr and PE) are available for lumped-model catchments.

## National and regional maps
- National river-flow maps (for GB) show changes in mean monthly flows and exceedance statistics (Q95, Q70, Q10) by 2050s across over 1,000 catchments using CERF-based modelling.
- Regional groundwater maps cover the MABSWEC Chalk aquifer region, showing changes in mean groundwater levels for March, June, September, and December across six 30-year slices (2030s–2080s) for each of 11 climate projections.
- Outputs are provided as PNG (maps) and ASC (gridded data) files, with regional data accessible via BGS and Future Flows portals.

## Briefing notes and end-user guidance
- Briefing notes accompany datasets to assist scientists, water managers, and policymakers; designed for non-scientific readers and provide interpretation guidance and usage recommendations.
- Notes are supplied with data packages and available on project pages.

## References and related methodologies
- Key references include FAO Crop Evapotranspiration guidelines (FAO-56), elevation-dependent snowmelt modeling, and CERF input-estimation methods, reflecting the methodological foundation for climate downscaling, bias correction, and hydrological modelling.