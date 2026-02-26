# Public perceptions of tidal energy: can you predict social acceptability across coastal communities?

- Overview
  - Investigates public perceptions of tidal energy around the Bristol Channel, focusing on three case study sites in North Devon and Somerset (Taw Torridge estuary; Minehead/Watchet; Weston-super-Mare/Burnham-on-Sea).
  - Tests whether national coastal typologies (MMO typology) based on social, economic, and demographic variables can predict local support or opposition to tidal energy developments.
  - Data collected through a face-to-face survey (March–April 2018) targeting coastal residents; aims to understand drivers of perception and inform planning and stakeholder engagement.

- Data collection scope and context
  - Case study sites are spatially distinct to compare attitudes by location and demographics, enabling empirical testing of typology-based predictions.
  - Typology classes used include Coastal retreats (A1), Coastal challenges (B1), Cosmopolitan coast (C1), and Coastal fringe (D2).
  - Survey administered to adults (18+) living in coastal areas with tidal energy potential; responses anonymised.

- Survey design and content (structure of data collection)
  - Part 1: Use and perceptions of the local coast
    - Measures frequency of various coastal activities (recreational use, tourism impact, etc.).
    - Assesses importance of local environmental features (marine mammals, birds, fish, beaches, habitats, peace, and view) and place attachment factors (reliance on natural landscapes, wildlife, outdoor recreation, etc.).
  - Part 2: Generating electricity using tidal energy
    - Self-assessed informativeness about tidal energy.
    - Attitudes toward renewables, UK leadership in tidal tech, and perceived challenges.
    - Analytic Hierarchy Process (AHP) exercise to rank importance of four tidal-energy attributes: local environmental impact, local job creation, reliability, and cost of energy (pairwise comparisons on a 1–9 scale).
  - Part 3: Tidal energy developments in your area
    - Opinions on hypothetical tidal-energy developments near home; directs respondents to subsequent questions based on stance (oppose, neutral, support).
    - Scenarios for opposition (Q13) and support (Q16) include actions such as attending consultations, commenting, demonstrations, contacting developers, and petitioning.
  - Part 4: Ownership and financing of tidal energy developments
    - Likelihood of supporting or investing in tidal-current developments owned by various actors (UK Government, local council, large energy company, manufacturer, local community).
    - Investment willingness and influence of financial return versus broader environmental or community goals (Q19).
    - Additional questions about openness to community investment and alternative energy investments.
  - Part 5: About you and your household
    - Demographics (length of residence, gender, age, household composition, employment status, income, qualifications).
    - Previous investment in local community projects; experience with public consultation and activism; willingness to participate in follow-up photo-based study.

- Data types and measures
  - Quantitative scales:
    - Frequency of coastal activities (multiple options per activity).
    - Importance ratings for environmental features and place-attachment factors (Likert-type scales).
    - Self-reported knowledge and attitudes toward tidal energy.
    - AHP-derived attribute weights (pairwise comparisons across four characteristics).
    - Opposition/support stance on potential tidal developments (5-point scale).
    - Likert-style ratings on ownership/investment scenarios and influence factors (financial return vs environmental goals; social influence; affordability).
  - Categorical and demographic variables:
    - Gender, age group, duration at address and near coast, employment, income band, qualifications, household composition, prior investments, and prior engagement with public consultations.
  - Open-ended items:
    - Additional comments about why the local coast matters (Q7) and general comments about tidal energy (Q20).

- Data analysis and methods
  - Exploratory Factor Analysis (EFAs) on responses related to coastal use and place-attachment/attitude constructs:
    - Polychoric correlations to handle ordinal data.
    - Kaiser–Meyer–Olkin (KMO) adequacy checks.
    - Oblimin oblique rotation to allow variable correlation.
  - Analytic Hierarchy Process (AHP) weights:
    - Computed via eigenvalue methods in R; weights aggregated across respondents using geometric means.
  - Opposition to tidal development:
    - Logistic regression to model the likelihood of opposing a local tidal project as a function of variables.
    - ANOSIM (species/analytical) in Primer-E v6 for multivariate analysis of explanatory variables by site and typology.
  - Data handling and privacy:
    - Data anonymised; all data included in deposited dataset except surveyor names.

- Purpose and use of the data
  - Data collected to understand public perceptions of wind and tidal energy developments and identify key drivers of acceptance or opposition.
  - Designed to complement a qualitative study in the same geographic areas, enabling richer, mixed-method insights.
  - Outputs intended to inform marine planning, stakeholder engagement, and future energy siting discussions by linking place attachment, typology class, and attitudes to tidal energy.

- Completeness and provenance
  - Data collected by a commercial survey firm (Marketing Means, Devon) on behalf of Plymouth Marine Laboratory; authors responsible for interpretation.
  - All data included in the deposited dataset except interviewers’ names; ethics approval obtained.

- Practical implications for data work and products
  - Potential data products:
    - Predictive models of local opposition to tidal energy based on demographic, place-attachment, and typology variables.
    - AHP-derived importance weights for project design considerations (environmental impact, job creation, reliability, cost).
    - Site- and typology-based comparisons of acceptance patterns to guide targeted engagement strategies.
  - Data integration opportunities:
    - Cross-walk with MMO coastal typology maps to identify communities more or less amenable to tidal developments.
    - Multivariate profiles linking environmental values, place attachment, and stated willingness to invest or participate.

- References and context
  - Grounded in prior research on public attitudes to offshore energy, place attachment, and perception of renewable projects; cites methodological guidance for EFAs, AHP, and multivariate analyses.