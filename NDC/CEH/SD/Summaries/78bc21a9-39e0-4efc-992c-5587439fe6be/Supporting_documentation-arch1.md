# Supporting documentation for data: Feeney et al. (2022). Forecasting riverine erosion hazards to electricity transmission towers under increasing flow magnitudes, Climate Risk Management , 36, 100439, https://doi.org/10.1016/j.crm.2022.100439

## Overview
- Dataset accompanying the Feeney et al. (2022) paper on predicting river erosion threats to electricity transmission towers in the River Mersey, UK.
- Contains model inputs/outputs for CAESAR-Lisflood, scenarios of increasing flow, and supporting analyses to reproduce figures and results.
- Aims to aid transparency, teach application of CAESAR-Lisflood, and support scenario planning for critical infrastructure resilience.

## Dataset scope and objectives
- Provides inputs to a 4.5 km reach study along the River Mersey and outputs from CAESAR-Lisflood, including calibrated erosion models (Low and High) and 12 future channel-change projections.
- Includes processed results (ArcMap/Excel), R scripts, and data to reproduce analyses and figures from the paper.
- Supports learning and replication of CAESAR-Lisflood applications at reach-scale and informs adaptation planning for transmission towers.

## Data contents (major components)
- Calibrated Runs: two erosion-model calibrations (High and Low) with input and output files to run CAESAR-Lisflood from 1976–2018.
- Channel_Changes: historical river-channel change mapping and comparisons between Low/High erosion models.
- DoD (Differences of Difference): height-change datasets comparing real-world LiDAR (2006–2018/2019) with modelled scenarios; includes scenario-based raster data and point shapefiles for risk mapping.
- Flows: six future-flow scenarios (baseline, +10% to +50%) with historic flow data and sediment flux inputs; exceedance probabilities for geomorphologically effective flows.
- R_scripts: seven R scripts to reproduce analyses and plots; includes a README and an R project file.
- Towers: GIS data for National Grid transmission towers within the Mersey reach, including 30 m and 75 m buffers; Tower_LookUp_Table with erosion risk categories per tower.
- Third-party datasets and external sources: references and links to CAESAR-Lisflood tools, EA LiDAR, NRFA flows, BGS materials, OS/EDINA maps, and National Grid towers.

## Data collection and generation methods
- Primary data sources (Jan 2020): NRFA continuous-flow data (1976–2018) for Ashton Weir; Environment Agency LiDAR DEMs; BGS soil texture maps; Ordnance Survey maps and aerial imagery (1976/1993/2019 maps and 2005 imagery).
- Channel boundaries digitised from maps/images and merged to quantify historical erosion/deposition for calibration.
- CAESAR-Lisflood simulations run on an 8-PC Liverpool cluster; two best calibrations produce “High” and “Low” erosion models.
- Future flow scenarios (2018–2050) derived by applying percent increases to Calibrated_High and Calibrated_Low outputs, producing 12 scenario simulations (6 flow scenarios × 2 calibrations).
- Outputs include not only channel-change data but also visualizations, DEM updates, and sediment data for interpretation.

## Nature and units of recorded values
- Simulated hydro-morphological variables:
  - Lateral erosion/deposition rates (m^2 yr^-1)
  - Elevations, elevation differences, flow depths, sediment grain sizes (m)
  - Mean daily discharge (m^3 s^-1)
  - Daily sediment fluxes by grain-size fractions (m^3 day^-1)

## Quality control
- CAESAR-Lisflood is deterministic; identical inputs yield identical results.
- Provided input files to reproduce all described simulations; recommended CAESAR-Lisflood v1.9j for replication.
- Analyses and figures were cross-validated in R (v4) before publication and data submission.

## Data structure (folder overview)
- Calibrated Runs: High and Low erosion model inputs (bedrock, flows, DEM, sediment, configuration) plus results (animations, d50top, elev, elevdiff, grain.dat, Mersey_outputQ&s, waterdepth) and a Mersey output file.
- Channel_Changes: Shapefile-based river-change maps and Changes_comared.csv (areas eroded/deposited; limited to reliable periods 1993–2005 and 2005–2018).
- DoD: LiDAR-based real-world DoD (EA LiDAR) and DoD derived from simulations for Low/High erosion; scenario-based erosion/deposition raster data; Scenarios subfolder with high/low erosion and raster-to-points for risk mapping near towers.
- Flows: High/Low subfolders with historic and future flow inputs, including Exceedance_probabilities_of_GEFs.csv, historic_flows.csv, and Sediment fluxes.csv.
- R_scripts: Seven scripts to reproduce analyses and figures, plus a READ ME and an R project file.
- Towers: Tower-related data such as Tower_summaries.csv, 2019–2050 erosion/deposition data by tower, and a Shapefiles folder with tower locations and buffers.
- Includes Tower_LookUp_Table.csv summarizing erosion metrics and risk category per tower.

## CAESAR-Lisflood input files structure
- DEM file: mersey_dem_15m.txt (ASCII raster)
- Bedrock file: bedrock.txt (lowered values; buildings treated as unerodible)
- Flow input file: historic_flows.txt (14 columns; Day, Discharge, placeholders, and 10 sediment-flux columns)
- Sediment grain-size input: generated by GrainfileMaker; grid-cell centroids, identifiers, placeholders, and 9 grain-size thickness columns across multiple layers
- Model configuration: optional XML file; can be loaded in CAESAR-Lisflood or generated from provided tables to replicate results
- Notes: The historic flows in calibration have zero sediment columns; scenario inputs use scenario-derived sediment fluxes from calibration modelling.

## CAESAR-Lisflood output files structure
- d50top{n}.txt: surface median grain size per grid cell (m); {n} minutes since start
- elev.dat{n}.txt: cell elevations (m)
- elevdiff{n}.txt: net elevation change since start; negative = deposition, positive = erosion
- grain.dat{n}.txt: updated grain-size distributions by layer per grid cell
- waterdepth{n}.txt: water depth per grid cell
- Mersey_outputQands.txt: daily discharge and sediment loads at outlet
- Visual outputs: animation images (mysavedimage{n}.png) and animation.kml for Google Earth visualization

## Third-party datasets and external sources
- CAESAR-Lisflood tools and input utilities
- EA LiDAR DEM data
- NRFA daily flow data
- BGS UKSO sediment/soil materials
- National Grid tower data and network maps
- OS/EDINA base maps and aerial imagery

## Reproducibility and usage
- Fully documented dataset designed to enable replication of the paper’s analyses and figures.
- Includes scripts and project structure to reproduce statistical analyses and generate risk maps near transmission towers.
- Suitable for learners and practitioners applying CAESAR-Lisflood to reach-scale geomorphic forecasting and infrastructure resilience planning.

## Access and version notes
- CAESAR-Lisflood version recommended: 1.9j (free download)
- R environment used for analyses: R v4.x
- Version date of the dataset: 16/10/2022
- External links and data sources provided to obtain original input datasets and model tools.