# GWAVA Modelling- UPSCAPE

## Purpose and scope
- Document describes the GWAVA 5.0 model setup and its application to the Cauvery Basin for assessing water availability under natural and anthropogenic stresses.
- Aims to support monitoring and decision-making by providing a structured, data-rich modelling framework.

## Model overview
- GWAVA is a large-scale, semi-distributed gridded water resources model that estimates local runoff per grid cell using a lumped probability distribution model (PDM).
- Core components: soil moisture storage (PDM), surface storage, and groundwater storage, plus a demand-driven routine for anthropogenic stresses.
- Demand modules cover domestic (urban and rural), industrial, livestock, and irrigation needs; irrigation demand is dynamic in time and space, while other demands are defined as user-specified and temporally static.
- In Cauvery Basin, modelling uses a 0.125 degree grid (444 cells) and includes major and minor reservoirs, water transfers, and agriculture within command and rural areas.

## Spatial and temporal setup
- Spatial resolution: 0.125 degree grid; Cauvery Basin disaggregated into 444 cells.
- Temporal framing includes baseline (1986–2005) and future projections across multiple scenarios with daily data outputs.
- Data outputs are organized into seven CSV files detailing baseline, climate ensembles, and socio-economic scenarios.

## Climate and socio-economic scenarios
- Climate inputs are drawn from an ensemble of CMIP-style climate models (e.g., BCC-CSM1-1, IPSL-CM5A-LR, MIROC-ESM, MIROC-ESM-CHEM, NorESM1-M) to represent future climate conditions.
- Scenarios used:
  - Representative Concentration Pathways (RCPs): RCP4.5 and RCP8.5.
  - Shared Socio-Economic Pathways (SSPs): SSP1 (SDG-focused, low material growth), SSP2 (business as usual), SSP3 (sector-centric, higher degradation).
- Combinations include climate ensembles alone and combined climate-socioeconomic ensembles (SSPs) for 2041–2060 and 2061–2080.

## Variables, units, and data descriptors
- Table of variables includes:
  - TotQ: Total runoff (m3/s) – mean over grid cell and day.
  - aqlevel: Aquifer level (m below ground level) – mean over grid cell and day.
  - Urban_dems, Rural_dems, Livestock_dems, Industrial_dems, Irrigation_dems – various demands (m3/s) or related categories.
  - Unfulfilled demands (uf_*) for urban, rural, livestock, industrial, irrigation – represent unmet demand (m3/s).
- All outputs are daily values, intended to capture spatially averaged conditions within each grid cell.

## Data quality and model validation
- Calibration: performed at 14 gauging stations using SIMPLEX auto-calibration with four parameters (surface and groundwater routing, soil moisture capacity PDM parameter, rooting depth multiplier).
- Validation: conducted at the same 14 stations plus 200 groundwater wells, using a different time period.
- Performance metrics: Kling-Gupta Efficiency (KGE) values reported per site (range observed across calibration/validation periods), indicating variable predictive performance across sites (e.g., some sites higher, others lower, with a few negative validations).

## Data structure and access
- Output data are provided in seven CSV files with a consistent header structure:
  - Four initial columns: xll (lower-left x coordinate), yll (lower-left y coordinate), year, timestep (Julian day).
  - Baseline and ensemble files are named to indicate period, scenario, and type (e.g., Baseline_1986_2005.csv; Ensemble_climate_2041_2060.csv; SSPs_2041_2060.csv; Ensemble_climate_SSPs_2041_2060.csv, etc.).
  - Variable listings follow Table 2 descriptions (daily mean values for each grid cell).
- File naming conventions include markers for baseline, ensemble climate (RCPs), SSPs, and combined ensemble scenarios, with separate files for 2041–2060 and 2061–2080 periods.

## Supporting documentation and acknowledgements
- Acknowledges CMIP and associated climate modeling groups and infrastructure support for climate data.
- Documented as UK Centre for Ecology & Hydrology work, with collaboration across Bangor, Edinburgh, Wallingford, and Lancaster institutions.