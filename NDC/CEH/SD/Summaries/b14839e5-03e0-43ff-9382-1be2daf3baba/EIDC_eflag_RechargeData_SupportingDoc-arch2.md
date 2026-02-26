# Distributed potential recharge projections for the UK, based on UK Climate Projections 2018 (UKCP18) data, from the Enhanced Future Flows and Groundwater (eFLaG) project Supporting Documentation

## Overview
- Dataset provides 2 km gridded daily projections of potential groundwater recharge for mainland Great Britain, covering 1981–2080.
- Based on the BGS distributed groundwater recharge model (ZOODRM) driven by bias-corrected UKCP18 climate projections (Regional Climate Models, RCMS).
- Includes corresponding gridded observation-driven recharge time series for 1962–2018.
- Created by the British Geological Survey (BGS) in collaboration with UK Centre for Ecology & Hydrology (UKCEH) and HR Wallingford; funded by the Met Office as part of the Strategic Priorities Fund Climate Resilience Programme (contract P107493).
- Data support groundwater monitoring and policy assessment, enabling comparison between observed-driven and model-driven recharge under climate scenarios.

## Data generation methods

### ZOODRM
- Distributed recharge model applied over Great Britain on a 2 km × 2 km grid.
- Employs FAO Crop Evapotranspiration Paper 56 approach (modified) to compute potential recharge as a fraction of rainfall excess after evaporative losses and soil moisture deficit, using a runoff coefficient.
- Historically used to assess 21st-century recharge changes across UK river basins and groundwater bodies.

### UKCP18 Data Processing and Bias Correction
- UKCP18 provides 12 km, high-resolution climate projections (HadGEM3-GC3.05 and HadREM3-GC705) for 1980–2080.
- Outputs are processed to daily 1 km grids for precipitation and potential evapotranspiration (PE); for ZOODRM, precipitation is resampled to 2 km.
- Precipitation data are bias-corrected using monthly-mean bias correction.

## Nature and units of recorded values
- Recharge outputs expressed as millimeters per day (mm/day) on a 2 km grid.
- Spatial reference: British National Grid (BNG coordinate system).

## Quality control
- Two-stage calibration/evaluation:
  1) Baseline evaluation with observed climate data against observed river flows (UK National River Flow Archive) to assess catchment water balances.
  2) Evaluation when driven by climate-model outputs, comparing climate-model driven recharge against observation-driven recharge over a common baseline (1989–2018).

## Details of data structure

- Data format: NetCDF files.
- Grid and time:
  - 2 km spatial grid using British National Grid coordinates.
  - Time stored as days since 1950-01-01 (standard Gregorian calendar for simobs; 360-day calendar for simrcm).
- Slices and naming:
  - Data split into continuous 5-year time slices.
  - simobs: observation-driven daily gridded recharge (1962–2018).
  - simrcm: RCM-driven daily gridded recharge (1981–2080).
  - File naming:
    - simobs: eflag_gridded_potential_recharge- simobs - YEAR_FROM - YEAR_TO .nc
    - simrcm: eflag_gridded_potential_recharge- simrcm - RCM - YEAR_FROM - YEAR_TO .nc
  - RCM in file names is the UKCP18 RCM code (e.g., rcm1).

## Access and references
- Data available via the CEH data catalogue and related project documentation (see project references in the accompanying scientific literature).
- Key references include FAO (1998), Griffiths et al. (2006), Hannaford et al. (2022), Hughes et al. (2021), Mansour & Hughes (2004), and Murphy et al. (2018).

## Relevance for Analysts Monitoring the Environment
- Provides standardized, gridded, daily potential groundwater recharge data suitable for environmental monitoring and policy assessment.
- Enables direct comparison between observed-driven recharge and climate model-driven recharge under UKCP18 scenarios, supporting scenario analyses and trend detection.
- Supports integration with other environmental datasets (e.g., groundwater bodies, river flows) for extended monitoring and decision-making.
- Highlights data quality assurance steps and validation approach, increasing confidence in using the dataset for monitoring and reporting.
- Facilitates data access and transparency by maintaining consistent data structure (NetCDF, 2 km grid) and clear file-slicing conventions, aiding data discovery and reuse.