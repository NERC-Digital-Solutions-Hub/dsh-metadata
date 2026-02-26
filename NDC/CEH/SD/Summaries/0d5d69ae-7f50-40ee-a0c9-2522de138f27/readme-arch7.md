# fluvial flood maps of the present day 1 in 20 year return period, and corresponding flood extents for 3 SSP/RCP scenarios for the future (2070-2100)

## Overview
- A data deposit of fluvial flood maps for present-day 1 in 20 year return period and three future scenarios (2070–2100) under SSP/RCP pathways.

## Data content
- 4 GeoTiff files and 1 readme document.
- Present-day map: VNM_1in20.tif (Vietnam, 1 in 20-year return period).
- Future maps (each 1 in 20-year return period for the respective scenario):
  - VNM_ssp5rcp85_20.tif
  - VNM_ssp2rcp45_20.tif
  - VNM_ssp1rcp26_20.tif
- Flood depth is in metres; these maps depict fluvial (river) flooding only; no pluvial or coastal flooding; no flood defences included.

## Methods and model
- Generated with an updated global flood model (Fathom 2.0), incorporating channel conveyance updates and improved MERIT DEM elevation data.
- Future 2070–2100 return periods derived from CMIP6 projections (Hirabayashi et al., 2021).
- Present-day 1 in 20-year return period retained; future maps are created by selecting the nearest return period from the Fathom 2.0 suite (return periods available: 5, 10, 20, 50, 75, 100, 200, 250, 500, 1000) and extracting the corresponding flood map, then mosaicking across Vietnam.

## Experimental design and sampling
- Future return-period maps from Hirabayashi et al. (2021) are converted to the nearest available return period in Fathom 2.0.
- The resulting maps are mosaicked across Vietnam to create a country-wide set of scenarios.

## Data structure and usage
- File naming indicates country (VNM) and scenario; 20 denotes 1 in 20-year return period for future.
- 0 value in the raster corresponds to 0 m flood depth; consider reclassifying 0 as NoData or using a palette that starts at a flooded threshold (e.g., 0.1 m).
- For visualization, open GeoTiffs in GIS software (e.g., QGIS or ArcMap); for spatial and statistical analysis, use R or Python.

## Quality control
- The underlying flood model (Fathom 2.0) has been used in multiple publications (e.g., Bernhofen et al., Hawker et al., Hirabayashi et al., Mitchell et al., Neal et al., Rentschler et al., Yamazaki et al., Sampson et al.).

## Use in GIS
- Suited for map-based data visualisation to compare present-day and future flood extents under different climate scenarios.
- Provides a basis for assessing spatial risk, planning, and communication with policymakers or the public.

## Limitations
- Only fluvial flooding is represented; does not include pluvial or coastal flooding.
- No explicit representation of flood defences.

## References
- Bernhofen et al. 2022; Hawker et al. 2020; Hirabayashi et al. 2021; Mitchell et al. 2022; Neal et al. 2021; Rentschler et al. 2022; Yamazaki et al. 2017; Sampson et al. 2015.