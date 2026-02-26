# These data report the choice of female Drosophila in a basic two-choice test

## Overview
- Objective: establish baseline mate choice within species, assess assortative mating, reveal dominance effects via F1 testing, and determine mate choice frequency in backcross progeny.
- Subjects: female Drosophila choosing between D. sechellia and D. simulans males.
- Observation: four-hour test window; pairs mated are recorded; non-mated pairs are excluded from figures.
- Genetic lines and crosses: use of a D. simulans strain (Tsimbazaza) to create A2A2B line; wild-type D. sechellia (Cousin Island) bred to create D1A1C line; F1 females produced by D. sechellia males × D. simulans females, with backcrosses to A2A2B or D1A1C.

## Data resources and structure
- Data resource comprises two CSV files:
  - female_choice_inbred_lines.csv
  - female_choice_wild_type.csv
- File: female_choice_inbred_lines.csv
  - female: strain and genotype of the female used (F1 denotes hybrids from D1A1C × A2A2B; A2A2B/D1A1C denotes backcross progeny)
  - A2A2B_male, D1A1C_male: counts of females that selected the A2A2B or D1A1C male, respectively
  - n_mated: total number of matings with either a A2A2B or D1A1C male
- File: female_choice_wild_type.csv
  - female: species and strain of the female used
  - D_sechellia_13_male: number of females selecting a D. sechellia 13 male
  - D_simulans_Tsimba_male: number of females selecting a D. simulans Tsimba male
  - n_mated: number of females that mated during the test
  - n_tests: total number of tests performed (mated + not mated)

## Experimental design and data collection
- Setup: three tester females per trial; choice between two male species (D. sechellia vs. D. simulans).
- Procedure: observe courting flies for four hours; upon first mating, move the test chamber to -20°C to freeze the copulating pair; determine male species by distinctive genitalia.
- Post-processing: four-hour results; non-mating pairs excluded from figures.
- Strains used:
  - D. simulans -Tsimbazaza (Ansirabe, Madagascar) used to generate A2A2B line by five generations of single-female inbreeding.
  - Wild-type D. sechellia (Cousin Island) inbred to produce D1A1C line over five generations.
- Key terms:
  - F1: hybrid females from D. sechellia males × D. simulans females.
  - Crosses: A2A2B/D1A1C (F1 backcross to A2A2B); A2A2B/D1A1C (F1 backcross to D1A1C).

## Data provenance and interpretation
- Purpose of columns:
  - "female": identifies the female strain/genotype used in each test.
  - "Description": explains the genotype or cross context (e.g., F1, backcross lines, breeder lines).
  - "X_male": counts of females selecting a given male type (A2A2B or D1A1C or D. sechellia/D. simulans in wild-type data).
  - "n_mated": number of matings observed for the corresponding test group.
  - "n_tests" (wild-type data): total tests performed (including both matings and non-matings).
- Data scope: records outcomes of mate-choice tests and mating occurrences for defined genetic lines and wild-type crosses.

## Data quality, limitations, and governance
- Limitations:
  - Only mated pairs contribute to mate-choice counts in the figures; non-mated results are not counted there.
  - Four-hour observation window may exclude longer-term mate-choice dynamics.
  - Data limited to two Drosophila species and specific lines; may not generalize beyond these contexts.
- Quality notes:
  - Clear documentation of strains, crosses, and coding (F1, backcross designations) supports interpretability and reproducibility.
  - Male species identification relies on morphologic genitalia, which assumes accurate assessment.
- Stewardship implications for data leaders:
  - Metadata provides explicit lineage, cross designations, and mating outcomes; consider linking to raw videos or observations for richer context.
  - The dataset is static; no ongoing updates implied—appropriate for versioned data assets and clear citation.
  - Ensure discoverability by maintaining the two-file dataset with defined column semantics and cross-referenced strain descriptions.