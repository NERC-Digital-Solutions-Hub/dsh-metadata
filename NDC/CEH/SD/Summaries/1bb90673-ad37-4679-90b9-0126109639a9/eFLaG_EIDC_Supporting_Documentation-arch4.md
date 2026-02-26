# OVERVIEW Enhanced Future Flows and Groundwater (eFLaG) is a dataset of nationally consistent hydrological (river flow, groundwater level and groundwater recharge) projections for the UK, based on the latest UK Climate Projections (UKCP18; Murphy et al. 2019)

- Purpose: A national dataset of hydrological projections for climate impact assessment, driven by UKCP18 regional projections and bias-corrected for river flow, groundwater levels, and recharge.
- Coverage: Projections span 1981–2080; accompanying observation-driven data cover 1962/1963–2018 for river flow and groundwater-related variables.
- Partners and funding: Developed through a Met Office-led Strategic Priorities Fund Climate Resilience Programme collaboration; UKCEH, British Geological Survey (BGS) and HR Wallingford contributed.
- Data processing base: UKCP18 Regional 12 km projections, bias-corrected and fed into multiple hydrological and groundwater models.
- Intended use: Supports climate-resilience assessments by providing consistent, nationally representative hydrological time series and enabling comparative analysis across sites.

## DATA SCOPE AND STRUCTURE

- Spatial and temporal scope:
  - 200 catchments (river flow)
  - 54 boreholes (groundwater levels)
  - 558 groundwater bodies (recharge and groundwater context)
  - Time series from 1980s/1980s–2080s; observation-driven data for historical calibration/validation.
- Site metadata:
  - Catchment and borehole selection based on data quality, record length, strategic networks, and stakeholder input.
  - Groundwater bodies chosen to reflect major UK aquifers and hydrogeological characteristics; designed to align with Water Framework Directive needs.
  - Metadata files include site lists and associations (eFLaG_Station_Metadata.xlsx).
- Data outputs and units:
  - River flow: cubic metres per second (m3/s)
  - Groundwater levels: metres above Ordnance Datum (mAOD)
  - Groundwater recharge: millimetres per day (mm/day)
- Data packaging:
  - eFLaG_Dataset.zip contains 27 directories and 3304 CSV files.
  - Two main file groups:
    - simobs: observation-driven simulations for meteorology, river flow, groundwater levels, and recharge
    - simrcm: RCM-driven simulations for the same variables
  - File naming conventions link each file to a specific NRFA station, borehole, model (G2G, GR4J, GR6J, PDM, AquiMod, ZOODRM), and dataset type.

## DATA GENERATION AND MODELLING

- Core modelling framework:
  - River and groundwater models transform rainfall and potential evaporation into hydrological outputs.
  - Models used: G2G (Grid-to-Grid), GR4J and GR6J (water balance models), PDM (Probability Distributed Model), AquiMod (groundwater levels), ZOODRM (groundwater recharge).
- UKCP18 data processing:
  - Regional 12 km climate projections processed to produce 1 km gridded time series and catchment-averaged rainfall and PE for hydrological modelling.
  - Catchment averages derived using standard NRFA method.
- Ensemble and outputs:
  - Ensemble approach with 12 RCMs for simrcm outputs.
  - Simobs provides observed-driven baselines; simrcm provides climate-model-driven projections.
  - Calibration and parameter files provided (e.g., GR6J parameters, PDM parameters) within the dataset.
- Model validation and calibration:
  - Quality-controlled long-term data from national repositories:
    - River flows: UK National River Flow Archive (NRFA)
    - Groundwater levels: UK National Groundwater Level Archive (NGLA)
  - Two-stage evaluation:
    - Stage 1: Simobs vs observations (baseline data) using a range of metrics, with emphasis on low flows and overall flow regimes.
    - Stage 2: Simobs and simrcm performance over baseline period, using flow duration curves and low-flow frequency curves (since climate models don’t reproduce exact historical sequences).
  - Evaluation metrics include Nash-Sutcliffe Efficiency (various focuses), Kling-Gupta Efficiency, Absolute Percent Bias, Mean Absolute Percent Error, and Q95-based measures, among others.

## DATA DISCLOSURE, ACCESS, AND DISCIPLINARY PRACTICES

- Data structure and discoverability:
  - All data are stored as CSV files in a defined folder structure (3304 files total), enabling programmatic access and reproducibility.
  - Documentation references to metadata catalogs and site lists accompany the dataset (eFLaG_Station_Metadata.xlsx; NRFA/NGLA data repositories).
- Data quality, provenance, and governance:
  - Long-term, quality-controlled inputs from NRFA and NGLA underpin model calibration and evaluation.
  - Clear documentation of model types, calibration parameters, and evaluation metrics supports transparency and reproducibility.
- Updates and reuse:
  - Dataset is structured to support scenario comparison, sensitivity analyses, and cross-site planning for water resources and drought resilience.
  - Model parameter files are provided, enabling re-use or re-calibration with alternative inputs or updated climate projections.

## END-USER VALUE FOR DATA LEADERS

- Strategic data alignment:
  - Provides a coherent, nationally consistent hydrological projection dataset aligned with UKCP18, enabling organization-wide data strategy for climate resilience and water resource planning.
- Comprehensive data coverage:
  - Combines multiple hydrological and groundwater models across numerous key UK sites, facilitating end-to-end assessment of future flows, groundwater levels, and recharge.
- Quality and trust:
  - Rigorous two-stage validation against long-term observed records ensures credible projections for policy and operational use.
- Discoverability and collaboration:
  - Rich metadata, explicit site lists, and standardized file structures improve discoverability, enabling cross-team use and potential collaboration with national data networks.