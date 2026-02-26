# Future flows and Groundwater Levels - SC090016

## Executive summary
- The project aims to provide nationally consistent datasets and products to assess climate change impacts on river flows and groundwater across Great Britain.
- Key outputs include climate time series, hydrological and groundwater level simulations, river flow and groundwater maps, regional snapshots, and briefing notes for decision-makers.
- All products are accessible via dedicated web pages with licensing that is free for non-commercial use; commercial use may incur fees.

## Datasets and products
- Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded climate time series (precipitation and potential evapotranspiration) for GB, 1951–2098.
- Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater levels for 282 river sites and 24 boreholes, derived from FF Climate.
- 11-member ensemble of daily catchment-average precipitation (APr) and PET (PE) time series for 282 river sites and 24 boreholes.
- National maps of changes in river flow statistics for most large GB rivers (e.g., mean monthly flows, low-flow stats).
- Regional maps of changes in groundwater level and river flow statistics for one region.
- Briefing notes for decision-makers on using the results.

## Access and licensing
- FF Climate data are associated with DOIs and are accessible via the CEH Gateway, NRFA, and BGS websites under licensing conditions.
- Non-commercial use is free; commercial use may require a fee agreed with CEH/BGS.
- Documentation and data usage guidance available with data packages and on project websites.

## Data description and methodological notes
- HadRM3-PPE time series are downscaled from 25-km to 1-km and bias-corrected to align with observations; spatial heterogeneity within grid cells is incorporated.
- Available precipitation (APr) time series are derived from bias-corrected precipitation and temperature fields, correcting for snowmelt effects with an elevation-dependent snowmelt model.
- Temperature time series are downscaled and bias-corrected; detailed 5-km intermediate products are not publicly released.
- Potential evapotranspiration (PE) is computed at 1-km resolution using FAO56 Penman–Monteith with bias-corrected temperatures.
- Data are available as NetCDF files (FF-HadRM3-PPE) and large-volume APr/PE files (55 files each for APr and PE per ensemble member; total period 1950–2098).
- Climate realizations reflect UKCP09 A1B scenario; the dataset captures variability rather than reproducing exact historical sequences.

## Structure of outputs by section
- Section II: FF-HadRM3-PPE climate time series (temperature, precipitation, PET) with downscaling and bias correction; data delivered as NetCDF.
- Section II.2: Details on FF-HadRM3-PPE for temperature, available precipitation (APr), and PE; file organization and sizes.
- Section II.3: Access and acknowledgement requirements (DOIs; CEH Gateway).
- Section III: Description of hydrological inputs and how catchments are represented (lumped vs (semi-)distributed models); availability of catchment-average APr/PE series for lumped models.
- Section IV: Future Flows Hydrology (FF-HydMod-CatID): 11 ensemble river flow and groundwater time series for 282 sites and 40 boreholes; available as per-site CSVs.
- Section V: National maps (2050s) of changes in river flow indicators derived from CERF models; outputs are PNG files at the river network scale.
- Section VI: Regional groundwater maps (MABSWEC region) showing changes in mean monthly levels across six 30-year slices; outputs include ASCII grids and PNGs.
- Section VII: Briefing notes designed for scientists, water managers, and policymakers; provided with data packages.
- Section VIII: References for methodologies and datasets.