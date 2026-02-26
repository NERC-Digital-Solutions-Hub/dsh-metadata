# Does meiotic drive alter male mate preference?

## Overview
- Study investigates whether meiotic drive (XSR) alters male mate preference in Teleopsis dalmanni, compared to wildtype XST.
- Data derived from two binary choice experiments designed to mimic natural sex-ratio and timeframes.
- Data are provided in two CSV files: Male_preference_experiment_1_data.csv and Male_preference_experiment_2_data.csv.
- Contact: a.pomiankowski@ucl.ac.uk
- Publication: Finnegan et al., 2019, Behavioural Ecology (DOI: 10.1093/beheco/arz176).

## Experimental design
- Two experiments:
  - Experiment 1: focal male eyespan constrained to a narrow range of trait values to test genotype effects (SR vs ST) on mating behavior independent of eyespan.
  - Experiment 2: focal male eyespan unconstrained, drawn from its natural distribution to assess the direct effect of eyespan and its association with genotype on mate preference.
- Males presented with two females (one large, one small) and allowed to mate during a short period, reflecting wild conditions.

## Data structure and content
- Data files contain records from two experiments.
- Key entities:
  - Male.ID: unique identifier for each male.
  - Date: date of mating.
  - 1st / 2nd / 3rd, etc.: mating events with small (S) or large (L) female.
  - Eyespan: male eyespan (mm) — experiment 2 only.
  - Thorax: thorax length (mm) — experiment 2 only.
  - Total.large or L.Matings: total matings with large females.
  - Total.small or S.matings: total matings with small females.
  - Total.matings: total matings (large + small).
  - Preference or Pref: calculated as Pref = (CL - CS) / (CL + CS), where CL and CS are copulations with large and small females, respectively.
  - Genotype: SR or ST, determined by X-linked microsatellite markers.
  - Pref1 / Pref2 / Pref3 etc.: individual mating-level preferences.
  - Notes on header interpretations: “1st / 2nd / 3rd, etc.” captures mating sequence with S or L; “Eyespan” and “Thorax” relate to experiment 2 measurements.

## Data standards and governance considerations
- Metadata needs:
  - Clear definition of genotype labeling (SR vs ST) and how it relates to XSR drive.
  - Explicit description of experimental design differences between Experiment 1 and Experiment 2 (eyespan constraint vs natural distribution).
  - Units for all measurements (Eyespan and Thorax in millimeters).
  - Explanation of how Preference is computed, including how CL and CS are counted.
  - Description of the two female size categories (large vs small) and mating windows.
- Provenance and lineage:
  - Linkings between male IDs and mating sequences across experiments.
  - Documentation of data processing steps (e.g., calculation of Pref, handling of multiple matings).
- Access and reuse:
  - Data available as CSV files; author contact provided for data-related inquiries.
  - Consider licensing, versioning, and citation requirements when sharing or reusing the data.
- Data quality checks to perform:
  - Validate consistency between Total.matings and the sum of Total.large and Total.small.
  - Verify Pref values are within the expected range [-1, 1] and correspond to CL and CS counts.
  - Check that Eyespan and Thorax data (Experiment 2) align with individual records where available.

## Practical use and interpretation
- Enables analyses of:
  - Whether SR (meiotic drive) vs ST genotype influences male mate preference.
  - How restricting eyespan (Experiment 1) vs natural eyespan variation (Experiment 2) modulates mate choice.
  - Relationship between physical trait (eyespan) and genotype with mating outcomes.
- Relevant to researchers studying sexual selection, meiotic drive, and the interaction between genotype, phenotype, and mate choice.

## Potential considerations and caveats
- Incomplete text available for some headers in the description; ensure full dataset documentation is consulted for any additional fields or nuances.
- Results depend on controlled experimental conditions; extrapolation to natural populations should consider ecological and demographic factors not captured in the experiments.
- Ensure careful alignment of the two experiments when performing meta-analyses, given their differing manipulation of eyespan.