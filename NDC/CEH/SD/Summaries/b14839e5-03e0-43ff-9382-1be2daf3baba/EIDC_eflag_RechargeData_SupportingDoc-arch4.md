# Distributed potential recharge projections for the UK, based on UK Climate Projections 2018 (UKCP18) data, from the Enhanced Future Flows and Groundwater (eFLaG) project Supporting Documentation

## Overview
- Dataset includes 2 km gridded daily projections of potential groundwater recharge for mainland Great Britain from 1981 to 2080.
- Based on the BGS distributed groundwater recharge model (ZOODRM) driven by bias-corrected UKCP18 climate projections (12 km) and includes corresponding gridded observation-driven recharge time series (1962–2018).
- Raw, un-regionalised recharge simulations used to derive area-averaged groundwater recharge estimates at the groundwater-body scale (link provided).
- Funded by the Met Office-led component of the Strategic Priorities Fund Climate Resilience Programme; collaboration among BGS, UKCEH, and HR Wallingford, with dataset creation by BGS in collaboration with UKCEH.

## Data generation methods
- ZOODRM: A distributed recharge model applied on a 2 km × 2 km grid across mainland Britain, using FAO Drainage and Irrigation Paper 56 (modified) to compute potential recharge as a fraction of rainfall excess after soil evaporation and moisture deficits.
- Purpose: Provide recharge estimates to drive groundwater simulators and assess 21st-century recharge changes.
- Data streams:
  - simobs: Observation-driven daily gridded potential recharge (1962–2018).
  - simrcm: RCM-driven daily gridded potential recharge (1981–2080).

## UKCP18 Data Processing and Bias Correction
- UKCP18 regional projections produced by HadGEM3 and HadREM3GA705, offering 12 high-resolution UK-wide climate projections (1980–2080).
- Outputs converted to 1 km daily time series of precipitation and potential evapotranspiration (PE); for ZOODRM, precipitation data are resampled to 2 km.
- Precipitation data bias-corrected using monthly-mean bias correction.

## Nature and units of recorded values
- Outputs are in millimeters per day (mm/day) on a 2 km grid aligned to the British National Grid.
- Time coordinates:
  - simobs: standard Gregorian calendar (days since 1950-01-01).
  - simrcm: 360-day calendar (days since 1950-01-01).
- Spatial coordinates: British National Grid (meters).

## Quality control
- Two-stage calibration/evaluation:
  1) Baseline observed climate data: evaluate ZOODRM against observed river-flow-derived water balances (UK National River Flow Archive).
  2) Climate model data: compare climate-model-driven recharge with observation-driven recharge over the common baseline (1989–2018).

## Details of data structure
- Data stored as NetCDF files, using a consistent 2 km grid and British National Grid coordinates.
- Time indexing differs between data streams:
  - simobs: days since 1950-01-01 (Gregorian calendar).
  - simrcm: days since 1950-01-01 (360-day calendar).
- File organization:
  - Shaped into continuous 5-year time slices.
  - simobs files named eflag_gridded_potential_recharge-simobs-YEAR_FROM-YEAR_TO.nc
  - simrcm files named eflag_gridded_potential_recharge-simrcm-RCM-YEAR_FROM-YEAR_TO.nc
  - RCM codes example: rcm1, etc.

## References
- FAO (1998) Crop evapotranspiration guidelines (FAO 56).
- Griffiths et al. (2006) rainfall interception and soil moisture model.
- Hannaford et al. (2022) Hydrological projections for the UK from UKCP18 (eFLaG, EIDC).
- Hughes et al. (2021) National-scale groundwater recharge impact under climate change.
- Mansour & Hughes (2004) ZOODRM user’s manual.
- Murphy et al. (2018) UKCP18 Land Projections: Science Report.

## Data access and related materials
- Area-averaged groundwater recharge estimates at groundwater-body scale: link provided in the overview (https://catalogue.ceh.ac.uk/documents/1bb90673-ad37-4679-90b9-0126109639a9).
- Background methodological article: https://essd.copernicus.org/preprints/essd-2022-40/
- Additional related publications: UKCP18 science and groundwater recharge assessments (e.g., Journal of Hydrology 2021).