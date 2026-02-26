# These data report the choice of female Drosophila in a basic two-choice test.

## Overview
- Investigates female mate choice between D. sechellia and D. simulans.
- Aims: establish a baseline for mate choice within species, quantify assortative mating, reveal dominance effects via F1s, and determine mate-choice frequency in backcross progeny.
- Experimental setup observes mating outcomes over four hours; only mated pairs contribute to results.

## Experimental design
- Three tester females are given a choice between D. sechellia and D. simulans males.
- After the first mating, the test chamber is frozen at -20°C to preserve the pair.
- Mating status is determined by inspecting male genitalia, which differ between the species.
- Non-mated pairs are excluded from the reported figures.

## Strains and crosses
- D. simulans strain Tsimbazaza (from Ansirabe, Madagascar) used to generate the A2A2B line by five generations of single-female inbreeding.
- Wild-type D. sechellia strain (Cousin Island) inbred for five generations to produce the D1A1C line.
- F1: hybrid females produced by crossing D. sechellia males with D. simulans females.
- F1 backcrosses are described as A2A2B/D1A1C and its components (A2A2B_male and D1A1C_male refer to the number of test females that selected that male type).

## Data resources
- two files:
  - female_choice_inbred_lines.csv
  - female_choice_wild_type.csv

## Data columns explained

- Inbred lines data (female_choice_inbred_lines.csv)
  - female: The strain/genotype of the female used in a preference test (includes F1 females from crossing D1A1C x A2A2B; A2A2B/D1A1C; D1A1C; and A2A2B lines).
  - A2A2B_male: The number of females that selected an A2A2B male.
  - D1A1C_male: The number of females that selected a D1A1C male.
  - n_mated: Total number of females that mated with either an A2A2B or a D1A1C male.
  - (Note: The description for some fields is truncated in the source; the counts reflect mating outcomes per female line.)

- Wild-type data (female_choice_wild_type.csv)
  - female: The species/strain of the female used (e.g., D_sechellia_13_male, D_simulans_Tsimba_male, etc.).
  - D_sechellia_13_male: Number of females that selected a D. sechellia 13 male.
  - D_simulans_Tsimba_male: Number of females that selected a D. simulans Tsimba male.
  - n_mated: Number of females that mated during the test.
  - n_tests: Total number of tests performed (mated + not mated).

## How to use the data
- Compute mate-choice preferring indices by comparing counts of matings with each male type.
- Compare inbred-line crosses to wild-type results to assess effects of genotype and lineage on assortative mating.
- Analyze dominance effects by examining F1 and backcross compositions.
- Use n_mated and n_tests to assess mating rates and potential sampling variability.

## Key considerations and limitations
- Only mating pairs are included in the reported figures; non-mated pairs are excluded from counts.
- The four-hour observation window and the freezing step are specific to this experimental protocol.
- Data interpretation depends on correct identification of male species via genitalia post-macth.