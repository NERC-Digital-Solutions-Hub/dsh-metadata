# Enhanced Future Flows and Groundwater (eFLaG)

## Purpose and scope
- A nationally consistent UK hydrological dataset providing projections of river flow, groundwater levels, and groundwater recharge.
- Based on UKCP18 regional projections (12 km) with bias correction applied, covering 1981–2080; accompanies observation-driven data for 1962–2018 (1963 for river flow).
- Developed through a Met Office–led partnership (CR19_4 UK Climate Resilience) by UKCEH, BGS, and HR Wallingford.
- Sites: 200 catchments (river flow), 54 boreholes (groundwater levels), and 558 groundwater bodies (recharge).
- Data are organized to support climate resilience planning and water resources assessment at national, regional, and local scales.

## Catchment and site selection
- River flows: NRFA gauging stations compiled into a metadatabase, prioritizing long records, hydrometric quality, and representativeness of UK hydrology; stakeholder input used to influence site selection.
- Groundwater levels: 54 high-quality boreholes from the BGS National Groundwater Level Archive, chosen for regular monitoring, minimal abstractions impact, and long records (≥10 years); strategically important boreholes identified for drought risk assessment.
- Groundwater recharge: aggregated over 588 groundwater bodies across England, Wales, and Scotland to reflect hydrogeological characteristics and align with Water Framework Directive implementation; groundwater body shapefiles are available with the dataset.

## Data generation and modelling approach
- Core inputs: rainfall and potential evapotranspiration (PE) driving river flow, soil moisture, groundwater levels, and recharge.
- UKCP18 regional projections are downscaled to provide 1 km gridded meteorology and catchment-averaged series; catchment averages derived via standard NRFA methods.
- Modelling suite:
  - G2G (Grid-to-Grid) – distributed hydrological model producing river flows across gauged and ungauged locations (m3/s).
  - GR4J and GR6J – lumped daily hydrological models; GR6J improves low-flow simulations and groundwater exchange.
  - PDM – flexible lumped rainfall–runoff model (runoff production and routing behaviors).
  - AquiMod – lumped groundwater model simulating borehole groundwater levels (mAOD).
  - ZOODRM – distributed recharge model (mm/day) across a 2 km × 2 km grid.
- Outputs are provided as site-specific time series (simobs: observed-data-driven) and climate-model-driven (simrcm) runs; model parameters are supplied in CSV files within the eFLaG_dataset.zip.
- Units: river flows (m3/s); groundwater levels (mAOD); recharge (mm/day).

## Quality control and validation
- Data sourced from national repositories: UK National River Flow Archive (NRFA) and UK National Groundwater Level Archive (NGLA).
- Two-stage evaluation:
  - Stage 1: calibrate/validate models using baseline observed climate data (simobs) with multiple performance metrics (e.g., NSE, Nash–Sutcliffe, Kling Gupta, absolute percent bias, MAPE, Q95 error) across various flow regimes (low, high, average).
  - Stage 2: compare simobs and simrcm using flow-duration and low-flow frequency curves to assess statistical characteristics rather than exact day-to-day sequences.
- Full validation metrics and methods described in related works (e.g., Hannaford et al., in prep).

## Data structure and access
- Data are organized as CSV files within a dataset folder (eFLaG_Dataset.zip) containing 27 directories and 3,304 files.
- Two main file groups:
  - simobs (observation-driven): daily meteorology (precipitation + snowmelt + PET), river flows, groundwater levels, and groundwater recharge; years: meteorology 1961–2018; river flows 1963–2018; groundwater 1962–2018; recharge 1962–2018.
  - simrcm (RCM-driven): daily meteorology, river flows, groundwater levels, and groundwater recharge for 1980–2080 (meteorology) and 1981–2080 (recharge); river flows and groundwater data extend to 2080.
- File naming conventions:
  - simobs: ukcp18_simobs_[nrfa-station-number/borehole-name].csv; for river/groundwater data: modelname_simobs_nrfa-station-number.csv; AquiMod_simobs_borehole-name.csv; zoodrm_simobs_groundwater-body-name.csv.
  - simrcm: ukcp18_simrcm_[nrfa-station-number].csv; modelname_simrcm_nrfa-station-number.csv; AquiMod_simrcm_borehole-name.csv; zoodrm_simrcm_groundwater-body-name.csv.
- NRFA station numbers and borehole names are documented in eFLaG_Station_Metadata.xlsx.
- Deliverables include the eFLaG_dataset.zip with all files and accompanying figures and metadata.

## Deliverables, metadata, and usage
- Nationally consistent, ensemble-based hydrological projections to support climate resilience, drought planning, and water resource management in the UK.
- Data provenance, site metadata, and model parameter files are provided to enable reproducibility and reuse in downstream analyses.
- Challenges for analysts to consider: scale alignment between regional UKCP18 inputs and site-level hydrological responses; integration of multiple models with varying structures; data access and processing requirements due to large file volumes.