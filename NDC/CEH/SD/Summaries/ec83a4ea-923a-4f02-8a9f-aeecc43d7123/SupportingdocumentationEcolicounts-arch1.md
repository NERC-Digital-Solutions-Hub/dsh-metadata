# Supporting documentation

- This dataset comprises a single CSV file named Ecolidatafaeces.csv, containing 38 columns that describe E. coli counts in pig faeces alongside extensive metadata from the North Wyke farm platform.

- Content and structure
  - Sample metadata
    - Sample number, Sample type (freshly voided vs. floor), Collection method (fresh vs. grab), Sampling date
    - Animal identifiers (Animal 1–4; grouped animals pooled at initial sampling)
    - Farmlet (blue, green, red), Cohort (1 or 2; cohort changes at slaughter)
    - Date medicated, Medication (drug name), Reason for medication
  - Microbiological data
    - E. coli counts at dilutions 10-1 to 10-4 (with and without antibiotics)
    - For each antibiotic condition: Tet (tetracycline), Ceph (cephalexin), Marb (marbofloxacin), Merop (meropenem)
    - Means: E. coli CFU/g wet weight, Mean Log E. coli CFU/g wet weight, E. coli CFU/g dry weight, Mean Log10 E. coli CFU/g dry weight
    - Antibiotic-specific counts include 10-1, 10-2, 10-3 (and corresponding means) for Tet, Ceph; fewer details for Meropenem given in the dataset description
  - Other measurements
    - % DM (gravimetric dry matter)
    - TMC (too many colonies to count), NS (not sampled), ND (no data)
  - Note: Samples are pooled (nine libraries from 30 animals grouped 3, 3, and 4 per farmlet)

- Methods
  - Sample preparation
    - 1 g faecal material into 9 ml sterile Ringers solution; prepare serial 10-fold dilutions
    - Plate 0.1 ml aliquots in duplicate on Membrane Lactose Glucuronide Agar (MLGA)
    - Antibiotics added to MLGA post-autoclaving and before pouring plates
    - Antibiotic concentrations: 16 mg/L tetracycline; 16 mg/L cephalexin; 1.0 mg/L marbofloxacin; 8 mg/L meropenem
    - Incubate plates inverted at 44.5 ± 0.2 °C for 18–24 h
  - Dry matter determination
    - ~50 g faecal material dried at 105 °C until constant weight
    - % dry matter calculated as 100 − ((fresh wt − dry wt) / fresh wt) × 100
  - Data provenance
    - Establishment license XA11784A2; project license P592D2677

- Use and considerations for analysts
  - The dataset enables analysis of how E. coli counts respond to antibiotic exposure (Tet, Ceph, Marb, Merop) across dilutions and weight basis (wet/dry), and how counts vary by farmlet, cohort, and medicated status.
  - Missing values are indicated by NS (not sampled) or ND (no data); pooling and weighting across libraries should be accounted for in analyses.
  - For robust comparisons, consider the difference between wet weight CFU/g and dry weight CFU/g (and their log transformations), as well as potential effects of sampling date, medicated status, and farmlet.

- Potential analytical insights
  - Correlations between antibiotic exposure and E. coli counts at different dilutions
  - Differences in counts across farmlets (blue, green, red) and cohorts
  - Impact of medicated date and medication type on E. coli prevalence
  - Relationship between % DM and observed CFU/g measurements
  - Data cleaning considerations due to NS/ND entries and pooled samples