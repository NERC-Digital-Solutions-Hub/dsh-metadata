# Description

- This deposit contains fluvial flood maps for present-day 1 in 20 year return period and corresponding future flood extents for three SSP/RCP scenarios for 2070–2100, with changes in flood return periods estimated from CMIP6 projections to extract maps from a global flood model.
  
## Collection/generation methods

- Flood maps produced with an updated global flood model (Fathom 2.0), building on Sampson et al. (2015).
- Updates include improved channel conveyance capacity (Neal et al., 2021) and a higher-accuracy elevation dataset (MERIT DEM; Yamazaki et al., 2017).
- Future return periods derived from Hirabayashi et al. (2021) CMIP6 projections; only the present-day 1 in 20 year return period is used for future projections.

## Nature and Units of recorded values

- Flood maps estimate inundation depth in metres for present-day and three future scenarios.
- Return period represented: 1 in 20 year for both present and future.
- Maps cover fluvial flooding only (rivers); do not include pluvial or coastal flooding, and do not explicitly include flood defences.

## Quality control

- Fathom 2.0 has been used in multiple publications (e.g., Bernhofen et al. 2022; Hawker et al. 2020; Mitchell et al. 2022; Rentschler et al. 2022).

## Details of data structure

- Contains 4 GeoTiff files and 1 readme:
  - VNM_1in20.tif (present day 1 in 20) – 4.6 MB
  - VNM_ssp5rcp85_20.tif – 5.3 MB
  - VNM_ssp2rcp45_20.tif – 5.5 MB
  - VNM_ssp1rcp26_20.tif – 5.5 MB
- VNM = Vietnam (ISO3); 0 value corresponds to 0 m flood depth. Recommendation: set 0 as NoData or start palette at a small flooded value (e.g., 0.1 m).
- For visualization, GIS programs (QGIS/ArcMap) recommended; for analysis, use R or Python.

## Experimental design/Sampling regime

- Future return period maps from Hirabayashi et al. (2021) are converted to the nearest available return period in the Fathom 2.0 suite (5, 10, 20, 50, 75, 100, 200, 250, 500, 1000).
- Flood inundation maps corresponding to each return period are mosaicked across Vietnam.

## Analytical methods

- Present-day map can be compared to flood observations; skill scores computed include critical success index, hit rate, false alarm ratio, and bias.
- Observations originate from remote sensing, photographs, newspaper articles, wrack marks, etc.

## Use in GIS Software

- For visualization, open each GeoTiff in GIS software (QGIS or ArcMap).
- Note: 0 value = 0 m; may set as NoData or start palette at a flooded threshold (e.g., 0.1 m).
- Spatial and statistical analysis are well-suited to R or Python.

## References

- Cited works related to model and data sources, including Bernhofen et al. (2022); Hawker et al. (2020); Hirabayashi et al. (2021); Mitchell et al. (2022); Neal et al. (2021); Rentschler et al. (2022); Yamazaki et al. (2017); Sampson et al. (2015).