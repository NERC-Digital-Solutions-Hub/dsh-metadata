# Source apportionment of nutrient contributions to rivers in England and Wales modelled with SAGIS

- Purpose and scope
  - Estimates loads and in-river concentrations of nitrates and phosphates from multiple sector sources for England and Wales.
  - Results are summarised at Water Framework Directive (WFD) waterbody catchment scales and modelled with the SAGIS framework.
  - Aids catchment management decisions by identifying and quantifying pollution sources and predicting the impact of mitigation measures.

- SAGIS modeling framework
  - Developed under the UK Water Industry Research Programme with support from the Environment Agency and SEPA.
  - A decision-support tool to help regulators and stakeholders plan effective measures to meet WFD water quality expectations.
  - Combines input loads from major sector sources with a water quality model to predict in-stream concentrations.

- Input data and sources (how loads are estimated)
  - Diffuse sources: Agriculture (arable and livestock), Highways (major roads, not Wales), Urban runoff, Onsite wastewater treatment systems (OsWwTS), Atmospheric deposition.
  - Point sources: Wastewater treatment works (WwTW) effluent, Storm tanks/combined sewer overflows (CSOs), Industrial discharge.
  - Input loads per source are calculated using source-specific methods; data sources include national and regional datasets.
  - Key data sources per source (examples):
    - WwTW effluent: EA WIMS data (2010–2012), MCERTS (2010–2012).
    - River flow: EA flow archive (2001–2004).
    - Industrial discharge: EA Pollution Inventory.
    - CSOs and storm tanks: EA CSO locations, CIP monitoring, rainfall data, CORINE land use.
    - OsWwTS: predicted septic tank locations, UKWIR literature, PSYCHIC/PSYCHIC-derived transmissivity, sewer maps, occupancy rates.
    - Agriculture: 2012 agricultural census; PSYCHIC for phosphorus, MAGPIE/NEAP N for nitrogen.
    - Highways: HAWRAT; rainfall, highway network maps, mean event concentrations.
    - Urban runoff: rainfall, CORINE land use, literature concentrations.

- Simulation workflow and outputs
  - Inputs are routed into an upgraded SIMCAT river water quality model to mix loads with flow and predict in-stream concentrations.
  - SIMCAT performs a Monte Carlo simulation of river mixing and basic processes (partitioning and first-order decay).
  - Outputs are predicted concentrations at model features and every 1 km of river length.
  - Observed data (where available) are included to provide comparison and context.

- Uncertainty and limitations
  - National-scale input data and models, with limited refinement at local scales.
  - Confidence is considered good for catchments larger than approximately 50 km2.

- Dataset structure and format
  - For each pollutant, results are organized into five shapefiles covering England and Wales.
  - Shapefile attributes (representative examples):
    - ReachNo, ReachName, GISCode, X/Y coordinates, DISHeadKM (distance along the reach).
    - MeanConc_m (mean concentration), LCLimMnCon and UCLimMnCon (confidence limits for concentration).
    - MeanLdKGd and LCLimMnLd, UCLimMnLd (mean load and confidence limits).
    - ObsConc and ObsConcUCL/ObsConcLCL (observed concentrations and limits, if available).
    - SWConc, IMLoad, INLoad, MILoad, LSLoad, ARLoad, HWLoad, URLoad, ATLoad, BGLoad, STLoad, LKLoad and corresponding Conc/Load values (source-specific concentrations/loads).
  - Outputs include location-specific concentrations, loads, and associated uncertainty metrics, with upstream/downstream context relative to features.

- Data provenance and references
  - Environment Agency WFD catchments (Cycle 2 dataset).
  - UKWIR (Chemical Source Apportionment under the WFD) final report.
  - PSYCHIC model for phosphorus and sediment mobilisation.
  - MAGPIE modelling framework for nitrate losses.

- Practical relevance for analysts
  - Provides a reproducible, standardized framework to apportion nutrient sources and evaluate potential mitigation effects across large catchments.
  - Delivers harmonised, GIS-ready data (shapefiles) with explicit uncertainty metrics and per-source attribution for integrated environmental health assessments and policy scrutiny.