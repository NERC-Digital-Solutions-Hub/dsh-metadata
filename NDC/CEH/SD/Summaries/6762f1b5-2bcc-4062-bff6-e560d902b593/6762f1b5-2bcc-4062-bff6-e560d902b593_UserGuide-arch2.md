# Management options for biodiverse farming, 2006-2009 Ecology Data USER GUIDE

## Overview
- Integrates social science and ecology to predict how farm land-use decisions affect biodiversity (weeds, birds, and mammals) under different economic, policy, and management scenarios.
- Studies 48 lowland UK arable farms across Bedfordshire, Lincolnshire, and Norfolk; focuses on 500 fields over three years.
- Develops an integrated modelling framework combining farmer decision-making, weed dynamics, bird populations, and farm-level economics to inform policy and practice.

## Data architecture and variables
- Weed data file structure (alldataanonymised.txt) with:
  - Spatial-temporal keys: year, census time, county, farm, field, crop, quadrat, x/y coordinates.
  - Density quartiles for seven weed species (Alopecurus myosuroides, Avena fatua, Stellaria media, Chenopodium album, Fallopia convolvulus, Papaver rhoeas, Poa annua) with coded density levels (0, L, M, H, V) and NA for missing data.
- Dutch-style density states mapped at 20 m x 20 m quadrats within fields; 3 censuses per year (spring, summer, autumn).
- Non-weed habitat and farm-structure data collected (hedges, ditches, trees, boundaries) to link vegetation with bird models.

## Field methods and data collection
- Field-scale weed surveys:
  - 20 x 20 m quadrats; 200 quadrats per field; 10 fields per farm; 48 farms total.
  - Three censuses per year to capture seedling, mature weed stages in crops, and fall-back crops.
- Weed focus groups:
  - Economic weeds (yield reducers), ecological weeds (bird food), and highly visible weeds.
- Farm mapping:
  - Document field boundaries, hedges, ditches, trees to support integration with bird models and management analyses.

## Analytical approach
- Weed modelling:
  - Density-state to field-scale mean density conversions; correct for misclassification bias.
  - Linear mixed models relate field mean densities to:
    - Previous weed densities
    - Herbicide applications
    - Farmer stated preferences (environmental factors, etc.)
  - Within-field population dynamics analyzed with density-structured approaches (zero/low/med/high/very high states).
- Bird modelling:
  - Abundance models for 31 farmland bird species using:
    - Landscape composition (from Land Cover Map 2000)
    - Field boundary structure
    - Cropping data
  - Generalized linear models with Poisson error and log link; model selection via information-theoretic approaches.
  - Habitat heterogeneity analyzed at scales 1 km2, 9 km2, 25 km2, linking heterogeneity to abundance.
  - Field-scale predictions using Whittingham et al. models to relate boundary habitat features to bird territories.
- Integrated socio-ecological modelling:
  - Prototype predictions under scenarios (e.g., rising biofuel prices) with hypothetical social objectives; extended to include stated farmer preferences.
  - Interweaves social data with ecological models to predict outcomes for birds and weeds under changing management and policy.

## Social dimensions: farmer decision-making
- Multi-Criteria Decision Analysis (MCDA) used to capture farmer objectives and constraints.
- Data input into a Silsoe Whole Farm Model (SFARMMOD) extended for multiple objectives via mixed-integer programming.
- Developed a hierarchy of seven land-use objectives and 14 measurable criteria; used interactive decision-support software to elicit satisfaction curves and Swing weights.
- Analysis reveals substantial heterogeneity among farmers in:
  - Profit importance and risk tolerance
  - Preferred crop numbers and management complexity
  - Attitudes toward agri-environment schemes and non-profit goals (e.g., landscape quality, wildlife)
- Farmer background data compiled to contextualize field/farm variation.

