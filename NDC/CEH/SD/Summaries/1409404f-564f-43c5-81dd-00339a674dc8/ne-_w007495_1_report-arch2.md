# environmental biodiversity '

## Overview

- Aims: develop data-driven, spatially targeted agri-environment schemes (AES) that balance productive farming with biodiversity and ecosystem services; design contracts that reward farmer collaboration to maximize habitat gains; estimate costs and benefits to inform policy reform post-Brexit.
- Core approach: synthesize biodiversity values, conduct two discrete choice experiments (DCEs) with farmers, and use species distribution modelling (SDM) to quantify ecological benefits; produce cost-benefit insights for targeted land-management schemes.
- Stakeholders: findings of interest to policymakers and academics (DEFRA, Natural England, SEPA) focusing on transaction costs and policy design. Emphasizes making underlying data accessible and reusable.

## Data and datasets

- Data sources and scope:
  - DCEs: two experiments with a total sample of 309 farmers in northern England; eight choice tasks per respondent; aimed at valuing participation in habitat-building schemes.
  - Survey population: 348 farmers completed the survey and both DCEs; geographic focus dominated by Cumbria, North Yorkshire, Lancashire, and surrounding English counties.
  - Species data: presence data for the Western honeybee (Apis mellifera) from the UK National Biodiversity Network (NBN) used for SDM.
- Data structure and availability:
  - Two CSV files (experiment1 and experiment2) containing 26 columns each with anonymized respondent IDs, choice data, attribute levels, and socio-economic controls; panel format with eight tasks per respondent; balanced panel completed.
- Outputs of interest for monitoring:
  - Willingness-to-accept (WTA) estimates by scheme attribute (location, land quality, area, type, coordination) and respondent characteristics (AES participation, education, age, farm size, income source, social indicators).

## Methods

- Discrete choice experiments (DCEs)
  - Scheme design:
    - Scheme 1: annual payment to create habitat on retired land (trees vs natural regeneration); attributes include location on land, land quality, area, and payment.
    - Scheme 2: adds a coordination bonus to connect habitats across farms via ecological corridors; includes number of neighboring farms to coordinate with, corridor width, and a coordination bonus.
  - Design and analysis:
    - D-efficient design using priors; conditional logit model (McFadden) used to estimate attribute coefficients.
    - Eight choice tasks per respondent; randomised task order to reduce fatigue; target around 300 respondents for statistical power.
  - Data coding: detailed attribute level specification for both schemes; includes priors and description of variables.
- Species distribution modelling (SDM)
  - MaxEnt modelling with presence-only data to predict Apis mellifera distribution.
  - Predictor variables: monthly temperatures, precipitation, land use, distance to freshwater, PM2.5, population density; climate data from HadUK-Grid; land use from Land Cover Map 2019.
  - Evaluation: AUC (TPR vs FPR) to assess predictive accuracy; analysis of variable contributions to model performance.
- Integration plan
  - Plan to combine DCE results (costs and participation likelihood) with SDM outputs (ecological benefits) in a future cost-benefit analysis of the spatially targeted AES.

## Key hypotheses and scheme descriptions

- Scheme 1: habitat features created on retired land (trees vs natural regeneration) with annual payment; no coordination.
- Scheme 2: adds coordination (with neighbours) to connect habitats via ecological corridors; premium for coordination grows with number of participants.
- Hypotheses around adoption
  - Higher opportunity costs (e.g., high-yield land) increase WTA to participate.
  - Stronger social ties or prior collaboration with neighbours lower coordination costs and increase willingness to participate in Scheme 2.
  - Participation in existing AES lowers perceived barriers to adopt the new schemes.
- Data design specifics
  - Attributes and priors structured to reflect expected costs and benefits; design aims to capture trade-offs between payment, land parcel size, feature type, location, and coordination costs.

## Results

