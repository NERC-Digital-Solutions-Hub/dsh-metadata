# Source apportionment of nutrient contributions to rivers in England and Wales modelled with SAGIS

## Overview
- Estimates loads and in-river concentrations of nitrates and phosphates from multiple sector sources across England and Wales.
- Results are summarized at Water Framework Directive (WFD) waterbody catchment scale and modelled with SAGIS.

## Framework and purpose
- SAGIS (Source Apportionment-GIS) framework developed under the UK Water Industry Research Programme with Environment Agency (EA) and SEPA.
- Primary objective: assist regulators and stakeholders, particularly the Water Industry, in planning effective measures to identify and quantify pollution sources and predict the impacts of mitigation to meet WFD water quality expectations.

## Data inputs and source-specific methods
- Sources considered (diffuse and point):
  - Agriculture nutrients
  - Highways runoff
  - Urban runoff
  - Onsite wastewater treatment systems (OsWwTS)
  - Atmospheric deposition
  - Wastewater treatment works (WwTW) effluent
  - Storm tanks/combined sewer overflows (CSOs)
  - Industrial discharge
- Methodologies vary by source (e.g., calculated vs. measured/reported) and rely on specific datasets:
  - WwTW effluent: EA WIMS data (2010–2012), MCERTS (2010–2012)
  - River flow: EA flow archive (2001–2004)
  - Industrial discharge: EA Pollution Inventory
  - CSOs and storm tanks: EA CSO data, CIP chemical monitoring, rainfall, CORINE land use
  - OsWwTS: EA-predicted locations, literature-derived concentrations, PSYCHIC, sewer network maps
  - Agriculture: 2012 agricultural census; PSYCHIC and MAGPIE models for phosphorus and nitrate dynamics
  - Highway runoff: HAWRAT tool and related inputs
  - Urban runoff: rainfall, land use, literature concentrations
- Key datasets and models:
  - PSYCHIC model for phosphorus and sediment mobilisation
  - MAGPIE framework for nitrate losses
  - CORINE land use data, rainfall inputs, and network maps

## Modelling approach and outputs
- Input loads are stored in a database; diffuse sources provided as mass per year per km2; point sources as mean and SD of annual concentrations and flow.
- Loads are routed into an upgraded SIMCAT river water quality model to simulate mixing, first-order decay, and other processes.
- SIMCAT uses Monte Carlo simulation to generate predicted in-river concentrations along the river, at 1 km resolution.
- River network and baseline flows derived from EA WFD catchments; outputs are targeted to model features along reaches.

## Uncertainty and limitations
- Uncertainty arises from national-scale inputs, with less refinement at local scales.
- Confidence in model outputs is considered good for catchments larger than ~50 km2.
- Local-scale verification may be limited by data gaps and quality of input datasets.

## Data format and structure
- For each pollutant (nitrates and phosphates), outputs are distributed across five shapefiles covering England and Wales.
- Shapefile attributes include:
  - ReachNo, GISCode, DISHeadKM, MeanConc_m, LCLimMnCon, UCLimMnCon, MeanLdKGd, LCLimMnLd, UCLimMnLd
  - Feature identifiers (FeatName, US_DS_Feat, ReachName)
  - Spatial coordinates (X, Y)
  - Observed data fields (ObsFlow, ObsQ90Flow, ObsQ95Flow, ObsQ99Flow, ObsConc, NumSamples, ObsConcUCL, ObsConcLCL)
  - Concentrations and loads associated with specific sources (SWConc, IMLoad, INLoad, MILoad, LSLoad, ARLoad, HWLoad, URLoad, ATLoad, BGLoad, STLoad, LKLoad and related Conc fields)
- File naming and structure are designed to support aggregation and cross-source analyses across the national catchment scale.

## Applications for monitoring and policy
- Provides a decision-support framework to identify major nutrient sources and quantify their contributions to in-river concentrations.
- Enables assessment of potential mitigation strategies and their expected impact on water quality to meet WFD targets.
- Supports catchment management planning, regulatory reporting, and stakeholder engagement by delivering transparent, source-specific contributions and uncertainty measures.

## Provenance and references
- Primary source: Comber et al. (2013) Development of a Chemical Source Apportionment Decision Support Framework for Catchment Management. Environ. Sci. Technol. 47, 9824-9832.
- Related datasets and models:
  - Environment Agency WFD catchments and water quality datasets
  - UKWIR reports on Chemical Source Apportionment under the WFD
  - PSYCHIC model (phosphorus and sediment mobilisation)
  - MAGPIE modelling framework for nitrate losses