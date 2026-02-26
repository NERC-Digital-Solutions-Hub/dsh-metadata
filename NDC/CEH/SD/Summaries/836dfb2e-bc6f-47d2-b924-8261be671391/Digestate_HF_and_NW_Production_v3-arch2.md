# Digestate_HF_and_NW_Production.csv

- Overview
  - Supplement to supporting documentation for data series; details the data structure for Digestate_HF_and_NW_Production.csv.
  - Data come from a 2017 wheat trial conducted at Henfaes Research Centre (HF) and North Wyke (NW) with digestate and nitrogen treatments.
  - Dataset contains 7 columns and 90 rows, capturing yield-related measurements across multiple treatments and sites.

- Dataset Structure (columns and meanings)
  - Site: HF (Henfaes) or NW (North Wyke).
  - Plot: Experimental plot number.
  - Block: Blocking factor of a randomised block design (1–5).
  - Treatment: Digestate-related treatments
    - C = zero N control
    - D = digestate
    - AD = acidified digestate
    - DNI = digestate with nitrification inhibitor (DMPP)
    - ADNI = acidified digestate with nitrification inhibitor (DMPP)
    - Plus nitrogen add rates: N-75, N-150, N-225, N-300 (kg N ha-1 via NH4NO3)
  - Plant_yield: Whole plant yield at 100% dry matter (tonnes per hectare, t ha-1).
  - Grain_yield: Grain yield at 100% dry matter (t ha-1).
  - TGW: Thousand grain weight at 100% dry matter (grams).
  - All yield data are reported at 100% dry matter; NA indicates not assessed.

- Experimental scope and design
  - Trials conducted at two sites: HF and NW.
  - Plot sizes differ by site and treatment category:
    - HF: 1.2 m x 6.5 m harvest area for nitrogen addition rate treatments.
    - HF: 1.2 m x 14 m harvest area for C, D, AD, DNI, ADNI treatments.
    - NW: 2 m x 4.5 m harvest area for nitrogen addition rate treatments.
    - NW: 2 m x 9 m harvest area for C, D, AD, DNI, ADNI treatments.
  - Experimental design includes a randomised block structure with multiple plots per block.

- Treatments and nitrogen regime details
  - Digestate-based treatments (D, AD, DNI, ADNI) are evaluated against control (C).
  - Nitrogen fertilization levels include N-75, N-150, N-225, N-300 (kg N ha-1) to compare with digestate treatments.

- Purpose and relevance for environmental monitoring
  - Provides standardized yield data to assess environmental health and policy performance related to digestate use and nitrogen management.
  - Facilitates cross-site comparison (HF vs NW) and integration with other environmental datasets.
  - Supports data quality practices by clearly defining data provenance, units, and measurement scope.

- Data provenance and documentation context
  - The dataset is a structured component of a larger supporting documentation package (as referenced by Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).
  - Aims to enable storage, access, and potential combination with other relevant datasets for broader monitoring and analysis.