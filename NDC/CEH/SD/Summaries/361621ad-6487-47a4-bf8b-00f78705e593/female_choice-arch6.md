These data report the choice of female Drosophila in a basic two-choice test. The goals of these experiments were to, 1) establish a baseline for mate choice within species, 2) determine the extent of assortative mating, 3) reveal dominance effects by testing F1 individuals, and 4) determine the frequency of mate choice in backcross progeny.

## Overview of the study
- Objective: quantify female mate choice when presented with two male partners (D. sechellia vs. D. simulans).
- Experimental setup: three tester females per trial observed for four hours as they could mate with one of two male types.
- Outcome determination: if a mating occurred, the test chamber was frozen at -20°C to preserve the pair and identify the male species by distinct genitalia; non-mated pairs are not included in the results.

## Experimental design and subjects
- Species and strains:
  - D. simulans -Tsimbazaza strain (Madagascar) used to generate A2A2B line.
  - Wild-type D. sechellia (Cousin Island) used to generate D1A1C line.
- Crosses and definitions:
  - F1 females are hybrids from D. sechellia males x D. simulans females.
  - Backcross progeny involve crossing F1 females back to parental lines, producing lineage designations such as A2A2B/D1A1C; A2A2B males; D1A1C males.
- Data collection window: four hours per test, with mating outcomes recorded.

## Data resources (files and what they contain)
- female_choice_inbred_lines.csv
  - female: strain/genotype of the female used in the test (e.g., inbred lines; F1 notation such as D1A1C or A2A2B, and combined line designations like A2A2B/D1A1C).
  - A2A2B_male: number of females that selected an A2A2B male.
  - D1A1C_male: number of females that selected a D1A1C male.
  - n_mated: total number of matings observed (across both male types).
- female_choice_wild_type.csv
  - female: describes the wild-type female tested (e.g., D_sechellia_13).
  - D_sechellia_13_male: number of females that selected a D. sechellia 13 male.
  - D_simulans_Tsimba_male: number of females that selected a D. simulans Tsimba male.
  - n_mated: number of matings observed.
  - n_tests: total number of tests performed (mated plus not mated).

## Key use and interpretation
- The data enable estimation of:
  - Baseline mate-choice preferences within and between species/strains.
  - Strength and direction of assortative mating.
  - Dominance effects as revealed by F1 females in backcross analyses.
  - Frequency of mate choice in backcross progeny across different genotypes.
- Practical notes:
  - Only mating events contribute to the data; non-mating tests are not included in the mating counts.
  - Male species identity is confirmed post-matrimony via morphological traits (genitalia).