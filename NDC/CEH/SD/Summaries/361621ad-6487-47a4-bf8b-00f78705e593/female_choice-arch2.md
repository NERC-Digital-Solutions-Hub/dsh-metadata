# These data report the choice of female Drosophila in a basic two-choice test.

## Aim and scope
- Establish a baseline for mate choice within Drosophila species.
- Determine the extent of assortative mating.
- Reveal dominance effects using F1 hybrids.
- Determine mate-choice frequency in backcross progeny.

## Experimental design
- Three tester females per trial choose between D. sechellia and D. simulans males.
- Courting flies observed for four hours.
- Upon first mating, the test chamber is moved to -20°C to freeze the copulating pair.
- Male species identification is done by analyzing male genitalia (distinct between species).
- Trials after four hours: non-mating pairs are excluded from analysis.

## Strains and crosses
- D. simulans strain Tsimbazaza (from Ansirabe, Madagascar) used to generate A2A2B line by five generations of single-female inbreeding.
- Wild-type D. sechellia (from Cousin Island) inbred for five generations to produce D1A1C line.
- F1 females produced by crossing D. sechellia males with D. simulans females.
- Backcross lines:
  - A2A2B/D1A1C
  - A2A2B: progeny from F1 backcross to A2A2B
  - D1A1C: backcross progeny to D1A1C

## Data resources (files)
- female_choice_inbred_lines.csv
- female_choice_wild_type.csv

## Column descriptions

- Inbred_lines file (female_choice_inbred_lines.csv)
  - female: strain and genotype of the female used in the test (e.g., F1, A2A2B/D1A1C, D1A1C)
  - A2A2B_male: number of females that selected an A2A2B male
  - D1A1C_male: number of females that selected a D1A1C male
  - n_mated: total number of matings observed
  - Description: explanation of the female and cross nomenclature (e.g., A2A2B_male, D1A1C_male, F1)

- Wild_type file (female_choice_wild_type.csv)
  - female: species/strain of the female used in the test
  - D_sechellia_13_male: number of females that selected a D. sechellia 13 male
  - D_simulans_Tsimba_male: number of females that selected a D. simulans Tsimba male
  - n_mated: number of females that mated
  - n_tests: total number of tests performed (mated + not mated)

## How to interpret the data
- For each cross or strain, compare the counts choosing one male species over the other to assess mate-choice bias and potential assortative mating.
- Use n_mated relative to n_tests to understand mating success within the four-hour window.
- Analyze F1 results to infer dominance effects in mate-choice preference.

## Applicability for monitoring and data use
- Data provide a standardized, transparent dataset for comparing mate-choice behavior across strains and backcrosses.
- Can be integrated with other datasets to enhance understanding of sexual selection and reproductive isolation.
- Structured in CSV format with clear column definitions to facilitate QA, cleaning, and downstream analysis.
- Data management aligns with practices to store, publish, and enable access to underlying data and methodologies.