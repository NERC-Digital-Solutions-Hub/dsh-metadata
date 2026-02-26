# Management options for biodiverse farming, 2006-2009 Ecology Data USER GUIDE

## Overview
- Multidisciplinary project integrating sociology, agricultural science, economics, and ecology across 48 arable farms in Bedfordshire, Lincolnshire, and Norfolk (UK).
- Aims to model farm land-use decisions and biodiversity responses (weeds, birds) within a socio-economic framework.
- Produces large-scale, multi-layer datasets to support integrated modelling and policy analysis.

## Data governance, structure, and stewardship

- Datasets
  - Dataset 1: Background information on farmer circumstances and decision-making.
  - Dataset 2: Comprehensive farm activity descriptions used to parameterise land-use models.
  - Dataset 3: Detailed crop management data for weed surveys (fields surveyed; anonymized; not suitable for archiving due to identifying information in some components).
- Weed data (Dataset 3)
  - Density-state data for 20x20 m quadrats across fields, three censuses per year over three years, seven weed species.
  - Approximately 2 million data points.
  - Anonymized field/farm identifiers; spatial mapping to support field-scale analyses.
- Anonymization and archiving
  - Datasets 1 and 3 prepared for archiving; Dataset 2 contains identifying information and is not suitable for open archiving under anonymity constraints.
- Variable coding and metadata
  - Table 1 provides detailed variable descriptions and codings (e.g., year, census timing, county, farm, field, crop, quad, x/y coordinates, species density quartiles with coded labels such as L, M, H, V, 0, NA).
  - Clear descriptions support interoperability and re-use by data stewards and researchers.
- Temporal and spatial scope
  - Three-year data collection, multiple spatial scales: quadrats (20x20 m) within fields; fields within farms; landscape-scale bird data (1 km squares).
- Data quality and processing
  - Density-state models and state-to-mean conversions developed to address misclassification biases.
  - Linear mixed models used to relate field-level mean weed densities to prior densities, herbicide applications, and farmer preferences.
- Data usage and provenance
  - Data underpin integrated models linking weed dynamics, bird populations, farm management, and socio-economic factors.
  - Outputs inform policy simulations (e.g., set-aside, environmental stewardship) and farm-level decision support.
- Access and engagement
  - Data prepared to support internal and external analyses; archiving plan in place for accessible datasets, with sensitive components restricted.
  - Outputs include model parameters, stakeholder analyses, and policy-relevant scenarios.

## Aims, framework, and scope (data-related context)

- Objectives
  - Integrate sociology, agricultural science, economics, and ecology to explain and predict impacts of economic, environmental, technological, regulatory, and social changes on farming practice and biodiversity.
  - Focus on crop weeds, farmland birds, and four mammal species, enabling extension to other groups.
- Conceptual framework
  - Farmer decisions modeled as rational economic behaviour with risk appetite and non-profit objectives (e.g., habitat/conservation goals) influencing management.
  - Feedback loops where biodiversity outcomes influence farming decisions and landscape structure (hedges, woods) in turn affect ecology and profitability.
- Study design implications for data governance
  - Need to capture both production-driven and non-production incentives, with robust linkage between socio-economic data and ecological measurements.
  - Emphasis on cross-scale data integration (field, farm, landscape) to support predictive modelling and policy evaluation.

## Field methods and data capture (data-centric view)

- Field sampling design
  - 48 farms across three counties; 500 fields mapped; each field subdivided into 20x20 m quadrats (quadrats: 200 per farm across 10 fields per farm).
  - Three weed censuses per year (spring seedlings, summer mature weeds in crops, autumn mature weeds in sugar beet/new winter crops).
- Weeds and habitat data
  - Seven weed species tracked; densities recorded in density states (0, L, M, H, V; with NA as missing).
  - Detailed habitat features recorded (field boundaries, hedges, ditches, trees) to enable integration with bird models.
- Bird data and landscape data
  - Bird abundance modeled using Breeding Bird Survey data across 880 1 km squares (2007), with enhanced landscape and boundary data; landscape categories from CEH Land Cover Map 2000.
- Data lineage
  - Data linked across weed, bird, farm management, and social data to support integrated analyses.

## Analytical methods and data interpretation (data-focused)

- Weeds
  - Density-state data transformed to field-mean densities; linear mixed models relate densities to previous densities, herbicide usage, and farmer preferences.
  - Within-field population dynamics explored via density-structured models (20x20 m quadrats).
  - Key drivers vary by species; crop type strongly influences recruitment and abundance; herbicide effects are negative but highly variable.
- Birds
  - Habitat-abundance models using landscape composition, boundary structure, and cropping; Poisson GLMs with information-theoretic model selection.
  - Habitat heterogeneity analyzed at multiple scales (1, 9, 25 km^2) to assess scale-dependent drivers.
  - Field-scale habitat-use models (Whittingham et al.) adapted to farm maps to predict breeding densities under management changes.
