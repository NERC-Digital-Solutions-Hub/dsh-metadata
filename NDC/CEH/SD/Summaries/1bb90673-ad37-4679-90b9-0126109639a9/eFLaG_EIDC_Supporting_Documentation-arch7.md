# OVERVIEW Enhanced Future Flows and Groundwater (eFLaG) is a dataset of nationally consistent hydrological (river flow, groundwater level and groundwater recharge) projections for the UK, based on the latest UK Climate Projections (UKCP18; Murphy et al. 2019).

## Scope and Timeline
- Projections span from 1981 to 2080; an accompanying observation-driven dataset covers 1962 (1963 for river flow) to 2018 for river flow and groundwater level/recharge.
- Project funded by the Met Office through the Strategic Priorities Fund Climate Resilience Programme; collaboration between UKCEH, BGS and HR Wallingford.
- Driven by UKCP18 Regional 12 km projections with bias correction; outputs provided as 1 km gridded and catchment-averaged time-series.
- Spatial coverage: 200 catchments (river flow), 54 boreholes (groundwater levels), and 558 groundwater bodies (groundwater recharge).

## Data Generation and Processing
- Core workflow: rainfall and potential evapotranspiration (PE) from UKCP18 are used to drive hydrological and groundwater models, building on approaches from Future Flows and Groundwater Levels (FFGWL).
- UKCP18 processing converts regional projections into 1 km grids and catchment averages for hydrological modelling.
- Model ensemble:
  - Hydrological: G2G (Grid-to-Grid), GR4J, GR6J, PDM
  - Groundwater: AquiMod (levels) and ZOODRM (recharge)
- Outputs are provided at site scale (catchment or borehole) and, for G2G, at 1 km grid when applicable.

## Models and Outputs
- G2G: distributed hydrological model providing river flows at gauged and ungauged locations (units: m3/s).
- GR4J/GR6J: daily lumped hydrological models; GR6J emphasizes low flows and groundwater exchange; outputs in m3/s.
- PDM: a flexible lumped rainfall-runoff model; outputs in m3/s.
- AquiMod: lumped groundwater model; outputs as groundwater level time-series (mAOD).
- ZOODRM: distributed recharge model (2 km x 2 km grid); outputs as potential recharge (mm/day).
- Calibrated model parameters provided in eFLaG_dataset.zip; all outputs reported in consistent units (mostly m3/s for flows, mAOD for levels, mm/day for recharge).

## Data Structure and Access
- Data stored as CSV files, organized into two groups:
  - simobs: observation-driven simulations for meteorology, river flows, groundwater levels, and recharge
  - simrcm: RCM-driven simulations for the same variables
- Year ranges:
  - simobs: meteorology (precip with snowmelt + PET) 1961–2018; river flow 1963–2018; groundwater levels 1962–2018; groundwater recharge 1962–2018
  - simrcm: meteorology 1980–2080; river flow 1982–2080; groundwater levels 1982–2080; groundwater recharge 1981–2080
- File naming conventions:
  - simobs: ukcp18_simobs_[NRFA station number or borehole name].csv for meteorology; modelname_simobs_nrfa-station-number.csv for river/groundwater/recharge
  - simrcm: ukcp18_simrcm_[station or borehole].csv for meteorology; modelname_simrcm_nrfa-station-number.csv for river/groundwater/recharge
- Dataset package: eFLaG_Dataset.zip contains 27 directories and 3,304 files.
- Site metadata: eFLaG_Station_Metadata.xlsx lists NRFA station numbers and borehole names.

## Data Quality Control and Validation
- Primary data sources: UK National River Flow Archive (NRFA) and UK National Groundwater Level Archive (NGla).
- Two-stage validation approach:
  - Step 1: Calibration and evaluation using baseline observed climate data (simobs runs) against observations across multiple metrics, with a focus on low-flow performance and regime characteristics.
  - Step 2: Comparison of simobs and simrcm over the common baseline period using flow duration curves and low-flow frequency curves (national-scale assessment rather than day-to-day replication).
- Evaluation metrics (examples): Nash-Sutcliffe Efficiency (general, high flows, low flows), log-transformed NSE, Modified Kling Gupta Efficiency, Absolute Percent Bias, Mean Absolute Percent Error (MAPE), Q95 Absolute Percent Error, Low-Flow Volume, and percentiles-based metrics.
- Full validation details: Hannaford et al. (in prep).

## GIS-Relevance and Practical Considerations
- The dataset provides nationally consistent, spatially explicit hydrological projections suitable for map-based analyses and policy-relevant GIS visualisations.
- GIS workflows can:
  - Aggregate 1 km grid outputs to catchments or groundwater bodies for map products.
  - Compare across multiple models (G2G, GR4J, GR6J, PDM) and scenarios.
  - Assess future river flows, groundwater levels, and recharge at catchment/borehole scales.
- Data handling considerations:
  - Large volume: 3,304 files; plan for storage and processing.
  - Requires alignment of metadata (NRFA IDs, borehole names) with spatial layers for accurate mapping.
  - Units vary by variable; ensure consistency when building maps (flows in m3/s, levels in mAOD, recharge in mm/day).

## References and Metadata
- Core references include UKCP18 science report, NRFA catchment rainfall methodology, and eFLaG methodological papers (detailed references provided in the document).
- Metadata and station/borehole identifiers are available in the accompanying Excel workbook (eFLaG_Station_Metadata.xlsx).