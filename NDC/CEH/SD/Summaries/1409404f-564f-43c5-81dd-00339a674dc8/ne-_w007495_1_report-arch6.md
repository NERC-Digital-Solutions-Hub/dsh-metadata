environmental biodiversity '

## Overview
- A research project funded by the Natural Environment Research Council assessing cost-effective, spatially targeted agri-environmental schemes to balance agricultural production with biodiversity and ecosystem services.
- Combines data-defined methods to estimate biodiversity values, assess transaction costs, and design habitat-based contracts that encourage neighbourly collaboration to boost habitat gains.
- Aims to inform policy design for post-Brexit elms-style schemes and quantify transaction costs to improve reliability of policy forecasts.

## Data sources and datasets
- Discrete Choice Experiments (DCEs):
  - Survey of 348 farmers in northern England (Cumbria, Northumberland, Durham) to elicit willingness to participate in two environmental land management (ELM) schemes and a coordination variant.
  - Two main DCE experiments (Experiment 1 and Experiment 2) plus a combined scheme variant (Experiment 3) capturing different design attributes.
- Species Distribution Modelling (SDM):
  - Occurrence data for Western honeybee (Apis mellifera) from the UK National Biodiversity Network (NBN) for 2019.
  - Environmental predictors: temperature (monthly min/max), precipitation, land use, distance to freshwater, PM2.5, population density, HadUK-Grid climate data, Land Cover Map 2019.
- Data products and formats:
  - Two CSV files: NE_W007495_1_experiment1.csv and NE_W007495_1_experiment2.csv (each with 26 variables; panel format; 8 choice tasks per respondent; anonymised IDs).
  - Appendix includes example choice cards and data dictionary descriptions.
- Geographic and socio-economic context:
  - Farm locations; farm size, ownership, income source, AES participation, education level, community engagement, and farming practices.
  - Flood risk perceptions and neighbour-sharing behaviours.

## Data structure and format
- Panel dataset structure:
  - Each row represents a single choice task; two alternatives per task plus a status-quo option.
  - 8 tasks per respondent; 348 respondents; balanced panel (8 completed tasks per respondent).
- Key variables included:
  - Respondent-level: gender, age, farm_age, education, farm size, land ownership, primary income, main product, AES participation, social/community metrics.
  - Task-level: choice (A/B/opt-out), contract attributes for option A and B (type of habitat, land location on land, land quality, area, payment), and scheme coordination attributes (number of neighbours, corridor width, coordination bonus, etc.).
  - Data dictionary and tables describe all 26 columns and their coding.

## Methodology and analysis
- Discrete Choice Experiments (DCE):
  - Scheme 1: Habitat creation alone (annual payment, land parcel size, habitat type).
  - Scheme 2: Adds agglomeration/coordination bonus for connecting habitats with neighbours via ecological corridors.
  - Experimental design and priors:
    - D-efficient experimental design with priors informed by economic theory and UK studies.
    - 8 choice tasks per respondent; randomised task order to reduce fatigue bias.
  - Modelling:
    - Mixed or standard multinomial logit (MNL) models used to estimate willingness-to-accept (WTA) payments associated with attribute changes.
    - Coefficients interpreted as average changes in WTA (£/year) for continuous attributes and relative changes for categorical attributes.
- Scheme design and attributes (Experiment 1 and 2):
  - Attributes include: type of Habitat Feature (planted trees vs natural regeneration), location (in-field vs river edge vs field boundary), land quality (prime/high-yield vs rough/wet/steep), area, annual payment.
  - Scheme 2 adds: coordination with neighbours, corridor width (10m vs 20m), and a one-off coordination bonus.
- Data quality and preprocessing:
  - Responses with incomplete final questions removed; dataset balanced; anonymised respondent IDs.
  - In Experiment 3 (DCE 3), additional attributes include coordination with neighbours, corridor width, and coordination bonuses; results presented as MNL estimates.
- Species distribution modelling (SDM):
  - MaxEnt modelling with presence-only NBN data to predict Apis mellifera habitat suitability.
  - Evaluates contribution of predictors and model performance (AUC/sensitivity analyses) to assess potential bee response to scheme-induced habitat changes.
  - Spatial resolution: 25m rasters; 2019 data; predictors include land use, climate, and proximity to water bodies and population density.

