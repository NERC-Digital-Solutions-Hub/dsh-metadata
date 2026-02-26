# Future flows and Groundwater Levels - SC090016

## Executive overview
- Aimed to provide nationally consistent datasets and products to assess climate change impacts on river flows and groundwater across Great Britain.
- Based on HadRM3-PPE ensemble (UKCP09), producing multiple climate and hydrology-focused outputs for robust impact analyses.
- Key products include climate time series, hydrology time series, national and regional river flow maps, regional groundwater maps, and decision-maker briefing notes.
- Data access is via dedicated portals with licensing; non-commercial use is free, commercial use may incur fees.

## Datasets and products
- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded daily precipitation and potential evapotranspiration (PET) time series for Great Britain.
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater level time series for 282 river sites and 24 boreholes.
- 11-member ensemble of daily catchment-average precipitation and PET time series for 282 river sites and 24 boreholes.
- National maps (snap shots) of changes in river flow statistics for most large GB rivers.
- Regional maps of changes in groundwater level and river flow statistics for one region.
- Briefing notes for decision-makers on how to use results.

## Data details and methodology
- Temporal coverage: 1951–2098; designed to explore climate change effects over the next century.
- Spatial resolution: climate time series at 1-km; original HadRM3-PPE operates at 25-km with downscaling and bias correction to reflect small-scale variation.
- Data formats and volumes:
  - FF-HadRM3-PPE AP r: 55 NetCDF files (11 ensemble members × 5 time spans) totaling about 18.5 GB per file set; entire AP r dataset ranges 1950–2098.
  - FF-HadRM3-PPE-PE (PET): 55 NetCDF files, about 1.25 GB each; entire PE dataset ranges 1950–2098.
- Bias correction and downscaling:
  - Temperature downscaled to 5-km then bias-corrected; used to generate 1-km inputs.
  - Available precipitation (APr) derived from bias-corrected precipitation with a snow-melt model to reflect surface water availability for hydrological models.
- Climate outputs are ensemble-based to capture natural climate variability; not intended to reproduce historical weather sequences exactly.
- Temperature detail: intermediate 5-km downscaled/bias-corrected series; not publicly released.
- Data accessibility: NetCDF format for climate time series; large data volumes necessitate segmented downloads; DOIs assigned for data sets.

## Access, licensing, and acknowledgment
- Data hosted on CEH Gateway and related repositories; licensing governs non-commercial vs. commercial use.
- DOIs for datasets:
  - Future Flows Climate: Prudhomme et al., 2012; doi provided; to be cited in all uses.
  - Future Flows Hydrology: Haxton et al., 2012; doi provided; to be cited in all uses.
- Access points:
  - CEH Gateway (special licensing), National River Flow Archive (NRFA), British Geological Survey (BGS) websites.
  - National River Flow Archive and BGS pages host model-specific inputs and outputs.
- Acknowledgement and citation are required when using datasets.

## Output structure by product type

- FF-HydMod-CatID (Future Flows Hydrology)
  - 282 river sites and 40 boreholes; 11 ensemble members; daily river flow and monthly groundwater levels.
  - Availability: as CSV for lumped-model catchments; multiple files may exist if more than one hydrological model was used.
  - Access/acknowledgement: DOI and CEH gateway/NRFA/BGS pages with special licensing.

- FF-HadRM3-PPE climate time series and derived inputs
  - 11-member climate ensemble; 1-km gridded precipitation and available precipitation; 1-km PET-derived inputs.
  - AP r and PET outputs stored as multiple NetCDF files to improve download/manageability.
  - Temperature time series exist but are intermediate and not public.

- Catchment-average climate time series
  - For lumped models (PDM, CERF, BGS): CSV files with catchment-averaged AP r and PE across all ensemble members (1951–2098).
  - For CLASSIC/ZOOM models: climate data not provided at catchment level; climate insights can be extracted from FF-HadRM3-PPE data.

- National river flow maps (2050s)
  - Eleven sets (one per FF-HadRM3-PPE ensemble member) showing changes in mean monthly flows and exceedance percentiles (Q95, Q70, Q10).
  - Derived using CERF rainfall-runoff models across 1,000+ catchments; changes linked to observed baseline rainfall/runoff.

- Regional groundwater and river flow maps
  - Groundwater level changes for MABSWEC Chalk aquifer region; six 30-year time-slices (2030s–2080s) and four seasonal months per slice.
  - Outputs provided as ASCII grids (.asc) and regional maps (.png); available via BGS and future-flows portals.

- Briefing notes
  - Prepared to aid interpretation for scientists, water managers, and policymakers; written for non-scientific readers.
  - Included with data packages to guide usage and interpretation.

## Practical implications for data support
- Enables cross-location comparison due to a consistent methodological framework; supports spatio-temporal analysis of climate change impacts on GB rivers and groundwater.
- Provides multiple realizations to quantify climate variability and associated hydrological responses.
- Requires attention to licensing for commercial use and handling of large NetCDF/CSV data volumes; proper citation essential for all uses.
- Useful for downstream analyses in fisheries, ecology, water resource planning, and policy development.

## References
- FAO Penman-Monteith method (Allen et al., 1998) for PET.
- Snowmelt modelling (Bell & Moore, 1999).
- CERF methodology for precipitation inputs (Keller et al., 2006).