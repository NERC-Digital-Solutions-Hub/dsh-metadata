# Source apportionment of nutrient contributions to rivers in England and Wales modelled with SAGIS

## Overview
- Estimates of loads and in-river concentrations of nitrates and phosphates for England and Wales, modelled with SAGIS.
- Results summarised at Water Framework Directive (WFD) waterbody catchment scale.
- Aims to identify and quantify pollution sources and predict effects of mitigation measures to meet WFD water quality expectations.

## SAGIS framework and aims
- Source Apportionment-GIS (SAGIS) developed to aid regulators and stakeholders (notably Water Industry) in planning measures to quantify pollution sources and predict mitigation impacts.
- Supports decision-making for water quality improvement under the WFD.

## Input data and source-specific methods
- Loads and concentrations are derived from major sectorial sources (diffuse and point) and routed through a river water quality model.
- Source-specific methodologies and datasets include:
  - Wastewater treatment works (WwTW) effluent: calculated; datasets from EA WIMS (2010–2012) and MCERTS (2010–2012).
  - River flow: measured/reported; EA flow archive (2001–2004).
  - Industrial discharge: measured/reported; EA Pollution Inventory.
  - Combined sewer overflows (CSOs): calculated; EA CSO data, CIP chemical monitoring, rainfall, CORINE land use.
  - Storm tanks/excess from FFT: calculated; WwTW locations, CIP monitoring, rainfall, CORINE land use.
  - On-site wastewater treatment systems (OSWwTS): calculated; EA predicted septic tank locations, literature concentrations, PSYCHIC transmissivity, sewer networks, occupancy data.
  - Agriculture nutrients: modeled with PSYCHIC for phosphorus and NEAP-N for nitrogen; 2012 agricultural census data.
  - Highway runoff: modeled with HAWRAT; rainfall, road networks, mean event concentrations.
  - Urban runoff: calculated; rainfall, CORINE land use, urban literature concentrations.
- All inputs are stored as estimated loads (diffuse, per year per km2) or mean/SD concentrations (point sources); combined in SIMCAT for in-stream concentrations.

## Modeling approach and outputs
- Input loads are stored in a database and routed into the SIMCAT river quality model to predict in-river concentrations.
- SIMCAT uses Monte Carlo simulation to account for variability in river mixing and first-order processes (partitioning, decay).
- Outputs provide predicted concentrations and loads at model features along river reaches, every 1 km of river stretch.

## Uncertainty and applicability
- National-scale inputs; local refinements are limited.
- Confidence in model outputs is considered good for catchments larger than approximately 50 km2.

## Data format and dataset contents
- For each pollutant, results are provided in five shapefiles covering England and Wales.
- Shapefile attributes include:
  - ReachNo, ReachName, Description, GISCode, X/Y coordinates.
  - DISHeadKM (distance along reach), US_DS_Feat (location relative to feature).
  - MeanConc_m (mean concentration in mg/L); LCLimMnCon and UCLimMnCon (95% confidence limits).
  - MeanLdKGd (mean load in kg/day); LCLimMnLd and UCLimMnLd (confidence limits).
  - Observed and statistical fields: ObsFlow, ObsQ90Flow, ObsQ95Flow, ObsQ99Flow, ObsConc, NumSamples, ObsConcUCL, ObsConcLCL.
  - Concentration and load contributions by source categories (SWConc, IMLoad, INLoad, MILoad, LSLoad, ARLoad, HWLoad, URLoad, ATLoad, BGLoad, STLoad, LKLoad, etc.) and their associated concentrations/loads.
- File naming convention specifies the pollutant reported in each file.

## Metadata and references
- Data sources and methodological background documented in:
  - Environment Agency (2015). WFD Surface Water Management Catchments Cycle 2.
  - UKWIR (2012). Chemical Source Apportionment under the WFD.
  - PSYCHIC model description (Davison et al., 2008).
  - MAGPIE modelling framework (Lord & Anthony, 2000).