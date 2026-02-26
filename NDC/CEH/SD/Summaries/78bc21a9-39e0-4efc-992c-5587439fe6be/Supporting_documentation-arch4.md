# Supporting documentation for data: Feeney et al. (2022). Forecasting riverine erosion hazards to electricity transmission towers under increasing flow magnitudes, Climate Risk Management , 36, 100439, https://doi.org/10.1016/j.crm.2022.100439

## Overview
- Documents the dataset and methods behind Feeney et al. (2022) on riverine erosion hazards to electricity transmission towers in the UK.
- Purpose is transparency and reproducibility: provides inputs, outputs, and code to reproduce analyses and figures.
- Authors include UKCEH, University of Liverpool, and National Grid UK; Feeney is the data custodian.
- Version date: 16/10/2022; part of the UK Climate Resilience Programme; data linked to CAESAR-Lisflood modeling of the River Mersey reach from present day to 2050.

## Data provenance, custody, and reproduction
- Data custodian: Christopher Feeney (UKCEH); clearly documented authorship and responsibilities.
- Data intended for reuse and learning about the CAESAR-Lisflood model and its application to erosion hazards on critical infrastructure.
- CAESAR-Lisflood is third-party software; dataset provides the exact version used (v1.9j) and guidance to download it.
- R scripts (R version 4.x) and an R project file are included to facilitate reproduction of analyses and figures.

## Dataset content and structure
- Six main folders containing core model data and results:
  - Calibrated Runs
  - Channel_Changes
  - DoD
  - Flows
  - R_scripts
  - Towers
- Additional components supporting context and replication:
  - Changes_at_towers: 13 files including Tower_summaries.csv and 12 scenario-based files (H/L erosion) with erosion/deposition at tower locations (2019–2050).
  - Shapefiles: National Grid transmission towers and 30 m & 75 m buffers around each tower.
  - Tower_LookUp_Table.csv: metadata and erosion hazard risk categories for towers (Figures 7 & 8 in the paper).
- Third-party datasets referenced for model inputs and validation:
  - Environment Agency LiDAR (EA), NRFA flow data, BGS UKSO, OS/EDINA maps, National Grid towers.

## Data collection, generation, and modelling approach
- Primary datasets compiled in January 2020; historical flow data (NRFA) spanning 31/05/1976–31/05/2018; LiDAR-derived DEMs; soil textures from BGS/UKSO; historical OS maps and aerial imagery for channel changes.
- CAESAR-Lisflood used to simulate river channel changes along a 4.5 km reach of the River Mersey, with scenarios extending to 2050.
- Calibration uses historical channel changes to derive two erosion parameter sets: High and Low erosion models.
- Six future flow scenarios (Baseline, +10%, +20%, +30%, +40%, +50%) combined with High/Low calibrations yield 12 simulations.
- Outputs include calibrated inputs, model outputs, and derived figures/animations; DoD (digital elevation/DoD) calculations analyzed for erosion/deposition patterns.

## Data content details and file types
- Calibrated Runs
  - High and Low erosion inputs: bedrock.txt, High/Low_Erosion.xml, historic_flows.txt, mersey_dem_15m.txt, mersey_seds_15m.txt.
  - Results subfolder with animations, d50top, elev.dat, elevdiff, grain.dat, Mersey.dat, waterdepth files, and an animation.kml.
  - CAESAR-Lisflood input structure includes DEM, bedrock, flow input (historic_flows.txt), sediment grain input, and a model configuration file (.xml).
- Channel_Changes
  - Change_19762019.shp: digitised river channel changes from 1976, 1993, 2005, 2019.
  - Changes_comared.csv: areas eroded/deposited between years for Low/High erosion models (excluding 1976–1993 spin-up period).
- DoD
  - DoDs between 2006–2018 for real-world LiDAR and 2018–2050 simulated conditions (Low/High erosion).
  - Includes Sampled_values.csv (erosion/deposition totals per grid cell) and Scenarios with input/output DoD files for 2018–2050 runs.
  - DoD outputs used to create risk maps intersected with tower buffers (Figures 9 & 10).
  - DoD and raster outputs available in Scenarios/High/Erosion and Scenarios/Low/Erosion folders.
- Flows
  - High and Low folders with historic_flows.csv, Exceedance_probabilities_of_GEFs.csv, Sediment_fluxes.csv, plus six future-flow scenario inputs (baseline and +10% to +50%).
- R_scripts
  - Seven scripts to reproduce analyses and plots (Calibration_DoDs.R, Calibration_TimeSeries.R, DoD_histograms.R, Flow_Stats.R, Flow_TimeSeries.R, Scenario_erodep_pdfs.R, Scenario_TimeSeries.R); includes a README and an R project file.
- Towers
  - Changes_at_towers: 13 files with tower-level erosion/deposition data (2019–2050) and Tower_summaries.csv.
  - Shapefiles: tower polygons and 30 m & 75 m buffers.
  - Tower_LookUp_Table.csv: tower erosion hazard risk categories and related metadata.

## Data structure and file-level details
- DoD and outputs are provided in ASCII .txt and .csv/.shp formats for ease of loading into GIS and R.
- Input and output files use consistent naming conventions (e.g., mersey_dem_15m.txt, bedrock.txt, historic_flows.txt, d50top{n}.txt, elev.dat{n}.txt, elevdiff{n}.txt, grain.dat{n}.txt, waterdepth{n}.txt).
- Images and animation tools (mysavedimage{n}.png, animation.kml) enable geolocated visualization of results.

## Data quality, reproducibility, and limitations
- CAESAR-Lisflood is a deterministic model: identical inputs and settings yield identical results.
- Model calibration relies on historical channel-change data; future projections are scenario-based with inherent uncertainty, particularly in erosion calibration.
- The dataset is provided primarily to enable transparency and learning; modeling assumptions and third-party software introduce uncertainties beyond the raw data.
- Users are encouraged to download CAESAR-Lisflood v1.9j to replicate the exact workflow.

## External datasets and access
- Environment Agency LiDAR data; NRFA daily flow data; BGS Parent Material map; Ordnance Survey/EDINA base maps; EDINA aerial imagery; National Grid tower data.
- Access links are provided within the dataset documentation and third-party dataset references.

## Reproducibility and governance considerations for Data Leaders
- Clear data stewardship: Feeney acts as data custodian; versioned dataset with explicit authorship and responsibilities.
- Comprehensive provenance: detailed description of data sources, calibration, model versions, and workflow enables traceability and auditability.
- Structured data assets: six core folders plus auxiliary files provide a complete, navigable data lineage from inputs to outputs.
- Code and workflows: seven R scripts and an R project file, plus CAESAR-Lisflood input/output structures, support end-to-end replication of analyses and visualizations.
- Discoverability and interoperability: data are provided in common GIS-friendly formats (Shapefiles, ASCII .txt, CSV, DoD rasters) with clear naming conventions and documentation.
- Infrastructure needs: replicating results requires access to third-party software (CAESAR-Lisflood) and appropriate computing resources (8-PC cluster used for simulations).

## Key practical takeaways for data strategy
- When dealing complex geospatial/time-series modeling data, provide end-to-end reproducibility assets (model inputs/outputs, code, and versioned datasets).
- Include clear data custodian roles, versioning, and links to external data sources to ensure data integrity and reuse.
- Offer both raw inputs and derived outputs (e.g., DoD, tower risk summaries) to support different stakeholder use cases (policy planning, risk assessment, infrastructure resilience).
- Document data structure and file formats thoroughly to reduce onboarding time for new users and to facilitate cross-team collaboration.