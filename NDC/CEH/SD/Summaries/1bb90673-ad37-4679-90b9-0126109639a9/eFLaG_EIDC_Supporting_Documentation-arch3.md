# eFLaG: Enhanced Future Flows and Groundwater

- A dataset of nationally consistent hydrological projections for the UK, covering river flow, groundwater levels, and groundwater recharge.
- Based on UKCP18 projections (Regional 12 km) with bias correction; spans 1981–2080 for projections and 1962/1963–2018 for observation-driven data.
- Joint project funded by the Met Office and UK Climate Resilience programme; partners: UKCEH, BGS, and HR Wallingford.
- Workflow links UKCP18 inputs to hydrological and groundwater models to produce site-specific time series across the UK:
  - 200 river catchments
  - 54 groundwater boreholes
  - 558 groundwater bodies
- Outputs include both simulated and observed data, designed for use in policy scrutiny, monitoring, and decision-making.

## Catchment selection

- River flows
  - Compiled metadata for all NRFA gauging stations; attention to national networks (e.g., UKBN2), historical datasets, and overlap with prior projects.
  - Selection criteria prioritise data length, data quality, and representativeness of UK hydrological/geographical variation; stakeholder input from workshops informs site choice.
- Groundwater levels
  - 54 boreholes selected from the BGS National Groundwater Level Archive (NGLA) to cover principal UK aquifers.
  - Criteria: regular monthly monitoring, long records (≥10 years), minimal abstraction impacts, strategic importance for drought risk assessment and water resources planning.
- Groundwater recharge
  - Aggregated across 588 groundwater bodies representing England, Wales, and Scotland; aligned with known hydrogeological characteristics and Water Framework Directive implementation.

## Data generation methods

- Core modelling approach
  - Translates rainfall and potential evaporation (PE) into river flow, soil moisture, groundwater levels, and recharge.
  - Builds on Future Flows and Groundwater lineage with advances since 2013, aligned to drought/hydrology modelling developments.
- UKCP18 processing
  - Uses 12 km regional UKCP18 projections; produces both 1 km gridded and catchment-averaged timeseries.
  - Catchment averages calculated using standard NRFA methods.
- Modelling suite (at-site simulations)
  - Hydrological models: GR4J, GR6J, and PDM (daily lumped rainfall–runoff, with GR6J improving low-flow simulation).
  - Groundwater models: AquiMod (groundwater level time-series) and ZOODRM (groundwater recharge).
  - Outputs provided as:
    - G2G: Grid-to-grid hydrological outputs (m3/s)
    - GR4J/GR6J: Daily flows (m3/s)
    - PDM: Daily flows (m3/s)
    - AquiMod: Groundwater levels (mAOD)
    - ZOODRM: Groundwater recharge (mm/day)
- Model ensembles
  - 12 UKCP18 regional climate model runs used to form an ensemble of projections.

## Data quality and processing

- Quality control sources
  - River flows: UK National River Flow Archive (NRFA)
  - Groundwater levels: UK National Groundwater Level Archive (NGLA)
- Model evaluation framework
  - Two-stage evaluation approach:
    1) Simulations driven by baseline observed climate data (simobs) tested against observations.
    2) Simobs vs simrcm (climate-model-driven) evaluated; for climate-model runs, focus on statistical characteristics rather than day-to-day sequence.
  - Metrics used include multiple Nash-Sutcliffe efficiency variants (for high/low flows), Kling-Gupta Efficiency, Absolute Percent Bias, Mean Absolute Percent Error, Q95 errors, Low Flow Volume, and MAM30-based errors.
  - Step 2 uses flow duration and low-flow frequency curves to compare statistical characteristics rather than exact timing.
- Data structure and storage
  - Dataset comprises 3304 CSV files organized by variable, model, and catchment/borehole.
  - Two main groups:
    - simobs: observation-driven simulations for meteorology, river flows, groundwater levels, and recharge (1961–2018 for meteorology; 1963–2018 for flows; 1962–2018 for groundwater).
    - simrcm: RCM-driven simulations for the same variables (1980–2080 meteorology; 1982–2080 flows and groundwater).
  - File naming conventions include ukcp18_simobs_ for station/borehole data and modelname_simobs_ for river/groundwater data; similar patterns for simrcm.
- Data availability
  - eFLaG_Dataset.zip contains 27 directories and 3304 files with standardized outputs suitable for policy analysis and monitoring.

## Practical implications for monitoring and policy

- Standardized, nationally coherent projections support scrutiny of environmental health measures across policy areas.
- Data provenance and governance
  - Clear linkage to UKCP18 inputs and documented processing steps facilitate traceability and reproducibility.
  - Emphasizes openness and the potential need to share underlying data and metadata to enable robust monitoring.
- Applicability to decision-making
  - Daily time-series at catchment or borehole scale enable assessment of drought/flood risk, water resource planning, and scenario testing under climate change.
  - The suite supports assessment of low-flow frequencies, drought characteristics, and groundwater recharge dynamics across the UK.
- Barriers and considerations for monitoring frameworks (as highlighted by the project context)
  - Metadata completeness and consistency across datasets.
  - Access to and sharing of underlying data can be a barrier; eFLaG demonstrates a structured, shareable dataset design.
  - Handling of data gaps and ensuring ongoing data updates to maintain relevance for policy.
  - Managing data transformation needs and ensuring interoperability with existing monitoring systems.