# These data report the choice of female Drosophila in a basic two-choice test

## Overview
- Purpose: report female mate-choice in a two-choice setup to establish baseline mating patterns within species, assess assortative mating, reveal F1 dominance effects, and determine mate-choice frequency in backcross progeny.
- Context: behavioral genetics study using Drosophila species to compare mate preferences between D. sechellia and D. simulans.

## Experimental design and data collection
- Subjects: three tester females per test, presented with a choice between D. sechellia and D. simulans males.
- Observation: flies observed for four hours; mating events recorded.
- Post-mating handling: once the first pair mated, the test chamber was frozen at -20°C until the copulating pair could be identified.
- Male species identification: based on distinct male genitalia.
- Inclusion criteria: only pairs that mated contributed to the dataset; non-mated tests are excluded from the figure dataset.

## Biological provenance and cross design
- Strains:
  - D. simulans Tsimbazaza: from Ansirabe, Madagascar; used to generate A2A2B line by five generations of single-female inbreeding.
  - D. sechellia wild-type from Cousin Island: inbred for 5 generations to produce D1A1C line.
- Crosses and definitions:
  - F1: hybrid females from crossing D. sechellia males with D. simulans females.
  - A2A2B, D1A1C: backcross progeny lines used in the inbred-line dataset.
- Data resources: two CSV files encompass all data described below.

## Datasets and variables
- File 1: female_choice_inbred_lines.csv
  - female: strain and genotype of the female used in a preference test (F1 denotes F1 females; A2A2B/D1A1C denotes backcross types).
  - A2A2B_male: number of females that selected the A2A2B male.
  - D1A1C_male: number of females that selected the D1A1C male.
  - n_mated: total number of mated females (with either A2A2B or D1A1C).
  - Description: notes on the combination and counts (e.g., A2A2B/D1A1C; A2A2B = progeny from the F1 backcross to A2A2B; D1A1C = progeny from the F1 backcross to D1A1C).
- File 2: female_choice_wild_type.csv
  - female: species/strain of the female used in the test (e.g., D_sechellia_13).
  - D_sechellia_13_male: number of females selecting a D. sechellia 13 male.
  - D_simulans_Tsimba_male: number of females selecting a D. simulans Tsimba male.
  - n_mated: number of mated females.
  - n_tests: total number of tests performed (mated + not mated).

## Data quality, processing and limitations
- Quality controls: mating confirmed; male species verified by genitalia; non-mated pairs excluded from outcome figures.
- Processing: data describe counts per female/line and backcross lineage; consistent with four-hour observation window.
- Limitations:
  - Potential incomplete capture of user needs and future applicability since some data are restricted to specific crosses and lines.
  - Observational window and laboratory conditions may influence mating rates and generalizability to other contexts.

## Data governance, metadata, and sharing
- Metadata needs:
  - Clear definitions of abbreviations (F1, A2A2B, D1A1C).
  - Cross design, line provenance, and mating criteria.
  - Observation conditions (duration, freezing protocol, genitalia-based identifications).
- Sharing and storage recommendations:
  - Store the two CSV files with stable file naming and version control.
  - Provide a data dictionary and methodological notes alongside the files.
  - Capture lineage information and mating outcomes to support reproducibility and downstream discovery.
- Access considerations:
  - Data are organized to support discovery and reuse by researchers and data stewards; ensure accessible via appropriate data portals with proper licensing and citation guidance.