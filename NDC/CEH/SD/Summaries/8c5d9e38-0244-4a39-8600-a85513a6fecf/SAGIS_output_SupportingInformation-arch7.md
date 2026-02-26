# Source apportionment of nutrient contributions to rivers in England and Wales modelled with SAGIS

## Overview
- Dataset estimates loads and in-river concentrations of nitrates and phosphates from multiple sector sources for England and Wales.
- Results are summarized at the Water Framework Directive (WFD) waterbody catchment scale and modelled with SAGIS.
- Aimed at supporting catchment management decisions and regulatory planning.

## SAGIS framework
- Source Apportionment-GIS (SAGIS) was developed under UKWIR with EA and SEPA support.
- Purpose: a decision support tool to identify and quantify pollution sources and predict impacts of mitigation measures to meet WFD water quality expectations.
- Integrates input loads from major sector sources (diffuse and point) with a water quality model to predict in-stream nutrient concentrations.

## Input data and source methodologies
- Input loads are estimated using methods tailored to each source, then routed through SIMCAT for in-stream concentration predictions.
- Key sector sources include:
  - Wastewater treatment works (WwTW) effluent
  - Industrial discharge
  - Combined sewer overflows (CSOs)
  - Storm tanks / excess flow
  - Onsite wastewater treatment systems (OSWwTS)
  - Agriculture (diffuse) and related farming sources
  - Highway runoff
  - Urban runoff
  - Atmospheric deposition
- Datasets used for inputs include:
  - WwTW effluent: EA WIMS (2010–2012) and MCERTS data (2010–2012)
  - River flow: EA flow archive (2001–2004)
  - Industrial discharge: EA Pollution Inventory
  - CSOs and storm tanks: EA CSO data, CIP chemical monitoring, rainfall, CORINE land use
  - OSWwTS: predicted septic tank locations, UKWIR literature concentrations, PSYCHIC transmissivity, sewer network data, occupancy rates
  - Agriculture: 2012 Agricultural Census; PSYCHIC phosphorus model; MAGPIE nitrate model references
  - Highway runoff: HAWRAT tool, standard rainfall, highway maps
  - Urban runoff: rainfall, CORINE land use, literature concentrations
- Outputs are stored as inputs to an upgraded SIMCAT river water quality model, enabling Monte Carlo-style river mixing and process simulations.

## Data products and shapefile structure
- For each pollutant, results are delivered as five shapefiles covering England and Wales.
- Shapefile attributes (common structure) include:
  - ReachNo, ReachName, Description, GISCode, X, Y (British National Grid coordinates)
  - DISHeadKM (distance along SAGIS-SIMCAT reach)
  - MeanConc_m (average concentration) with LCLimMnCon and UCLimMnCon (confidence bounds)
  - MeanLdKGd (average load) with LCLimMnLd and UCLimMnLd (confidence bounds)
  - ObsFlow and ObsQxxFlow (observed flow metrics)
  - ObsConc and ObsConcUCL/ObsConcLCL (observed concentration and bounds)
  - NumSamples (number of samples)
  - SWConc/ SWLoad, IMLoad, INLoad, MILoad, LSLoad, ARLoad, HWLoad, URLoad, ATLoad, BGLoad, STLoad, LKLoad (average concentrations/loads by source category)
  - FeatName (feature name) and US_DS_Feat (relation to feature: upstream, downstream, or at)
  - Additional concentration/load fields for each sector (e.g., background, agricultural, industrial, etc.)
- The five shapefiles together provide a comprehensive, spatially explicit view of concentrations and loads along river reaches, with uncertainty estimates.

## Uncertainty and limitations
- The dataset is national-scale and not refined to local detail; local resolution and precision may be limited.
- Confidence in model outputs is considered good for catchments larger than ~50 km2.
- Uncertainty is propagated through the SIMCAT Monte Carlo approach and dependent on input data quality and resolution.

## Format, usage, and GIS considerations
- Data are provided as shapefiles designed for GIS analysis and map-based visualization.
- Projections are in the British National Grid; suitable for UK-based spatial analyses and integration with catchment-scale mapping.
- Suitable for GIS specialists to:
  - Visualize spatial distribution of nutrients along reaches
  - Compare concentration and load estimates by pollutant and source
  - Assess uncertainty bounds and observed data
  - Combine SAGIS outputs with other catchment management tools and datasets
  - Support evidence-based decision-making for mitigation measures under the WFD framework

## References and context
- Environment Agency (2015). WFD Surface Water Management Catchments Cycle 2 dataset.
- UKWIR (2012). Chemical Source Apportionment under the WFD. Final UKWIR report.
- PSYCHIC model for phosphorus/sediment mobilisation (Davison et al., 2008).
- MAGPIE modelling framework for nitrate losses (Lord & Anthony, 2000).