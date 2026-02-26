# Details of data structure to ' Digestate_HF_and_NW_N2O_cum.csv '

- Overview
  - Supplement to supporting documentation for data series; dataset from digestate wheat trial 2017 conducted at Henfaes Research Center (HF) and North Wyke (NW).
  - 40 rows capturing N2O flux data across two sites and multiple digestate-related treatments.
  - Treatments: C (control, zero N), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
  - Blocking factor: 1–5; plots used as the basis for yield measurements, with some plots reserved for monthly samplings at 150 kg N ha-1.

- Dataset structure and fields
  - Column headers (as described): Site, Treatment, Block, Plot, Date, N2O_qa1, N2O_qa2, N2O_qa3.
  - Site: HF (Henfaes) and NW (North Wyke).
  - Treatment: C, D, AD, DNI, ADNI.
  - Block: 1–5, representing the randomized block design.
  - Plot: Plot numbers from which yield measurements were derived; note that plots 1, 19, 25, 31, and 47 were used for monthly samplings for the 150 kg N ha-1 treatment.
  - Date: date when each measurement was taken.
  - N2O_qa1: All N2O flux data for each chamber/plot across the experimental period used to derive cumulative values.
  - N2O_qa2: Cumulative N2O flux data where data fits with R^2 < 0.6 were removed and replaced with zero flux.
  - N2O_qa3: Cumulative N2O flux data where data fits with R^2 < 0.6 were removed and all negative Flux_N2O values were replaced with zero.

- Data quality and processing notes
  - R^2 threshold for qa2 and qa3 is described as 0.6; this value is noted as arbitrary and adjustable for both QA fields.
  - Data cleaning approach ensures removal of poorly fitting fits and elimination of negative flux values to produce robust cumulative metrics.

- Experimental design and plot specifications
  - Plot sizes and harvest areas differ by site:
    - HF: 1.2 m × 6.5 m (harvest area) for nitrogen addition rate experiments; 1.2 m × 14 m for other treatments.
    - NW: 2 m × 4.5 m (harvest area) for nitrogen addition rate experiments; 2 m × 9 m for other treatments.

- Context and provenance
  - The dataset is part of a larger documentation suite; details reference additional supporting documentation (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf) and data series described therein.

- Purpose and use
  - Designed to enable monitoring of environmental conditions (N2O flux) across treatments and sites, supporting assessment of environmental health and policy-relevant performance over time.
  - Emphasizes standardized data structure, metadata clarity, and reproducible QA procedures to facilitate analysis and data sharing.