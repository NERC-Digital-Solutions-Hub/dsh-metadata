# Forecasting riverine erosion hazards to electricity transmission towers under increasing flow magnitudes

## Overview
- Supporting documentation for Feeney et al. (2022) describing a dataset that models river erosion threats to electricity transmission infrastructure in the UK.
- Aims to aid transparency, inform monitoring policies, and support adaptation planning for critical infrastructure under climate-driven flow increases.
- Uses CAESAR-Lisflood to simulate river channel changes along a 4.5 km reach of the River Mersey and to generate erosion/deposition scenarios up to 2050.

## Data collection and context
- Primary data sources (collected January 2020): 
  - NRFA daily flow records (1976–2018)
  - Environment Agency LiDAR-derived DEMs (resampled to 15 m)
  - BGS soil texture data (9 sediment grain-size fractions)
  - OS maps and EDINA aerial imagery (1976, 1993, 2005, 2019; 2005 imagery)
- Channel changes calibrated against historical maps/images; used to calibrate erosion parameters.
- Modelling scope:
  - Calibration runs: High and Low erosion parameterizations
  - Scenarios: Baseline plus 10–50% flow magnitudes (six future flow scenarios)
  - Combinations: 2 calibrations × 6 flow scenarios = 12 simulations
- Outputs support hazard assessment for 40 National Grid towers within the Mersey reach.

## Modelling approach and calibration
- Model: CAESAR-Lisflood (coupled cellular automata erosion and 2D hydrodynamics)
- Deterministic simulations: identical inputs yield identical outputs
- Calibrations:
  - High erosion and Low erosion parameter settings
  - Use historical flows (1976–2018) and observed channel changes for calibration
- Scenario design:
  - Baseline and six increase-in-flow scenarios (plus 10% to 50% in 10% steps)
  - Each calibration combined with each scenario yields 12 total simulations
- Outputs used to evaluate erosion hazard to towers and inform adaptation planning

## Data structure and contents
- Six main folders containing the dataset:
  - Calibrated Runs (High and Low erosion models; input and output files for each)
  - Channel_Changes (historical changes and comparisons between models)
  - DoD (Difference of DEMs; real and simulated DoDs for 2006–2018 and 2018–2050)
  - Flows (historic and scenario-based flow and sediment inputs)
  - R_scripts (seven R scripts to reproduce analyses and figures)
  - Towers (tower-related data and buffers)
- Key input files (CAESAR-Lisflood):
  - mersey_dem_15m.txt (DEM)
  - bedrock.txt (erodible bedrock with buildings treated as unerodible)
  - historic_flows.txt (daily flows; 1976–2018)
  - mersey_seds_15m.txt (sediment fractions)
  - base_scenario / plus_10_percent … plus_50_percent flow inputs (Scenarios)
  - GrainfileMaker-generated grain size inputs (surface and subsurface layers)
  - XML configuration files for model setup
- Key outputs:
  - d50top{n}.txt, elev.dat{n}.txt, elevdiff{n}.txt, grain.dat{n}.txt, waterdepth{n}.txt (per time step)
  - Mersey_outputQands.txt (daily discharge and sediment loads)
  - DoDs (elevation differences; real and modelled)
  - Animation images and animation.kml for Google Earth
- Tower-related data:
  - Tower_summaries.csv (metadata for each tower; erosion/deposition by year 2019–2050)
  - Shapefiles and Tower_LookUp_Table.csv (tower erosion hazard classifications; 30 m and 75 m buffers)

## Data governance, reproducibility, and access
- Emphasis on transparency and openness:
  - Public sharing of underlying data and scripts where possible
  - CAESAR-Lisflood v1.9j recommended for replication
  - Full R scripts (R v4.x) to reproduce analyses and figures
  - A READ ME and project file accompany the dataset
- Reproducibility:
  - Deterministic model; identical inputs yield identical outputs
  - Input/output structures and file naming standardized to facilitate replication
- External data and third-party tools:
  - CAESAR-Lisflood and tools (RasterEdit, GranfileMaker)
  - EA LiDAR, NRFA, BGS UKSO, National Grid, OS/EDINA
  - Links provided for data access and external datasets

## Use in monitoring frameworks and policy decisions
- Enables monitoring of environmental health and infrastructure risk under climate-change scenarios:
  - Quantifies erosion/deposition risk at each tower location and across time
  - Produces risk maps (Figures 7–10 in the related paper) and tower-specific summaries
  - Supports scenario planning for infrastructure resilience and prioritization of interventions
- Data products suitable for governance:
  - DoD analyses to identify areas of concern and to verify model predictions
  - Tower_LookUp_Table and Tower_summaries for decision-makers evaluating vulnerabilities
  - Open access inputs and outputs to inform future monitoring approaches and data governance standards

## Limitations and uncertainties
- Uncertainty in long-term river channel forecasting; sensitive to erosion parameter calibrations
- Need for broader reach/catchment-scale modelling to refine timing of large floods and intervention effectiveness
- DoD-based comparisons rely on model calibrations; real-world verification requires continued data collection and monitoring

## Practical guidance for use
- For researchers and policymakers:
  - Use provided inputs to run CAESAR-Lisflood v1.9j and reproduce results
  - Leverage the DoD outputs and tower risk data to inform monitoring programs and mitigation planning
  - Consider both High and Low erosion calibrations to bracket uncertainty in erosion processes
- For data management teams:
  - Follow the six-folder data structure and file naming conventions
  - Use the included R_scripts and R project to reproduce analyses
  - Refer to external data sources and ensure metadata and data governance standards are maintained at data origin