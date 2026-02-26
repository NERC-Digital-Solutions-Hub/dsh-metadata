# Data resource: Questionnaire surveys of greenspace users on perceptions of experimentally manipulated urban meadows

## Overview
- Data consist of questionnaire outcomes from greenspace users regarding perceptions of urban meadows with manipulated diversity and sward height, plus associated respondent socio-economic data.
- Experimental meadows located in Bedford and Luton; informed consent obtained; originally collected in 2014 under the Fragments, functions and flows NERC BESS project; later re-analyzed for a 2021 paper in People and Nature.
- Data resource comprises one CSV file (Data_Phase 2_AsUsed_ForPublicArchive.csv) with 1020 rows and 21 columns.

## Experimental design and sampling
- 9 experimental meadows per site (3 diversity levels x 3 height levels) across 4 sites.
- 30 greenspace users surveyed at each location/site.
- Locations include four Bedford/Luton sites with precise site codes and coordinates provided.

## Data collection and transformation
- Data collected via questionnaire administered to greenspace users.
- Respondents provided informed consent; responses checked during data entry; non-matching categorical responses excluded.

## Nature and units of recorded values
- Variables include:
  - Treatment and meadow characteristics: site code, diversity (low/medium/high), height (short/medium/tall), and a 9-level treatment descriptor combining diversity and height.
  - Perception-related measures: Q1_PerceivedDiversity (perceived plant diversity), Q2_PrefScore (liking on a 1–10 scale).
  - Eco-knowledge and environmental cognition: plantid_EcoKnowledge, totalWL_EcoCentrism (wildlife features in garden plans), visitlength, visitfreq, othergsfreq, visitcount, etc.
  - Demographics and socioeconomics: gender, age, income, employ, edu, ukresident, ethnic.
- Data types include both numeric (e.g., scores, counts) and categorical responses (e.g., diversity, height, treatment).

## Analytical methods and usage
- The presented data have not been analyzed within this data resource.
- Prior analyses (Southon et al. 2017; 2018) used multivariate analysis and mixed-effects models in R to relate meadow characteristics to user responses.
- A subsequent analysis (Jones et al., 2021, People and Nature) applied mixed effects models and Bayesian modelling to explore how user characteristics shape perceptions within a cultural services framework.

## Quality control and ethics
- Ethical approval obtained from the University of Sheffield’s Research Ethics Committee (Landscape Architecture Ethics Panel).
- Data entry quality checks performed; responses outside categorical options excluded.

## Data structure details
- Dataset: Data_Phase 2_AsUsed_ForPublicArchive.csv
- Rows: approximately 1020
- Columns: 21
- Key fields:
  - SITE (location code), Sample/SampNo (respondent and data point identifiers)
  - Diversity, Height (meadow characteristics)
  - Treatment description (nine combinations of Diversity x Height)
  - Q1_PerceivedDiversity, Q2_PrefScore (perception measures)
  - plantid_EcoKnowledge, totalWL_EcoCentrism, visitlength, visitfreq, othergsfreq, visitcount (environmental cognition and visitation behavior)
  - Demographics: gender, age, income, employ, edu, ukresident, ethnic

## Reuse potential and relevance for environmental monitoring
- Demonstrates how evidence of perceived aesthetic and cultural ecosystem services from urban meadows can be standardized for monitoring over time.
- Enables integration with other environmental datasets to enhance value and provide broader access to underlying data.
- Suitable for policy evaluation on urban greenspace design, biodiversity cues in landscapes, and public well-being related to cultural ecosystem services.
- Supports standardized reporting formats and data sharing to facilitate scrutiny of environmental health and policy performance.