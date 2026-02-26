# Future flows and Groundwater Levels - SC090016

## Overview
- A national, consistent framework of datasets and products to assess climate change impacts on river flows and groundwater across Great Britain.
- Based on HadRM3-PPE ensemble runs (UKCP09) to generate multiple realizations of future climate and hydrological responses.
- Key outputs include gridded climate time series, hydrological time series, catchment averages, and maps of changes, plus decision-maker briefing notes.
- Access is via dedicated web portals with licensing; non-commercial use is free, commercial use may incur fees.

## Datasets and Products
- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded daily precipitation and potential evapotranspiration time series for Great Britain (1951–2098).
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater levels at 282 river sites and 24 boreholes (from FF Climate via hydrological/groundwater models).
- 11-member ensemble of daily catchment-average precipitation and PET time series for the same 282 sites and 24 boreholes.
- National maps of changes in river flow statistics (mean monthly flows, low-flow statistics) for most large rivers.
- Regional maps of changes in groundwater level and river flow statistics for one region.
- Briefing notes for decision-makers on how to use results.

## Access, Licensing, and Acknowledgement
- All products available under licensing conditions; non-commercial use free; commercial use may require a fee.
- Requires full citation (DOIs provided) and acknowledgement of data custodians (CEH, BGS, Environment Agency, Defra, UKWIR).
- FF-HadRM3-PPE climate data accessible via CEH Gateway, NRFA, and BGS with project DOIs.
- FF-Hydrology data accessible via CEH Gateway, NRFA, and BGS with project DOIs.

## Data Formats, Volume, and Transfer
- FF-HadRM3-PPE: NetCDF files; 1951–2098; 11 ensemble members; 1-km resolution after downscaling.
- Available precipitation (APr): 11 ensemble members saved as 55 files; total ~18.5 GB.
- Potential evapotranspiration (PE): 11 ensemble members saved as 55 files; total ~1.25 GB.
- Temperature downscaled to 5-km for bias correction; intermediate 5-km series not publicly released.
- Data volumes reflect large, gridded time series suitable for hydrological and groundwater modelling.

## Methodology and Assumptions
- HadRM3-PPE outputs at 25-km resolution; bias-corrected and downscaled to 1-km to capture spatial heterogeneity and improve hydrological realism.
- Snow processes modelled with elevation-dependent snow-melt; snowpack timing affects runoff availability.
- Available precipitation (APr) used as input to hydrological/groundwater models; AP r series derived from bias-corrected precipitation and temperature.
- Potential evapotranspiration computed via FAO56 Penman-Monteith; 1-km PET used for hydrological modelling.
- Climate time series span 1951–2098; 11 ensemble members under the A1B scenario to capture climate variability.
- Outputs do not reproduce exact historical weather sequences; they provide multiple realizations of plausible climate and hydrological responses.

## Hydrological Modelling
- Two modelling approaches:
  - Lumped catchments (PDM, CERF, BGS): require catchment-averaged inputs; provide CSV time series of APr and PE for each ensemble member (1951–2098).
  - (Semi-)distributed models (CLASSIC and ZOOM): rely on grid-based inputs; climate data can be extracted from FF Climate as needed rather than delivered as separate climate datasets.
- For lumped models, APr and PE time series are delivered as two CSV files per catchment (one for APr, one for PE) per ensemble member.

## Section Highlights and Outputs
- Section II: Future Flows Climate details the ensemble construction, downscaling, bias correction, and data products (temperature, precipitation, and PET) and their public availability.
- Section III: Ensemble catchment-average climate time series for lumped models (APr and PE) and access restrictions for grid-specific data.
- Section IV: Future Flows Hydrology describes the river-flow and groundwater-level time series at study sites, ensemble structure, and access.
- Section V: National river-flow maps illustrating 2050s changes across Great Britain using 11 climate realizations; methodology involves CERF rainfall-runoff modelling and change-factor downscaling.
- Section VI: Regional groundwater maps (MABSWEC region) showing changes in mean monthly groundwater level for March, June, September, and December across six 30-year slices.
- Section VII: Briefing notes prepared to aid interpretation and application by scientists, managers, and policymakers.
- Section VIII: References to foundational methods and models (e.g., FAO-56, CERF, snowmelt modelling).

## Use Cases and Applications
- Enables consistent, comparable assessments of climate-change impacts on river flow and groundwater across Britain.
- Supports risk assessment, water resource planning, ecology and fisheries studies, and policy development by providing multiple climate realizations and associated hydrological responses.
- Facilitates uncertainty analysis and scenario comparison through ensemble outputs and national/regional mapping of changes.