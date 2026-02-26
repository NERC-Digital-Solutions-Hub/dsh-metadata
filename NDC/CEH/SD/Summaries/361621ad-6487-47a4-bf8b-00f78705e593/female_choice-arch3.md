# These data report the choice of female Drosophila in a basic two-choice test

- Goals of the experiments:
  - Establish a baseline for mate choice within species
  - Determine the extent of assortative mating
  - Reveal dominance effects by testing F1 individuals
  - Determine the frequency of mate choice in backcross progeny

- Experimental design and procedure:
  - Three tester females choose between D. sechellia and D. simulans males
  - Courting flies observed for four hours
  - Upon the first mating, the test chamber is moved to -20°C to freeze the copulating pair
  - Male species determined by inspecting distinct male genitalia
  - Pairs that did not mate are excluded from figures

- Subjects and strains:
  - D. simulans strain Tsimbazaza ( Madagascar) used to generate the A2A2B line by five generations of single-female inbreeding
  - Wild-type D. sechellia from Cousin Island inbred for five generations to produce the D1A1C line
  - F1 females: hybrids from D. sechellia males × D. simulans females

- Data resources (files):
  - female_choice_inbred_lines.csv
  - female_choice_wild_type.csv

- Data structure and key variables:
  - Inbred lines dataset (female_choice_inbred_lines.csv):
    - female: strain/genotype of the female (F1 denotes hybrids from D1A1C × A2A2B)
    - A2A2B_male: number of females that selected the A2A2B male
    - D1A1C_male: number of females that selected the D1A1C male
    - n_mated: total number of females that mated with either male
  - Wild-type dataset (female_choice_wild_type.csv):
    - female: species/strain of the female
    - D_sechellia_13_male: number of females selecting a D. sechellia 13 male
    - D_simulans_Tsimba_male: number of females selecting a D. simulans Tsimba male
    - n_mated: number of matings
    - n_tests: total tests performed (mated + not mated)

- Data collection and processing notes:
  - Mate choice is determined by observed mating events within a four-hour window
  - Male identification is based on distinct genitalia
  - Data include both inbred-line crosses and wild-type comparisons, enabling assessments of genetic background effects on mate choice

- Applicability and considerations for monitoring and governance:
  - Demonstrates a structured approach to capturing behavioral choice data with clear metadata and variable definitions
  - Highlights importance of explicit criteria for inclusion (mated pairs only) and documentation of experimental conditions (freeze timing, observation window)
  - Illustrates data organization that supports reproducibility, transparency, and potential integration into larger behavioral monitoring frameworks
  - Points to practical considerations for data sharing and standardization (clear column descriptions, linkage between experimental design and data) relevant to monitoring initiatives in environmental health and policy evaluation