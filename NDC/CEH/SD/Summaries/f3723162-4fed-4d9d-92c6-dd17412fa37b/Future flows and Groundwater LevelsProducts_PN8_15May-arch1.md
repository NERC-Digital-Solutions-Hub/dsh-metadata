# Future Flows and Groundwater Levels - SC090016

## Overview
- Aims to provide datasets and products to assess climate-change impacts on river flows and groundwater across Great Britain within a nationally consistent framework.
- Based on ensemble runs from the Hadley Centre regional climate model HadRM3-PPE (under UKCP09 scenarios), generating 11-member ensembles for multiple datasets.
- Outputs enable evaluation of changes in river flow and groundwater levels from 1951 to 2098 with multiple realizations to capture climate variability.
- Products include national and regional maps, time series at numerous sites, and briefing notes for decision-makers.
- Access is licensed: non-commercial use is free; commercial use may incur fees via CEH/BGS licensing teams.

## Datasets and Products
- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded time series for precipitation and potential evapotranspiration (PET); covers Great Britain.
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater levels for 282 river sites and 24 boreholes (derived from Future Flows Climate using HydMod).
- 11-member ensemble of daily catchment-averaged precipitation and PET time series for 282 river sites and 24 boreholes.
- National maps of changes in river flow statistics for most large GB rivers (mean monthly flows and low-flow statistics).
- Regional maps of changes in groundwater level and river flow statistics for one region.
- Briefing notes for decision-makers on using results.
- All datasets are available via dedicated web pages with licensing conditions.

## Data Characteristics and Processing
- Climate time series: 1951–2098, downscaled from 25-km HadRM3-PPE to 1-km, bias-corrected to match observations; spatial downscaling incorporates sub-grid variability.
- Available precipitation (APr): created by applying snow-melt and temperature adjustments; used as input to hydrological and groundwater models.
- Potential evapotranspiration (PET): derived at 5-km resolution (downscaled temperature) using FAO56 Penman-Monteith; 1-km PET time series provided for consistency with APr.
- Data formats and volume: climate data (NetCDF), APr and PET time series saved in multiple files to improve access (e.g., 55 files for APr and 55 for PET per ensemble); large total data volume (~18.5 GB for APr and 1.25 GB per PET subset).
- Model inputs: lumped (PDM/CERF/BGS) catchments use catchment-averaged APr and PE; CLASSIC and ZOOM models require gridded inputs, with climate data extractable from FF Climate as needed.
- Uncertainty and limitations: HadRM3-PPE time series are not physically identical to observed weather sequences; biases corrected but residual differences remain; downscaling methods are statistical, not physically-based.

## Access, Licensing, and Acknowledgement
- Datasets have DOIs and must be cited when used:
  - FF Climate: Prudhomme et al., 2012, DOI provided.
  - FF Hydrology: Haxton et al., 2012, DOI provided.
- Access portals: CEH Gateway, National River Flow Archive (NRFA), British Geological Survey (BGS) websites.
- Licensing: dedicated agreements; non-commercial use free; commercial use may require a fee and licensing approval.
- Briefing notes accompany datasets and are also available on project pages.

## Regions and Data Details
- National River Flow maps: 11 ensemble members showing 2050s changes in river flow statistics via CERF models across >1,000 catchments; regionalized to river reaches within catchments.
- Regional groundwater mapping (MABSWEC): regional Chalk aquifer study; 264 ASCII grid files of changes in mean groundwater levels for March, June, September, December across six 30-year slices (2030s–2080s); 11 projections.
- Access to regional maps: available as PNG maps or ASCII grids via BGS and FF portals.

## Briefing and Use Cases
- Briefing notes designed for scientists, water managers, and policymakers; explain methodology, interpretation, and guidance for using datasets.
- Suitable for analyses of fishery, freshwater ecology, water availability, and climate-change impact planning; enables cross-region comparisons and scenario testing.

## Key Considerations for Analysts
- Use FF-HadRM3-PPE climate time series to drive hydrological and groundwater models, keeping in mind downscaling and bias correction uncertainties.
- Leverage multiple ensemble realizations (11 members) to quantify climate variability and uncertainty in river flow and groundwater projections.
- When working with lumped models, prefer catchment-averaged APr and PE inputs; for grid-based models, extract climate inputs from FF Climate as needed.
- Utilize national and regional maps to frame anticipated changes by horizon (e.g., 2050s) and to identify hotspots for resource planning.
- Reference DOIs and licensing terms in any dissemination or publication of results.