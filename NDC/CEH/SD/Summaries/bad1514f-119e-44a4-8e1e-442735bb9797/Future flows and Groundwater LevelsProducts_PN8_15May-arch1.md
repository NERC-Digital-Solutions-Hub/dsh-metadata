# Future flows and Groundwater Levels - SC090016

- Aim and scope
  - Develop a nationally consistent framework to assess climate change impacts on river flow and groundwater recharge across Great Britain.
  - Produce datasets and products enabling comparison across locations and over time, including multiple realizations of climate variability.
  - Cover a 1951–2098 period with a focus on the next 100 years for planning and adaptation.

- Key datasets and products
  - Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded climate time series (precipitation and potential evapotranspiration) derived from the HadRM3-PPE regional climate model ensemble underpinning UKCP09.
  - Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow time series and monthly groundwater levels for 282 river sites and 24 boreholes, derived from Future Flows Climate using hydrological/groundwater models (HydMod).
  - 11-member ensemble of daily catchment-average precipitation and PET time series for the same 282 river sites and 24 boreholes.
  - National maps of changes in river-flow statistics (mean monthly flows and low-flow statistics) for most large GB rivers.
  - Regional maps of changes in groundwater levels and river-flow statistics for one region.
  - Briefing notes for decision-makers on how to use the results.

- Data access and licensing
  - All datasets/products are available via dedicated CEH/BGS/NRFA portals under licensing; non-commercial use is free, commercial use may require an agreed fee.
  - Data are referenced with DOIs and must be cited in use (citations provided for FF-HadRM3-PPE Climate and FF-Hydrology).
  - Access details include the CEH Gateway and National River Flow Archive pages; briefing notes accompany data packages.

- Data characterization and methodology
  - HadRM3-PPE time series are at 25-km resolution and daily time steps; bias-corrected and downscaled to 1-km to better represent local hydrology.
  - Available precipitation series (APr) accounts for snow dynamics via elevation-dependent snow-melt modelling; continues to use a downscaling approach to 1-km.
  - Potential evapotranspiration (PET) is derived from FAO56 Penman-Monteith using downscaled temperature data; provided at 1-km resolution.
  - Climate time series span 1951–2098; 11 ensemble realizations capture climate variability; products are designed to represent plausible futures under UKCP09 A1B.
  - For hydrological modelling, APr and PET serve as inputs; lumped (PDM, CERF, BGS) and (semi-)distributed (CLASSIC, ZOOM) catchment approaches are used, with climate inputs supplied accordingly (lumped models receive catchment-averaged inputs; distributed models use gridded inputs or extract climate data as needed).
  - The climate time series are provided as NetCDF files (FF-HadRM3-PPE) and related inputs (APr/PE) in multiple files to facilitate download. Large data volumes are noted (tens of gigabytes per dataset group).

- Section-by-section products and access
  - Section II: FF-HadRM3-PPE climate time series (1951–2098, 1-km; 11 members) with downscaled temperature, available precipitation (APr), and PET (PE) datasets; NetCDF format.
  - Section III: Catchment-scale climate data for lumped models (PDM/CERF/BGS) provided as CSV with 11-member ensemble catchment-average APr and PE; for CLASSIC/ZOOM models, climate data are accessible via FF-HadRM3-PPE but not provided as pre-aggregated climate datasets.
  - Section IV: FF-Hydrology time series (1951–2098) for 282 river sites and 40 boreholes; 11-member ensembles; CSV per site (one file per site, containing all ensemble members); multiple models when used.
  - Section V: National river-flow maps (2050s) derived from CERF-based wide-area modelling; 11 member realizations showing changes in mean flow, monthly flows, and Q95/Q70/Q10 exceedance percentiles; maps produced at catchment scale and allocated to river reaches.
  - Section VI: Regional groundwater-change maps for the Marlborough/Berkshire Downs and southwestern Chilterns Chalk aquifer (MABSWEC) region; 11 projections across six 30-year slices; ASCII grids of changes in mean monthly groundwater level for March, June, September, December.
  - Section VII: Briefing notes to aid interpretation and use; provided with datasets and accessible on the project site.
  - Section VIII: References to foundational methods (FAO input methods, snowmelt model, CERF inputs).

- Geographic coverage and time horizons
  - Great Britain-wide climate and hydrology; GB river networks and 282 river sites plus 24 boreholes for groundwater levels.
  - 2050s river-flow changes (V.1) and six 30-year slices for regional groundwater (VI) extend through the 21st century.
  - Outputs enable analysis of climate-change impacts on river flows and groundwater at both national and regional scales, with multiple realizations to assess variability.

- Notable limitations
  - Climate time series are not physically identical to observed weather sequences; a bias-correction and downscaling approach is applied to align statistics with observations, but discrepancies remain inherent to downscaled model outputs.
  - PET and precipitation inputs are model-derived; some sub-grid variability and local processes may not be fully captured in all models, particularly for CLASSIC/ZOOM without direct climate datasets.

- Purpose of outputs for analysts
  - Enables consistent, comparable analyses of climate-change impacts on water availability, aquatic environments, and related decision-making.
  - Supports exploration of uncertainty and climate variability through multiple ensemble realizations.
  - Provides data suitable for fishery, freshwater ecology, and water-resource planning at national and regional scales.