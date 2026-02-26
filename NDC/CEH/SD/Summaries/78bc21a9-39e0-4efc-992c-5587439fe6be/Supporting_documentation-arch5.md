# Supporting documentation for data: Feeney et al. (2022). Forecasting riverine erosion hazards to electricity transmission towers under increasing flow magnitudes, Climate Risk Management , 36, 100439, https://doi.org/10.1016/j.crm.2022.100439

## Overview
- Documents the dataset associated with the Feeney et al. (2022) study on river erosion hazards to electricity transmission towers in a 4.5 km reach of the River Mersey, UK, under multiple increasing flow scenarios.
- Context: UK Climate Resilience Programme project on Erosion Hazards in River Catchments; funded by Natural Environment Research Council (Grant NE/S01697X/1).
- Time horizon and scope: present-day to 2050; uses CAESAR-Lisflood for hydro-morphodynamic modelling; multiple synthetic flow scenarios (no change to +50%).

## Data custodians, authors, and versioning
- Custodian and corresponding author: Christopher Feeney, UKCEH.
- Other authors: Samantha Godfrey (University of Liverpool), James Cooper (University of Liverpool), Andrew Plater (University of Liverpool), Douglas Dodds (National Grid UK).
- Version date: 16/10/2022.
- Purpose: provide transparency and reproducibility for data collection, model inputs/outputs, and analyses; includes scripts and files to reproduce figures and results.

## Data contents at a glance
- Main data categories:
  - Inputs to CAESAR-Lisflood (model runs)
  - Model outputs (calibrated High/Low erosion models and 12 future-flow scenarios)
  - DoDs (difference of DEMs) and related raster data
  - Flows and sediment flux data by grain size
  - R scripts to reproduce analyses and figures
  - Tower-related data (locations, erosion/deposition at towers, risk categorisation)
  - Shapefiles for National Grid towers and buffer zones
  - Tower lookup and summaries
- File structure highlights:
  - Calibrated Runs (High and Low) with bedrock.txt, <High/Low>_Erosion.xml, historic_flows.txt, mersey_dem_15m.txt, mersey_seds_15m.txt; results include animation PNGs, d50top, elev.dat, elevdiff, grain.dat, Mersey.dat, waterdepth, and animation.kml.
  - Channel_Changes: historical channel change data and comparison CSVs.
  - DoD: DoDs from LiDAR (EA_LIDAR_diffs) and modelled DoDs (High_ero_diffs, Low_ero_diffs), plus Scenarios with erosion/deposition cell analyses and Raster_to_Points vectors.
  - Flows: six future flow scenarios with historic_flows.csv and sediment fluxes; exceedance probabilities for geomorphologically effective flows (GEFs).
  - R_scripts: seven R scripts to reproduce analyses and plots; includes a READ ME and an R project file.
  - Towers: 13 files including Tower_summaries.csv; 40 tower records with erosion/deposition data 2019–2050; Shapefiles with tower locations and 30 m/75 m buffers.
  - Tower_LookUp_Table.csv: tower-specific erosion/hazard risk categories.
- Third-party and external datasets referenced (not provided in this package but required for replication).

## Data collection and generation methods
- Primary data sources (collected January 2020 or sourced for calibration):
  - NRFA daily flow data (Ashton Weir) for 1976–2018.
  - Environment Agency LiDAR-derived DEMs (15 m resolution) for terrain inputs.
  - BGS UK soil texture data (9 grain-size fractions) via UK Soil Observatory.
  - Ordnance Survey maps and EDINA aerial imagery (4.5 km Mersey reach; 1976, 1993, 2019 maps; 2005 imagery).
- Modelling approach:
  - CAESAR-Lisflood used to simulate river channel changes from 1976 to 2018 and to create future flow scenarios (2018–2050).
  - Two calibration configurations: High erosion and Low erosion, representing parameter sensitivity.
  - Six future flow scenarios (Baseline, +10%, +20%, +30%, +40%, +50%), resulting in 12 total simulations when combined with High/Low calibrations.
  - Simulations run on an 8-PC Windows cluster (University of Liverpool).
- Outputs and inputs prepared for reproducibility:
  - Input files suitable for CAESAR-Lisflood v1.9j (downloadable from SourceForge).
  - R scripts and datasets prepared to reproduce analyses and figures.

## Nature and units of recorded values
- Simulated hydro-morphological variables, including:
  - Lateral erosion and deposition rates (m^2 yr^-1).
  - Elevations, elevation differences, flow depths, and sediment grain-size fractions (m).
  - Mean daily discharge (m^3 s^-1).
  - Daily sediment fluxes across nine grain-size fractions (m^3 day^-1) and total.

