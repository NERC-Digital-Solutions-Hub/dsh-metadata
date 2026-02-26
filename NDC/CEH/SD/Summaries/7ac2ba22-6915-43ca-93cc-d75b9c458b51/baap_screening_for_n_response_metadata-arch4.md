# BAAP_Screen_Aberdeen_0N.csv and BAAP_Screen_Aberdeen_100N.csv data description

## Overview
- Datasets describe trait values for 229 rice BAAP cultivars grown under two nitrogen treatments (0% N and 100% N) over six weeks.
- Purpose: identify cultivars with high nitrogen use efficiency (NUE) and explore quantitative trait loci (QTL) and candidate genes for NUE.
- Data linked to a broader BAAP resource with a genome-wide SNP marker database (2 million SNPs).

## Experimental design and data collection
- Germplasm: 229 Bengal and Assam Association Panel (BAAP) cultivars; related to Norton et al. 2018.
- Treatments: 0N (no added nitrogen) and 100N (16.12 g urea per box, representing ~40 kg N ha-1 in a first split).
- Setup: controlled environment room; soil/sand mix; boxes sized 160 cm x 70 cm x 27 cm; 600 kg soil/sand per box.
- Plant layout: 230 genotypes sown in a 23 x 10 grid; two seeds per genotype, thinned to one plant; four replicates per treatment paired as one 0N and one 100N box; replicate 1 of 100N excluded due to liner leak.
- Growth conditions: 28°C day / 25°C night; 12 h light; ~400 μmol m-2 s-1 PAR; humidity > 50%.
- Timeline and measurements: starting from week 2, weekly measurements of plant height and tiller number; weekly Nitrogen Balance Index (NBI) and Chlorophyll Index (ChI) via Dualex; harvest at week 6 with shoot dry weight (g) after drying at 80°C for 48 h.

## Data structure and units
- Traits recorded: Plant height (cm), Tiller number (count), Nitrogen Balance Index (NBI; no unit), Chlorophyll Content (ChI; no unit), Shoot biomass (g; dry weight of above-ground tissue).
- Data organization: provided as two CSV files, one per treatment (0N and 100N), with 11 columns per file including replicate, treatment, BAAP ID, BAAP name, X and Y coordinates, plus trait data.

## Quality control and data cleaning
- Replicate 1 in the 100N treatment was removed from analysis due to a leak affecting environment consistency.
- Initial data entry underwent checks in Minitab to identify unusual observations; corrections were made only where data-entry errors were confirmed.

## Data content and metadata
- File-level information:
  - BAAP_Screen_Aberdeen_0N.csv: raw data for 0N treatment (five traits).
  - BAAP_Screen_Aberdeen_100N.csv: raw data for 100N treatment (five traits).
- Column structure: replicates, treatment indicator, BAAP ID, cultivar name, X and Y coordinates, followed by G-K trait data.
- Descriptive means (summary statistics) included for each trait in each treatment:
  - 0N means: Plant height ~74.1 cm; Tillers ~2.09; NBI ~17.0; ChI ~12.2; Shoot biomass ~0.70 g.
  - 100N means: Plant height ~77.4 cm; Tillers ~2.69; NBI ~34.0; ChI ~26.2; Shoot biomass ~0.96 g.
- Additional context: data structure aligns with a broader BAAP framework and SNP marker data referenced in Norton et al. (2018) for potential integrative analyses.

## Provisions for data use and reuse
- Clear linkage to a wider data ecosystem: 2 million SNP markers for the BAAP panel enable GWAS and integration with phenotypic data to identify NUE-associated loci.
- Data provenance includes collection date (Sept–Oct 2020), location (University of Aberdeen), and principal contributors (Y. Hazzazi, A. Tantray; supervised by A. Price and G. Norton).
- Funding acknowledged from UK GCRF South Asia Nitrogen Hub and supporting fellowships.

## Access and references
- Files to access: BAAP_Screen_Aberdeen_0N.csv and BAAP_Screen_Aberdeen_100N.csv.
- Reference for genetic panel: Norton GJ et al. 2018, Frontiers in Plant Science (BAAP genome-wide association mapping context).