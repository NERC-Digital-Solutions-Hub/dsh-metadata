# Does meiotic drive alter male mate preference?

## Overview
- Two binary-choice experiments with Teleopsis dalmanni males carrying either the XSR meiotic drive chromosome (SR) or the wildtype XST chromosome (ST).
- Experiment 1 constrains focal male eyespan to a narrow range to test genotype effects on mating behavior independent of eyespan.
- Experiment 2 uses unf constrained eyespan drawn from its natural distribution to assess the direct effect of eyespan and its association with genotype on mate preference.
- Data are collected to understand how meiotic drive genotype and physical traits influence male mate preference in a wild-analogous context.

## Datasets
- Two CSV files:
  - Male_preference_experiment_1_data.csv
  - Male_preference_experiment_2_data.csv
- Each row corresponds to a focal male and his mating records.

## Experimental design
- Two binary-choice trials per male: presented with two females (one large, one small).
- Males of two genotypes (SR or ST) mate freely for a short period.
- Design mirrors the sex-ratio and time-frame conditions under which mate preference is expressed in the wild.

## Key variables and column headers
- Male.ID: Unique identifier for each male.
- Date: Date of mating.
- 1st / 2nd / 3rd, etc.: Mating records indicating whether the male mated with the small (S) or large (L) female on that trial.
- Eyespan: Male eyespan (mm) — available in Experiment 2 only.
- Thorax: Male thorax length (mm) — available in Experiment 2 only.
- Total.large or L.Matings: Total matings with a large female.
- Total.small or S.matings: Total matings with a small female.
- Total.matings: Total matings (large + small).
- Preference or Pref: Male preference, calculated as Pref = (CL - CS) / (CL + CS), where CL is times mated with a large female and CS with a small female.
- Genotype: SR or ST, determined by X-linked microsatellite markers.
- Pref1 / Pref2 / Pref3 etc.: Individual mating preference measures for each record.

## How to interpret and analyze the data
- Compare mean Pref between SR and ST genotypes, with Experiment 1 controlling for eyespan and Experiment 2 examining the role of natural eyespan variation.
- In Experiment 2, analyze how Eyespan relates to Pref and interacts with Genotype.
- Consider modeling CL and CS (counts of large vs small matings) directly (e.g., binomial models) as an alternative to using Pref.
- Track dataset provenance and metadata for reproducibility; the data accompany the Behavioural Ecology article (2019) with DOI provided.