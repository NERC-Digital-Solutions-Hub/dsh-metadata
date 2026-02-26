# Coalburn Forest Research Catchment

- Overview
  - The Coalburn catchment in Northumberland (1.5 km2) is the UK’s longest-running forest hydrology study, instrumented in 1967.
  - Forest management changed over time (planted 1972/73, ~30% felled by around 2018), enabling analysis of forest growth and disturbance on river flows.
  - The dataset spans 55 years of precipitation, discharge, potential evapotranspiration (PET), other meteorological data, and snow depths (1967–2022), with hourly data available from 1993 onward.

- Data Coverage and Scope
  - Key variables: precipitation, discharge, PET, other meteorological measurements, snow depth, water balance (annual).
  - Time range: 1967–2022 for many series; hourly data 1993–2022; snow depth 2004–2022; annual water balance 1967–2022.
  - Spatial data accompany the time series (catchment boundary, elevation rasters, land use rasters for pre- and post-logging periods).

- Data Formats and File Organization
  - File formats include CSV, GeoTIFF, GPKG, JPG, PNG.
  - Sample data groups:
    - Time series: rainfall-PET-1993-2022-daily.csv; rainfall-PET-1993-2022-hourly.csv; discharge-1993-2022-daily.csv; discharge-1993-2022-hourly.csv; metdata-1993-2022-hourly.csv.
    - Historical and specialized series: rainfall-discharge-PET-1967-1971-daily.csv; rainfall-discharge-PET-1976-1980-daily.csv; rainfall-discharge-PET-1986-1989-daily.csv; several hourly datasets for specific periods.
    - Snow depth: snow-depth-2004-2022-daily.csv.
    - Water balance: water-balance-1967-2022-annual.csv.
    - Spatial data: catchment.gpkg; dem-catch-5m.tif; catch-50m.tif; dem-50m.tif; landuse-2016-prelogging.tif; landuse-2018-postlogging.tif; boundary images.
  - General note: much hourly data are derived from 15-minute measurements with specific aggregation rules (e.g., hourly discharge is the mean of 15-minute values; rainfall is the sum).

- Time Series Details and Data Granularity
  - Pre-1990 daily data: recorded 09:00 to 08:00; example given 13/12/1977 covers 12/12/1977 09:00 to 13/12/1977 08:00.
  - Post-1990 daily data: recorded 01:00 to 00:00; hourly data interpolated from 15-minute measurements where applicable.
  - Post-1993 hourly data: 00:00–23:00; rainfall values anchored to 00:15, 00:30, 00:45, 01:00 timestamps when derived from 15-minute data.

- Quality Control and Data Handling
  - Extensive quality control applied; some data have been infilled or adjusted to ensure consistency between measurement types.
  - Pre-1993 precipitation data involve disaggregation from monthly storage gauges using nearby daily data; undercatch in snow events addressed via multiple sources.
  - Post-1993 precipitation adjustments: Environment Agency tipping bucket gauge values increased by ~14% to align with storage gauges; cross-comparisons indicate a ~9% difference between areal-averaged storage gauges and tipping bucket data, with an additional wind-adjustment (~5%) to reconcile with wind effects.
  - Some periods feature infilling using nearby stations or daily data; long-term corrections are noted but instantaneous-event validity may be limited.

- Data Gaps, Anomalies, and caveats
  - Discharge data gaps: 22/10/1972–11/7/1973; 21/12/1974–4/1/1975; 1/10/1981–13/10/1981; 5/12/1985–16/12/1985; 18/6/1990–1/7/1991; 4/12/1991–16/12/1991; 26/6/2019–22/08/2019.
  - Several periods with questionable discharge measurements (e.g., 2010 snowmelt period; 7/1/2013–3/7/2013).
  - The boundary dataset CEH boundary should not be used; use catchment.gpkg for the well-defined catchment boundary.
  - Some post-logging data reflect storm and environmental changes (e.g., Storm Arwen 2021) with uncertain hydrological impacts.
  - Land-use rasters document 2016 pre-logging and 2018 post-logging states; approximately 30% of canopy felled between 2016–2018.

- Spatial Context and Boundaries
  - Catchment boundary is well defined within catchment.gpkg; OSGB 1936 British National Grid coordinates (EPSG:27700) used.
  - Supplementary spatial data include high-resolution elevation models and land-use classifications relevant to forest cover and management.

- Land Use, Forestry, and Hydrological Impacts
  - Tree heights progressed from ~7 m (1992) to ~19 m (2014); canopy closure occurred around 1996.
  - Between 2016–2018, around 30% of forest was felled; land-use rasters capture pre-logging forest, post-logging forest, and logged areas.
  - Post-logging hydrological implications documented as unknown in places; dataset supports testing forest-growth-cycle impacts on hydrology.

- Potential Uses for Data Analysts
  - Hydrological modelling and non-stationary hydrology analyses over a forest growth cycle.
  - Investigations into correlations between forest structure changes (growth, logging) and river discharge, using multi-decadal data.
  - Validation and calibration of climate- and land-use-driven hydrological models; assessment of data quality, gaps, and infilling approaches.
  - Cross-scale analysis combining time-series data with spatial land-use and DEM data to understand catchment responses.

- Access, Metadata, and References
  - Datasets are designed to be discoverable with metadata; multiple files and spatial data accompany the time-series data.
  - Key references: Birkinshaw, Bathurst, & Robinson (2014); Robinson (1998); Robinson et al. (1998) documenting forest hydrology changes and water balance.
  - Data sources include long-term storage gauges, tipping-bucket rainfall gauges, Eskdalemuir PET, and near-catchment weather stations, with careful cross-validation and corrections across periods.