# Distributed potential recharge projections for the UK, based on UK Climate Projections 2018 (UKCP18) data, from the Enhanced Future Flows and Groundwater (eFLaG) project Supporting Documentation

## Overview
- Dataset provides 2 km gridded daily projections of potential groundwater recharge across mainland Great Britain from 1981 to 2080, using the BGS ZOODRM distributed recharge model driven by bias-corrected UKCP18 climate projections (12 km).
- Includes corresponding gridded observation-driven recharge time series covering 1962 to 2018.
- Data originate from the eFLaG project (funded by the Met Office through the Strategic Priorities Fund Climate Resilience programme) and were created by the British Geological Survey (BGS) in collaboration with UK Centre for Ecology & Hydrology (UKCEH) and HR Wallingford.
- Aims to support monitoring and evaluation of groundwater-related environmental health and inform future decisions; raw simulations underpin area-averaged groundwater recharge estimates at groundwater-body scales (link to underlying data in CEH).

## Data generation and methods
- ZOODRM (distributed groundwater recharge model) operates on a 2 km grid and estimates potential recharge by applying a FAO 56-based approach (removing evaporation and soil moisture deficit from rainfall to compute potential recharge as a fraction of excess water).
- UKCP18 inputs are 12 km regional climate projections (HadGEM3-GC3.05 and HadREM3GA705); outputs are bias-corrected to provide 1 km daily series of precipitation and potential evapotranspiration (PE), then resampled to 2 km for ZOODRM consistency.
- Observed climate baseline used for calibration/validation is embedded in the observation-driven simulations (simobs) from 1962 to 2018; RCM-driven simulations (simrcm) cover 1981 to 2080.
- Observational and model-based baselines underpin quality checks and evaluation of recharge projections.

## Data quality, evaluation, and governance
- Quality control includes a two-stage calibration/evaluation:
  - Stage 1: evaluate recharge simulations driven by observed climate data against observed river flows (UK National River Flow Archive) to assess catchment water balance representation.
  - Stage 2: compare climate-model-driven recharge against observation-driven recharge over a common baseline period (1989–2018).
- Documentation and scientific context are linked to accompanying journal articles for deeper methodological details.

## Data structure, format, and access
- Data stored as NetCDF files on a uniform 2 km grid in British National Grid coordinates; times are encoded as days since 1950-01-01.
- Time indexing:
  - simobs: daily times on a standard Gregorian calendar (1962–2018).
  - simrcm: daily times on a 360-day calendar (1981–2080).
- File organization:
  - simobs files named eflag_gridded_potential_recharge-simobs-YEAR_FROM-YEAR_TO.nc
  - simrcm files named eflag_gridded_potential_recharge-simrcm-rcm-YEAR_FROM-YEAR_TO.nc (RCM code like rcm1)
- Data slices are organized into continuous 5-year time slices for ease of use.
- The 2 km grid and NetCDF format facilitate integration with groundwater models and monitoring workflows.

## Units and spatial-temporal details
- Units: millimeters per day (mm/day) for recharge values.
- Spatial reference: British National Grid (metres).
- Temporal reference:
  - simobs: days since 1950-01-01, Gregorian calendar.
  - simrcm: days since 1950-01-01, 360-day calendar.

## Use in monitoring, reporting, and policy
- Supports assessment of potential groundwater recharge under climate change, enabling scenario analyses relevant to environmental health monitoring and policy decisions.
- Provides a basis for deriving area-averaged recharge estimates at groundwater-body scales, aiding regional water-resource management and resilience planning.
- Publicly documented with metadata and associated datasets available via the CEH data catalog, promoting transparency and reproducibility.

## Collaborators, funding, and references
- Collaboration: British Geological Survey (BGS) with UK Centre for Ecology & Hydrology (UKCEH) and HR Wallingford.
- Funding: Met Office–led component of the Strategic Priorities Fund Climate Resilience Programme (CR19_4 UK Climate Resilience).
- Key references include sources on ZOODRM, UKCP18 data processing and bias correction, and prior hydrological projection work (detailed in the supporting documentation).

## Notes and caveats
- Simrcm uses a 360-day calendar, which may affect direct cross-year comparisons with simobs.
- Differences exist between observed-data-driven and climate-model-driven simulations, reflecting model biases and the bias-correction step.
- The dataset provides raw, un-regionalised recharge simulations used to derive area-averaged estimates; users should consult the linked CEH document for derivation details and interpretation.