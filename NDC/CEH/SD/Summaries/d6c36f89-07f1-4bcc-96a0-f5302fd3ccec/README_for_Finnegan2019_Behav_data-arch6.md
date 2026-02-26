# Does meiotic drive alter male mate preference?

## Overview
- Datasets from two experiments investigating differences in male mate preference in Teleopsis dalmanni carrying a XSR meiotic drive chromosome versus wildtype XST.
- Two binary choice trials per male to measure strength of mate preference, with two females (one large, one small) presented and mating allowed for a short period.
- Experiments mirror sex-ratio and time-frame observed in the wild.
- Data are provided in two CSV files corresponding to Experiment 1 and Experiment 2.

## Datasets
- Male_preference_experiment_1_data.csv
- Male_preference_experiment_2_data.csv

## Experimental design
- Experiment 1: Focal male eyespan constrained to a narrow range to test genotype differences (SR vs ST) in mating behavior independent of eyespan.
- Experiment 2: Focal male eyespan unconstrained and drawn from its natural distribution to assess the direct effect of eyespan and its association with male genotype on mate preference.

## Data dictionary / Column headers (key fields)
- Male.ID: Unique identifier for each male.
- Date: Date of mating.
- 1st / 2nd / 3rd, etc.: Mating records indicating whether the mate was the small (S) or large (L) female on that trial.
- Eyespan: Male eyespan in millimeters (experiment 2 only).
- Thorax: Male thorax length in millimeters (experiment 2 only).
- Total.large or L.Matings: Total matings with a large female.
- Total.small or S.matings: Total matings with a small female.
- Total.matings: Total matings (large and small combined).
- Preference or Pref: Male preference calculated as Pref = (CL - CS) / (CL + CS), where CL is the number of matings with large females and CS with small females.
- Genotype: Male genotype (SR or ST), determined by X-linked microsatellite markers.
- Pref1 / Pref2 / Pref3 etc.: Individual mating records (per-mating preference data).

## Key variables and calculations
- Preference (Pref): A normalized measure of bias toward large versus small females, ranging from -1 to 1.
- Genotype association: Compare preference and mating patterns between SR and ST genotypes.
- Experiment-specific measures: Experiment 1 emphasizes genotype effect independent of eyespan; Experiment 2 incorporates eyespan as a potential covariate.

## Considerations for data use
- The data facilitate analyses of how meiotic drive (SR) may influence male mate choice, and how eye morphology (eyespan) interacts with genotype to shape preferences.
- Useful for reproducibility of the original analyses, re-computation of Pref, and integration with per-mating records (Pref1, Pref2, etc.) for deeper behavioral insights.
- Enables cross-experiment comparison by genotype and by eye morphology (where available).