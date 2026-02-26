# Does meiotic drive alter male mate preference?

## Overview
- Describes two experiments investigating whether X-linked meiotic drive (SR) vs. wildtype (ST) influences male mate preference in Teleopsis dalmanni.
- Two binary-choice trials where focal males choose between two females differing in size (large vs. small) under conditions designed to reflect wild-type mating contexts.
- Data are released as two CSV files corresponding to Experiment 1 and Experiment 2, with user guidance on column headers and derived metrics.

## Datasets and file contents
- Files:
  - Male_preference_experiment_1_data.csv
  - Male_preference_experiment_2_data.csv
- Each file records per-male mating data across multiple matings with large (L) and small (S) females.
- Key measurements include:
  - Male identifiers, mating dates, and the sequence of matings (1st, 2nd, 3rd, etc.).
  - Eyespan and thorax measurements (experiment 2 only).
  - Totals: number of matings with large females (L.matings), small females (S.matings), and overall matings.
  - Genotype: SR or ST, determined by X-linked microsatellite markers.
  - Preference index: Pref, calculated as (CL - CS) / (CL + CS), where CL = matings with large females and CS = matings with small females.
  - Pref1, Pref2, Pref3, etc.: per-mating preference values.
  - Additional per-mating records (e.g., 1st/2nd/3rd mating) describing which female size was chosen.

## Experimental design
- Experiment 1: Focal male eyespan constrained to a narrow range of trait values. Tests whether genotype (SR vs. ST) affects mating behavior independent of eyespan.
- Experiment 2: Focal male eyespan unconstrained and drawn from its natural distribution to assess direct effects of eyespan and its association with genotype on mate preference.
- Both experiments use two female types (large vs. small) and short mating windows intended to mimic natural sex-ratio and time-frame conditions.

## Variables and data structure
- Male.ID: Unique male identifier.
- Date: Mating date.
- 1st / 2nd / 3rd, etc.: Records of mating order and which female size was chosen.
- Eyespan: Male eyespan in millimeters (experiment 2 only).
- Thorax: Male thorax length in millimeters (experiment 2 only).
- Total.large or L.Matings: Total matings with large females.
- Total.small or S.matings: Total matings with small females.
- Total.matings: Total matings (large + small).
- Preference or Pref: Overall mate preference index for the male.
- Genotype: SR or ST.
- Pref1 / Pref2 / Pref3, etc.: Individual mating-level preference values.

## Calculations and interpretation
- Preference index (Pref) is a normalized measure of bias toward large vs. small females across matings.
- Per-mating preferences (Pref1, Pref2, ...) provide detail on choice dynamics within each male’s sequence of matings.
- Genotype-context: Allows comparison of mate preference across SR vs. ST males, and assessment of whether eyespan or other morphological factors modulate preference (especially in Experiment 2).

## Data quality, limitations, and notes for reuse
- Eyespan and thorax measurements are only available for Experiment 2; Experiment 1 lacks these morphometrics.
- Genotype is inferred from X-linked microsatellite markers; ensure provenance and marker details are consulted if reusing for genetic analyses.
- The dataset includes per-mating records alongside aggregated totals, enabling both granular and summary analyses.
- Source information: data from two experiments described in the 2019 Behavoural Ecology article by Finnegan et al.; DOI provided for reference; contact email available for correspondence.

## Potential data products and visualization ideas for GIS-like workflows
- Create per-male profiles combining genotype, morphological data (eyespan, thorax), and preference metrics to produce interactive dashboards.
- Build heatmaps or choropleth-like visuals (where applicable metadata exists) showing distribution of preference across genotypes and, in Experiment 2, across eyespan ranges.
- Time-series style panels showing how mating sequence (Pref1, Pref2, Pref3, …) evolves within individuals.
- Spatial-analogous mapping concepts could be explored if locations or population metadata are appended, enabling visualization of genotype-preference patterns across sampling sites or populations.
- Data provenance links to the original study and DOI, enabling researchers to connect behavioral metrics with theoretical models of meiotic drive and mating preferences.