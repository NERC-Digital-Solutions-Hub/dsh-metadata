# Source apportionment of nutrient contributions to rivers in England and Wales modelled with SAGIS

## Overview
- Estimates of loads and in-river concentrations of nitrates and phosphates from multiple sector sources across England and Wales, summarised at Water Framework Directive (WFD) catchment scale.
- Modelled with the SAGIS framework to support regulators and stakeholders in planning measures to identify, quantify, and mitigate pollution sources and meet WFD water quality expectations.
- National-scale dataset; outputs include concentrations and loads with associated uncertainty.

## Data sources and modelling approach
- Sector sources (diffuse and point): Agriculture (arable and livestock), Highways, Urban runoff, Onsite wastewater treatment systems, Atmospheric deposition, Wastewater treatment works (WwTW) effluent, Storm tanks/CSOs, Industrial discharge.
- SAGIS workflow:
  - Derives input loads for each source using source-specific methods and key datasets.
  - Routes loads into an upgraded SIMCAT river water quality model to predict in-river concentrations by mixing loads with river flow (Monte Carlo simulation).
  - Outputs concentrations along each model feature and at every 1 km of river reach.
- Input datasets by source include:
  - WwTW effluent: EA WIMS data (2010–2012), MCERTS (2010–2012).
  - River flow: EA flow archive (2001–2004).
  - Industrial discharge: EA Pollution Inventory.
  - CSOs and storm tanks: EA CSO locations, CIP monitoring data, rainfall, CORINE land use.
  - OSWwTS (septic tanks): EA-predicted locations, literature concentrations, transmissivity data, sewer maps, occupancy rates.
  - Agriculture: 2012 Agricultural census; PSYCHIC model for phosphorus and sediment, NEAP-N for nitrate.
  - Highway runoff: HAWRAT tool, rainfall, highway maps, AVG concentrations.
  - Urban runoff: rainfall, CORINE land use, literature concentrations.
- Outputs and structure:
  - Diffuse inputs provided as mass per year or per month per km²; point sources as mean and SD of annual concentrations and flow.
  - Shaped outputs used by SIMCAT to produce predicted concentrations and loads across the river network.

## Data structure and format
- The dataset is stored in five shapefiles per pollutant covering England and Wales; each file corresponds to a pollutant.
- Common attributes (Table 3 mappings):
  - ReachNo, ReachName, GISCode, X/Y coordinates, DISHeadKM (distance along reach), ObsFlow and various observed flow/concentration fields.
  - MeanConc_m and ObsConc (milligrams per litre) with confidence bounds (LCLimMnCon, UCLimMnCon; ObsConcLCL/ObsConcUCL).
  - MeanLdKGd and Load fields with lower/upper confidence bounds (LD-related: LCLimMnLd, UCLimMnLd).
  - Feature-derived fields: FeatName, US_DS_Feat, SWConc, IMLoad, INLoad, MILoad, LSLoad, ARLoad, HWLoad, URLoad, ATLoad, BGLoad, STLoad, LKLoad, and corresponding concentration/load values per source category.
- Coverage: nationwide, across all WFD catchments in England and Wales.

## Uncertainty and limitations
- Uncertainty arises from national-scale inputs and simplified local refinements.
- Confidence is described as good for catchments larger than approximately 50 km²; local-scale precision may be limited.

## Governance, provenance and reuse
- SAGIS framework developed under the UK Water Industry Research Programme (UKWIR) with support from the Environment Agency and SEPA.
- Purpose-built decision support tool to aid regulators and the water industry in planning measures and evaluating the impacts of mitigation actions to meet water quality standards.
- Data sources and methodologies are documented, enabling traceability of inputs, assumptions, and models; formats (shapefiles) facilitate integration with geographic information systems for further analysis and dissemination.

## Practical implications for Data Leaders
- Key data assets include multi-sector input loads, routine river flow data, and model outputs linking loads to in-river concentrations.
- Emphasizes the importance of metadata, provenance, and transparent methodologies for joinable, citable datasets across catchments.
- Demonstrates the value of an integrated, GIS-enabled, model-based approach for national-scale environmental data products and decision support.
- Highlights limitations associated with national-scale modelling when tailoring solutions for local context, underscoring the need for local refinement where necessary.