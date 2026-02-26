# Distributed potential recharge projections for the UK, based on UK Climate Projections 2018 (UKCP18) data, from the Enhanced Future Flows and Groundwater (eFLaG) project Supporting Documentation

## Overview
- 2 km gridded daily projections of potential groundwater recharge for mainland Great Britain, 1981–2080 (and corresponding observation-driven time series 1962–2018).
- Generated with the British Geological Survey (BGS) ZOODRM distributed groundwater recharge model, driven by bias-corrected UKCP18 regional climate projections at 12 km resolution.
- Includes raw, un-regionalised recharge simulations used to derive area-averaged recharge estimates at the groundwater-body scale.
- Project funded by the Met Office-led component of the Climate Resilience Programme; collaboration between UK Centre for Ecology & Hydrology (UKCEH), BGS and HR Wallingford.

## Data generation methods
- ZOODRM (2 km grid)
  - A distributed recharge model using the FAO 56 approach to estimate potential recharge as a fraction of rainfall after removing evaporation and soil moisture deficit, employing a runoff coefficient.
  - Previously used to assess 21st-century seasonal recharge changes across UK river basins and groundwater bodies.
- UKCP18 Data Processing and Bias Correction
  - UKCP18 regional projections (HadGEM3-HC3.05/HadREM3-GC3.05) produced at 12 km; bias-corrected to 1 km daily precipitation and potential evapotranspiration (PE).
  - For ZOODRM, precipitation and PE are resampled to 2 km and bias-corrected (monthly means).
- Nature and units
  - Recharge outputs in mm/day on a 2 km grid, British National Grid coordinates.

## Quality control
- Two-stage calibration/evaluation:
  1) Baseline observed climate data: compare model results to UK National River Flow Archive observations to assess catchment water balances.
  2) Baseline climate model data: compare climate-model-driven recharge to observation-driven recharge over 1989–2018.

## Data structure
- Format and organization
  - Stored as NetCDF files on a 2 km British National Grid grid; times as days since 1950-01-01.
  - Data split into continuous 5-year time slices for easy handling.
  - Two main data streams:
    - simobs: Observation-driven daily gridded recharge, 1962–2018.
    - simrcm: RCM-driven daily gridded recharge, 1981–2080.
- Time and spatial indexing
  - simobs time: Gregorian calendar (days since 1950-01-01).
  - simrcm time: 360-day calendar (days since 1950-01-01).
  - Spatial: British National Grid (metres).
- File naming conventions
  - simobs: eflag_gridded_potential_recharge-simobs-YEAR_FROM-YEAR_TO.nc
  - simrcm: eflag_gridded_potential_recharge-simrcm-RCM-YEAR_FROM-YEAR_TO.nc
  - RCM codes example: rcm1, etc.
- Data availability
  - Raw recharge simulations used to derive area-averaged groundwater recharge estimates at groundwater-body scale available separately (link provided in documentation).

## Access, references, and notes for users
- Related data and methods described in more detail in the accompanying journal article and ESSD preprint:
  - ESSD preprint: essd-2022-40 (link in documentation)
  - Hydrological projections for the UK based on UKCP18 (Hannaford et al. 2022)
  - UKCP18 Land Projections: Murphy et al. 2018
- Key references for methods:
  - FAO Crop evapotranspiration (FAO 56)
  - Griffiths et al. 2006 (interception and soil moisture model)
  - Mansour & Hughes 2004 (ZOODRM user manual)
  - Hughes et al. 2021 (national-scale groundwater recharge under climate change)
- Data usage notes for GIS specialists
  - Suitable for map-based visualization and spatial analyses at 2 km resolution across Great Britain.
  - Compare observation-driven vs model-driven recharge projections; enables spatial mapping of potential recharge under UKCP18 scenarios.
  - Be aware of calendar differences between simobs (Gregorian) and simrcm (360-day) time axes when aligning time series.