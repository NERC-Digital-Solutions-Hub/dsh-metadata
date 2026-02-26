# Coalburn Forest Research Catchment

## Overview
- 1.5 km2 catchment in Kielder forest, Northumberland, UK; longest running forest research catchment in the UK.
- Instrumented since 1967; 30% of catchment felled between 2016 and 2018.
- Data aim: support hydrological modelling and understanding how forest management affects river flows.

## Data Coverage and Time Span
- Time span: 1967–2022 (55 years of data).
- Variables: precipitation, discharge, potential evapotranspiration (PET), other meteorological data, and snow depths.
- Temporal resolution:
  - Hourly data available from 1993–2022 (from 15-minute measurements; 09:00 hourly values derived from 08:15–09:00 data).
  - 1967–1993: mix of hourly and daily data; pre-1990 daily data recorded 09:00–08:00, post-1990 daily data recorded 01:00–00:00.

## Data Files and Formats
- File formats include CSV, GEOTIFF, JPG, PNG, and GPKG.
- Key data files:
  - rainfall-PET-1993-2022-daily.csv
  - rainfall-PET-1993-2022-hourly.csv
  - discharge-1993-2022-daily.csv
  - discharge-1993-2022-hourly.csv
  - metdata-1993-2022-hourly.csv
  - rainfall-discharge-PET-1967-1971-daily.csv
  - rainfall-discharge-PET-1976-1980-daily.csv
  - rainfall-discharge-PET-1986-1989-daily.csv
  - rainfall-discharge-March1977-July1978-hourly.csv
  - rainfall-discharge-January1986-December1989-hourly.csv
  - rainfall-discharge-June1979-December1980-hourly.csv
  - snow-depth-2004-2022-daily.csv
  - water-balance-1967-2022-annual.csv
  - catchment.gpkg (catchment boundary)
  - dem-catch-5m.tif, catch-50m.tif, dem-50m.tif (spatial data)
  - landuse-2016-prelogging.tif, landuse-2018-postlogging.tif (land use)
  - aerial-image-and-boundary.png, OS-map-and-boundary.png
  - felled-forest-2016-2018.jpg, met-station-photo.jpg
- Spatial data uses OSGB 1936 / British National Grid (EPSG:27700).

## Data Quality, Processing, and Quality Control
- Extensive quality control applied; PET data from Eskdalemuir (≈45 km NW).
- PET calculated with Penman-Monteith equation; Chess PET ~10% higher than used here.
- Time series construction:
  - Hourly values derived from 15-minute measurements (e.g., 09:00 hourly discharge is mean of 00:15–09:00 intervals; rainfall is sum of 00:15–01:00 intervals).
  - Pre-1990 daily data: 09:00–08:00 window; post-1990 daily data: 01:00–00:00 window.
- Pre-1993 precipitation:
  - From four monthly storage gauges; daily values disaggregated using nearby daily data (with acknowledged undercatch in snow events).
- Post-1993 precipitation:
  - Environment Agency tipping bucket (TBR) gauge at site 12; corrected to align with areal-average storage gauges (approx. +9% correction, plus wind-adjustment of +5% for site 12).
  - Some infilling with Wiley Sike rainfall data (2015, 2015–2016, 2020 periods) due to gaps; 2020 data show potential forest-cover-related precipitation measurement issues.
- Data gaps and anomalies:
  - Discharge data gaps in several periods (listed in document).
  - 2010 period (14:00 15/01/2010 to 08:00 21/01/2010) questionable; 2013 period likely affected by subzero temperatures.
  - 26/06/2019–22/08/2019 discharge data missing.
- Water balance:
  - Up to 2003: rainfall totals from Robinson (1998) and Birkinshaw (2014) using multiple storage gauges.
  - Post-2003: corrected EA TBR rainfall totals to align with overlap period and wind effects.
- Boundary accuracy:
  - Provided catchment boundary is well defined; caution against using a boundary dataset from CEH that is described as incorrect.

## Spatial Data and Boundary
- Catchment boundary: catchment.gpkg (well defined; earlier CEH boundary dataset should not be used).
- Elevation and land use:
  - dem-catch-5m.tif: 5 m resolution DEM for catchment.
  - catch-50m.tif and dem-50m.tif: 50 m resolution elevation grids.
  - landuse-2016-prelogging.tif and landuse-2018-postlogging.tif: forest (type 1) and grass (type 2); logging (type 3) post-logging.
- Bounding box:
  - Lower left: lat 55.08943, long -2.49526
  - Upper right: lat 55.10761, long -2.46651

## Gaps, Anomalies, and Known Issues
- Discharge data missing for multiple periods as noted above.
- Post-1993 rainfall corrections are long-term averages; instantaneous events may not perfectly reflect corrections.
- Infilling in some periods introduces uncertainties; forest management (Arwen storm impact, 2016–2018 logging) may influence hydrology but effects are not fully quantified in dataset.

## Use and Applications
- Suitable for hydrological modelling and analysis of forest impact on river flows.
- Data supports analysis of long-term forest growth cycles, canopy closure, and logging effects on catchment hydrology.
- Metadata-rich dataset enabling cross-comparison with other studies (e.g., Robinson and Birkinshaw).

## References
- Birkinshaw, S. J., Bathurst, J. C., & Robinson, M. (2014). 45 years of non-stationary hydrology over a forest plantation growth cycle, Coalburn catchment, Northern England. Journal of Hydrology, 519, 559-573.
- Robinson, M. (1998). 30 years of forest hydrology changes at Coalburn: water balance and extreme flows. Hydrol. Earth Syst. Sci., 2, 233-238.
- Robinson, M., Moore, R.E., Nisbet, T.R., Blackie, J.R. (1998). From moorland to forest: the Coalburn catchment experiment. Institute of Hydrology Report no. 133.