- Integration and modelling
  - SFARMMOD: a profit-maximising linear programming model extended to incorporate conservation decisions and non-production activities via multi-objective optimization and MAUT (multi-attribute utility theory).
  - Social data (farmer preferences) integrated to inform land-use decisions; results show improved predictive power over profit-only models.
  - Stakeholder and decision analyses used to parameterize socio-economic components and assess policy scenarios.
- Interdisciplinarity and validation
  - Regular project meetings and cross-team collaboration to align ecological, social, and economic data and models.
  - Taxonomy of socio-economic methodologies and evaluation of integration approaches to bridge ecological and social sciences.

## Farmer decisions, preferences, and behavior (data-informed)

- Decision context and objectives
  - Seven land-use objectives with 14 criteria measured via decision-support tools and SWING weighting, enabling elicitation of farmer utility curves.
  - Data capture includes willingness to trade off profit against other objectives; revealed substantial variability across farmers.
- Key findings from integration
  - High income priority correlates with intensive chemical inputs; biodiversity preferences did not reliably translate into reduced herbicide use, indicating misalignment between stated preferences and management actions.
  - Variation exists in preferences for crop diversity, with non-monotonic satisfaction curves for some farmers, suggesting context-dependent optimality.
  - Time not farming and management complexity also influence decision-making, with risk attitudes and farmer backgrounds shaping land-use choices.

## Stakeholders and policy relevance (data angle)

- Stakeholder analysis
  - Interactive stakeholder mapping to classify interest and influence in habitat, information, production, regulation, and other functions of farmland biodiversity.
  - Evidence of potential conflicts between habitat/information-focused stakeholders and production-focused stakeholders.
- Implications for data sharing and governance
  - Stakeholder data underpin policy-relevant scenarios; sensitive stakeholder positions may inform governance strategies and data-access decisions.

## Integrated modelling framework and outputs (data-centric)

- Integrated framework
  - Combines farmer utility-based land-use planning with weed and bird population models; enables scenario analysis (e.g., set-aside changes, biofuel price shifts).
  - Outputs can be linked to policy questions such as the impact of Environmental Stewardship (ES) options and subsidies on biodiversity and farm profitability.
- Policy scenario insights
  - Overwintered stubble (e.g., 6% of land) can be efficient for some farms but highly dependent on crop system, soils, and rainfall.
  - Removing mandatory set-aside can have marked bird population effects, especially when coupled with high commodity prices.
  - ES options compete for points; certain habitat measures (e.g., skylark plots) may be less adopted than hedgerow/margin management due to opportunity costs.
- Data-to-policy connections
  - Integrated model outputs used to quantify ecological responses (weed and bird dynamics) to policy changes and economic signals.
  - Pareto analyses illustrate trade-offs (e.g., profit vs. overwintered stubble) across different farm types.

## Capacity-building, dissemination, and impacts

- Training and capacity
  - Post-docs and students trained; field assistants and external collaborators engaged; cross-disciplinary training in quantitative methods (R, multi-model inference).
- Knowledge transfer
  - Datasets and models used to inform stakeholders, policy discussions, and academic publications.
  - Outputs include software tools for stakeholder analysis and integrated modelling approaches to be used in future research.
- Outputs and publications
  - Datasets, modeling approaches, and several peer-reviewed papers (e.g., integration taxonomy, weed population dynamics, predictive weed models).
  - Policy and practice contributions through stakeholder tools and advisory roles with Defra and other agencies.

## Data management and long-term considerations

- Data accessibility
  - Anonymized data prepared for archiving where appropriate; identifying information restricted to dataset 2.
- Data standards and interoperability
  - Standardized variable coding (Table 1) to enable cross-study reuse; alignment with ecological and socio-economic modelling frameworks.
- Ongoing data needs
  - Need for continued data collection to support dynamic policy scenarios (e.g., changes in EU/UK agricultural policy, climate variability) and to extend models to additional biodiversity and management outcomes.

## Key takeaways for Data Stewards

- The project generates large, multi-scale, multi-domain datasets (weeds, birds, farm management, socio-economic preferences) with explicit data provenance and a clear metadata framework (variable table, coding schemes).
- Data governance considerations are central: anonymization, archiving eligibility, data-sharing constraints, and linking socio-economic data to ecological outcomes require careful governance planning.
- Documentation supports interoperability: detailed variable descriptions, measurement scales, and the hierarchical structure (quadrats, fields, farms, landscapes) enable reproducibility and reuse in integrated modelling.
- The datasets enable policy-relevant analysis, including trade-offs between profitability and biodiversity outcomes, and scenarios around environmental stewardship, set-aside, and agrochemical regimes.
- Ongoing data stewardship needs include robust archiving of anonymized field/ farm activity data, clear access controls for identifying information, and governance frameworks to facilitate future cross-disciplinary data integration.