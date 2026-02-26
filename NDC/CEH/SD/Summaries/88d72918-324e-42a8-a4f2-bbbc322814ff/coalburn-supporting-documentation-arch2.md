# Coalburn Forest Research Catchment

- The Coalburn catchment (1.5 km2) in Kielder Forest, Northumberland, is the UK's longest-running forest research catchment. Instrumented in 1967; replanted with conifer in 1972/73; mature trees now with about 30% of the catchment felled.

## Summary of Data and Purpose
- Provides 55 years of data (1967–2022) including precipitation, discharge, potential evapotranspiration (PET), other meteorological data, and snow depths.
- Data are quality-controlled and suitable for hydrological modelling and analyses of forest effects on river flows.
- Supports environmental monitoring and policy evaluation through a consistent, long-term dataset.

## Temporal Coverage and Resolution
- Time span: 1967–2022 (data products extend to 2022; some time series begin earlier with varying formats).
- Hourly data available from 1993 onward; a mix of hourly and daily data for 1967–1993.
- Data processing notes:
  - Where 15-minute data exist, hourly values are derived (e.g., hourly discharge is the mean of 15-minute values; rainfall is the sum of 15-minute values).
  - Pre-1990 daily data are recorded 09:00–08:00; Post-1990 daily data are recorded 01:00–00:00.

## Variables and Data Files (Key Products)
- Precipitation, PET, discharge, snow depth, and met data (hourly and daily formats).
- Selected file examples:
  - rainfall-PET-1993-2022-daily.csv
  - rainfall-PET-1993-2022-hourly.csv
  - discharge-1993-2022-daily.csv
  - discharge-1993-2022-hourly.csv
  - metdata-1993-2022-hourly.csv
  - snow-depth-2004-2022-daily.csv
  - water-balance-1967-2022-annual.csv
- Spatial data accompanying the time series:
  - catchment.gpkg (Geopackage catchment boundary)
  - dem-catch-5m.tif, catch-50m.tif, dem-50m.tif (DEM and extent)
  - landuse-2016-prelogging.tif, landuse-2018-postlogging.tif
  - aerial-image-and-boundary.png, OS-map-and-boundary.png
- Notes: All data are stored on standard formats (CSV, GeoTIFF, GPKG, etc.). OSGB grid coordinates (EPSG:27700).

## Data Quality, Processing and Calibration
- PET calculated from Eskdalemuir data ( ~45 km NW ) using Penman–Monteith equation; CHESS PET values typically ~10% higher.
- Post-1993 precipitation adjustments: Environment Agency tipping bucket gauge at site 12 adjusted to align with areal storage gauges, with a long-term correction (~9% areal consistency plus wind-related 5% adjustment in some periods).
- Pre-1993 precipitation: derived by disaggregating monthly storage gauge totals from nearby stations due to sparse daily measurements; hourly data for this period infilled where possible using nearby gauges.
- Hourly data for various periods between 1967–1989 were infilled using available daily data and nearby gauges; some extensive infilling details are documented (e.g., 1977–1978, 1986–1989 periods).
- Water balance annual totals before 2003 come from Birkinshaw et al. (2014) using multiple storage gauges; post-2003 totals use corrected TBR (with cross-over period 1992–2003 used for correction).
- Quality control acknowledges potential over-snow undercatch and data gaps; data are considered reliable where gaps exist, but some events (snowmelt, freezing periods) are flagged.

## Spatial Boundaries and Boundaries Note
- Catchment boundary provided in catchment.gpkg is the authoritative boundary; a CEH-provided boundary shapefile is marked incorrect and should not be used.
- Spatial context: All data align to GB Ordnance Survey grid (OSGB 1936/British National Grid, EPSG:27700).
- Bounding box coordinates provided for reference:
  - Lower left: lat 55.08943, long -2.49526
  - Upper right: lat 55.10761, long -2.46651

## Discharge Data – Gaps and Anomalies
- Notable missing periods: 22/10/1972–11/7/1973; 21/12/1974–4/1/1975; 1/10/1981–13/10/1981; 5/12/1985–16/12/1985; 18/6/1990–1/7/1991; 4/12/1991–16/12/1991; 26/6/2019–22/08/2019.
- Some suspect periods due to snowmelt or freezing conditions (e.g., 2010, 2013) are flagged.

## Precipitation Data – Pre-1993 and Post-1993 Details
- Pre-1993: Uses four monthly storage gauges with disaggregation to daily values using nearby stations (Spadeadam, Bower, Chirdon, Kielder Dam) to address undercatch during snow events.
- Post-1993: Uses Environment Agency tipping bucket gauge at site 12; adjustments applied to reconcile with areal storage gauge estimates; long-term correction applied; wind-related adjustments also noted.
- Some infilling across 2015–2019 periods using Wiley Sike data (9 km SW) with multiplicative factors to reflect higher Coalburn rainfall; potential issues observed from Feb 2020 onward in cross-checks.

## Meteorological Data and PET
- Eskdalemuir data used for PET and meteorology; PET derived via Penman–Monteith; CHESS PET is ~10% higher than used here.
- Met data (air temperature, humidity, net radiation, wind, vapor pressure deficit) provided for the hourly series.

## Land Use and Forest Change
- Forest canopy dynamics documented: average tree heights rose from ~7 m (1992) to ~19 m (2014), with canopy closure by the mid-1990s.
- Large-scale logging: around 30% of forest felled between 2016–2018 (logged area shown in imagery).
- Storm Arwen (Nov 2021) caused substantial tree damage; hydrological impact remains uncertain.

## Applications and Use Case
- Suitable for hydrological modelling across a forest growth cycle.
- Useful for analysing the hydrological impact of forest management, logging, and canopy changes on river flows.
- Enables long-term environmental health assessment and policy performance evaluation through standardized, documented datasets.

## References and Documentation
- Birkinshaw, S. J., Bathurst, J. C., & Robinson, M. (2014). 45 years of non-stationary hydrology over a forest plantation growth cycle, Coalburn catchment, Northern England. Journal of Hydrology, 519, 559-573.
- Robinson, M. (1998). 30 years of forest hydrology changes at Coalburn: water balance and extreme flows. Hydrology and Earth System Sciences, 2, 233-238.
- Robinson, M., Moore, R.E., Nisbet, T.R., Blackie, J.R. (1998). From moorland to forest: the Coalburn catchment experiment. IH report no. 133.