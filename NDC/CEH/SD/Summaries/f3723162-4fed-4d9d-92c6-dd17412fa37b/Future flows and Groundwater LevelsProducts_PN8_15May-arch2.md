# Future flows and groundwater levels - SC090016

## Executive summary
- A climate-change impact assessment project for Great Britain, delivering standardized datasets and products to evaluate river flows and groundwater levels over time.
- Based on 11-member HadRM3-PPE regional climate model ensembles (UKCP09 framework) with downscaling and bias correction to enable hydrological modelling.
- Outputs include:
  - Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded precipitation and potential evapotranspiration time series (1951–2098).
  - Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater levels at 282 river sites and 24 boreholes.
  - 11-member ensemble of precipitation and PET catchment-averaged time series for the same sites.
  - National and regional maps showing changes in river flow statistics (mean monthly flows, low-flow statistics) and groundwater/river flow indicators.
  - Briefing notes for decision-makers.
- Data are available under licensing (non-commercial free; commercial use may incur fees). DOIs and gateway access provided.

## Datasets and products
- FF-HadRM3-PPE: 11-member ensemble of 1-km gridded daily precipitation and PET time series for Great Britain (1951–2098).
- FF-HydMod-CatID: 11-member ensemble of daily river flow and monthly groundwater levels for 282 river sites and 24 boreholes.
- 11-member ensemble of daily catchment-averaged precipitation and PET time series for the same sites.
- National maps (snap shots) of changes in river-flow statistics for most large rivers.
- Regional maps of changes in groundwater level and river-flow statistics for one region.
- Briefing notes for decision-makers.

## Access, licensing and acknowledgement
- Data are distributed via dedicated websites under licensing agreements; non-commercial use is free; commercial use may require a fee.
- FF-HadRM3-PPE data has DOI: 10.5285/bad1514f-119e-44a4-8e1e-442735bb9797; datasets available through the CEH Environmental Informatics Data Centre Gateway.
- FF-HydMod-CatID data has DOI: 10.5285/f3723162-4fed-4d9d-92c6-dd17412fa37b; accessible via CEH Gateway, NRFA, and BGS with special licensing.
- Acknowledgement and citation requirements are specified for both FF-Climate and FF-Hydrology datasets.

## Methodology and data processing (key points)
- HadRM3-PPE climate time series are downscaled to 1-km and bias-corrected to align with observed statistics, addressing known biases in regional climate models.
- Available precipitation (APr) time series are derived from bias-corrected, downscaled precipitation and temperature inputs, used for hydrological modelling.
- Potential evapotranspiration (PET) is computed at 5-km resolution using FAO56 Penman-Moore methods and then provided at 1-km resolution for consistency with input data.
- Time series span 1951–2098; 11 ensemble members are designed to capture climate variability and provide multiple realizations rather than exact historical sequences.
- Data are provided in NetCDF for climate time series; APr and PET data also supplied as CSV/NetCDF; some supporting data (e.g., model inputs) are distributed as ASCII grids or PNG maps.

## Data formats and storage
- Climate time series: NetCDF files (1-km resolution; 11 ensemble members; 1951–2098).
- Available precipitation and PET: separate NetCDF/CSV files (per ensemble member; 1951–2098).
- River flow and groundwater levels (FF-HydMod-CatID): CSV files per site with 11 ensemble members; separate files if multiple hydrological models are used.
- National/regional maps: PNG image files illustrating changes by 2050s or other horizons.
- Regional groundwater changes: ASCII grid (.asc) files and PNG maps for the MABSWEC region.
- Briefing notes: provided in zipped data packages.

## How analysts can use these products
- Enables consistent, comparable assessment of climate-change impacts on water resources across Great Britain.
- Supports long-term planning and policy evaluation by providing multiple climate realizations and time-series data rather than single, interpolated projections.
- Facilitates integration with other monitoring datasets (ecology, fisheries, water availability) due to standardized formats and broad spatial coverage.
- Helps quantify changes in river-flow statistics (mean flows, low-flow metrics) and groundwater levels, supporting adaptation planning and resilience assessments.

## Notes on scope and limitations
- Climate time series are statistically downscaled and bias-corrected; while designed for hydrological applications, they are not physically perfect reproductions of real climate.
- The 11 ensemble members capture variability but do not reproduce exact historical weather sequences; results are best used for scenario analysis and trend assessment rather than exact forecasts.
- Some data products (e.g., temperature intermediate series) are not publicly released to focus on inputs relevant to hydrological modelling.

## End-user guidance
- Reference the provided DOIs and gateway URLs when using the data.
- Adhere to licensing terms, especially for commercial use.
- Utilize briefing notes to interpret methodology and applicability for specific fisheries, ecology, or water-resource planning tasks.