## Key findings
- Willingness to participate (WTA) and scheme design:
  - Scheme location matters: features along field boundaries or river edges are valued lower in compensation than features in the field interior/middle; overall location substantially influences WTA.
  - Land quality has a smaller effect than location; higher-quality land slightly increases WTA.
  - Area of habitat features and land retirement carry opportunity costs; larger areas increase WTA estimates.
  - Farmers already enrolled in AES or with higher education levels show lower WTA and higher likelihood of participation.
  - Farm size correlates with higher compensation requirements, indicating greater opportunity costs on larger, more productive farms.
  - Social/community engagement alone was not a strong driver for participation in coordination schemes; past sharing of equipment with neighbours lowers coordination costs and increases willingness to participate in connectivity schemes.
- Scheme 2 (coordination and corridors) results:
  - Coordination with neighbours increases perceived costs, particularly with wider corridors; 20m corridors have higher WTA (£157) than 10m.
  - Coordinating with two neighbours generally increases WTA; coordinating with one neighbour can reduce WTA, suggesting asymmetric coordination costs.
  - Coordination bonuses reduce WTA slightly, indicating some incentive effect for collaboration.
  - Sharing equipment with neighbours lowers WTA for coordination schemes, highlighting practical benefits of established local networks.
- District and demographic patterns:
  - Younger, more educated farmers with prior exposure to government ELM schemes more likely to participate.
  - Shared boundaries between farms associated with higher WTA in some model specifications, while equipment sharing lowers WTA.
- SDM findings:
  - Land use is the strongest predictor of honeybee habitat suitability; broadleaved woodland and acid grassland are more favorable than arable land.
  - Distance to freshwater, population density, and certain climate variables also significantly influence bee presence.
  - MaxEnt model performance indicates meaningful predictive capability; arable areas are least suitable for honeybees, suggesting conversion of some arable land could yield habitat gains.
- Policy-relevant implications:
  - Estimated annual payments of roughly £200–£500 per 500–1000 m² feature, plus coordination bonuses, could incentivize farmer participation and habitat connectivity.
  - Narrow corridors are preferable for cost-effective connectivity enhancements.
  - Targeted, spatially explicit schemes informed by SDM outputs can optimize biodiversity benefits and reduce overall public spending.
  - Potential policy tool: combine DCE-derived cost data with SDM-derived ecological benefits to generate spatially explicit cost-benefit maps for policymakers.

## Data quality, limitations, and considerations
- Sampling and data limitations:
  - Pandemic-related delays affected farmer contact and participation; some regions or farm types may be underrepresented.
  - Geographic bias potential in NBN-based SDM data; citizen-science presence data can introduce sampling bias, though Koerger and colleagues note limited impact on predictions for this context.
  - Taste heterogeneity and unobserved factors may not be fully captured; future work aims to refine models and address heterogeneity.
- Data completeness and reproducibility:
  - Clear data dictionary and appendix with example choice cards enhance interpretability and reuse.
  - Data linked to a grant number and institutional affiliations; future dissemination could include spatial targeting maps and cost-benefit tools for policymakers.

## Data products and usage
- Primary data products:
  - Experiment 1 and Experiment 2 CSV files (NE_W007495_1_experiment1.csv, NE_W007495_1_experiment2.csv) containing anonymised respondent-level and task-level data, with 8 choice tasks per respondent.
  - Data dictionary and Appendix with example choice cards and variable explanations.
- Potential data products for end users:
  - Cost-benefit modeling inputs combining DCE-derived WTA with SDM-derived habitat benefits to produce spatially explicit policy scenarios.
  - Spatial targeting maps showing where habitat retirement and corridor connections yield the greatest biodiversity and economic returns.
  - Summary dashboards or pivot tables for local authorities to explore scheme uptake determinants (e.g., impact of location, land quality, AES participation, education) and plan targeted outreach.
- Reuse and dissemination:
  - Methodological templates for similar DCE and SDM studies; priors and design considerations for efficient choice experiments.
  - Framework for evaluating transaction costs of collaborative agri-environmental schemes and their implications for policy design.

## Conclusion and policy implications
- The research suggests that targeted, modest annual payments (£200–£500 per 500–1000 m²) combined with coordination bonuses can incentivize farmers to create habitat features and connect habitats across farms.
- Corridor design should favor narrower widths to minimize costs while maintaining ecological connectivity.
- Engagement tends to be higher among younger, educated farmers with prior exposure to ELMs; practical coordination (e.g., sharing equipment) reduces participation costs.
- SDMs indicate strong ecological benefits from habitat conversion away from arable land toward woodland or grassland, with potential national-scale savings in pollination-related yield losses.
- The integrated data approach provides policymakers with a data-driven toolkit to evaluate spatially targeted agri-environmental schemes and to forecast both costs and biodiversity benefits across landscapes.