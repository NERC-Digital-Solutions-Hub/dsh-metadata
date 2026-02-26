# Coalburn Forest Research Catchment

- UK forest hydrology dataset for Coalburn catchment (1.5 km2) in Kielder Forest, Northumberland; instrumented since 1967; long-running experiment with substantial forest growth and logging history.
- 55 years of meteorological and hydrological data, enabling analysis of forest effects on river flows and hydrological processes.

## Data Coverage and Time Span

- Variables: precipitation, discharge, potential evapotranspiration (PET), other meteorological data, snow depth.
- Time span: 1967–2022 (data continuity for many series; some pre-1993 data are daily or aggregated; hourly data available 1993–2022).
- Time resolution:
  - Hourly data: 1993–2022 (derived from 15-minute measurements; hourly values are averages or sums as described).
  - Daily data: 1967–1993 for some variables; 1993–2022 for others.
- PET and meteorological data are sourced from Eskdalemuir (45 km NW).

## Data Files and Formats

- File types include CSV, GeoTIFF, GPKG, JPG, PNG.
- Key data files (representative list):
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
  - snow-depth-2004-2022-daily.csv
  - water-balance-1967-2022-annual.csv
  - catchment.gpkg (Geopackage, catchment boundary)
  - dem-catch-5m.tif, catch-50m.tif, dem-50m.tif (DEM and spatial rasters)
  - landuse-2016-prelogging.tif, landuse-2018-postlogging.tif
  - aerial-image-and-boundary.png, OS-map-and-boundary.png
  - felled-forest-2016-2018.jpg, met-station-photo.jpg
- Spatial data uses OSGB 1936 / EPSG:27700 coordinates.

## Data Quality, Processing, and Provenance

- Extensive quality control applied; data suitable for hydrological modelling and data analysis of forest impact on river flows.
- Pre-1993 daily data: lines up 09:00–08:00; hourly data are derived when available by aggregating 15-minute measurements.
- Post-1990 daily data: recorded 01:00–00:00 (with 24-hour cycles).
- PET and meteorological data: from Eskdalemuir; PET calculated via Penman-Monteith; CHESS PET datasets discussed as higher by ~10%.
- Pre-1993 precipitation: sourced from multiple storage gauges and disaggregated using nearby stations; includes documented undercatch during snow events.
- Post-1993 precipitation: Environment Agency tipping bucket (TBR) gauge; correction factors applied to align with areal storage gauge estimates and wind effects (long-term average correction; event-scale corrections may not hold).
- Data infilling and gaps: selective infilling using nearby gauges or daily totals; detailed QA notes cover periods with gaps or questionable measurements.
- Notable references for data quality and interpretation:
  - Birkinshaw, Bathurst, & Robinson (2014)
  - Robinson (1998) and related IH reports
- Boundary/shapefile caution: catchment boundary polygon in catchment.gpkg; other boundary shapefiles on CEH site exist but not to be used as provided here due to boundary inaccuracies.

## Time Alignment, Units, and Metadata

- Time conventions and units described per file (tables summarize variable names, units, date ranges, and data coverage).
- Units include mm for precipitation and PET (daily or hourly), and m3/s or mm/day for discharge, with corresponding date-time stamps in each file.
- Snow depth measured at Eskdalemuir (2004–2022 daily).

## Spatial Data and Boundaries

- Catchment boundary: catchment.gpkg (well-defined boundary due to historical ditching when instrumented).
- Elevation and land use rasters: dem-50m.tif, dem-catch-5m.tif, catch-50m.tif, landuse-2016-prelogging.tif, landuse-2018-postlogging.tif.
- Bounding box (approximate): lower left lat 55.08943, long -2.49526; upper right lat 55.10761, long -2.46651.
- All spatial data referenced in OSGB 27700 coordinates.

## Data Gaps, Anomalies, and caveats

- Discharge data gaps: 22/10/1972–11/7/1973; 21/12/1974–4/1/1975; 1/10/1981–13/10/1981; 5/12/1985–16/12/1985; 18/6/1990–1/7/1991; 4/12/1991–16/12/1991; 26/6/2019–22/08/2019.
- Specific questionable periods: 2010-02 window (14:00–08:00) and 2013-01/03 research notes; snowmelt effects suspected during some periods.
- 2016–2018 logging: about 30% of forest felled; hydrological impact uncertain; canopy closure progression noted in tree-height history.
- Boundary shapefile warning: do not rely on alternate boundary shapefiles from CEH; use the provided catchment.gpkg.

## Use Cases and How This Supports Data Work

- Ideal for long-term hydrological analysis and modelling of forest influence on river discharge and catchment water balance.
- Enables cross-comparison of pre- and post-logging hydrology and canopy effects when combined with land-use rasters.
- Supports data product development for self-serve exploration (e.g., dashboards or pivot-based analyses) by providing harmonised time series and accompanying metadata.
- Useful for validating hydrological models that require long historical rainfall, discharge, PET, and snow depth data in a forested catchment.

## Key Notes for Data Support

- Understand the ask: identify data subsets (e.g., hourly vs daily, pre- vs post-1990) and align with modelling needs.
- Verify data sufficiency and quality: leverage the QA notes, correction factors for precipitation, and documented data gaps.
- Prepare data products: consider combining rainfall, discharge, PET, and met data with spatial layers (land use, elevation) to enable self-serve analyses.
- Be aware of data provenance and limitations: long-term averaging corrections for precipitation, and event-scale uncertainties due to measurements and infill.