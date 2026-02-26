# Management options for biodiverse farming, 2006-2009 Ecology Data USER GUIDE

## Overview
- An integrated socio-economic-ecological research project in the UK, studying how farm land-management affects biodiversity.
- 48 arable farms across Bedfordshire, Lincolnshire, and Norfolk; 500 fields; three-year field data.
- Data collected span economics, farmer decision-making, weeds, and birds; with a strong emphasis on map-based representations and spatial analysis.
- Aims to produce predictive, map-enabled models to inform policy and farming practice.

## Aims and Objectives
- Integrate sociology, agricultural science, economics, and ecology to explain and predict impacts of economic, environmental, technological, regulatory, and social changes on farming, livelihoods, and biodiversity.
- Focus on three biodiversity components: crop weeds, farmland birds, and four mammal species (rabbit, hare, fox, roe deer).
- Develop scalable methodologies to extend to other functional/taxonomic groups.
- Deliver integrated models to evaluate policy alternatives and their ecological and economic consequences.

## Conceptual Framework
- Farmers’ decisions are not purely profit-maximising; risk attitudes, hunting/game shooting, and conservation goals influence management.
- Decisions drive landscape change (hedges, woods) and biodiversity; biodiversity feedback influences future management.
- Study area concentrates on lowland UK arable systems, with 48 farms representing typical variation.

## Stakeholders
- Stakeholder analysis to map interest and influence on arable land management.
- An interactive Stakeholder Analysis Tool was developed to classify stakeholders (e.g., farmers, government, industry) by interest and influence.

## Field Methods
- Weed study focuses on three categories: economic weeds (yield reducers), ecological weeds (bird food), and visually prominent weeds.
- Density-structured population models used: discrete density states (0, low, medium, high, very high) per 20x20 m quadrat.
- 200 quadrats per field, across 10 fields per county, over three yearly censuses (spring, summer, autumn).
- Detailed farm mapping captured habitat features (hedges, ditches, trees) to link weed data with bird models and management decisions.

## Analytical Methods
- Estimate state frequencies while correcting misclassification biases; convert to field-scale mean densities with variance.
- Linear mixed models relate mean field weed densities to prior weed densities, herbicide applications, and farmer preferences.
- Analyses cover both field-scale means and within-field population dynamics to understand drivers of weed abundances.

## Farmer Decisions, Objectives and Preferences
- Used Multi-Criteria Decision Analysis (MCDA) to elicit farmer objectives and preferences for inputs into predictive land-use models.
- Employed a silsoe Whole Farm Model (SFARMMOD) extended to multiple objectives using mixed-integer programming.
- Developed a seven-objective hierarchy with 14 criteria; interactive decision-support tooling to capture farmer satisfaction curves and Swing weighting, enabling farmer-driven input into model parameters.
- Collected farm management records and background variables to contextualize field/farm variation.

## Birds: Abundance, Habitat, and Landscape Context
- Bird models built from BTO/JNCC/RSPB Breeding Bird Survey data (880 1 km squares) for 31 species.
- Habitat variables grouped into: landscape features, field boundary structure, and cropping; models used Poisson GLMs with information-theoretic model selection.
- Additional analyses assessed how landscape heterogeneity (CEH Land Cover Map 2000) across scales (1, 9, 25 km2) influences abundance.
- Field-scale habitat models (based on Whittingham et al. 2005, 2006) predicted breeding densities from boundary and habitat features; used to evaluate management scenarios.
- Integrated socio-economic bird modelling to predict bird responses to land-use changes; linked to farmer preferences.

## Integrated Modelling Framework
- Silsoe Whole Farm Model (SFARMMOD): profit-maximising LP model extended to include conservation decisions, non-production activities, and non-profit goals.
- Non-cropped land uses (hedges, ditches, woodlands) modeled as regional scenario variables; forestry/landscape features treated as exogenous maintenance needs.
- Multi-Attribute Utility Theory (MAUT) used to encapsulate conservation, landscape, and lifestyle values; piecewise linear utility functions with mixed-integer optimization to handle non-convexities.
- Integrated model capable of: predicting optimal farm management, measuring deviations from optimum, and projecting ecological outcomes (weeds, birds) under policy and economic changes.

## Interdisciplinarity and Method Integration
- Challenge: harmonizing small-scale ecological methods with whole-farm and socio-economic scales.
- Adopted semi-mechanistic modelling and regression approaches to enable cross-disciplinary integration while preserving ecological validity.
- Regular meetings and cross-team collaboration to align methodologies; post-docs contributed to joint outputs.

## Data and Outputs: Datasets and Visualisations
- Weed dataset: density-state maps for seven weed species across 500 fields, three years, ~2 million data points; field-scale maps (20x20 m cells) illustrate spatial distribution (Figure 7).
- Weed–management relationships: negative but variable responses to herbicide applications; limited association with nitrogen input; species-specific drivers (Table 1 highlights).
- Bird-data outputs: abundance models across landscapes and boundaries; maps and models at 1 km and field scales; habitat- and crop-related findings.
- Non-technical outputs: taxonomies of socio-economic methods; stakeholder tool; 2–3 major datasets for archiving; papers and conference presentations.

## Integrated Outputs and Policy-Relevant Scenarios
- Integrated analyses show profit-maximising alone poorly predicts farmer behavior; adding stated preferences improves predictive power.
- Farm-level findings include substantial variability in weed density responses to management and strong influence of crop type on weed dynamics.
- Policy scenarios explored include: overwintered arable stubbles, skylark plots, and set-aside removal; integration with price signals and subsidy regimes to assess bird and weed outcomes.
- Examples of policy insight: potential costs and trade-offs of mandatory overwintered stubbles; regional differences in the cost-effectiveness of environmental measures.

## Knowledge Transfer, Engagement, and Impacts
- Data on farmer attitudes and management patterns used to explain weed abundance and management heterogeneity.
- Models used to evaluate policy options (e.g., set-aside changes) and farm advisory tools.
- Stakeholder-tool and interdisciplinary methods shared with universities, policy bodies, and research partners.

## Policy and Practice Implications
- Findings support including farmer motivations and non-profit objectives in land-use models to better predict biodiversity outcomes.
- Highlights the importance of non-crop habitat (hedgerows, woodlands) and field boundaries in shaping bird populations.
- Demonstrates the potential ecological consequences of herbicide regulation changes and agricultural policy shifts.

## Capacity Building and Training
- Training of undergraduate assistants, post-docs, and partner institutions; dissemination through society meetings and workshops.
- Development of software tools and modelling approaches with potential for broader adoption.

## Climate Change, Herbicide Resistance, and Future Work
- Climate variability and extreme weather highlighted as influential on management efficacy and outcomes.
- Herbicide regulation changes anticipated to increase reliance on diverse management strategies and increase potential resistance issues.
- Proposals for further work include habitat-inclusive predictions, scaling non-crop habitat data collection, and expanding models to other policy contexts.

## Spatial Data and GIS-Relevant Aspects
- Spatially explicit data collection and mapping are central: 20x20 m quadrats, 500 fields, and 48 farms with boundary/habitat features.
- Weed density states mapped across fields allow rapid broad-scale assessment and integration with farm-level decision models.
- Bird abundance analyzed at 1 km squares and linked to landscape heterogeneity at multiple scales (1, 9, 25 km2).
- Non-cropped habitat features (hedges, ditches, woodlands) linked to both weed and bird models for integrated spatial forecasting.
- Outputs include field-scale weed maps, boundaries and habitat feature layers, and scenario-based predictions that can be translated into map-based policy briefs or decision-support visuals for farmers and policymakers.