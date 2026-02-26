# Urban hydro-meteorological observation data 2016-2018  - Ouagadougou, Burkina Faso

## Overview
- Time series of rainfall, water level, and river flow in Ouagadougou, Burkina Faso (2016–2018) as part of the DFID AMMA-2050 project.
- Purpose: understand hydrological function and support hydrological model development.
- In-situ data collected using tipping bucket raingauges and pressure level sensors; river flows derived from level measurements via site-specific rating curves.
- UK Centre for Ecology and Hydrology (UKCEH) designed and set up the network; data processing conducted by UKCEH.
- Notable data gaps due to equipment malfunction and dry-season periods affecting pressure level sensors (PLS).

## Experimental design and sampling regime
- Equipment and sampling details provided for each site (Dam3, 2ie, Saaba, Rimkieta south, Rimkieta north, Kamboince).
- Sensor types:
  - Dam3: PLS level sensors, hourly depth records; monthly equipment inspections; gaps due to malfunction.
  - 2ie: Tipping bucket rainfall gauge, 15-minute time step.
  - Saaba, Rimkieta (south and north): PLS level (flow) sensors with varying time steps (5-minute to 5-minute) and depths referenced to bed level.
  - Kamboince: Tipping bucket rainfall gauge, 15-minute time step.
- Data start and end dates vary by site (2016–2018 range); Hartford details include coordinates and elevations.

## Site summaries
- Dam3: PLS at dam outlet; central Ouagadougou; depth measured hourly; data gaps common, especially in 2017.
- 2ie: Rainfall at city centre location near central dam system.
- Saaba: PLS at culvert with ~12.7 m span; upstream area ~77 km²; mixed urban and bare earth.
- Rimkieta South: PLS at culvert; upstream ~73 km²; minor attenuation from Boulimougou dam.
- Rimkieta North: PLS at culvert; upstream ~192 km²; predominantly low-density urban and bare earth.
- Kamboince: Rainfall gauge at northern city location; minimal obstructions to rainfall.

## Transformation and quality control methods
- Flow rating curves derived from intermittent spot gauging during storms (velocity and depth measurements across transects).
- Depth-to-flow conversion: use cross-sectional area and velocity data to estimate flow; apply derived rating curves to time-series depths.
- Erroneous measurements removed after visual QC of rating curves.
- Final rating curves linked to depth data in an Oracle database to produce time-series flows.
- Rainfall and dam level data visually inspected to remove suspect values.

## Data structure and recorded values
- Data packaged as 6 time-series CSV files plus a metadata CSV.
- Flow files: date_time, flow (m³/s), missing data index; minimum flow value is 0 m³/s; M denotes missing values.
- Dam level file: date_time, level (mAOD), missing data index; minimum depth 0 m (per peripheral instrument siting); M denotes missing values.
- Rainfall files: date_time, rainfall (mm), missing data index; minimum rainfall 0.2 mm per 15-minute interval; periods with no rain recorded as 0; M denotes missing values.
- Summary meta-data CSV provides site-level context.
- Data spans:
  - Dam3: 01/06/2016 – 24/11/2018
  - 2ie: 13/07/2016 – 25/09/2018
  - Saaba: 01/06/2016 – 24/11/2018
  - Rimkieta South: 31/05/2016 – 24/11/2018
  - Rimkieta North: 31/05/2016 – 03/10/2017
  - Kamboince: 12/08/2016 – 10/10/2017

## Notes on data availability and caveats
- Data gaps occur due to equipment malfunction and periods when PLS were withdrawn.
- Some data points may be lower than reference levels (e.g., dam depth can drop below the stated zero level due to siting).
- Visual QC and manual checks were employed to ensure data usability; data users should account for missing segments and potential QC flags.