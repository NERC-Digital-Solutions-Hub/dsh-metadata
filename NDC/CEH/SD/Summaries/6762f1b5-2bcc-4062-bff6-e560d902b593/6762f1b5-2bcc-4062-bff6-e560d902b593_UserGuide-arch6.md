# Management options for biodiverse farming, 2006-2009 Ecology Data USER GUIDE

- A multi-disciplinary project integrating sociology, agricultural science, economics, and ecology to model how farm land-use decisions affect biodiversity in the UK.
- Study scope: 48 arable farms across Bedfordshire, Lincolnshire, and Norfolk; field-scale weed dynamics, bird populations, and farmer decision-making; three-year data collection across 500 fields.

## Data and variables

- Weed data file: alldataanonymised.txt with detailed coding for:
  - Temporal/spatial: year, census, county, farm, field, quad, x, y
  - Cropping: crop type per field
  - Species density quartiles for seven weeds (e.g., Alopecurus myosuroides, Chenopodium album, Papaver rhoeas, etc.)
  - Density states: 0, NA, L, M, H, V per 20 m2
- Field methods: 20x20 m quadrats within fields; three censuses per year (spring, summer, autumn)
- Field/habitat data: key habitat features (hedges, ditches, trees) collected to link weed data with bird models
- Weed survey graphical representation: Figure S1 detailing quadrat grid and presence coding

## Datasets and data governance

- Three core datasets produced:
  - Background information on farmer circumstances and decision-making data
  - Comprehensive description of activity on each farm to parameterise land-use models
  - Detailed crop-management data for fields surveyed for weeds
- Anonymity: Dataset with identifying information about farms is not suitable for archiving; other datasets prepared for archiving
- Weed dataset scale: ~2 million data points (density-state maps across fields and years)

## Analytical methods for weeds and field-scale dynamics

- Density-state estimation: statistical methods to estimate frequency of each density state and derive field-scale mean and variance
- Field-scale modeling: linear mixed models relating mean weed densities to
  - Previous weed densities
  - Herbicide applications
  - Farmer-stated environmental and other preferences
- Within-field dynamics: analysis aimed at dissociating sources of variability (within-field density dynamics, scaling up to farm level)
- Key results highlight: strong species-specific drivers; herbicide use reduces density but effects are highly variable; crop type and background density substantially influence weed abundance

## Birds: abundance, habitat, and landscape context

- Data sources: Breeding Bird Survey data from 880 1 km squares in lowland Britain (2007)
- Habitat variables: three sets
  - Landscape features (woodland, grassland, etc.)
  - Boundary characteristics (hedges, trees, ditches)
  - Cropping (crop presence/types)
- Modeling approaches: generalized linear models (Poisson) with information-theoretic model selection
- Habitat heterogeneity analyses: density-heterogeneity at scales of 1 km2, 9 km2, 25 km2
- Field-scale modeling: use of published territory-use models (Whittingham et al.) to predict breeding densities based on boundary features and cropping
- Integrated bird modeling: coupling bird models with socio-economic farming model to predict population changes under land-use scenarios

## Integrated socio-economic-ecological modeling

- Framework: align farmer decisions with economic, social, and ecological outcomes
- SFARMMOD: Silsoe Whole Farm Model
  - Original: profit-maximizing linear programming for land-use and operations
  - Extensions: incorporate non-production activities, conservation decisions, and non-profit goals
  - Non-cropped areas (hedges, ditches, woodlands) included as regional scenario variables; not all are decision variables due to data limitations
- Multi-Attribute Utility Theory (MAUT): elicitation of farmer values and goals to model decision-making
  - Utility curves: piecewise linear segments derived from farmer preferences
  - Optimization: mixed-integer programming to address non-convex utility, enabling multi-objective optimization
- Social data integration: stated preferences collected via decision-support software; used to parameterize farmer-profit-conservation trade-offs
- Outputs: model accounts for conservation interventions, stewardship schemes, and the broader landscape context

## Stakeholder analysis and interdisciplinarity

- Stakeholder mapping: interactive mapping of interest and influence for arable land management (habitat, information, production, regulation)
- Interdisciplinary integration: cross-disciplinary data collection and modeling challenges addressed with new methods to enable large-scale integration
- Collaboration: regular project meetings; cross-team post-docs contributed to joint outputs and inter-disciplinary papers

## Integrated analysis and policy-relevant scenarios

- Key integrated outputs:
  - Policy-relevant scenarios combining weed dynamics, bird populations, and farm economics
  - Predictions of overwintered stubble viability under different subsidies and crop rotations
  - Assessment of Environmental Stewardship (ES) schemes, including potential under- or over-valuation of management options
  - Cost assessments for mandates (e.g., 10% overwintered stubble) and Pareto trade-offs across profit vs. biodiversity goals
- Notable findings:
  - Non-profit objectives (risk, number of crops, conservation preferences) improve predictive power beyond profit-maximization alone
  - Crop management variables (cropping choices) are more tractable for habitat management, yet non-crop landscape features often dominate bird abundance and habitat quality
  - High income aspirations correlate with intensive herbicide use, but do not necessarily translate to reduced biodiversity
  - Landscape-scale non-crop features are critical for bird habitats; data availability for these features is more limited but essential for accurate modeling

## Outputs, knowledge transfer, and impacts

- Knowledge products:
  - Datasets describing farmer attitudes, management activity, and weed abundance
  - Weed density maps and field-scale distribution visuals
  - Integrated models linking farmer decisions to weed and bird populations
  - A stakeholder analysis tool for mapping interest/influence
- Publications and presentations:
  - Journal articles on integrating socio-economics and ecology; weed population modeling; and interdisciplinary modeling approaches
  - Stakeholder tool demonstrations to practitioners and academics
- Policy relevance:
  - Informs best-practice farm management and policy design for biodiversity targets
  - Assists in assessing social and economic consequences of biodiversity conservation
  - Guides future research proposals on climate-related agricultural changes and herbicide resistance

## Capacity-building and training

- Training of undergraduates and early-career researchers in weed surveys, data analysis, and multi-model inference
- Involvement of participants in external conferences and workshops; dissemination to policymakers and practitioners

## Future directions and ongoing work

- Continued integration of social and ecological models to address policy questions more robustly
- Exploration of non-market preferences and risk attitudes in land-use planning
- Extension to larger-scale policy scenarios, including climate change impacts and herbicide regulation changes
- Development of automated weed-detection technologies aligned with project data streams