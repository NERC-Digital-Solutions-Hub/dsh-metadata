# This deposit contains fluvial flood maps of the present day 1 in 20 year return period, and corresponding flood extents for 3 SSP (Shared Socioeconomic Pathway)/RCP(Representative Concentration Pathway) scenarios for the future (2070-2100). Change in flood return periods are estimated using CMIP6 projections and subsequently used to extract flood maps from a global flood model

## Overview
- Provides present-day and future fluvial flood inundation maps for Vietnam, focusing on the 1 in 20 year return period and three future climate scenarios (SSP/RCP combinations) for 2070–2100.
- Future changes in return periods are derived from CMIP6 climate projections and used to extract corresponding maps from a global flood model.

## Methods and model
- Flood maps generated with Fathom 2.0, an updated global flood model (building on Sampson et al. 2015); improvements include channel conveyance capacity (Neal et al., 2021) and MERIT DEM elevation data (Yamazaki et al., 2017).
- Future return periods (2070–2100) are derived from Hirabayashi et al. (2021) CMIP6 projections and mapped to the nearest available return period in Fathom 2.0 (5, 10, 20, 50, 75, 100, 200, 250, 500, 1000 years).
- The analysis presents only fluvial flooding; no coastal or pluvial components, and no explicit flood defenses are included.

## Data products (Nature and units)
- Flood maps express inundation depth in metres.
- Return period is 1 in 20 years for both present-day and future scenarios.
- Geographic scope: Vietnam; future maps created by mosaicking across Vietnam for the specified return periods.

## Data structure and files
- 4 GeoTiff files and 1 readme in the record:
  - VNM_1in20.tif (present day)
  - VNM_ssp5rcp85_20.tif (future SSP5/RCP8.5)
  - VNM_ssp2rcp45_20.tif (future SSP2/RCP4.5)
  - VNM_ssp1rcp26_20.tif (future SSP1/RCP2.6)
- File names indicate ISO3 country code (VNM = Vietnam) and scenario/return period (20-year frame).

## Experimental design
- Future return periods from Hirabayashi et al. (2021) are mapped to the nearest available return periods in Fathom 2.0.
- For each scenario, the corresponding 20-year flood map is extracted and mosaicked across Vietnam to produce a country-wide set of maps.

## Analytical methods
- Present-day flood map is compared with flood observations (remote sensing, photographs, newspaper articles, wrack marks).
- Skill metrics computed: critical success index, hit rate, false alarm ratio, and bias.

## Use in GIS and data handling
- Visualization: Open GeoTiff files in GIS software (QGIS or ArcMap). Recommendation to treat 0 depth as either no-data or use a color scale starting above a small flooded threshold (e.g., 0.1 m).
- Analysis: Perform spatial and statistical analysis in R or Python.

## Data quality, validation, and governance
- Quality control: Fathom 2.0 has been employed in multiple publications (e.g., Bernhofen et al. 2022; Hawker et al. 2020; Hirabayashi et al. 2021; Mitchell et al. 2022; Neal et al. 2021; Rentschler et al. 2022; Yamazaki et al. 2017; Sampson et al. 2015).
- Metadata and openness: Includes a readme and clearly labeled files; guards and limitations noted (e.g., no defense features, only fluvial flooding).
- Reproducibility: Ties future projections to CMIP6-based climate models and a consistent flood model framework (Fathom 2.0).

## Limitations and caveats for monitoring frameworks
- Only fluvial (riverine) flooding is represented; pluvial and coastal flood risks are not included.
- No explicit incorporation of flood defenses or infrastructure; depth values are raw inundation depths without defense attenuation.
- Data transformation steps (mapping future return periods to nearest available values) introduce approximation.
- Public sharing of dataset and accompanying metadata improves transparency but requires governance to ensure ongoing data quality and up-to-date metadata.

## References (selected)
- Bernhofen et al., 2022; Hawker et al., 2020; Hirabayashi et al., 2021; Mitchell et al., 2022; Neal et al., 2021; Rentschler et al., 2022; Yamazaki et al., 2017; Sampson et al., 2015.