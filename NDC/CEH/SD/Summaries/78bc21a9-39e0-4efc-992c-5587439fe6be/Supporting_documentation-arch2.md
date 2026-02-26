# Supporting documentation for data: Feeney et al. (2022). Forecasting riverine erosion hazards to electricity transmission towers under increasing flow magnitudes, Climate Risk Management , 36, 100439, https://doi.org/10.1016/j.crm.2022.100439

- Purpose and scope
  - Provides transparent data and methods to forecast river erosion hazards affecting electricity transmission towers along the River Mersey, UK.
  - Uses CAESAR-Lisflood hydrodynamic–landscape evolution modelling to project channel change from present day to 2050 under multiple increasing flow scenarios.
  - Supports adaptation planning for critical infrastructure by producing hazard indicators and risk maps for towers.

- Authors, custodian, and version
  - Authors: Feeney (UKCEH), Godfrey, Cooper (University of Liverpool), Plater (University of Liverpool), Dodds (National Grid UK).
  - Data custodian: Christopher Feeney (UKCEH).
  - Version date: 16/10/2022.

- Key objectives and findings (as per abstract)
  - Riverbank erosion poses significant threats to transmission towers; interventions may be required to avert destabilisation.
  - Erosion threats scale with increasing flow magnitudes; model calibration strongly influences projected erosion, highlighting uncertainty in long-term forecasts.
  - Long-term simulations aid adaptation planning for towers; follow-up, reach- and catchment-scale work needed to time large floods and assess protective measures.
  - Outputs include calibrated High/Low erosion models and 12 future projections (2018–2050) across six flow scenarios.

- Data contents at a glance
  - Model inputs and configurations:
    - River reach inputs for CAESAR-Lisflood (4.5 km Mersey reach): DEM, bedrock, historical flows, sediment grainsize inputs.
    - Channel-change boundaries from 1976–2019 OS maps and aerial imagery.
    - Model calibration runs: two configurations labeled High and Low erosion.
    - Historic flows (1976–2018) and sediment flux context; 9 grain-size fractions for scenario runs.
  - Model outputs and processed data:
    - Calibrated Run results for High and Low erosion models.
    - DoD (difference of DEMs) products for real and simulated conditions (2006–2018/2019).
    - Scenario outputs for 2018–2050 under six future flow magnitudes, for both High and Low erosion calibrations.
    -Processed outputs in ArcMap, Excel, and R; including images, grain-size, elevation, and discharge data.
  - Code and reproducibility:
    - R scripts to reproduce analyses and figures (Calibrations, DoDs, flows, scenarios, etc.).
    - An accompanying R project file to navigate six data folders.
  - Tower-related data and risk assessment:
    - Tower metadata (40 towers) with 30 m and 75 m buffer zones.
    - Tower erosion/deposition summaries, and a lookup table categorising tower erosion hazard risk.
    - DoD-based risk maps informing Figures 7–10 of the associated paper.

- Data structure and organization
  - Six main folders:
    - Calibrated Runs (High and Low; input and result files)
    - Channel_Changes (historical channel changes and comparisons)
    - DoD (DoDs for real and simulated conditions; scenarios)
    - Flows (historic and scenario flow inputs)
    - R_scripts (seven scripts plus README for reproducibility)
    - Towers (towers shapefiles, buffers, and Tower_LookUp_Table)
  - Additional components:
    - Third-party datasets and external links (CAESAR-Lisflood, EA LiDAR DEMs, NRFA flow data, UKSO, National Grid towers, EDINA maps).
    - CAESAR-Lisflood input files structure (DEM, bedrock, flow input, sediment grainfile, model XML/config).
    - CAESAR-Lisflood output files structure (d50top, elev, elevdiff, grain, waterdepth, Mersey_outputQands, animation images, and KML).

- CAESAR-Lisflood modelling details (inputs and outputs)
  - Inputs:
    - DEM: mersey_dem_15m.txt; bedrock.txt (erodibility lowered to reflect subsurface bedrock).
    - Flow input: historic_flows.txt with daily discharge and 10 sediment columns (columns 5–14 cover 9 grain-size fractions; historic runs had all grains 0 due to calibrations).
    - Sediment grain size input: grainfile with coordinates, identifiers, placeholder, and 9 grain-size thicknesses across depth layers.
    - Model configuration: XML file with parameters; can be edited to replicate results.
  - Outputs:
    - Surface median grain size (d50top{n}.txt), elevations (elev{n}.txt), elevation changes (elevdiff{n}.txt).
    - Grain-size characteristics per grid cell (grain.dat{n}.txt), water depth (waterdepth{n}.txt).
    - Daily discharge and sediment flux outputs (Mersey_outputQands.txt; also available as Mersey.DAT).
    - Visualizations: animation images and Google Earth-friendly animation.kml.
  - Simulations:
    - Calibrated Runs: High and Low erosion models calibrated against historical channel changes (1976–2018).
    - Scenario runs: 6 future flow scenarios (Baseline, +10% to +50%) for both High and Low erosion calibrations; total of 12 scenario simulations.
    - DoD-based analyses for erosion/deposition across years and scenarios.

- Quality control and reproducibility
  - CAESAR-Lisflood is deterministic; identical inputs yield identical results.
  - Provided complete input files for all simulations; users can download CAESAR-Lisflood v1.9j to reproduce runs.
  - Analyses were cross-validated with R (ver. 4) scripts and again prior to data submission.

- Data access and reuse
  - Third-party tools and data cited with links (CAESAR-Lisflood, EA LiDAR, NRFA, BGS UKSO, National Grid towers, EDINA).
  - Instructions and files enable users to reproduce results or adapt methods to other reach-scale studies.
  - Dataset supports environmental monitoring workflows by enabling transparency, standardization, and data sharing for hydromorphological risk assessment.

- Relevance to environmental monitoring and policy performance
  - Demonstrates how to integrate multi-source data (topography, flows, sediments, infrastructure) into a standard modelling workflow for long-term hazard forecasting.
  - Produces actionable products: risk maps for towers, erosion/deposition trends, and scenario-based planning inputs for adaptation strategies.
  - Highlights the importance of model calibration, uncertainty assessment, and the value of making inputs, outputs, and code openly accessible for scrutiny and reuse.

- Limitations and uncertainties
  - Erosion predictions are sensitive to calibration of the erosion processes; long-term forecasts carry notable uncertainty.
  - Additional reach- and catchment-scale modelling recommended to refine flood timings and evaluate protective measures for towers.

- External datasets and tools
  - CAESAR-Lisflood core model (download link provided).
  - Environment Agency LiDAR DEMs, NRFA flow data, BGS parent material maps, National Grid tower data, OS EDINA base maps.

- Data custodian contact
  - Feeney, Christopher (UKCEH) as corresponding author and data custodian.