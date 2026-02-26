# Distributed potential recharge projections for the UK, based on UKCP18 data, from the Enhanced Future Flows and Groundwater (eFLaG) project Supporting Documentation

- What this dataset is
  - 2 km gridded daily projections of potential groundwater recharge for mainland Great Britain, 1981–2080, produced using the ZOODRM distributed recharge model driven by bias-corrected UKCP18 climate projections (12 km resolution).
  - Gridded observation-driven time series of potential groundwater recharge covering 1962–2018 (raw, un-regionalised recharge simulations used to derive area-averaged recharge at groundwater-body scale).

- Data generation and methods
  - ZOODRM: a distributed recharge model (2 km grid) that estimates potential recharge by applying a FAO 56-based approach to rainfall minus evapotranspiration and soil moisture deficit, using a runoff-coefficient framework.
  - UKCP18 data processing: regional (RCM) 12 km climate projections were bias-corrected (monthly mean bias correction) and downscaled to 2 km to feed ZOODRM. Precipitation and potential evapotranspiration time series form the climate inputs.
  - Purpose: support groundwater modeling and assessment of climate-change impacts on recharge.

- Quality assurance and validation
  - Two-stage calibration/evaluation:
    - Stage 1: model driven by observed climate data evaluated against observed river-flow records (UK National River Flow Archive) to assess water-balance performance.
    - Stage 2: comparison of climate-model-driven recharge with observation-driven recharge over a common baseline period (1989–2018).

- Data format, structure, and units
  - File format: NetCDF.
  - Spatial grid: fixed 2 km British National Grid coordinate system.
  - Time basis:
    - simobs (observation-driven): Gregorian calendar, days since 1950-01-01 (1962–2018).
    - simrcm (RCM-driven): 360-day calendar, days since 1950-01-01 (1981–2080).
  - Time slicing: data split into continuous 5-year slices.
  - File naming:
    - simobs: eflag_gridded_potential_recharge-simobs-YEAR_FROM-YEAR_TO.nc
    - simrcm: eflag_gridded_potential_recharge-simrcm-rcm-YEAR_FROM-YEAR_TO.nc
  - Units: millimeters per day (mm/day).

- Data provenance and access
  - Project and collaboration: eFLaG project funded by the UK Met Office-led component of the Strategic Priorities Fund Climate Resilience Programme (contract P107493); collaboration among British Geological Survey (BGS), UK Centre for Ecology & Hydrology (UKCEH), and HR Wallingford.
  - Related data: raw observation-driven simulations available via the CEH data catalogue; associated scientific articles and data papers provide details on model setup, processing, and validation.

- Relevance for analysts
  - Enables testing hypotheses about how groundwater recharge responds to climate change at high spatial resolution (2 km) across Great Britain.
  - Supports development and validation of groundwater models, scenario analyses, and impact assessments for policy and management decisions.
  - Facilitates correlation analyses between recharge proxies and climate variables, and prediction of recharge changes under UKCP18-informed scenarios.
  - Provides both observed-data–driven and climate-model–driven baselines for robust comparison and uncertainty assessment.