# These data report the choice of female Drosophila in a basic two-choice test

## Overview
- Purpose: Establish mate-choice baselines within species, assess assortative mating, reveal dominance effects via F1 hybrids, and determine mate-choice frequency in backcross progeny.
- Species/strains involved:
  - D. simulans Tsimbazaza (Madagascar) used to generate A2A2B line.
  - Wild-type D. sechellia (Cousin Island) bred to produce D1A1C line.
  - F1: hybrid females from D. sechellia males × D. simulans females.
- Experimental setup: Three tester females choose between D. sechellia and D. simulans males; observed for four hours.
- Outcome handling: When the first mating occurs, the test chamber is frozen at -20°C; male species identified by distinct male genitalia. Non-mating pairs are not included in the final figure.

## Datasets
- female_choice_inbred_lines.csv: records from tester females across inbred lines and backcrosses, capturing the cross type and mating outcomes.
- female_choice_wild_type.csv: records from tester females using wild-type strains, capturing species/strain choices and mating outcomes.

## Data fields (columns)
- female_choice_inbred_lines.csv
  - female: strain and genotype of the female used (e.g., F1 denoting females from the D1A1C × A2A2B cross; A2A2B/D1A1C; A2A2B_male; D1A1C_male)
  - Description: interpretation of the line or cross (e.g., A2A2B_male = number of females that selected the A2A2B male)
  - n_mated: total number of mated females (i.e., those that mated with either A2A2B or D1A1C)
- female_choice_wild_type.csv
  - female: strain of the female tested
  - D_sechellia_13_male: number of females that selected a D. sechellia 13 male
  - D_simulans_Tsimba_male: number of females that selected a D. simulans Tsimba male
  - n_mated: number of females that mated during the test
  - n_tests: total number of tests performed (mated + not mated)

## Experimental lines and crosses
- D. simulans Tsimbazaza: Madagascar strain used to derive inbred lines
- D1A1C: wild-type D. sechellia lineage (Cousin Island) inbred for five generations
- A2A2B: D. simulans-derived line introduced via backcross
- F1: hybrid females from crossing D. sechellia males with D. simulans females
- Cross types captured in the data files include A2A2B, D1A1C, and their backcrosses

## Data provenance and interpretation
- Observations are restricted to mating events; pairs that do not mate are excluded from the figure.
- Data support analyses of baseline mate choice within and between species, assortative mating tendencies, dominance in F1 females, and backcross mating frequencies.

## GIS-relevant applications and visualization ideas
- Georeferencing strains:
  - Link strain origins (Madagascar, Cousin Island) to geographic coordinates for spatial visualization.
- Strain-level maps:
  - Create map layers showing counts of matings or preferences by female genotype (e.g., A2A2B vs D1A1C) or by wild-type strains.
- Spatial comparison of mating outcomes:
  - Visualize geographic clustering of mating preferences if additional locality data are available.
- Data integration:
  - Combine with other datasets to produce choropleth or thematic maps of mate-choice tendencies by strain, cross type, or generation (e.g., F1 vs backcross).

## Quality, notes, and caveats
- Non-mated pairs are not included in the final figures, which affects the interpretation of total testing effort.
- Definitions of column values rely on explicit cross designations (e.g., which male was selected by a given female and how many mated).

## Access
- Data resources consist of:
  - female_choice_inbred_lines.csv
  - female_choice_wild_type.csv