## Quality control and reproducibility
- CAESAR-Lisflood is deterministic; identical inputs and settings yield identical results.
- dataset includes all necessary input files to run the model for described simulations.
- Reproducibility checks:
  - Model version used: CAESAR-Lisflood v1.9j.
  - Analyses and figures reproduced in R (R version 4.x); scripts verified before publication and data deposition.
  - An explicit R project file and a README accompany the R_scripts.

## Data structure and file organization (detailed)
- Calibrated Runs
  - High and Low folders containing:
    - bedrock.txt (erodibility, with buildings treated as unerodible)
    - High_Erosion.xml / Low_Erosion.xml (model parameters)
    - historic_flows.txt (daily discharge 1976–2018)
    - mersey_dem_15m.txt (historical DEM)
    - mersey_seds_15m.txt (sediment texture)
    - Results subfolder with:
      - Animation PNGs
      - d50top{n}.txt, elev.dat{n}.txt, elevdiff{n}.txt
      - grain.dat{n}.txt, Mersey.dat, waterdepth{n}.txt
      - Mersey_outputQ&s.txt (flow and sediment data)
      - animation.kml
- Channel_Changes
  - Change_19762019.shp (digitized channel changes; 1976–1993–2005–2019)
  - Changes_compared.csv (areas eroded/deposited between periods; 1993–2005 and 2005–2018; 1976–1993 excluded)
- DoD
  - EA_LIDAR_diffs, High_ero_diffs, Low_ero_diffs, Scenarios (DoD rasters)
  - Sampled_values.csv (erosion/deposition totals by scenario)
  - Scenarios subfolders include Input files to run CAESAR-Lisflood (2018–2050) and a Results folder containing DoD outputs for Figure 6
  - Raster_to_Points shapefiles for risk mapping around towers
- Flows
  - High and Low folders
  - Exceedance_probabilities_of_GEFs.csv
  - historic_flows.csv
  - Sediment_fluxes.csv
- R_scripts
  - Calibration_DoDs.R, Calibration_TimeSeries.R, DoD_histograms.R, Flow_Stats.R, Flow_TimeSeries.R, Scenario_erodep_pdfs.R, Scenario_TimeSeries.R
  - READ ME with script descriptions
  - R project file for navigation
- Towers
  - Tower_summaries.csv (metadata on each tower; year installed; erosion/deposition data)
  - Shapefiles (tower locations with 30 m and 75 m buffers)
- Tower_LookUp_Table.csv
  - Summary of erosion/deposition at each tower and hazard risk category
- External datasets (referenced but not hosted in this package)
  - CAESAR-Lisflood and input tools
  - EA DEM data, NRFA daily flow data, BGS UKSO, National Grid towers, EDINA base maps

## Third-party datasets and software prerequisites
- CAESAR-Lisflood and helper tools (RasterEdit, GranfileMaker) via SourceForge
- EA LiDAR DEM data
- NRFA daily flow data
- BGS Parent Material map
- EDINA OS maps and aerial imagery
- National Grid tower data (for risk assessment; buffer analyses)
- CAESAR-Lisflood v1.9j recommended for replication
- R (version 4.0.x used for scripts) and accompanying R project file

## Governance, provenance, and use considerations for Data Stewards
- Clear data provenance: authors, custodian, project context, and versioning dates documented.
- Detailed metadata and structured data: explicit descriptions of inputs, model configurations, outputs, and data relationships.
- Reproducibility emphasis: complete set of input files, scripts, and replication instructions; deterministic modelling.
- Access to external data and licenses: references to third-party sources and downloadable datasets; ensure compliance with external data licenses when reusing.
- Data quality and limitations: model-based DoDs and scenario-based forecasts rely on calibration; some comparisons exclude early periods due to spin-up and data limitations.
- Data governance challenges aligned with this dataset:
  - Complex, multi-format data across many folders and subfolders.
  - Interoperability across GIS formats, ASCII rasters, and CSVs.
  - Large data volume from multiple scenario runs and temporal snapshots.
  - Dependence on externally maintained modelling software and data sources.

## Key takeaways for Data Stewards
- This dataset exemplifies rigorous provenance, reproducibility, and governance practices for complex, model-based environmental data.
- It provides a comprehensive package: inputs, calibrated outputs, scenario results, DoDs, risk mappings, and code to reproduce analyses.
- Important to maintain versioning, provide clear metadata, and host or reference all external dependencies to enable reuse by other researchers and practitioners.
- When updating, ensure consistency across model configurations, input sources, and output schemas, and document any changes to calibrations, flow scenarios, or data sources.