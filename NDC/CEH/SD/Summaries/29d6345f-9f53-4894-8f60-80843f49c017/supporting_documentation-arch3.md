# Greenspace users’ perceptions of experimentally manipulated urban meadows

- Overview
  - Data from questionnaire surveys of greenspace users assessing perceptions of experimentally manipulated urban meadows varying in floral diversity (low/medium/high) and sward height (short/medium/tall).
  - Experimental meadows located in Bedford and Luton; data collected by the authors with informed consent; originally part of the Fragments, functions and flows NERC BESS project (2014) and later re-analysed for a 2021 paper in People and Nature.
  - The dataset supports modelling cultural ecosystem services and user perceptions in relation to meadow design.

- Experimental design
  - Nine meadow types per site (3 diversity levels × 3 height levels).
  - Four sites: Bedford (Chiltern Ave, Goldington Green, Brickhill Heights) and Luton (Bramingham Road).
  - 30 greenspace users surveyed at each location, totaling 1020 responses across 36 plots/meadows.

- Data collection and variables
  - Method: self-administered questionnaires completed by greenspace users.
  - Recorded outcomes include: perceived diversity (Q1_PerceivedDiversity) and a user preference score (Q2_PrefScore) on a 1–10 scale.
  - Additional variables include: plant knowledge (plantid_EcoKnowledge), wildlife/eco-centred attitudes (totalWL_EcoCentrism), visit patterns (visitlength, visitfreq, othergsfreq, visitcount), and demographic attributes (gender, age, income, employment, education, UK residency, ethnicity).
  - Data structure uses a single CSV with 1020 rows and 21 columns; NA indicates no response.

- Analytical methods used with the dataset
  - Prior analyses (Southon et al. 2017, 2018) employed multivariate analyses and mixed effects models in R to link meadow characteristics with user responses.
  - Jones et al. (2021, People and Nature) applied mixed effects models and Bayesian modelling to examine how different user characteristics shape perceptions within a cultural services framework.

- Data quality, ethics, and governance
  - Ethically approved by the University of Sheffield’s Research Ethics Committee.
  - Data entry checks performed; responses not matching categorical options excluded.
  - Data are intended for open sharing via public archive, though care is needed regarding metadata completeness and data governance.

- Data structure and access
  - Core data file: Data_Phase 2_AsUsed_ForPublicArchive.csv (1,020 rows × 21 columns).
  - Key fields include: SITE, Sample, SampNo, Diversity, Height, Treatment description; Q1_PerceivedDiversity; Q2_PrefScore; plantid_EcoKnowledge; totalWL_EcoCentrism; visitlength; visitfreq; visitcount; othergsfreq; demographic fields (gender, age, income, employ, edu, ukresident, ethnic), and NA for missing responses.
  - Column descriptions provide codes (e.g., site codes CA, BK, GG, BR) and category labels (low/medium/high diversity; short/medium/tall height).

- Implications for monitoring frameworks
  - Demonstrates how to integrate ecological treatment variation with socio-economic survey data to measure cultural ecosystem services and aesthetic/value perceptions.
  - Highlights practical data management needs: metadata completeness, data governance, openness, timely data sharing, and standardised data cleaning.
  - Reveals challenges common in environmental health monitoring data: data gaps, data silos, complex transformation of datasets, and clear communication of findings to stakeholders.
  - Provides measures that can inform policy decisions on urban meadow design to enhance perceived site quality and well-being, while illustrating the importance of linking ecological interventions to public perception outcomes.