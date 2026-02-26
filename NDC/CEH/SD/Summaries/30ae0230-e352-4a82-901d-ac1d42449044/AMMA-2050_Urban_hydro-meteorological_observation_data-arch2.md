# Urban hydro-meteorological observation data 2016-2018  - Ouagadougou, Burkina Faso

## Overview
- Timeframe: 2016–2018
- Location: Ouagadougou, Burkina Faso
- Project context: DFID-funded AMMA-2050 (African Monsoon Multidisciplinary Analysis)
- Purpose: Collect hydro-meteorological time series to understand hydraulic function and support hydrological model development
- Data types: rainfall, water level, and river flow collected across multiple sites in the city

## Data collection and sites
- In-situ instruments:
  - Tipping bucket raingauges (Casella, 0.2 mm resolution)
  - Pressure level sensors (HOBO MX2001) for water level
  - Spot gauging for flow measurements
- Network design and processing:
  - Designed by UK Centre for Ecology and Hydrology (UKCEH)
  - Processing performed by UKCEH
- Sites and characteristics:
  - Dam3: level at dam outlet (central Ouagadougou); hourly depth; data gaps due to malfunctions
  - 2ie: rainfall in city centre (15-min interval)
  - Saaba: level (flow) at culvert, 5-min to 12-min intervals depending on site
  - Rimkieta South: level (flow), 5-min intervals
  - Rimkieta North: level (flow), 5-min intervals
  - Kamboince: rainfall, 15-min intervals
- Spatial attributes:
  - Each site includes latitude, longitude, elevation (mASL)
  - Sampling start and end dates vary by site

## Experimental design and processing
- Rating curves:
  - Derived by intermittent spot gauging during storm events (velocity and depth across transects)
  - Flow estimated from depth using site-specific rating curves, cross-sectional area, and measured velocity
- Data transformation:
  - Depth-to-flow conversions applied to time-series depth data
  - Oil- and QC-driven: only QC’d data retained
- Quality checks:
  - Visual inspection of rainfall and dam level data
  - Removal of erroneous measurements based on rating curves and inspection
- Data integration:
  - Time series stored in an Oracle database
  - Final products include derived flow time series for each site

## Data structure and recorded values
- Data files:
  - 6 CSV time-series files plus a meta-data CSV
- File structure:
  - Flow: date_time, flow (m3/s), missing data index (M indicates missing)
  - Dam level: date_time, level (mAOD), missing data index
  - Rainfall: date_time, rainfall (mm), missing data index
- Value conventions:
  - Flow minimum 0 m3/s
  - Rainfall minimum 0.2 mm per 15 minutes; zero values when no rain
  - Depth minimum 0 m (level at dam periphery may go below this)
  - Missing values denoted by M

## Data quality, gaps, and limitations
- Data gaps due to equipment malfunction and dry-season periods with PLS withdrawal
- Incomplete data for some sites (e.g., Rimkieta North data end 2017)
- Overall emphasis on QC’d, auditable data and associated meta-data for site-specific context

## Access, usage, and purpose for analysts
- Outputs support understanding hydrological function and development of hydrological models for Ouagadougou
- Data produced and curated by UKCEH in collaboration with 2iE; part of AMMA-2050
- Primary data products are time-series of flows, dam levels, and rainfall with accompanying site metadata
- For analysts: consider data gaps and site-specific rating curves; use in conjunction with other data sources to enhance monitoring value and accessibility of underlying data