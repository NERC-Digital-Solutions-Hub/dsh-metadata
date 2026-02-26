# Details of data structure to ' Digestate_HF_and_NW_N2O_v2.csv'

- Purpose and scope
  - Supplement to supporting documentation for data series; describes the data structure of Digestate_HF_and_NW_N2O_v2.csv
  - Dataset from the digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW)
  - Contains 8 columns and 2800 rows of N2O flux data

- Sites and treatments
  - Site: HF and NW
  - Treatment codes: C (zero nitrogen control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP)
  - Blocking factor: Block values 1–5 (randomised block design)
  - Plot: plot numbers; certain plots (1, 19, 25, 31, 47) used for monthly samplings for treatment 150 kg N ha^-1
  - Date: measurement date

- Data fields (columns)
  - N2O_qa1: All N2O flux data for each chamber/plot across the entire experimental period (used to derive cumulative values)
  - N2O_qa2: Cumulative N2O flux data; values with R^2 < 0.6 removed and replaced with zero flux
  - N2O_qa3: Cumulative N2O flux data; values with R^2 < 0.6 removed and all negative N2O flux values replaced with zero
  - Plot size details (harvest area) vary by site and treatment

- Data quality and processing notes
  - R^2 threshold used to flag and remove unreliable fits (0.6) for qa2 and qa3
  - NA denotes Not Assessed

- Experimental design and data collection specifics
  - Plot sizes:
    - HF: 1.2 m × 6.5 m harvest area for nitrogen addition rates; 1.2 m × 14 m for C, D, AD, DNI, ADNI
    - NW: 2 m × 4.5 m harvest area for nitrogen addition rates; 2 m × 9 m for C, D, AD, DNI, ADNI

- Implications for data management (Data Leaders)
  - Clear mapping of sites, treatments, blocks, plots, and measurement dates aids discoverability and reuse
  - QA processing steps (qa2, qa3) require careful documentation of R^2 thresholds and zero-replacement rules
  - Metadata should preserve the distinctions between sites and treatment definitions for cross-site analyses
  - Potential considerations for standardizing data structures across experiments to reduce fragmentation and duplication of effort