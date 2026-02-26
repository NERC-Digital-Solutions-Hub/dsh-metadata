# Coalburn Forest Research Catchment

## Overview
- UK’s longest-running forest research catchment, located in Kielder forest, Northumberland (1.5 km²).
- Instrumented since 1967; forest planted in 1972/73; mature trees with around 30% of catchment felled in recent years.
- Dataset spans 55 years (1967–2022) of precipitation, discharge, potential evapotranspiration (PET), other meteorological data, and snow depths; hourly data from 1993 onward.
- Extensively quality controlled; suitable for hydrological modelling and analysis of forest impacts on river flows; supports map-based GIS data visualisations.

## Data assets (time series)
- Rainfall, PET, discharge, and meteorological data in multiple CSV formats:
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
- Description and timing:
  - Hourly data derived from ~15-minute measurements; hourly values are means (discharge) or sums (precipitation) of 15-minute intervals.
  - Pre-1990 daily data cover 09:00–08:00; post-1990 daily data cover 01:00–00:00 (with 15-minute interval handling as described).
  - PET and other meteorological data from Eskdalemuir (45 km NW); PET via Penman-Monteith method.

## Spatial data and geography
- Spatial data formats:
  - catchment.gpkg (Geopackage) – authoritative boundary for the catchment.
  - dem-catch-5m.tif – 5 m resolution catchment elevations (No data = 0).
  - catch-50m.tif – 50 m resolution catchment mask.
  - dem-50m.tif – 50 m resolution elevation data for the catchment extent.
  - landuse-2016-prelogging.tif – 50 m resolution pre-logging land use (forest = 1, grass = 2; no data = -9999).
  - landuse-2018-postlogging.tif – 50 m resolution post-2018 land use (forest = 1, grass = 2, logged = 3; no data = -9999).
- Additional visuals and context:
  - aerial-image-and-boundary.png
  - OS-map-and-boundary.png
  - felled-forest-2016-2018.jpg
  - met-station-photo.jpg
- Coordinate reference system:
  - All spatial data use OSGB 1936 / British National Grid (EPSG:27700).

## Boundary, data integrity, and caveats
- Catchment boundary correctness:
  - The provided catchment boundary (catchment.gpkg) is the correct boundary; the CEH boundary shapefile referenced elsewhere is incorrect and should not be used.
- Bounding box:
  - Lower left: lat 55.08943, long -2.49526
  - Upper right: lat 55.10761, long -2.46651
- Discharge data gaps and questionable periods:
  - Missing: 22/10/1972–11/7/1973, 21/12/1974–4/1/1975, 1/10/1981–13/10/1981, 5/12/1985–16/12/1985, 18/6/1990–1/7/1991, 4/12/1991–16/12/1991, and 26/6/2019–22/08/2019.
  - Several time windows with suspect data due to snowmelt or freezing (e.g., 2010, 2013 periods).
- Precipitation data notes:
  - Pre-1993: derived from monthly storage gauges with disaggregation to daily values using nearby stations; known undercatch during snow events.
  - Post-1993: from Environment Agency tipping bucket gauge at site 12; corrected upward by ~14% to align with areal precipitation, plus wind-related adjustments (~5%) to harmonise long-term totals with earlier studies.
  - Some infilling of gaps using Wiley Sike data for selected periods (Feb–Mar 2015 and Feb–Nov 2015; Feb 2020 onward shows potential inconsistencies).
- Data quality and processing:
  - Extensive quality control; PET data from Eskdalemuir; CHESS PET values ~10% higher than used here.
  - Water balance and rainfall adjustments reflect cross-period calibrations (1992–2003 overlap used for corrections).

## Land use and forest dynamics
- Forest canopy and height changes over time:
  - Tree heights: ~7 m (1992), ~9 m (1996), ~15 m (2010), ~19 m (2014).
  - Canopy closure progressed from partial to complete by the mid-1990s.
- Logging event:
  - Approximately 30% of forest felled between 2016–2018 (documented in felled-forest-2016-2018.jpg).
- Post-disturbance considerations:
  - Storm Arwen (2021) caused widespread tree fall; hydrological impacts not quantified here.

## How GIS specialists can use this dataset
- Map-based data products:
  - Combine time-series data with spatial layers (DEM, land use, and boundary) for hydrological and forest-change analyses.
  - Visualize rainfall, discharge, and PET trends alongside land-use transitions and canopy changes.
- Data packaging and integration:
  - Use catchment.gpkg as the authoritative boundary for GIS analyses; avoid incorrect boundary shapefiles.
  - Align time series to the spatial context via the provided DEMs and land-use rasters (pre/post-logging) to study impacts on runoff, evapotranspiration, and snow dynamics.
- Temporal analysis:
  - Exploit hourly data 1993–2022 for high-resolution hydrological modelling; daily and annual data extend long-term trends and water balance assessments.
- Quality-aware analyses:
  - Be mindful of data gaps and corrections; apply the documented adjustments for precipitation and the flagged suspect discharge periods in modelling and visualization.

## References
- Birkinshaw, S. J., Bathurst, J. C., & Robinson, M. (2014). 45 years of non-stationary hydrology over a forest plantation growth cycle, Coalburn catchment, Northern England. Journal of Hydrology, 519, 559-573.
- Robinson, M. (1998). 30 years of forest hydrology changes at Coalburn: water balance and extreme flows. Hydrol. Earth Syst. Sci. 2, 233-238.
- Robinson, M., Moore, R.E., Nisbet, T.R., Blackie, J.R. (1998). From moorland to forest: the Coalburn catchment experiment. Institute of Hydrology Report no. 133, Wallingford, UK.