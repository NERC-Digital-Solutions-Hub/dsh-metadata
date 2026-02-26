# Future flows and Groundwater Levels - SC090016

## Executive summary
- Project to provide datasets and products for assessing climate change impacts on water across Great Britain within a nationally consistent framework.
- Based on the Hadley Centre regional climate model ensemble (HadRM3-PPE) underlying UKCP09 scenarios.
- Generated datasets/products include:
  - FF-HadRM3-PPE: 11-member ensemble of 1-km gridded climate time series (precipitation and potential evapotranspiration).
  - FF-HydMod-CatID: 11-member ensemble of daily river flow and monthly groundwater levels for 282 river sites and 24 boreholes.
  - 11-member ensemble of daily catchment-averaged precipitation and PET time series for the same sites.
  - National maps of changes in river flow statistics for most large GB rivers.
  - Regional maps of groundwater level and river flow statistics for one region.
  - Briefing notes for decision-makers.
- Temporal coverage: 1951–2098; spatial resolution: 1-km (climate), with regional/ catchment aggregates for hydrology.
- Access via dedicated web pages with licensing; non-commercial use free, commercial use potentially fee-based.

## Datasets and products (what’s produced)
- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded climate time series (precipitation and potential evapotranspiration) for GB.
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater levels at 282 river sites and 24 boreholes.
- 11-member ensemble of daily catchment-average precipitation and PET time series for 282 river sites and 24 boreholes.
- National maps (snapshots) of changes in river flow statistics for most large GB rivers (mean monthly flows, low-flow statistics).
- Regional maps (snapshots) of changes in groundwater level and river flow statistics for one region.
- Briefing notes for decision-makers on use of results.

## Data formats and access
- FF-HadRM3-PPE climate data provided as NetCDF files (1-km resolution, 1951–2098; 11 ensemble members).
- Available precipitation and temperature-derived datasets include:
  - Available precipitation (APr): 25-km downscaled to 1-km, bias-corrected, 1950–2098; stored as multiple NetCDF files for speed.
  - Potential evapotranspiration (PE): 1-km resolution, monthly, 1950–2098; stored as multiple NetCDF files.
- Catchment-average climate time series (APr and PE) for lumped models (PDM, CERF, BGS) provided as two CSV files per dataset, covering 1951–2098 (11 ensemble members).
- For classic/ZOOM (semi-distributed) models, climate data are not provided as aggregated files; climate information can be extracted from FF-HadRM3-PPE data as needed.
- Hydrology product (FF-HydMod-CatID) delivered as per-site CSV files (one file per site, containing 11 ensemble members; some sites have multiple model outputs).
- National river flow maps: PNG files showing changes by the 2050s for each GB river and each statistic (mean flow, monthly flows, Q95, Q70, Q10).
- Regional groundwater maps: ASCII grid (.asc) files for changes in mean monthly groundwater level (March, June, September, December) for six 30-year slices (2030s–2080s) across the MABSWEC region; additional regional groundwater maps (PNG) available via BGS.
- Access and acknowledgement:
  - DOIs and gateway access provided; data available under special licensing.
  - Non-commercial use free; commercial use may require a fee.
  - Data must be cited with the provided DOIs in any use.

## Project background and methods (key points)
- Rationale: climate change will alter river flows and groundwater recharge; need consistent UK-wide datasets to enable comparative assessment and adaptation planning.
- Climate data characteristics:
  - HadRM3-PPE time series at 25-km resolution, bias-corrected and downscaled to 1-km to capture spatial heterogeneity and ensure hydrological relevance.
  - Snowmelt and snow/ice considerations incorporated; available precipitation time series (APr) used as input to hydrological models.
  - Temperature downscaled and bias-corrected; PE computed with FAO56 Penman-Monteith method at monthly time steps.
  - 11 ensemble members to represent climate variability and uncertainty; outputs are designed to reflect plausible future climates under the A1B scenario.
- Data products are designed to enable both time-series analysis and spatial comparisons (national and regional scales).

## Temporal and spatial scope
- Climate time series: 1951–2098, 1-km resolution (climate inputs for hydrology).
- Hydrology: daily river flow and monthly groundwater levels for 282 river sites and 24 boreholes (1951–2098).
- Groundwater regional maps: six 30-year slices (2030s to 2080s) for the MABSWEC Chalk aquifer region; four monthly snapshots per slice.

## Access, licensing, and attribution
- Data hosted on CEH gateway and related UK institutions (NRFA, BGS).
- DOIs provided for climate and hydrology data; must be cited in all uses.
- Licensing terms: non-commercial use free; commercial use may require agreement and fees.

## How GIS specialists can use these data
- Climate inputs: NetCDF FF-HadRM3-PPE suitable for driving hydrological models or for direct statistical mapping of climate variables at 1-km resolution.
- Hydrology: per-site CSV time series enable GIS analysts to join with river networks and groundwater boreholes for spatial analyses, scenario comparisons, and uncertainty assessments.
- Catchment averages: CSV files allow rapid aggregation for lumped models or cross-site comparisons within catchments.
- Spatial outputs:
  - National river flow maps (PNG) for quick visualization of 2050s changes across GB rivers.
  - Regional groundwater maps (ASC/PNG) for focused groundwater planning in the MABSWEC region.
- Documentation and briefing notes: interpretive guidance for non-specialists to facilitate policy and management decisions.
- Data integration: when required, climate data can be downscaled or enhanced within existing GIS workflows; multiple ensemble members enable probabilistic or uncertainty analyses.

## Notes for users
- Climate data are not raw historical weather sequences; they are designed to represent plausible climate realizations for future periods with downscaled bias-corrected properties.
- Some intermediate products (e.g., 5-km temperature) are not publicly released; final 1-km climate inputs (APr, PE) and downstream hydrology outputs are the focus for public access.
- For model-specific climate inputs (CLASSIC/ZOOM), users may need to extract relevant climate information from FF-HadRM3-PPE rather than accessing pre-packaged climate time series.

## References
- Key methodological references include FAO guidance on evapotranspiration, elevation-dependent snowmelt modelling, and continuous estimation of river flows (CERF).