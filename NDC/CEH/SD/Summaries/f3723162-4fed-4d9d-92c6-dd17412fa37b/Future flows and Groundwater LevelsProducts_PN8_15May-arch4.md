# Future flows and Groundwater Levels - SC090016

- Purpose: Develop a nationally consistent framework to assess climate change impacts on river flows and groundwater across Great Britain by producing datasets and products based on the HadRM3-PPE UKCP09 ensemble. Aims to enable cross-location comparison, support adaptation, and inform decision-makers.

## Datasets and products

- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded climate time series (precipitation and potential evapotranspiration) for Great Britain, covering 1951–2098.
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater level time series for 282 river sites and 24 boreholes, derived from Future Flows Climate using HydMod models.
- 11-member ensemble of daily catchment-averaged precipitation and potential evapotranspiration time series for 282 river sites and 24 boreholes.
- National maps (snapshots) of changes in river flow statistics (mean monthly flows, low-flow statistics) for most large GB rivers.
- Regional maps of changes in groundwater level and river flow statistics for a selected region.
- Briefing notes for decision-makers on how to use the results.

## Data processing, formats, and access

- Climate time series are downscaled from 25-km HadRM3-PPE to 1-km resolution and bias-corrected to match observed statistics; a simple elevation-dependent snow-melt model accounts for snow processes. Available precipitation time series (APr) are derived and used as inputs for hydrological modeling.
- Temperature: downscaled and bias-corrected to 5-km; used to derive PE; intermediate product (not publicly released).
- Potential evapotranspiration (PE): computed at 5-km resolution using FAO56 Penman–Monteith; 1-km PE files provided for consistency with APr datasets.
- Data volumes: APr and PE datasets are large (e.g., 55 files each for APr and PE per ensemble, with multi-GB totals). Data are provided as NetCDF, with accompanying CSV/ASCII/PNG formats for specific products.
- Access and licensing: Datasets have Digital Object Identifiers (DOIs) and are accessible via the CEH Gateway, National River Flow Archive (NRFA), and British Geological Survey (BGS) websites under special licensing. Non-commercial use is free; commercial use may incur fees. Users must acknowledge the data with the specified citations.
- Regional and catchment modeling: For lumped groundwater models (PDM, CERF, BGS), ensemble catchment-average inputs are provided as CSV; for CLASSIC/ZOOM (distributed) models, climate information is available through FF Climate as needed. Regional groundwater maps for MABSWEC (Chalk aquifer) are provided as ASCII grids and PNGs.

## Access, acknowledgement and data governance

- FF-HadRM3-PPE climate data: DOI 10.5285/bad1514f-119e-44a4-8e1e-442735bb9797; downloadable via CEH Gateway; citation required.
- FF-Hydrology data: DOI 10.5285/f3723162-4fed-4d9d-92c6-dd17412fa37b; downloadable via CEH Gateway, NRFA, and BGS; citation required.
- Briefing notes accompany datasets; available in zipped packages and on project website for interpretation guidance.
- Coverage: England, Wales, Scotland; GB-wide framework with 11 ensemble members; time span 1951–2098; 1-km climate inputs for hydrological modeling; regional and national river flow and groundwater outputs.

## What this means for data leaders

- Supports a holistic data system view: provides a consistent, end-to-end framework linking climate projections to hydrology and groundwater outcomes across Great Britain.
- Enables user-centric, co-ownership style use: datasets are designed to be queried for various sectors (ecology, fisheries, water resources) and used for impact assessments with multiple realizations to capture climate variability.
- Improves data discoverability and comparability: standardized methodology, national scope, and clearly documented licenses and citations facilitate cross-region comparisons and benchmarking.
- Facilitates uncertainty analysis and scenario planning: 11 ensemble members and multiple output products (river flows, groundwater levels, and region-wide maps) support robust adaptation planning.
- Requires attention to governance and licensing: commercial usage may incur fees; users must adhere to licensing terms and provide proper acknowledgements.
- Highlights limitations to consider: outputs are bias-corrected and downscaled statistical products, not physically-based forecasts; some residual discrepancies with observations remain; historical weather sequences are not exactly reproduced within individual ensemble realizations.