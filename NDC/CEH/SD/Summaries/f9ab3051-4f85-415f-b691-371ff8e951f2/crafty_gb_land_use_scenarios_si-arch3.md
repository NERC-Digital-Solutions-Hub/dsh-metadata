# Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UKSSPs) and climate projections (UK-RCPs)

## Overview
- Provides decadal 1 km resolution land-use maps for Great Britain up to 2080, generated with the CRAFTY-GB agent-based model.
- Scenarios couple climate (UK-RCP) and socio-economic pathways (UK-SSP) to explore future land-system change under linked conditions.
- Data cover six UK-RCP-SSP combinations (RCP2.6-SSP1, RCP4.5-SSP2, RCP4.5-SSP4, RCP6.0-SSP3, RCP8.5-SSP2, RCP8.5-SSP5).

## Data Access and Citation
- Dataset DOI: https://doi.org/10.5285/f9ab3051-4f85-415f-b691-371ff8e951f2
- Licence: Open Government Licence
- Citation: Brown, C. et al. (2023). Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UK-SSPs) and climate projections (UK-RCPs). NERC Environmental Information Data Centre.

## Authors
- C Brown; B Seo; P Alexander; V Burton; E.A. Chacón-Montalván; D. Dunford-Brown; M. Merkle; P.A. Harrison; R Prestele; E.L. Robinson; M Rounsevell and colleagues from multiple UK and international institutions.

## Summary of what the data represent
- Future land-use projections produced by CRAFTY-GB, a British adaptation of the CRAFTY agent-based modelling framework, at 1 km2 resolution for 2020–2080 in decadal steps.
- Integrates:
  - Climate pathways (UK-RCPs) and socio-economic pathways (UK-SSPs)
  - A global modelling framework to account for UK trade and global change
- Focused on Great Britain (excluding Northern Ireland due to data constraints).

## Data structure and content
- For each of the six SSP-RCP scenarios, outputs are 1 km gridded land-use maps as stacked raster files.
- Each raster stack contains seven bands, representing land use at each decadal timestep from 2020 to 2080.
- Land uses are encoded as Land Use Agents with indices from -1 to 15:
  - -1 Unmanaged
  - 0 Agroforestry
  - 1 Bioenergy
  - 2 Extensive arable
  - 3 Extensive pasture
  - 4 Intensive arable (fodder)
  - 5 Intensive arable (food)
  - 6 Intensive pasture
  - 7 Multifunctional mixed woodland
  - 8 Native woodland (conservation)
  - 9 Productive native broadleaf
  - 10 Productive native conifer
  - 11 Productive non-native broadleaf
  - 12 Productive non-native conifer
  - 13 Sustainable Arable
  - 14 Very Extensive Pasture
  - 15 Urban

## Data creation and modelling approach
- Core components:
  - Capitals: per-cell resources/attributes categorized as human, social, manufactured, financial, and natural (with natural further split into yields/suitabilities for arable, pastoral, and forest uses).
  - Agents: land-management forms (aligned with land-use types) that compete to manage each cell based on the value of the services they provide.
  - Services: provisioning, regulating, and cultural ecosystem services plus indicators (e.g., biodiversity, employment) whose demand and value are exogenously defined by scenario assumptions.
  - Exogenous drivers: climate (RCP) and socio-economic (UK-SSP) changes over time that alter capital values, agent characteristics, service demand, and governance objectives.
- Data inputs and calibration:
  - Capitals derived from UK-SSP projections (eight socio-economic indicators) and natural-capital classifications (ESC) plus arable/pasture suitabilities.
  - Protected areas and urban areas constrained by designations and a separate urban-allocations model.
  - Agent typologies based on observations (LCM2015, NFI) and designed to span a spectrum of intensities and multifunctionality.
- Data processing notes:
  - Input data gaps (coasts, islands) filled via regression, nearest-neighbour, or smoothing approaches.
  - Baseline 2020 alignment normalised when needed to ensure consistency with inputs.
- Urban development:
  - Independent urban allocation model projects 1 km urban surfaces decennially (2020–2100), driven by neighbourhood density, sprawl parameters, and protected/flood risk exclusions.
- Intensity representation for monitoring:
  - A continuous land-use intensity mapping, combining inputs, technology, and production levels to aid visualization and comparability across SSPs (not embedded in the provided Land Use Agent indices; represented via intensity scalars for visualization).

## Scenario details and rationale
- Six combined UK-RCP-SSP scenarios chosen to cover a broad range of climate and socio-economic futures and to allow analysis of different RCPs within the same SSP and vice versa.
- UK-SSP-specific narrative and quantitative inputs integrated with a global-land-system context (via LandSyMM) to reflect international trade and feedbacks.
- Urban, coastal, and island data gaps addressed to support UK-wide applicability; baseline allocation anchored to LCM2015 and NFI data.

## Model evaluation and validation
- TRACE-based (transparent, comprehensive model evaluation) assessment documented in Supporting Information S2 (Brown et al. 2022).
- Evaluation methods include unit tests, sensitivity/uncertainty analyses, comparisons to empirical data and other models, and stakeholder consultations.
- Historical replication validation against  UK land-cover data is limited due to inconsistent time-series data; instead, baseline alignment and agent-typology validation were undertaken:
  - Baseline allocations compared against LCM2015, EUNIS habitat classifications, CEH Land Cover Plus Fertilisers/Pesticides data.
  - Purpose: ensure the agent typology captures the range of British land-system characteristics and supports interpretation of results.

## Practical considerations for monitoring and governance
- Data licensing and openness facilitate reuse, but publicly sharing underlying datasets can be a barrier in some contexts; data governance and metadata accompany the dataset.
- The modelling framework emphasizes data provenance, cross-validation with diverse data sources, and clear documentation of assumptions to support decision-making.
- Outputs are designed to inform policy monitoring, scenario planning, and assessment of how climate and socio-economic futures might shape land-use change and ecosystem services in Britain.

## Key takeaways for monitoring practitioners
- A robust, scenario-based, 1 km resolution dataset linking climate and socio-economic futures to land-use change, with explicit agent-based mechanisms and service-driven competition, suitable for policy scenario testing and impact assessment.
- Comprehensive metadata, licensing, and governance considerations accompany the data to support transparent use and data sharing.
- While UK-wide in scope, Northern Ireland is not included due to data limitations; data gaps in coastal and island regions were addressed with targeted imputations.
- The framework provides a scalable approach to monitor land-use trajectories and ecosystem-service outcomes under multiple plausible futures, aiding governance and adaptation planning.