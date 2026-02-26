# Enhanced Future Flows and Groundwater (eFLaG)

- A nationally consistent UK dataset of hydrological projections (river flow, groundwater level, and groundwater recharge) based on UKCP18.
- Time coverage: projections 1981–2080; accompanying observation-driven data for 1962–2018 (river flow 1963–2018).
- Created through a Met Office–led collaboration (CR19_4 UK Climate Resilience) with UKCEH, BGS, and HR Wallingford.

## Purpose and Scope

- Provides standardised time-series for hydrology to assess environmental health and policy performance over time.
- Outputs suitable for national and sub-national monitoring across multiple variables and timescales.

## Coverage and Data Sources

- Spatial scope: 200 river catchments, 54 boreholes, 558 groundwater bodies (England, Wales, Scotland).
- Observation-driven data: river flow and groundwater levels/recharge (1962–2018 for observations; 1963–2018 for river flow observations).
- Underpinning data: UKCP18 Regional 12 km climate projections; bias-corrected for hydrological use.
- Catchment and groundwater body metadata linked to standard national datasets (NRFA and NGLA).

## Data Generation and Modelling

- Data processing: UKCP18 regional projections (12 km) bias-corrected and converted to catchment-averaged time-series using NRFA methodology.
- Hydrological and groundwater models used (at-site simulations):
  - River flow: G2G, GR4J, GR6J, PDM
  - Groundwater levels: AquiMod
  - Groundwater recharge: ZOODRM
- Outputs provided in standard units: river flows (m3/s), groundwater levels (mAOD), groundwater recharge (mm/day).
- Includes model parameter files (csv) for reproducibility.

## Catchment and Groundwater Body Selection

- River catchments: NRFA stations selected for data and hydrometric quality, long record length, represent UK hydrological/geographical variability, and stakeholder relevance.
- Groundwater: 54 boreholes selected from the BGS NGLA to cover principal UK aquifers, with long, high-quality, minimally impacted records.
- Recharge aggregation: spatially aggregated over 588 groundwater bodies to reflect hydrogeological characteristics and support Water Framework Directive applications.

## Quality Control and Evaluation

- Data quality hubs: UK National River Flow Archive (NRFA) and UK National Groundwater Level Archive (NGLA).
- Validation approach (two-stage):
  - Stage 1 (simobs): compare simulations driven by observed climate data against observations using diverse performance metrics (including NSE, Kling-Gupta, bias, MAPE; with special emphasis on low-flow and high-flow performance).
  - Stage 2 (simobs vs simrcm): compare simulations driven by observations and by climate-model runs using flow duration curves and low-flow frequency curves (focus on statistical characteristics rather than day-to-day sequence).
- Full validation metrics detailed in associated methodology publications.

## Data Structure and Access

- Dataset: eFLaG_Dataset.zip containing 27 directories and 3304 files.
- File groups:
  - simobs: observation-driven simulations for daily meteorology, river flows, groundwater levels, and groundwater recharge (1961–2018 for meteorology; 1963–2018 for river flows; 1962–2018 for groundwater).
  - simrcm: RCM-driven simulations for the same variables (1980–2080 for meteorology; 1982–2080 for river flows and groundwater; 1981–2080 for groundwater recharge).
- File naming conventions indicate model (G2G, GR4J, GR6J, PDM, AquiMod, ZOODRM), station/ borehole, and data type.
- All data accessible as part of the eFLaG_Dataset.zip; designed to be stored and uploaded to appropriate data portals for reuse.

## Applications for Environmental Monitoring

- Enables consistent, long-term assessment of environmental health and policy effectiveness across UK hydrology.
- Supports scenario analysis and drought/flood risk assessment by providing multiple model ensembles and climate projections.
- Facilitates integration with other datasets to enhance the value of monitoring outputs (addressing calls to increase dataset utility and improve data accessibility).

## Partnerships, Funding, and References

- Funded by Met Office component of the Strategic Priorities Fund Climate Resilience Programme (contract P107493).
- Partners: UKCEH, British Geological Survey (BGS), HR Wallingford.
- Based on UKCP18 projections and prior Future Flows and Groundwater Work, with extensive methodological literature and validation studies cited.