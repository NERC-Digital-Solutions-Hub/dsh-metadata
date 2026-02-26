# Public perceptions of tidal energy: can you predict social acceptability across coastal communities?

- Overview
  - Aim: Investigate whether social acceptability of tidal energy can be predicted across coastal communities using maps derived from social, economic, and demographic variables, tested within specific case-study areas along the Bristol Channel.
  - Relevance for GIS: Demonstrates integration of survey-derived social data with spatial typologies and census-based variables to produce map-based insights for planning and stakeholder engagement.

- Study area and typologies
  - Case-study sites (coastal England): Taw Torridge estuary (Northern Devon), Minehead/Watchet, and Weston-super-Mare/Burnham-on-Sea.
  - Purpose of site selection: allow comparisons of attitudes by location and demographics; assess applicability of spatial typologies.
  - MMO coastal typology used: four classes from Roger Tym & Partners/OCSI (A1 Coastal retreats; B1 Coastal challenges; C1 Cosmopolitan coast; D2 Coastal fringe), to explore whether maps derived from these categories predict support or opposition to tidal energy.

- Data collection (what was recorded and how)
  - Method: Face-to-face survey with general public during March–April 2018; participants 18+ from coastal Somerset and Devon.
  - Structure: three-part questionnaire plus demographics; approximately 15 minutes; anonymous and voluntary.
  - Key sections:
    - Part 1: Local coastal use and perceived importance of coastal features (marine mammals, birds, fish, beaches, habitats, peace, and views) and place attachment factors (reasons for living near coast, such as friends, family, culture, outdoor recreation, landscapes, wildlife).
    - Part 2: Tidal energy focus—self-rated information level, attitudes to renewable energy, and an Analytic Hierarchy Process (AHP) to weight four tidal-energy characteristics (local environmental impact, local job creation, reliability, cost of energy).
    - Part 3: Hypothetical tidal energy developments in respondents’ local area; likelihood of support or opposition; subsequent questions depending on stance.
    - Part 4–5: Ownership/financing considerations, further demographic details, and potential participation as volunteers.
  - Survey administration notes: randomization of certain questions where possible; instructions to capture street and town/village data; ethics and consent procedures included.

- Variables and data types for GIS use
  - Spatially relevant inputs: MMO coastal typology classifications; location-based responses related to place attachment, local environmental concerns, and economic considerations (job creation, cost, reliability).
  - Social data: perceived importance of environmental features, place attachment factors, and attitudes toward tidal energy, including preparedness to engage in public processes.
  - Economic/ownership dimensions: preferences regarding ownership/financing of tidal developments and willingness to invest or have local/community involvement.

- Data analysis approach (how the data were analysed)
  - Exploratory factor analysis (STATA) on local coastal environment use and place-attachment variables using polychoric correlations; Kaiser-Meyer-Olkin measure and Oblimin rotation to allow correlated factors.
  - Analytic Hierarchy Process (AHP) weights calculated via eigenvalue method in R; aggregated across respondents using geometric mean.
  - Logistic regression (STATA) to model how variables contribute to opposition to local tidal development.
  - Multivariate analysis of variance by group differences (ANOSIM, Primer-E v6) to explore variation in opposition by case study site and typology.
  - Completeness: dataset largely complete with all data included except surveyor names.

- Data provenance and ethical context
  - Researchers: Plymouth Marine Laboratory; survey data collected by Marketing Means (Devon) for the ADVENT project; ethical approval secured.
  - Purpose: to understand public perceptions of wind and tidal energy and identify key drivers to inform planning and engagement.
  - Data use: intended for broader dissemination and for development of data products to support planning and stakeholder communication.

- Implications for GIS and data products
  - Potential outputs: spatially explicit maps showing predicted acceptability of tidal energy across coastal communities, informed by MMO typology and census-derived variables.
  - Applications: assist policy colleagues, clients, and the public in understanding where tidal-energy developments may encounter higher or lower acceptance, and how place attachment and environmental concerns shape responses.
  - Data integration opportunities: merging survey-derived social factors with spatial layers (typology classes, demographics, environmental features) to create decision-support visualizations for coastal planning and stakeholder engagement.

- Limitations and context for GIS work
  - Geographic scope: three case-study sites; results may vary by location; spatial transferability should be tested with additional sites.
  - Data type: cross-sectional survey data; results reflect stated preferences and may be influenced by place attachment and social context.
  - Typology usage: analysis incorporates four MMO classes, which informs how maps might categorize communities for planning purposes.

- Practical takeaways for GIS specialists
  - Build map layers that encode social variables (place attachment, information level, attitudes) alongside typology classifications to create intuitive acceptability surfaces.
  - Use AHP-derived weights to map relative importance of tidal-energy characteristics (environmental impact, job creation, reliability, cost) across regions.
  - Employ spatial analysis to compare attitudes across sites, identifying potential hotspots of opposition or support to guide engagement strategies.
  - Leverage integrated datasets (survey responses, census-derived indicators, typology) to develop interactive tools for policymakers and stakeholders.