## Integrated whole-farm modelling (SFARMMOD) and MAUT
- SFARMMOD: profit-maximizing model extended to include conservation decisions, non-production activities, and non-profit goals.
- Non-cropped land uses (ditches, hedges, woodland) treated as region-specific scenario variables influencing maintenance, inputs, and revenue; not always active decision variables due to data limitations.
- Multi-Attribute Utility Theory (MAUT) used to capture farmer values and goals; yields piecewise linear utility curves and mixed-integer optimization to handle non-convexities.
- Outputs enable exploring trade-offs between profit, conservation, and management complexity across scenarios and landscapes.

## Stakeholder analysis and interdisciplinarity
- Stakeholder analysis tool developed and applied to map interest and influence across habitat, information, production, and regulation functions.
- Interdisciplinary collaboration highlighted as essential:
  - Ecologists and social scientists adapted data collection and modelling to support cross-scale integration.
  - Regular project meetings and cross-team interactions facilitated alignment of ecological and socio-economic components.

## Policy experiments and outputs
- Integrated models applied to policy questions, including:
  - Impacts of removing mandatory set-aside and alternative land-use scenarios coupled with price changes (biofuel-driven markets).
  - Economics of overwintered stubble as a habitat resource; 6% of ground could be efficient under certain crops/soils/rainfall.
  - Effectiveness and costs of agri-environment prescriptions (e.g., skylark plots) and their interaction with compensation levels.
  - Pareto trade-offs between profit and overwintered stubble area across different locations and soil types.
- Evidence that non-crop landscape features (boundaries, hedges, woodlands) and landscape heterogeneity often drive bird populations more than cropping per se, though cropping remains a tractable lever for habitat management.
- Findings indicate that profits alone poorly predict farmer behavior; incorporating risk preferences, conservation objectives, and management complexity improves predictive power.

## Data management, outputs, and dissemination
- Outputs include three datasets:
  - Farmer decision-making and socio-economic context
  - Detailed farm- and field-level activity data for model parameterization
  - Weed management and crop data from weed surveys
- Weed dataset comprises about 2 million data points (density-states across fields, farms, counties, years).
- Data anonymized; some datasets not suitable for archiving due to identifying farm-level details; others prepared for archiving.
- Publications and reports:
  - Key papers on integrating socio-economics and ecology; weed population modelling; and essential reviews of integrating social and ecological modelling.
  - Stakeholder tool and dissemination activities to practitioners and academics.
- Knowledge transfer:
  - Reports, workshops, and presentations to practitioners, universities, and policy bodies.
  - Training of post-docs, undergraduates, and research staff.

## Impacts and policy relevance
- The integrated framework demonstrates that:
  - Including farmer preferences and risk considerations improves predictive accuracy for land-use decisions and biodiversity outcomes.
  - Non-crop habitat management and landscape structure are critical levers for farmland bird populations.
  - Policy instruments (set-aside, hedgerows, stubbles, ES points) interact with economics and farmer incentives in complex ways; targeted subsidies may be necessary to align conservation with farmer behavior.
- Findings inform policy design, illustrating how to quantify ecological and economic consequences of changes in agricultural policy and stewardship schemes.

## Climate, resistance, and future directions
- Climate variability and extreme weather (dry springs, wet summers) influence management efficacy and biodiversity outcomes.
- Anticipates herbicide resistance issues as regulations tighten; potential increases in inputs, costs, and biodiversity trade-offs.
- Proposes expansion to phase IV RELU research to capitalize on farmer input and advisory expertise to forecast environmental changes.

## Analysts’ monitoring perspective: what to take away
- Standardized, linked datasets across ecology and socio-economics support longitudinal monitoring of environmental health and policy performance.
- The project exemplifies robust data verification, quality assurance, and data transformation to enable cross-disciplinary analyses.
- Outputs provide clear formats (descriptive reports, models, and policy scenarios) suitable for scrutiny by policymakers and stakeholders.
- Datasets and models offer a blueprint for scalable environmental monitoring that integrates ecosystem indicators (weeds, birds) with social drivers (farmer decisions, incentives) to track progress over time.