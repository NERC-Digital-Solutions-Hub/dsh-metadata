# Does meiotic drive alter male mate preference?

## Overview
- Two experiments tested whether male mate preference differs between Teleopsis dalmanni males carrying an XSR meiotic drive chromosome (SR) and those with the wildtype XST (ST).
- Experimental design used binary choice trials where focal males chose between a large and a small female, conducted to mirror sex-ratio and time-frame conditions observed in the wild.
- Experiment 1 constrained focal male eyespan to a narrow trait range to isolate genotype effects; Experiment 2 allowed eyespan to vary according to its natural distribution to assess direct effects of eyespan and genotype on mate preference.
- Data are provided as two CSV files containing per-male and per-mating records.

## Datasets and experiments
- Data files:
  - Male_preference_experiment_1_data.csv
  - Male_preference_experiment_2_data.csv
- Experimental setup:
  - Males of two genotypes (SR or ST) are presented with two females (one large, one small) and may mate across multiple opportunities.
  - Each mating is recorded with sequence (1st, 2nd, 3rd, etc.) indicating whether a mating occurred with the large or small female.
- Context:
  - The experiments are designed to mimic natural mating contexts to relate genotype and trait variation to mating decisions.

## Variables and metadata
- Core identifiers and timing:
  - Male.ID: unique male identifier
  - Date: date of each mating
- Mating records:
  - 1st / 2nd / 3rd, etc.: indicates which mating event (with large or small female)
  - Total.large or L.Matings: total matings with a large female
  - Total.small or S.matings: total matings with a small female
  - Total.matings: total matings across all events
- Phenotypic and trait measures (experiment 2 only):
  - Eyespan: distance between outer tips of eyes (mm)
  - Thorax: thorax length (mm)
- Preference measurement:
  - Pref: calculated as (CL - CS) / (CL + CS), where CL and CS are copulations with large and small females, respectively
  - Pref1 / Pref2 / Pref3, etc.: per-mating preference values
- Genotype and data provenance:
  - Genotype: SR or ST determined by X-linked microsatellite markers
- Data are organized to capture per-male mating sequences and aggregated outcomes, with explicit units (mm for Eyespan and Thorax) and clearly defined derived metrics (Preference).

## Data structure and measurement details
- Two experiments provide complementary views:
  - Experiment 1: constrained eyespan to isolate genotype effects on mating behavior
  - Experiment 2: unconstrained eyespan to assess direct influence of eyespan and genotype on mate preference
- Measurements are recorded at the level of individual matings and aggregated totals, enabling calculation of preference and comparison across genotypes and experimental conditions.

## Provenance and accessibility
- Publication context:
  - Data derived from two experiments reported in Does meiotic drive alter male mate preference? Behavioural Ecology (2019) by Finnegan, Nitsche, Mondani, Camus, Fowler, and Pomiankowski
- Data sharing and metadata:
  - The dataset includes a detailed description of column headers, units, and definitions, facilitating reuse and reproducibility
  - Genotype determination method is stated (X-linked microsatellite markers)

## Relevance to monitoring framework practices
- Demonstrates the value of:
  - Clear data dictionaries and variable definitions (e.g., Pref, CL, CS)
  - Derivation of metric(s) that directly reflect the outcome of interest (mate preference)
  - Recording both raw observations (mating events) and aggregated summaries (totals, preference)
  - Including relevant covariates and traits (eyespan, thorax) to disentangle direct and indirect effects
  - Linking data to provenance (authors, DOI) and measurement methods (genotyping approach)

## Considerations for data governance
- Metadata richness supports quality assurance and data governance:
  - Explicit units and measurement definitions aid validation and transformation
  - Genotype information and mating sequence data enable transparent auditing and reuse
- Potential governance considerations aligned with monitoring practices:
  - Ensuring dataset integrity across multiple experiments with consistent variable definitions
  - Maintaining openness of data and documentation to facilitate stakeholder scrutiny and reproducibility
  - Documenting data processing steps for derived metrics (e.g., Pref) to support traceability