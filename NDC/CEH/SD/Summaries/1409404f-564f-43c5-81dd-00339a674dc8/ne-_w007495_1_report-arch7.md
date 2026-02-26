# environmental biodiversity '

## Overview
- This project investigates designing cost-effective, spatially targeted agri-environmental schemes to balance productive farming with biodiversity and ecosystem services, focusing on pollination as a key service in the UK.
- It combines data-driven valuation (discrete choice experiments) with ecological modelling (species distribution modelling) to inform targeted policy and spatial targeting maps for potential schemes.
- Outputs aim to aid policymakers, academics, and practitioners in evaluating where and how to implement habitat features and ecological corridors on farms.

## Context and Aims for GIS work
- Goal: design schemes that reward farmers for creating habitat features and coordinating with neighbours to enhance habitat connectivity and pollination.
- Two schemes explored:
  - Scheme 1: annual payments to create habitat features on retired land (trees or natural regeneration) with no coordination.
  - Scheme 2: adds an agglomeration/coordination bonus for connecting habitats via ecological corridors between farms.
- Outputs include cost estimates, participation likelihoods, and spatial targeting maps combining land-use, habitat suitability, and connectivity considerations.

## Data, datasets, and GIS inputs
- Pollination value data and references drawn from UK literature; costs and benefits used to inform scenario economics.
- Species distribution modelling (SDM) data:
  - Occurrence data for Western honeybee (Apis mellifera) from UK National Biodiversity Network (NBN), 2019.
  - Predictor rasters at 25 m resolution: monthly temperatures, precipitation, land use, distance to water, population density, PM2.5, HadUK-Grid climate variables, Land Cover Map (2019).
- Land-use context and habitat maps to support spatial targeting and scenario testing.

## Methodology (GIS-relevant components)
- Discrete Choice Experiments (DCE)
  - Two separate experiments (Experiment 1 and Experiment 2) with 309–348 farmers in northern England.
  - Attributes include: type of habitat (planted trees vs natural regeneration), land location (in-field, river edge, field boundary), land quality (prime/high-yield vs rough/wet/steep), area to retire (500 vs 1,000 m2), annual payment (£200–£500).
  - Scheme 2 adds: coordination with neighbours (0, 1, or 2 neighbours), corridor width (10 m vs 20 m), and a one-off coordination bonus (£200–£500).
  - Data outputs: two CSV files (NE_W007495_1_experiment1 and NE_W007495_1_experiment2) with 26 columns per file, panel format (eight choice tasks per respondent), data dictionary and variable descriptions.
  - GIS relevance: translates survey preferences into spatially explicit costs and uptake likelihoods by land parcels, informing where incentives would be most efficient.
- Species Distribution Modelling (SDM)
  - MaxEnt modelling using presence-only NBN data for Apis mellifera (2019, 250 m-resolution context shown in figures).
  - Predictors: temperature (monthly min/max), precipitation, land use, distance to freshwater, PM2.5, population density.
  - Outputs: habitat suitability maps and variable importance (land use, distance to water, population density, winter temperatures).
  - GIS relevance: identifies areas where habitat features and corridors would most enhance bee presence and pollination services.
  
## Data structure and formats
- Discrete choice data
  - Experiment files: NE_W007495_1_experiment1.csv and NE_W007495_1_experiment2.csv
  - 26 columns per file, e.g., ID, Choice, Choice.situation, female, age, farm_age, edu_attain, hectare, owned, primary, product, aes, social, concern, boundary, sharing, plus scheme-specific attributes.
  - Panel format: eight choice tasks per respondent, with two alternatives plus a status-quo option; anonymised respondent IDs; 348 respondents completed all tasks.
- Summary results
  - DCE results presented as average changes in willingness-to-accept (WTA) per attribute, with standard errors and significance.
  - Scheme 2 results include interactions for coordination and corridor characteristics.

## Key findings (GIS interpretation)
- Scheme design insights
  - Scheme 1: location of features (field boundaries, river edges) generally more influential on uptake than land quality; WTA per area suggests higher compensation for central-field placements than periphery placements.
  - Scheme 2: coordination and corridor width significantly impact WTA; coordination with neighbours increases complexity and cost, with 20 m corridors posing higher WTA than 10 m ones. However, coordination bonuses can offset some costs.
- Socioeconomic factors
  - AES participation and higher education correlate with lower WTA and higher uptake likelihood.
  - Smaller farms and those with diversified income streams may have different participation costs; sharing equipment with neighbours reduces perceived coordination costs.
- Habitat and pollination payoff
  - Literature review estimates UK pollinator value benefits in the range of approximately £189–£378 million per year in avoided yield losses, with pollinator presence strongly tied to land-use type.
  - MaxEnt results show broadleaved woodland and grassland support higher pollinator suitability than arable land; arable land is the least suitable category for honeybees among the land-use classes examined.
- Spatial implications
  - Spatial targeting maps can be created to prioritize: (a) areas with suitable land-use types but insufficient pollinator habitat, (b) regions where corridor connectivity would yield substantial gains, and (c) parcels where retiring land is most cost-effective given opportunity costs.
  - Potential to simulate land-use changes (e.g., woodland/grassland) at 25 m pixels to visualize marginal habitat gains and inform policy decisions.

## Conclusions and GIS-specific implications
- Economic and ecological evidence suggests that targeted agri-environmental schemes with modest annual payments (£200–£500) and narrow corridors can incentivize habitat creation and connectivity, particularly when coordinated among neighbours.
- Younger, educated farmers with prior experience of government schemes are more likely to participate; equipment sharing and existing neighbour collaboration reduce coordination costs.
- Policy maps linking land parcel characteristics (location relative to boundaries or rivers, land quality), farmer characteristics, and corridor design can guide efficient allocation of funds.
- The study supports the development of spatially explicit decision-support tools for policymakers to evaluate where to implement habitat features and corridors, and how to structure coordination bonuses to maximize biodiversity and flood management benefits.

## GIS-oriented outputs and next steps
- Spatial targeting maps showing:
  - Optimal locations for habitat features (Scheme 1) by land location and quality, prioritising field-edge and river-edge placements.
  - Corridor networks (Scheme 2) with corridor width options (10 m vs 20 m) and coordination participant patterns; identify clusters of potential coordination benefits.
  - Areas where converting arable land to woodland/grassland yields the greatest pollination benefit, based on SDM.
- Data products and formats
  - Exportable maps and shapefiles indicating recommended parcels, feature sizes (500–1,000 m2), and suggested coordination links.
  - Cost surfaces and uptake probability rasters derived from DCE results to overlay with ecological suitability.
- Future work
  - Refine SDM with improved sampling, address taste heterogeneity, and extend to additional regions or land-use scenarios.
  - Integrate DCE priors more deeply with spatial design to produce policy-ready, GIS-based planning tools.