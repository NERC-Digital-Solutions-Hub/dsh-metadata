# Does meiotic drive alter male mate preference?

- Overview
  - Two experiments study whether male Teleopsis dalmanni with the XSR meiotic drive chromosome (SR) differ in mate preference from wildtype (ST) males.
  - Binary choice trials present two females (one large, one small) to assess mating preference under conditions mirroring wild population dynamics.

- Experimental design
  - Experiment 1: focal male eyespan constrained to a narrow trait range to test genotype effects on mating behavior independent of eyespan.
  - Experiment 2: focal male eyespan unconstrained and drawn from its natural distribution to assess direct effects of eyespan and its association with genotype on mate preference.

- Data files and structure
  - Two CSV data files: Male_preference_experiment_1_data.csv and Male_preference_experiment_2_data.csv.
  - Each row represents a single male and includes mating records across successive matings.

- Key variables and definitions
  - Male.ID: unique identifier for each male.
  - Date: date of each mating event.
  - 1st / 2nd / 3rd, etc.: record of mating with large (L) or small (S) female on each trial.
  - Eyespan: distance between outer tips of the eyes (mm); present in experiment 2 only.
  - Thorax: thorax length (mm); present in experiment 2 only.
  - Total.large or L.Matings: total matings with large females.
  - Total.small or S.matings: total matings with small females.
  - Total.matings: total number of matings.
  - Preference or Pref: calculated as Pref = (CL - CS) / (CL + CS), where CL and CS are counts of matings with large and small females, respectively.
  - Genotype: SR or ST, determined by X-linked microsatellite markers.
  - Pref1 / Pref2 / Pref3 etc.: individual mating-level preferences.

- Interpretation and potential analyses
  - Examine how genotype (SR vs ST) relates to overall mate preference and its variation across trials.
  - Assess the influence of eyespan (experiment 2) on preference and its interaction with genotype.
  - Compare outcomes between constrained (experiment 1) and unconstrained (experiment 2) eyespan designs to understand context dependence of mating preferences.

- Metadata and provenance
  - Source study: Finnegan, S. Nitsche, L. Mondani, M. Camus, K. Fowler, A. Pomiankowski (2019); Does meiotic drive alter male mate preference? Behavioural Ecology. DOI: https://doi.org/10.1093/beheco/arz176.
  - Data contact: a.pomiankowski@ucl.ac.uk.
  - Data format: two CSV files containing standardized headers and calculated preference metric.

- Data governance considerations for Data Leaders
  - Ensure metadata clarity: column definitions, units (mm for Eye span and Thorax), and genotype coding.
  - Maintain data provenance and versioning for the two experiments and both CSV files.
  - Facilitate discoverability and re-use by documenting the experimental design, measurement methods, and calculation of Pref.
  - Note potential ambiguities due to partial header descriptions in the provided text; consult the full data dictionary and the original publication for complete column details.