- Survey and sample characteristics
  - 348 farmers completed the survey; about two-thirds male; average age ~53; average farm size ~231.7 hectares (larger than regional averages); 72% report farming as primary income; 54% AES-enrolled; education levels span GCSE to postgraduate; flood concern moderately distributed.
- Discrete Choice Experiments (DCEs)
  - Scheme 1 findings (no coordination)
    - Location of features is more influential than land quality.
    - WTA adjustments (annual compensation) by location:
      - Features along field boundaries: £232 less per year than central field locations.
      - Features along river edges: £271 less per year than central field locations.
      - High-quality land yields a small additional WTA (£36 per year) relative to poor land.
    - Land area effect: marginal WTA of about £1.80 per square metre.
    - AES participation reduces WTA by ~£247/year; higher education reduces WTA substantially (various levels up to ~£36k depending on degree).
    - Farm size has a negative relationship with uptake; primary income status shows a positive but marginal effect.
  - Scheme 2 findings (coordination)
    - Coordination with neighbours increases costs; some results show stronger effects for wider corridors (20 m vs 10 m) and planted trees vs natural regeneration.
    - Coordination with two neighbours shows a positive WTA shift (costs higher) but not always statistically significant relative to no coordination.
    - Corridor width (20 m) raises WTA by about £157/year compared with 10 m.
    - Coordination bonuses reduce WTA by a small amount per coordinated farmer (roughly -£0.23 per year in the model).
    - AES participation continues to reduce WTA (≈£226/year); education and age affect participation similarly to Scheme 1; sharing equipment with neighbours lowers WTA further, indicating lower coordination costs when prior collaboration exists.
- Species distribution modelling (SDM)
  - MaxEnt model performance: high predictive accuracy with AUC substantially above 0.5; land use type is the strongest predictor of honeybee presence; distance to freshwater and population density also important.
  - Key habitat insights:
    - Broadleaved woodland and acid grassland are more suitable for honeybees than arable land.
    - Urban areas also suitable but less so after controlling for population density.
    - Arable land is least suitable; model indicates potential gains from converting arable to woodland or grassland in terms of pollinator presence.
- Integrated conclusions
  - Economic potential: annual payments of £200–£500 for 500–1000 m2 patches could effectively incentivize northern England farmers to create habitat; a coordination bonus can improve landscape connectivity.
  - Targeting and demographics: younger, better-educated farmers with prior exposure to AES are more likely to participate; sharing equipment with neighbours correlates with greater willingness to coordinate.
  - Cost considerations: regenerating vegetation along field edges may minimize government transfers; larger efficiency gains are linked to targeted, connectivity-focused schemes.
  - Benefits: protecting pollinators could avert £189–£378 million in yield losses for pollinated crops in the UK.
  - Policy relevance: results support designing spatially targeted Environmental Land Management (ELM) schemes that reward cooperation and habitat connectivity, with data-driven targeting maps and cost-benefit analysis to inform funding allocations.

## Conclusions and implications for monitoring and policy

- Practical takeaways for data-driven AES design
  - Spatial targeting: emphasize field-edge or boundary placements and corridor-based connectivity to maximize ecological benefits per unit cost.
  - Payment design: annual payments in the £200–£500 range are potentially effective for modest habitat patches; include coordination bonuses to incentivize neighbour collaboration.
  - Target groups: prioritize younger, educated farmers with prior AES exposure; leverage existing social networks and equipment-sharing practices to reduce coordination costs.
  - Data-enabled monitoring: robust datasets (DCE results, AES participation, SDM outputs, geospatial habitat maps) should be stored in accessible portals to enable scrutiny and reuse by policymakers and researchers.
- Next steps and ongoing work
  - Extend analyses to a cost-benefit framework combining DCE-derived costs with SDM-derived ecological gains.
  - Improve models to address sampling biases and taste heterogeneity; simulate grid-level land-use changes to identify areas with the strongest positive habitat responses.
  - Translate findings into spatial policy tools and maps to support the implementation and evaluation of targeted AES in England.