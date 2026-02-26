# Distributed potential recharge projections for the UK, based on UK Climate Projections 2018 (UKCP18) data, from the Enhanced Future Flows and Groundwater (eFLaG) project Supporting Documentation

## Overview
- 2 km gridded daily projections of potential groundwater recharge for mainland Great Britain, 1981–2080.
- Generated with the British Geological Survey (BGS) ZOODRM distributed recharge model, driven by bias-corrected 12 km UKCP18 regional climate projections.
- Includes gridded observation-driven recharge time series for 1962–2018.
- Outputs used to derive area-averaged groundwater recharge estimates at the groundwater-body scale (raw simulations available via CEH catalogue).
- Funded by the Met Office-led component of the UK Climate Resilience programme; collaboration between UKCEH, BGS, and HR Wallingford. The dataset is created by BGS in collaboration with UKCEH.

## What the dataset contains
- NetCDF files on a 2 km grid, with recharge values in mm/day.
- Time spans:
  - simobs: observation-driven daily recharge, 1962–2018.
  - simrcm: UKCP18 regional climate model (RCM) driven recharge, 1981–2080.
- Spatial reference: British National Grid coordinates (meters).
- Time reference:
  - simobs: days since 1950-01-01 (Gregorian calendar).
  - simrcm: days since 1950-01-01 (360-day calendar).

## Data generation methods
- ZOODRM (2 km grid): a distributed recharge model using FAO 56-based approach to compute potential recharge as a function of rainfall excess, evapotranspiration, soil moisture deficit, and a runoff coefficient.
- UKCP18 processing: downscaled from 12 km to 2 km to match ZOODRM; precipitation data bias-corrected using monthly-mean bias correction.
- Data types:
  - simobs: observation-driven recharge simulations (1962–2018).
  - simrcm: RCM-driven recharge simulations (1981–2080).

## Nature and units of recorded values
- Recharge outputs in millimetres per day (mm/day).
- Grid: regular 2 km, British National Grid.

## Quality control and validation
- Two-stage calibration/evaluation:
  1) Drive with baseline observed climate data; compare against observed river flows from the UK National River Flow Archive to assess water balance performance.
  2) Compare climate-model-driven recharge against observation-driven recharge over a common baseline period (1989–2018).

## Data structure and file organization
- File format: NetCDF.
- Time slices: continuous 5-year periods; divided into simobs (observation-driven) and simrcm (RCM-driven) groups.
- Time indexing:
  - simobs: standard Gregorian calendar (days since 1950-01-01).
  - simrcm: 360-day calendar (days since 1950-01-01).
- Spatial indexing: British National Grid (metres).
- File naming conventions:
  - simobs: eflag_gridded_potential_recharge-simobs-YEAR_FROM-YEAR_TO.nc
  - simrcm: eflag_gridded_potential_recharge-simrcm-RCM-YEAR_FROM-YEAR_TO.nc
  - RCM = UKCP18 RCM code (e.g., rcm1).

## How this data can be used (Data Support perspective)
- Build self-serve tools and dashboards to explore spatial and temporal patterns of potential groundwater recharge under UKCP18 scenarios.
- Combine with other hydrological data (e.g., river flows, groundwater bodies) for impact assessments and policy analysis.
- Validate and compare model-driven vs. observation-driven recharge patterns; assess uncertainty across scenarios.
- Transform and reformat NetCDF data for specific analyses, taking into account 2 km resolution, calendar differences (360-day vs Gregorian), and unit conventions (mm/day). 
- Access raw/referenced data and provenance for reproducibility via the CEH data catalogue (raw simulations: https://catalogue.ceh.ac.uk/documents/1bb90673-ad37-4679-90b9-0126109639a9).