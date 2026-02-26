# environmental biodiversity

- Overview
  - Academic research on designing cost-effective, spatially targeted agri-environmental schemes to balance productive agriculture with landscape biodiversity and ecosystem services.
  - Uses data-driven tools (discrete choice experiments and species distribution modelling) to estimate habitat value, evaluate farmer participation, and inform policy under post-Brexit reforms.

- Data landscape and sources
  - Discrete Choice Experiments (DCEs)
    - Two DCEs with 309–348 northern England farmers; eight choice tasks per respondent; compares habitat schemes with/without coordination.
    - Collected demographic, economic, and social attributes; includes residency/land location, AES participation, education, farm characteristics, and social ties (e.g., sharing equipment).
    - Data stored in two CSV files (experiment1 and experiment2) with 26 columns each; anonymised respondent IDs; panel format (8 tasks per respondent).
  - Species Distribution Modelling (SDM)
    - MaxEnt model for Apis mellifera (Western honeybee) using UK National Biodiversity Network (NBN) presence data (2019, presence-only).
    - Predictor variables: climate (monthly temps, precipitation), land use, distance to freshwater, PM2.5, population density, HadUK-Grid climate data, Land Cover Map 2019.
    - Raster data at 25m resolution; model evaluation via cross-validation and AUC.
  - Ancillary data and context
    - Geographic distribution of survey respondents; land-use maps; policy-linked datasets on pollination values and estimated economic benefits.

- Data architecture and metadata
  - DCE data structure
    - experiment1.csv and experiment2.csv share a common 26-column structure (ID, Choice, Choice.situation, demographic controls, land attributes, and scheme attributes).
    - Panel data: 348 respondents × 8 choice tasks per respondent; each task compares two options plus a no-participation opt-out.
  - Data dictionary and appendix
    - Tables listing attribute names, levels, priors, and variable descriptions for scheme attributes (habitat type, location, quality, area, payments) and coordination attributes (number of neighbours, corridor width, coordination bonus, payments).
    - Appendix includes example choice cards illustrating Scheme 1 (no coordination) and Scheme 2 (coordination).

- Methods and data processing
  - Experimental design and sample
    - DCEs designed to estimate willingness-to-accept (WTA) for participating in habitat schemes and coordinating with neighbours.
    - Priors guided by economic theory and UK policy context; D-efficient design to maximise information; randomised task order to reduce fatigue bias.
    - Recruitment from Cumbria, Northumberland, and County Durham; invitations sent to ~2,401 addresses; 36 in-person surveys to improve representation; most surveys completed online via Qualtrics.
  - Scheme 1: Habitat creation only
    - Attributes: type of habitat (planted trees vs natural regeneration), land location (in-field, river edge, field boundary), land quality (prime vs rough), area, annual payment.
  - Scheme 2: Habitat connectivity
    - Adds coordination component: number of neighbours to coordinate with, corridor width (10m vs 20m), one-off coordination bonus; annual payment per 100m of corridor.
  - Data processing and outcomes
    - Economic valuation: WTA estimates for each attribute; MNL (conditional logit) modelling to derive average changes in WTA by attribute.
    - Socioeconomic controls: AES participation, age, education, farm size, primary income status, social engagement indicators, and equipping-sharing behaviours.
  - Species distribution modelling (SDM)
    - MaxEnt modelling approach using presence-only data; evaluation via AUC; analysis of variable importance (land use, distance to freshwater, population density, climate variables).
    - Spatial interpretation to identify land-use configurations most suitable for honeybees and to project habitat gains from proposed schemes.

- Key findings
  - DCE results (WTA and preferences)
    - Scheme 1: Location of habitat features is more influential than land quality. Field-boundary and river-edge placements reduce required compensation compared to mid-field placements; higher land quality only marginally changes WTA.
    - Land area and habitat type matter; larger land blocks command higher compensation; higher education correlates with lower WTA (increased propensity to participate).
    - AES participation lowers WTA; older or larger farms generally increase compensation demands; farm size and primary income status show nuanced effects.
  - Scheme 2: Connectivity with neighbours
    - Coordination with neighbours increases costs; one-neighbour coordination shows modest WTA decrease, but two-neighbour coordination increases costs.
    - Wider corridors (20m) raise WTA relative to 10m; a coordination bonus lowers WTA slightly; sharing equipment with neighbours lowers participation costs, indicating lower coordination barriers when prior collaboration exists.
    - Younger, more educated farmers with prior exposure to government schemes are more likely to participate; general community involvement is less predictive of coordination willingness than prior neighbour collaboration.
  - SDM results
    - Land use is the strongest predictor of honeybee presence; broadleaved woodlands and acid grassland more suitable than arable land.
    - Proximity to water bodies, population density, and certain climate conditions (winter temperatures) significantly affect presence probabilities.
    - Policy-relevant implication: converting arable land to woodland or grassland could enhance pollinator habitat; urban areas remain suitable with caveats related to density.
  - Economic value and policy relevance
    - UK pollinator contributions to crop value estimated between £188.7M and £379M per year; stabilising pollination could avert yield losses and generate substantial welfare gains.
    - Anticipated policy implication: spatially targeted Environmental Land Management (ELM)-like schemes with modest annual payments (£200–£500) and coordination bonuses can effectively improve habitat connectivity and pollination services; narrower corridors are preferred for cost efficiency.

- Data quality, limitations, and challenges
  - Sampling and representativeness
    - Response bias toward male respondents; geographic coverage limited to the north of England; some postcodes could not be matched to valid locations.
  - Data limitations
    - DCE relies on stated preferences; WTA estimates depend on model specification and priors; potential taste heterogeneity not fully explored.
  - SDM limitations
    - Use of presence-only data (NBN) may introduce sampling bias; 2019 data may not capture recent shifts; spatial bias corrections (jackknife, background sampling) are necessary for robust inference.
  - Metadata and governance
    - Data dictionary and design documentation are provided; sensitivity to privacy preserved via anonymised respondent IDs; future data sharing and discoverability depend on metadata standards and platform integration.

- Implications for Data Leaders
  - Data integration and governance
    - Demonstrates integrating survey data (farmer preferences) with ecological data (pollinator distribution) to inform spatially targeted policy design.
    - Emphasises the importance of thorough metadata, data dictionaries, and clear data structures to enable reproducibility and cross-disciplinary use.
  - Data quality and standards
    - Highlights the need for addressing sampling bias in citizen-science-derived SDM data and ensuring robust cross-validation.
    - Suggests maintaining granular data (e.g., 25m raster land-use data) while acknowledging scale considerations for policy modelling.
  - Data products and dissemination
    - Generates actionable outputs: WTA estimates by attribute, optimization of corridor width and coordination, and spatial maps to guide targeted investments.
    - Proposes a framework to link economic valuation with ecological modelling, enabling policymakers to evaluate trade-offs and prioritize investments.

- Conclusion and next steps
  - Policy-ready insights indicate that targeted annual payments (£200–£500) for habitat creation, coupled with coordination-based incentives for habitat connectivity, can be effective.
  - Findings support prioritising natural regeneration along field edges for cost efficiency and leveraging farmer networks to enhance collaboration.
  - Future work aims to refine models, reduce biases, and extend spatial targeting maps to quantify marginal habitat gains from land-use changes, enabling more precise policy evaluation.