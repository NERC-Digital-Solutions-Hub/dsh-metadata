# Does meiotic drive alter male mate preference?

## Overview
- Two experiments tested differences in male mate preference in Teleopsis dalmanni carrying either a XSR meiotic drive chromosome or a wildtype XST chromosome.
- Binary choice trials: each focal male was presented with two females (one large, one small) and allowed to mate for a short period, designed to reflect wild-sex ratio and timing.
- Data are provided as two CSV files corresponding to Experiment 1 and Experiment 2, capturing detailed mating records and derived preference metrics.

## Data Files
- Male_preference_experiment_1_data.csv
- Male_preference_experiment_2_data.csv

## Experimental Design
- Experiment 1: Eyespan of focal males constrained to a narrow range of trait values to test genotype differences (SR vs ST) in mating behavior independent of eyespan.
- Experiment 2: Eyespan unconstrained and drawn from its natural distribution to assess the direct effect of eyespan and its association with male genotype on mate preference.

## Variables and Data Columns
- Male.ID: Unique identifier for each male.
- Date: Date on which the male mated.
- 1st / 2nd / 3rd, etc.: Record of mating with the small (S) or large (L) female on each successive mating.
- Eyespan: Male eyespan (mm) (experiment 2 only).
- Thorax: Male thorax length (mm) (experiment 2 only).
- Total.large or L.Matings: Total matings with a large female.
- Total.small or S.matings: Total matings with a small female.
- Total.matings: Total matings overall.
- Preference or Pref: Male preference calculated as Pref = (CL - CS) / (CL + CS), where CL = copulations with large females and CS = copulations with small females.
- Genotype: Male genotype (SR or ST) defined by X-linked microsatellite markers.
- Pref1 / Pref2 / Pref3 etc.: Individual mating-level preferences (per mating event).

## Purpose and Usage
- Provides standardized, exportable data to analyze how genotype (SR vs ST) and, in Experiment 2, eyespan, influence male mate preference.
- Derived metric (Pref) enables comparison across individuals and trials.
- Data can be used for reproducible analyses, including aggregation by genotype, eyespan category, or mating sequence.

## Data Provenance and Contact
- Original authors: S. Finnegan, L. Nitsche, M. Mondani, M. F. Camus, K. Fowler, A. Pomiankowski (2019).
- Publication: Does meiotic drive alter male mate preference? Behavioural Ecology. https://doi.org/10.1093/beheco/arz176
- Corresponding author: a.pomiankowski@ucl.ac.uk

## Relevance to Environmental Monitoring Analysts
- Demonstrates rigorous data collection and metadata definition for behavioral experiments, with clear variable definitions and derived metrics.
- Highlights standardization (consistent trial design, identical outcome measures) and data quality considerations (genotype verification, trial timing).
- Emphasizes data transparency and accessibility (two clearly described datasets) to enable reuse, replication, and integration with other datasets to increase value beyond single studies.
- Illustrates challenges parallel to environmental monitoring data: linking underlying data (individual mating events) to final outputs (overall preference scores) and enabling data sharing for broader scrutiny and policy-relevant insights.