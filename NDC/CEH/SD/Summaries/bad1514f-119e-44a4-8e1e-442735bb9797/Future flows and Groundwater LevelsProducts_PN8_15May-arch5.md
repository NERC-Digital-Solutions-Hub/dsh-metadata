# Future flows and Groundwater Levels - SC090016

## Overview
- Provides a nationally consistent framework to assess climate change impacts on river flows and groundwater across Great Britain.
- Based on ensemble runs from the Hadley Centre regional climate model HadRM3-PPE (UKCP09) producing multiple data products and datasets.
- Outputs support impact assessment for water availability, ecology, fisheries, and policy decisions.
- All products are available under licensing; non-commercial use is free, commercial use may incur fees agreed with licensing teams.
- Key data portals: CEH Gateway, National River Flow Archive (NRFA), British Geological Survey (BGS) websites; data are associated with DOIs.

## Datasets and products
- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded daily precipitation and potential evapotranspiration (PET) for Great Britain, spanning 1951–2098.
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater levels at 282 river sites and 24 boreholes, derived from FF Climate using HydMod models.
- 11-member ensemble of daily catchment-averaged precipitation and PET time series for the same sites, derived from FF Climate (for lumped-model inputs).
- National maps of changes in river flow statistics for major GB rivers (mean monthly flows and low-flow statistics).
- Regional maps of groundwater level and river flow statistics for one region (MABSWEC) using regional modeling.
- Briefing notes for decision-makers on how to use results.

## Processing, formats, and scope
- Climate data (FF-HadRM3-PPE) are downscaled from 25-km HadRM3-PPE with bias correction to align with observed statistics; 1-km resolution used for input to hydrological models.
- Available precipitation (APr) time series are generated to reflect snow/ice processes and monthly/daily variability; used as primary input to hydrological models.
- Potential evapotranspiration (PET) is computed at 5-km (monthly FAO56 Penman-Monteith) and reported at 1-km for consistency with APr.
- Time series cover 1951–2098; ensemble consists of 11 realizations to capture climate variability.
- Outputs are delivered as NetCDF (FF-HadRM3-PPE) for climate variables, CSV (catchment-averaged APr and PE for lumped models), ASCII grids (regional groundwater changes), and PNG (maps of flow changes).
- Data formats:
  - FF-HadRM3-PPE: NetCDF (1-km resolution, daily time steps).
  - Catchment-averaged inputs for lumped models: CSV (APr and PE, 11 ensemble members, 1951–2098).
  - PET/precipitation inputs for some models: separate NetCDF/CSV as applicable.
  - National river flow maps: PNG (for 2050s scenarios; 11 members from CERF-based simulations).
  - Regional groundwater maps: ASCII .asc grids and PNGs for regional visualization.
- Coverage and outputs:
  - England, Wales and Scotland; 282 river sites and 24 boreholes (plus 40 boreholes in FF-HydMod-CatID context).
  - National river flow statistics and 2050s scenario maps; regional maps for MABSWEC region.
  - Six 30-year time-slices for regional groundwater changes (2030s–2080s across six decades; 264 ASCII files).

## Access, licensing, and acknowledgement
- Digital Object Identifiers (DOIs) provided for primary datasets:
  - Future Flows Climate: 10.5285/bad1514f-119e-44a4-8e1e-442735bb9797
  - Future Flows Hydrology: 10.5285/f3723162-4fed-4d9d-92c6-dd17412fa37b
- Access via CEH Gateway, NRFA, and BGS with special licensing conditions.
- Acknowledgement required in usage with full citation of DOIs and project authors.
- Briefing notes accompany datasets to aid interpretation for scientists, managers, and policymakers.

## Data governance and stewardship considerations
- Consistent methodological framework enables cross-location comparability for governance and adaptation planning.
- Licensing terms must be reviewed and agreed prior to download; non-commercial usage is free, commercial usage may require fee agreements.
- Detailed provenance, model choices (lumped vs semi-distributed), and bias-correction/downscaling steps are documented to support data quality assessments and reproducibility.
- Data volumes are substantial (e.g., 18.5 GB per APr dataset group; multiple ensemble and file types), requiring efficient data management and metadata literacy.
- Data to support future-flow decision-making includes both climate inputs and derived hydrological outputs, enabling end-to-end analysis under UKCP09 scenarios.