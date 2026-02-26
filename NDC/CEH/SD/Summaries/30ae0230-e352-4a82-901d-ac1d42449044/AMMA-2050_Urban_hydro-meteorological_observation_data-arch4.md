# Urban hydro-meteorological observation data 2016-2018  - Ouagadougou, Burkina Faso

## Overview
- DFID AMMA-2050 project data (2016–2018) comprising time series of rainfall, water level, and river flow across Ouagadougou.
- In-situ data collected with HOBO MX2001 pressure level loggers and Casella tipping bucket rain gauges; spot gauging for flow rating curves.
- UK Centre for Ecology and Hydrology (UKCEH) designed the hydro-meteorological network; processing by UKCEH; collaboration with 2iE (Institut International d'Ingenierie de l'Eau et de l'Environment).
- Notable data gaps due to equipment malfunction and seasonal dry periods.

## Data contents
- Variables: rainfall (mm), water level (mAOD), and river flow (m3/s).
- Sites: Dam3, 2ie, Saaba, Rimkieta South, Rimkieta North, Kamboince (plus associated details).
- Sampling regimes by site:
  - Dam3: water level, hourly.
  - 2ie: rainfall, 15-minute.
  - Saaba: water level/flow, 5-minute.
  - Rimkieta South/North: water level/flow, 5-minute.
  - Kamboince: rainfall, 15-minute.
- Each site includes coordinates, elevation, data start/end dates, and time step.
- Data processing produced flow from depth via site-specific rating curves; rainfall data collected continuously; dam level data monitored.

## Experimental design and sampling regime
- In-situ monitoring at multiple sites with:
  - Pressure level sensors (PLS) for water level.
  - Tipping bucket rain gauges for rainfall.
  - Spot gauging using MFPro tools to derive flow ratings from depth during storms.
- Specifics summarized in site-by-site descriptions, including location context (e.g., downstream pumping station, city-center location) and upstream catchment sizes.

## Transformation and quality control methods
- Flow rating curves derived from intermittent spot gauging (velocity and depth) during storm events.
- Flow computed as depth-derived flow using cross-sectional area and measured velocity; rating curves applied to time-series depth data.
- Visual QC applied to rainfall and dam level data to remove erroneous values.
- Final rating curves linked depth to flow for each site and applied to time-series data stored in an Oracle database.

## Data structure and recorded values
- Total: 6 CSV time-series files plus a metadata CSV.
- Flow files (3): columns - date_time, flow (m3/s), missing data index; minimum flow 0; M denotes missing values.
- Dam level file: columns - date_time, level (mAOD), missing data index; minimum depth 0; M denotes missing values.
- Rainfall files (2): columns - date_time, rainfall (mm), missing data index; minimum rainfall is 0.2 mm in 15 minutes; zero values indicate no rainfall; M denotes missing values.

## Gaps, limitations, and considerations
- Data gaps due to equipment malfunction; significant gaps in 2017, and varying data end dates by site (e.g., Rimkieta North ends 2017).
- Potential measurement limitations at peripheral dam locations and during low-flow periods.
- Data are tied to specific equipment and processing methods (rating curves) that define how depth is converted to flow.