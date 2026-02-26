# Source apportionment of nutrient contributions to rivers in England and Wales modelled with SAGIS

## Overview
- Estimates loads and in-river concentrations of nitrates and phosphates from multiple sector sources for England and Wales, summarized at Water Framework Directive (WFD) waterbody catchment scale.
- Modelled with SAGIS (Source Apportionment-GIS) to aid regulators and stakeholders in planning measures to identify pollutant sources and predict impacts of mitigation.
- Data underpinning the model include both diffuse and point sources, routed through a river quality model to produce in-stream concentrations.

## SAGIS framework and input data
- SAGIS developed under the UK Water Industry Research Programme with support from the Environment Agency and SEPA.
- Primary objective: a decision support tool for planning Pollution Source Management and evaluating mitigation scenarios to meet WFD water quality expectations.
- Inputs comprise estimated loads for major sector sources (diffuse and point) and a water quality model (SIMCAT) to predict in-river concentrations.
- SIMCAT Monte Carlo framework provides flow and concentration uncertainties, delivering predictions every 1 km along the river network.

## Data sources, methods, and inputs
- For each source, inputs are estimated using methodology appropriate to the source (summarised in corresponding tables).
- Key sources and methods:
  - Wastewater treatment works (WwTW) effluent: calculated using EA WIMS data (2010–2012) and MCERTS (2010–2012).
  - River flow: measured/reported (EA flow archive, 2001–2004).
  - Industrial discharge: measured/reported (EA Pollution Inventory).
  - Combined Sewer Overflows (CSOs): calculated using EA CSO locations, CIP data, rainfall intensity, CORINE land use.
  - Storm tanks / intermittent discharges: calculated with WwTW locations, CIP data, rainfall, CORINE land use.
  - Onsite wastewater treatment systems (OSWwTS/septic tanks): calculated using predicted septic tank locations, literature concentrations, transmissivity data, sewer maps, occupancy rates.
  - Agriculture nutrients: modeled with PSYCHIC for phosphorus and NEAP N for nitrogen; 2012 agricultural census data used.
  - Highway runoff: modeled with HAWRAT; inputs from rainfall, highway maps, and mean event concentrations.
  - Urban runoff: calculated using rainfall, CORINE land use, and literature concentrations.
- Estimated inputs are stored in a database as diffuse-source loads (mass per year or month per km2) and point-source loads as mean and SD of annual concentrations and flow.
- These inputs are routed into the SIMCAT model to produce in-river concentrations at model features and at 1-km river segments.

## Format and structure of the dataset
- For each pollutant, results are delivered as five shapefiles covering England and Wales.
- Shapefile attributes include:
  - Reach-related fields: ReachNo, ReachName, GISCode, DISHeadKM, US_DS_Feat, X, Y.
  - Concentration fields: MeanConc_m, LCLimMnCon, UCLimMnCon, ObsConc, ObsConcLCL, ObsConcUCL, SWConc, IMConc, INConc, etc. (milligrams per litre).
  - Load fields: MeanLdKGd, LCLimMnLd, UCLimMnLd, SWLoad, IMLoad, INLoad, MILoad, LSLoad, ARLoad, HWLoad, URLoad, ATLoad, BGLoad, STLoad, LKLoad (kilograms per day).
  - Observed flow fields: ObsFlow, ObsQ90Flow, ObsQ95Flow, ObsQ99Flow (megalitres per day).
  - Metadata: Description, Units, NumSamples.
- The dataset spans the nationwide scale of England and Wales with model outputs on a per-reach basis.

## Uncertainty and limitations
- National-scale inputs mean local refinement is limited; results are less certain at finer spatial scales.
- Confidence in model outputs is considered adequate for catchments larger than ~50 km².
- Uncertainty is inherently linked to the input data quality, measurement coverage, and model assumptions within SIMCAT and PSYCHIC/NEAP frameworks.

## Provenance, use, and governance considerations
- Core provenance: Environment Agency WFD catchments data, UKWIR report on Chemical Source Apportionment, PSYCHIC and MAGPIE modelling frameworks.
- Intended use: regulatory decision support for planning measures to meet WFD targets; scenario analysis for pollution source mitigation.
- Data governance notes for Data Stewards:
  - Clear data lineage from multiple datasets (WIMS, MCERTS, Pollution Inventory, CIP, CORINE, HAWRAT, PSYCHIC, NEAP, census data).
  - Documentation of methodologies per source and the overall SAGIS/SIMCAT workflow.
  - National-scale scope with explicit mention of local applicability limitations; ensure appropriate metadata and caveats accompany any dissemination.
  - Format uses widely interoperable GIS shapefiles with rich per-feature attributes; coordinate system is British National Grid, facilitating integration with other UK datasets.
  - Regular updates would require re-running inputs with newer data (e.g., WwTW, flows, CIP, census) and re-validating SIMCAT outputs.