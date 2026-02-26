# Forecasting riverine erosion hazards to electricity transmission towers under increasing flow magnitudes

## Overview
- Supporting documentation for the Feeney et al. (2022) dataset accompanying the Climate Risk Management paper.
- Part of the UK Climate Resilience Programme on Erosion Hazards in River Catchments; funded by the Natural Environment Research Council (Grant NE/S01697X/1).
- Version date: 16/10/2022.
- Authors and data custodian: Christopher Feeney (UKCEH), Samantha Godfrey, James Cooper, Andrew Plater (University of Liverpool), Douglas Dodds (National Grid UK).

## Purpose and scope
- Provides transparent data and files to reproduce and understand the study forecasting river erosion hazards to electricity transmission towers along the River Mersey, UK.
- Uses CAESAR-Lisflood (coupled hydrodynamic and landscape evolution model) to simulate river channel changes from 1976 to 2050 on a 4.5 km reach.
- Explores multiple increasing flow magnitude scenarios (Baseline plus +10% to +50%) under two erosion calibrations (High and Low), delivering 12 scenario simulations.

## Data content and structure
- Inputs to model
  - River reach extent: 4.5 km along River Mersey (Partington vicinity).
  - Data sources: NRFA flows, Environment Agency LiDAR Digital Terrain Models (DTMs), BGS soil textures, UKSO soils, OS maps, EDINA aerial imagery.
  - Preparations: historical channel changes digitised from maps/images; bedrock and DEM inputs; sediment grain-size fractions and flow series.
- Model outputs
  - Calibrated erosion models: High and Low.
  - 12 future scenario simulations (6 flow scenarios × 2 calibrations).
  - Processed results in ArcMap, Excel, and R; animations and DoD maps.
  - DoD (Difference of DoDs) and tower-focused outputs for erosion/deposition assessment.
- Datasets and files organized into six folders:
  - Calibrated Runs (High, Low) with input and result files; includes bedrock.txt, historic_flows.txt, Mersey_dem_15m.txt, mersey_seds_15m.txt, and configuration XMLs.
  - Channel_Changes (historical changes and comparisons between Low/High erosion models).
  - DoD (real-world LiDAR DoD and modelled DoDs; scenarios and raster-to-points data for risk mapping).
  - Flows (historic_flows.csv and scenario-based flow inputs; exceedance probabilities for GEFs).
  - R_scripts (seven R scripts to reproduce analyses and figures; includes a README).
  - Towers (Shapefiles for National Grid towers and 30 m/75 m buffers; Tower_Summaries.csv and Tower_LookUp_Table.csv).
- Third-party datasets and tools
  - CAESAR-Lisflood and tools (RasterEdit, GranfileMaker).
  - EA LiDAR and DEM data; NRFA daily flow data; BGS UKSO material map.
  - National Grid tower data; OS/ EDINA base maps.
  - External links provided for data sources and CAESAR-Lisflood download.

## Data collection and generation
- Primary datasets collected January 2020; flows (1976-2018) from NRFA; LiDAR-derived DEMs from EA; soil textures from BGS/UKSO; historical channel boundaries from OS maps and aerial imagery.
- CAESAR-Lisflood calibration:
  - Two best-performing calibrations (High and Low) derived from 1976-2018 historical flows and sediment data.
  - 12 simulations produced using six future flow scenarios (Baseline plus +10% to +50%).
- Future flow scenarios
  - Baseline, +10%, +20%, +30%, +40%, +50% (applied to both High and Low erosion calibrations).
  - Outputs include flow, sediment flux, and DoD projections.

## Data types and units
- Simulated hydro-morphological variables:
  - Lateral erosion/deposition rates (m^2 per year).
  - Elevations, elevation differences, flow depths, sediment grain sizes (m).
  - Mean daily discharge (m^3 s^-1).
  - Daily sediment flux totals across 9 grain-size fractions (m^3 per day).

## Quality control and reproducibility
- CAESAR-Lisflood is deterministic; identical inputs yield identical outputs.
- Provided input files for all described simulations to enable replication.
- Model version used: CAESAR-Lisflood v1.9j; instructions/link to download included.
- Analyses and figures reproduced in R (v4); scripts tested prior to publication and data release.
- Comprehensive documentation and a READ ME accompany the dataset.

## Data structure details
- Calibrated Runs
  - High and Low subfolders containing: bedrock.txt, <High/Low>_Erosion.xml, historic_flows.txt, mersey_dem_15m.txt, mersey_seds_15m.txt, and results (animations, d50top, elev.dat, elevdiff, grain.dat, Mersey.dat, waterdepth, etc.).
- Channel_Changes
  - Change_19762019.shp (historical river channel changes by year), Changes_comared.csv (areas eroded/deposited for 1993-2005 and 2005-2018).
- DoD
  - EA_LIDAR_diffs, High_ero_diffs, Low_ero_diffs doDs (raster TIFFs) and 2006-2018 comparisons; Scenarios subfolder contains input/outputs for 2018-2050 DoD with Raster_to_Points shapefiles for risk mapping.
- Flows
  - High/Low folders with historic_flows.csv, Sediment fluxes.csv, and Exceedance_probabilities_of_GEFs.csv across six scenarios.
- R_scripts
  - Seven scripts to reproduce calibrations, DoDs, time series, flows, and scenarios; includes a READ ME and an R project file.
- Towers
  - Tower_Summaries.csv, 12 “2019-2050” files (H/L erosion scenarios) with annual erosion/deposition at each tower; 30 m and 75 m tower buffers in Shapefiles.
  - Tower_LookUp_Table.csv summarises erosion/deposition and erosion hazard category per tower for Figures 7 & 8.

## Usage and intended audience
- Designed for transparency and learning about CAESAR-Lisflood applications at reach-scale.
- Enables replication of analyses, exploration of erosion hazards to transmission towers, and development of risk maps.
- Data suitable for researchers, practitioners, and infrastructure planners assessing climate-related erosion risks to critical infrastructure.