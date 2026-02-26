# Description

- This deposit contains fluvial flood maps of the present day 1 in 20 year return period, and corresponding flood extents for 3 SSP/RCP future scenarios for the 2070–2100 period. Change in flood return periods is estimated using CMIP6 projections and used to extract flood maps from a global flood model.

## Data Content

- 4 GeoTiff files and 1 readme document.
- Present day file: VNM_1in20.tif (flood depth in metres for the 1 in 20 year return period).
- Future scenario files (each with the 20-year return period): 
  - VNM_ssp5rcp85_20.tif
  - VNM_ssp2rcp45_20.tif
  - VNM_ssp1rcp26_20.tif
- Filenames indicate Vietnam (ISO3: VNM) and the corresponding SSP/RCP scenario:
  - SSP5 RCP8.5
  - SSP2 RCP4.5
  - SSP1 RCP2.6

## Generation Methods

- Flood maps generated with an updated global flood model (Fathom 2.0), based on Sampson et al. 2015.
- Updates include improved channel conveyance capacity (Neal et al., 2021) and MERIT DEM elevation data (Yamazaki et al., 2017).
- Future 2070–2100 return periods derived from CMIP6 projections (Hirabayashi et al., 2021) and mapped to the nearest available return period in Fathom 2.0.
- Only present day 1 in 20 year return period is used for future maps.

## Data Values and Units

- Flood inundation depth estimated in metres.
- Return period: 1 in 20 year flood event for both present and future maps.
- Fluvial flooding only; does not include pluvial or coastal flooding and does not explicitly include flood defences.

## Quality Control

- Fathom 2.0 has been used in multiple publications, supporting reliability of the modeled flood extents (e.g., Bernhofen et al., 2022; Hawker et al., 2020; Hirabayashi et al., 2021; Mitchell et al., 2022; Neal et al., 2021; Rentschler et al., 2022; Yamazaki et al., 2017; Sampson et al., 2015).

## Data Structure and Files

- Four GeoTiff files and one readme:
  - VNM_1in20.tif (present day)
  - VNM_ssp5rcp85_20.tif
  - VNM_ssp2rcp45_20.tif
  - VNM_ssp1rcp26_20.tif
- File sizes: approximately 4.6–5.5 MB each.
- File naming convention indicates Vietnam (VNM) and scenario details.

## Experimental Design / Processing

- Future return period maps from Hirabayashi et al. (2021) are re-mapped to the nearest available return period in Fathom 2.0.
- Return periods covered: 5, 10, 20, 50, 75, 100, 200, 250, 500, and 1000.
- For each return period, the corresponding inundation map is extracted and mosaiced across Vietnam.

## Analytical Methods

- Present day flood map can be compared with observations (remote sensing, photographs, articles, wrack marks).
- Skill scores can be computed: critical success index (CSI), hit rate, false alarm ratio, bias.

## Use in GIS Software

- For visualization: open GeoTiff files in GIS (e.g., QGIS, ArcMap).
- Note: value 0 corresponds to 0 m flood depth. Consider treating 0 as NoData or use a palette that starts at a flooded threshold (e.g., 0.1 m).
- Spatial and statistical analysis are well-suited for R or Python.

## Scope and Limitations

- Flood maps cover river (fluvial) flooding only; do not include pluvial or coastal flooding.
- No explicit inclusion of flood defences.

## References

- Bernhofen et al., 2022; Hawker et al., 2020; Hirabayashi et al., 2021; Mitchell et al., 2022; Neal et al., 2021; Rentschler et al., 2022; Yamazaki et al., 2017; Sampson et al., 2015.