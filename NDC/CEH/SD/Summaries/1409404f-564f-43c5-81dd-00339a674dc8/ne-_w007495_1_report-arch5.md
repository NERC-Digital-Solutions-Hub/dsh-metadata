# environmental biodiversity

## Overview

- Purpose: Research on factoring biodiversity values into cost-effective, spatially targeted agri-environmental schemes to balance biodiversity with productive agriculture in the UK post-Brexit.
- Data outputs: Raw dataset from two discrete choice experiments (DCEs) and associated species distribution modelling (SDM) data to support cost-benefit analysis and spatial targeting maps.
- Relevance for data stewardship: Provides structured, publicly describable survey data and ecological modelling data with detailed metadata, suitable for replication and policy analysis.

## Datasets and structure

- Datasets provided
  - Two CSV files: NE-_W007495-_1_experiment1 and NE-_W007495-_1_experiment2
  - 348 respondents across the two experiments; each respondent completed 8 choice tasks per experiment
  - Data organized in a panel format; 26 columns per file; anonymised respondent IDs; each row is a choice task with two alternatives and a status-quo option
- Experimental design and content
  - Experiment 1 (Scheme 1): Habitat creation on retired land (two options differing by type, location, land quality, area, and annual payment)
  - Experiment 2 (Scheme 2): Habitat connectivity (adds coordination with neighbours, corridor width, and a coordination bonus)
  - Attributes and priors specified to enable efficient design; priors documented in Tables 3.1–3.3 and accompanying data dictionary
- Data dictionaries and appendices
  - Tables 3.1–3.3 provide common data fields and scheme-specific attributes
  - Appendix includes example choice cards used in the surveys

## Data structure and fields

- Core fields (example)
  - ID: anonymised respondent
  - Choice: A/B/opt-out
  - Choice.situation: 1–8 (task index within each experiment)
  - Demographics and controls: female, age, farm_age, edu_attain, hectare, owned, primary, product, aes, social, concern, boundary, sharing
  - Scheme 1 attributes (Experiment 1): contract type, location, quality, area, payment (A vs B)
  - Scheme 2 attributes (Experiment 2): contract type, coordination with neighbors, corridor width, coordination bonus, payment
- Data structure
  - Panel format: each respondent has 8 choice tasks per experiment
  - Two alternatives per task plus a status-quo option
  - Variables include socio-economic controls and scheme-specific attribute levels

## Data sources and provenance

- Discrete Choice Experiments
  - Collected via Qualtrics; recruitment in northern England (Cumbria, Northumberland, County Durham)
  - Invitations mailed to 2,401 addresses; supplementary in-person surveys (36)
- Ecological modelling (SDM)
  - Apis mellifera (Western honeybee) presence data from UK National Biodiversity Network (NBN), 2019
  - Environmental predictors: temperature (monthly min/max), precipitation, land use, distance to freshwater, PM2.5, population density
  - Land-use and climate data sources: Land Cover Map 2019, HadUK-Grid (Met Office)

## Methods and processing

- Discrete Choice Experiments (DCEs)
  - Theoretical basis: utility maximisation (Lancaster; conditional logit estimation)
  - Design: D-efficient choice tasks; priors inform attribute coefficients
  - Estimation: marginal willingness-to-accept (WTA) and related coefficients via conditional logit
  - Purpose: quantify farmers’ participation costs and coordination costs for habitat features and ecological corridors
- Scheme descriptions
  - Scheme 1: annual payment for habitat features on retired land (two option profiles)
  - Scheme 2: adds a coordination bonus for connecting habitats with neighbours; corridor width and number of neighbours influence costs
- SDM (MaxEnt)
  - Presence-only modelling for Apis mellifera using 2019 NBN data
  - Predictor variables include land use, temperature, distance to freshwater, population density, and air pollution
  - Model evaluation: AUC; variable contribution analysis
  - Outputs used to assess ecological benefits of proposed schemes and to map suitable habitat gains under scenarios

## Key findings

- DCE results (Scheme 1)
  - Location of features matters more than land quality; field-edge or river-edge locations reduce required compensation versus mid-field
  - Higher land quality has smaller effect on WTA
  - Average marginal WTA for land area is about £1.80 per square metre
  - Participants with prior AES participation tend to require lower compensation; higher education lowers WTA; larger farms may require higher compensation due to opportunity costs
- DCE results (Scheme 2)
  - Coordinating with neighbours increases costs; two neighbours incur higher WTA, though some effects are not always statistically strong
  - Narrower corridors (e.g., 20 m vs 10 m) increase WTA; higher coordination costs associated with wider corridors
  - Coordination bonuses can offset some coordination costs
  - Sharing equipment with neighbours and existing local social ties reduce coordination barriers
- SDM results
  - Land use is the strongest predictor of honeybee presence; arable land is least suitable, while broadleaved woodland and acid grassland are more suitable
  - Other important predictors: proximity to freshwater, population density, temperature patterns (winter cold), and air pollution
- Economic and policy implications
  - Pollinator services in the UK have estimated value ranges of £188.7M–£379M per year; protecting pollinators could avert yield losses in key crops
  - Preliminary policy guidance: annual payments of £200–£500 for 500–1000 m2 habitat features; coordination bonuses can improve habitat connectivity; corridors should be narrow to reduce costs
  - Demographics influence uptake: younger, more educated farmers with prior exposure to ELM schemes more likely to participate; sharing equipment with neighbours lowers participation costs
- Future work
  - plan to integrate DCE results with SDM outputs for cost-benefit analysis and generate spatially explicit policy maps
  - aim to extend models to quantify marginal habitat gains from woodland/grassland expansion on a 25 m grid

## Data governance, quality, and reuse considerations

- Provenance and documentation
  - Clear data dictionaries and design documentation accompany the datasets
  - Experimental design details (attributes, priors, and task construction) are documented to support replication
- Privacy and ethics
- Data quality and limitations
  - Pandemic delays and recruitment challenges noted; potential sampling biases acknowledged
  - SDM data based on presence-only citizen-science records; geographic matching issues in postcodes; geographic sampling bias discussed and addressed in interpretation
- Reproducibility and reuse
  - Data are organized for reuse in replication studies of DCEs and policy evaluation
  - Supports integration of social/economic survey data with ecological modelling outputs for policy analysis

## Recommendations for Data Stewards

- Metadata and provenance
  - Maintain comprehensive metadata, including data collection timeline, sampling frame, consent, and any data cleaning steps
  - Preserve versioning of datasets and accompany with data dictionaries and codebooks
- Data quality control
  - Document response rates, missing data handling, and potential biases; provide diagnostics where possible
- Privacy and governance
  - Ensure respondent anonymity is preserved; aggregate sensitive location data as needed
  - Clarify data access rights and licensing to enable controlled sharing with researchers
- Data formats and accessibility
  - Preserve consistent CSV formats and clear file naming (e.g., NE-_W007495-_1_experiment1/2)
  - Provide accompanying code or workflows for DCE analysis (e.g., conditional logit estimation) and SDM (MaxEnt) to support reproducibility
- Reuse and policy impact
  - Deliver spatially explicit outputs (e.g., maps of habitat suitability and cost-effectiveness) to aid policymakers
  - Integrate datasets with clear crosswalks between survey responses and ecological outcomes for holistic policy analysis