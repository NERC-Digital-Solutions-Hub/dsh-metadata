# Management options for biodiverse farming, 2006-2009 Ecology Data USER GUIDE

- Aims and scope
  - Integrate socio-economics, agriculture science, economics, and ecology to understand how farming practices affect biodiversity and to predict outcomes under different policy and market scenarios.
  - Study 48 lowland arable farms across Bedfordshire, Lincolnshire, and Norfolk to model decisions, weed dynamics, and bird populations.
  - Develop and apply integrated models that link farmer decisions, weed populations, and farmland bird abundance, enabling policy evaluation and scenario analysis.

- Conceptual framework
  - Farmers’ decisions are shaped by profit, risk, and non-economic values (e.g., conservation, landscape quality), not by profit alone.
  - Decisions influence landscape structure (hedges, woods, boundaries) and biodiversity (weeds, birds), with feedbacks from biodiversity to management and profitability.
  - An integrated, multi-scale model links field-level processes to farm-level and landscape-level outcomes.

- Study design and field methods
  - Weed components: focus on economically important and ecologically relevant weeds (e.g., Alopecurus myosuroides, Chenopodium album, Papaver rhoeas, Avena fatua, Stellaria media, Poa annua, Fallopia convolvulus).
  - Field sampling: 20×20 m quadrats; 200 quadrats per 10 fields across 48 farms; three censuses per year (spring, summer, autumn) over three years.
  - Habitat data: mapped key field boundary features and habitats to enable integration with bird and landscape models.

- Data and variable structure
  - Weed data file with multidimensional coding: year, census timing, county, farm, field, crop, quadrat, coordinates, and density quartiles for seven weed species.
  - Density states per quadrat: 0 (not present), L, M, H, V (with NA for missing data).
  - Data scale: approximately 2 million weed density observations across 500 fields and 48 farms.

- Analytical approaches for weeds
  - Density-state to mean-density conversion and population size estimates at field scale.
  - Corrections for misclassification biases; evaluation of model performance.
  - Linear mixed models linking field-mean weed densities to: previous weed densities, herbicide applications, and farmer preferences.
  - Within-field dynamics examined using density-structured models to separate sources of variability (between fields, farms, and management practices).

- Farmer decisions, objectives, and preferences
  - Used Multi-Criteria Decision Analysis (MCDA) to elicit farmer objectives and preferences, informing a multi-objective farming model.
  - Developed a hierarchy of seven land-use objectives with 14 criteria, captured via decision-support software and a swing weighting method.
  - Collected data to parameterize individual farm models, capturing variability among farmers and enabling clustering by preferences.
  - Farm management records and background variables were compiled to provide context for field- and farm-level variation.

- Birds: abundance, habitat, and landscape effects
  - Data sources: breeding bird survey data (BBS) across 880 1-km squares in lowland Britain (2007) for 31 focal farmland bird species.
  - Habitat variables classified into three sets: landscape features, boundary structure, and cropping.
  - Modelling approach: Poisson GLMs with information-theoretic model selection to relate bird abundance to habitat factors.
  - Habitat heterogeneity: assessed at 1 km^2, 9 km^2, and 25 km^2 scales using CEH Land Cover Map 2000; tested how heterogeneity influences bird abundance across scales.
  - Field-scale models: applied Whittingham et al. (2005, 2006) habitat-use frameworks to predict breeding densities based on boundary features and cropping.
  - Integrated modelling: linked socio-economic farming model outputs with bird-habitat models to predict responses to land-use changes, including policy scenarios.

- Integrated modelling framework
  - Silsoe Whole Farm Model (SFARMMOD) extended to include conservation decisions, non-production activities, and non-profit goals.
  - MAUT (Multi-Attribute Utility Theory) used to elicit farmer values and construct utility curves for nonlinear objectives; results fed into a mixed-integer optimization.
  - Model outputs include optimal land-use decisions, deviations from optimality, and integrated ecological predictions for birds and weeds.
  - Scenarios analyzed: set-aside removal, overwintered stubble, environmental stewardship options, and responses to price changes (bio-fuel era).
  - Data integration approach: link weed densities and bird responses with farming decisions in a coherent, scalable framework from field to landscape.

- Interdisciplinarity and stakeholder engagement
  - Recognized challenges of integrating ecological field methods (field-scale weed ecology) with broad-scale socio-economic modelling.
  - Implemented cross-disciplinary teams, regular project meetings, and post-doc collaborations to align ecological and social components.
  - Stakeholder analysis and mapping used to identify interests and influence across habitat, production, regulation, and information functions of farmland.
  - Four integration approaches identified: (a) outcomes measured as profit; (b) outcomes as profit plus conservation metrics; (c) ecological feedback to human decisions; (d) accounting for variability among decision-makers.
  - Taxonomy of socio-economic methodologies and a review of their use in agro-ecology to bridge communication gaps between disciplines.

- Outputs, data, and knowledge transfer
  - Datasets: three main datasets including farmer decision data, farm activity parameterization, and weed density data; weed dataset contains ~2 million data points; some data restricted to protect anonymity.
  - Publications: several peer-reviewed papers on integrating socio-economics and ecology, weed population modelling, and integrated agro-ecology modelling.
  - Knowledge transfer: social and ecological findings communicated to practitioners and policymakers; stakeholder tool shared with academic and policy institutions; various presentations and conferences.
  - Data governance: anonymization and archiving constraints discussed; some data not suitable for archiving due to identifying information.

- Impacts on policy and practice
  - Addresses policy-relevant questions: best measures to achieve bird targets; drivers of adoption of new farming methods; social and economic consequences of biodiversity conservation.
  - Demonstrates that including non-profit objectives (risk management, cropping diversity) improves predictive power over profit-only models.
  - Policy scenarios show how management options like overwintered stubble or set-aside interact with market conditions and policy instruments (e.g., Environmental Stewardship schemes).
  - Highlights the importance of non-crop habitat management (hedgerows, woodlands, boundaries) for birds and biodiversity, often more influential than cropping changes alone.
  - Provides a framework for habitat-inclusive predictions of policy impacts, acknowledging data limitations for non-crop habitats at national scales but enabling farm-scale analysis that can be scaled up.

- Capacity-building and training
  - Involved post-docs delivering talks, engaging in multi-disciplinary training, and training undergraduate field assistants (some pursuing PhDs).
  - Collaboration with external research partners (Defra, BBSRC, Royal Society, etc.) and dissemination through foundational methodological work (stakeholder analysis tool, utility-based farming modelling).

- Data management, governance, and challenges for monitoring
  - Data richness enables comprehensive monitoring across weed dynamics, farmer decisions, and bird populations, but data access and metadata quality can hinder sharing and reuse.
  - Field- and farm-level data integration required creating new measurement and modelling approaches to support larger-scale analyses without compromising data validity.
  - The framework demonstrates how to monitor socio-economic and ecological outcomes concurrently and how to incorporate stakeholder values into monitoring design.

- Non-technical summary (high-level implications)
  - Integrating social and ecological data improves understanding and prediction of farm landscapes and biodiversity outcomes.
  - Farmer objectives and attitudes significantly influence management and biodiversity, beyond what profit maximization would predict.
  - Weed and bird models show that non-crop habitat features and landscape context are key drivers of biodiversity, with cropping changes offering additional but variable leverage.
  - The integrated modelling approach supports evaluation of policy instruments (set-aside, ES schemes) and helps identify trade-offs between profitability and biodiversity conservation.