# Urban hydro-meteorological observation data 2016-2018  - Ouagadougou, Burkina Faso

## Overview
- Dataset from hydro-meteorological monitoring in Ouagadougou, Burkina Faso (2016–2018) as part of the DFID-funded AMMA-2050 project (amma2050.org).
- Contains time series of rainfall, water level, and river flow across Ouagadougou to support hydrological understanding and model development.
- In-situ data collected with tipping bucket raingauges and pressure level sensors; spot gauging used to derive river flow ratings.
- Network designed/set up by UK Center for Ecology and Hydrology (UKCEH) with 2iE; processing by UKCEH.
- Note: data gaps due to equipment malfunction and dry-season periods when pressure level sensors were withdrawn.

## Data collection, instrumentation, and sampling regime
- Instruments:
  - Pressure Level Sensor (PLS) HOBO MX2001 with Bluetooth data download.
  - Tipping bucket raingauges (Casella) with 0.2 mm resolution.
  - Spot gauging using MFPro with a 5 m rod for flow rating.
- Data flow:
  - Rainfall: 15-minute intervals (2ie site; rainfall data).
  - Water level/flow: various sites with hourly to 5-minute to 5-minute time steps (Dam3, Saaba, Rimkieta South/North, Kamboince).
- Site-specific details provided (location, coordinates, elevation, data start/end, time step, measurement units).
- Data processing:
  - Flow derived from depth using site-specific rating curves obtained from intermittent spot gauging during storms (depth, velocity, cross-sectional area).
  - Rainfall and dam level data visually inspected to remove erroneous values.
- Data management:
  - Data stored/derived within an Oracle database for flow time series.

## Site summaries
- Dam3 (central Ouagadougou): PLS at dam outlet; measures water level change relative to bed level; hourly depth; data gaps due to malfunction (QC’d data only).
- 2ie: Tipping bucket rainfall at 15-minute intervals; located at 2ie HQ in city centre near central dam system.
- Saaba: PLS at culvert crossing on a south Ouagadougou tributary; 12.7 m wide x 2 m height, downstream of central pillar; upstream area ~77 km2; 5-minute to 5-minute interval data.
- Rimkieta South: PLS at culvert on southern Rimkieta tributary; upstream ~73 km2; 5-minute data.
- Rimkieta North: PLS at culvert on northern Rimkieta tributary; upstream ~192 km2; 5-minute data.
- Kamboince: Tipping bucket rainfall at 15-minute intervals; located at 2ie grounds in Kamboince; upstream rainfall conditions unobstructed.
- Each site provides location-specific context (upstream area, urbanization, notable features) and precise data start/end dates.

## Transformation and quality control methods
- Rating curves:
  - Derived for three level-flow sites via intermittent spot gauging of storm flows (velocity and depth across transects).
  - Flow calculated as a function of depth and velocity using cross-sectional area measurements.
- Data cleaning:
  - Erroneous measurements removed after visual inspection of rating curves.
  - Rainfall and dam level data visually inspected to remove anomalies.
- Result: time series of flow (m3/s), depth (m), and rainfall (mm) with indicators for missing data.

## Data structure and recorded values
- Data files:
  - Six CSV files: time series for flow (three sites), dam level (one site), and rainfall (two sites).
  - One metadata CSV file providing site summaries.
- Columns:
  - Flow files: date_time, flow (m3/s), missing data index (M denotes missing values due to malfunction or QC).
  - Dam level file: date_time, level (mAOD), missing data index.
  - Rainfall files: date_time, rainfall (mm), missing data index.
- Units and ranges:
  - Flow: cubic metres per second (m3/s); minimum reported flow is 0 m3/s.
  - Level: depth relative to bed (m) and mAOD (meters above Ordnance Datum); minimum depth 0 m.
  - Rainfall: millimetres (mm); minimum rainfall 0.2 mm per 15-minute interval; periods with no rainfall recorded as 0 mm.
- Data coverage:
  - Data start and end dates vary by site (2016–2018 for multiple sites; some gaps due to equipment issues).
  - Overall, dataset provides multi-rate time series across several urban drainage and river flow monitoring points, suitable for hydrological analysis and model development.