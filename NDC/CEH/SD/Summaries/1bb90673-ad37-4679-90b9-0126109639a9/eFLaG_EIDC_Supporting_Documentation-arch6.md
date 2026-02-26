# Enhanced Future Flows and Groundwater (eFLaG)

## Overview and purpose
- Nationally consistent hydrological projections for the UK, based on UKCP18 regional climate projections (12 km resolution).
- Projections span 1981–2080; accompanying observation-driven data cover 1962–2018 (river flow: 1963–2018).
- Generated to support climate resilience by providing bias-corrected river flow, groundwater level, and groundwater recharge simulations.

## Data scope: sites, catchments, and bodies
- 200 catchments for river flow simulations.
- 54 boreholes for groundwater level simulations.
- 558 groundwater bodies representing principal aquifers across England, Wales, and Scotland for recharge simulations.
- Site metadata available in eFLaG_Station_Metadata.xlsx; site maps in project figures.
- Catchment and groundwater-body selection designed to reflect UK hydrological and hydrogeological variability and water industry relevance.

## Data generation methods
- Base climate input: UKCP18 Regional projections (HadGEM3-GC3.05 and HadREM3-GA705), processed to provide 1 km gridded and catchment-averaged precipitation and potential evaporation (PE).
- Hydrological and groundwater modelling ensemble:
  - Hydrological: GR4J, GR6J, and PDM models.
  - Groundwater: AquiMod (levels) and ZOODRM (recharge).
  - Outputs produced at site scale (catchment or borehole).
- Data processing and bias correction applied to UKCP18 regional outputs to generate eFLaG time-series.
- G2G (Grid-to-Grid) model used for spatially coherent river flow outputs (gauged and ungauged).
- Model parameter files and recharge calculations provided or accessible via dataset package.

## UKCP18 processing and bias correction
- UKCP18 regional climate outputs drive the ensemble, with bias correction applied before hydrological transformation.
- Time-series produced for river flow, groundwater levels, and recharge at site locations and scale.

## Model specifics
- G2G: distributed hydrological model producing flows on 1 km to catchment scales.
- GR4J: simple daily lumped model (4 parameters) for various catchments.
- GR6J: six-parameter variant enhancing low-flow and groundwater exchange representations.
- PDM: versatile lumped rainfall–runoff model, provided with calibrated parameters.
- AquiMod: lumped groundwater model delivering daily borehole-level simulations (mAOD).
- ZOODRM: distributed recharge model (2 km × 2 km grid) using a modified FAO-56 approach (potential recharge in mm/day).
- Calibrated parameter files are included; PDM parameters available on request.

## Data structure and accessibility
- eFLaG_Dataset.zip contains 27 directories and 3,304 CSV files.
- Data split into two main groups:
  - simobs: observation-driven simulations for meteorology, river flows, groundwater levels, and recharge; includes observed values where available.
  - simrcm: RCM-driven simulations for the same variables across the 12 UKCP18 regional climate models.
- File naming conventions (examples):
  - ukcp18_simobs_nrfa-station-number.csv (meteorology or river flow for a NRFA station)
  - AquiMod_simobs_borehole-name.csv (groundwater levels)
  - zoodrm_simobs_groundwater-body-name.csv (groundwater recharge)
  - modelname_simobs_nrfa-station-number.csv (RCM-driven river flow)
  - AquiMod_simrcm_borehole-name.csv (RCM-driven groundwater levels)
  - zoodrm_simrcm_groundwater-body-name.csv (RCM-driven recharge)
- Data availability:
  - simobs: meteorology (precip + snowmelt + PET) 1961–2018; river flow 1963–2018; groundwater levels and recharge 1962–2018.
  - simrcm: meteorology 1980–2080; river flow 1982–2080; groundwater levels and recharge 1981–2080.
- NRFA station numbers and borehole names are listed in the attached station metadata workbook.

## Quality control and validation
- Data sources:
  - River flows: UK National River Flow Archive (NRFA).
  - Groundwater levels: UK National Groundwater Level Archive (NGLA).
- Validation approach (two-stage):
  - Step 1: Simobs (observed-driven) vs observations for river flow and groundwater; multiple performance metrics.
  - Step 2: Simobs and simrcm evaluated on a common baseline period using statistical flow characteristics (flow duration curves and low-flow frequency curves) rather than day-to-day sequence due to climate model sequencing limitations.
- Evaluation metrics include:
  - Nash-Sutcliffe Efficiency (NSE) variants for high flows, low flows, and general performance (including log and square-root transforms).
  - Modified Kling-Gupta Efficiency (KGE) for various flow focuses.
  - Absolute Percent Bias (ABIAS), Mean Absolute Percent Error (MAPE).
  - Q95 Absolute Percent Error (Q95 APE), Low-Flow Volume (LFV), and various percentile-based metrics.
  - Absolute Percent Error in the mean annual minimum on a 30-day moving average (MAM30 APE).
- Full validation details are documented in Hannaford et al. (in prep).

## Outputs and usage
- Time-series products suitable for exploring river flows, groundwater levels, and recharge under climate change scenarios.
- Files provide both observed-driven baselines and climate-model-driven projections, enabling assessment of future hydrological and groundwater responses.
- Model parameter files (GR4J, GR6J, PDM) andAquiMod and ZOODRM configurations available within the dataset; PDM parameters can be requested via ForecastModelSupport@ceh.ac.uk.
- The dataset supports data exploration and product development by allowing self-serve analyses and end-user interpretation for policy and planning contexts.

## References and basis
- UKCP18 science and regional projections; foundational modelling and dataset lineage cited throughout, including NRFA, NGLA, and multiple hydrological and hydrogeological modelling studies and manuals.