# Supporting documentation

## Overview
- Describes a single dataset: Ecolidatafaeces.csv (CSV file with 38 columns).
- Captures faecal E. coli counts and related measurements from animals on the North Wyke farm platform.
- Includes sample type, collection method, sampling date, animal identifiers (up to four per pooled sample), farmlet (blue, green, red), cohort, medicated status, drug administered, and reason.
- Outputs include E. coli counts at multiple dilutions (10-1 to 10-4), mean CFU per gram (wet and dry weight), and corresponding log10 values.
- Antibiotic-supplemented media data for Tet, Ceph, Marb, and Merop are provided (counts and logs for 10-1 to 10-3).
- Additional metrics: % dry matter (%DM), “Too Many Colonies to Count” (TMC), and markers NS (not sampled) and ND (no data).
- Pooling details: nine libraries prepared from 30 animals grouped as 3, 3 & 4 per farmlet.

## Dataset Contents (Ecolidatafaeces.csv)
- Core data groups:
  - Sample metadata: Sample number, Sample type, Collection method (freshly voided vs floor; grab from rectum), Sampling date.
  - Animal identifiers: Animal 1–4 (grouped as a pooled sample).
  - Grouping variables: Farmlet (blue/green/red), Cohort (1 or 2).
  - Medication information: Date Medicated, Medication (drug name), Reason for administration.
  - E. coli counts: E.coli 10-1 to 10-4; Mean E.coli CFU/g wet weight; Mean Log E.coli CFU/g wet; Mean E.coli CFU/g dry weight; Mean Log10 E.coli CFU/dry wt g-1.
  - Antibiotic-supplemented counts: Ecoli Tet 10-1 to 10-3; Mean Tet E.coli wet weight CFU/g; Mean Log Tet; Mean Tet E.coli CFU/g dry weight; Mean Log10 Tet E.coli CFU/dry wt g-1; similarly for Ceph (cephalexin) and Ceph-related metrics; and Marb/Merop data (10-1 for each).
  - % DM: gravimetric dry matter of the faecal matter.
  - Other indicators: TMC (too many colonies to count), NS (not sampled), ND (no data).

## Methods
- Sample processing:
  - 1 g of faecal material transferred to 9 ml sterile Ringers solution; serial 10-fold dilutions prepared.
  - 0.1 ml plated in duplicate on Membrane Lactose Glucuronide Agar (MLGA); plates spread evenly.
  - Antibiotics added to MLGA at specified concentrations after autoclaving and prior to pouring plates:
    - 16 mg/L tetracycline
    - 16 mg/L cephalexin (Ceph)
    - 1.0 mg/L marbofloxacin (Marb)
    - 8 mg/L meropenem (Merop)
  - Incubation: 44.5°C (±0.2°C) for 18–24 hours.
- Moisture/dry matter:
  - Approximately 50 g of faecal material dried in oven at 105°C to constant weight.
  - % Dry Matter calculated as: 100 - (((fresh wt. - Dry wt.) / fresh wt.) × 100).
- Documentation:
  - Establishment licence XA11784A2 and project licence P592D2677 under which the work was conducted.
- Pooling context:
  - Nine libraries prepared from 30 animals, grouped as 3, 3 & 4 per farmlet.

## Data Handling and Quality
- Data are intended to be verified, quality assured, cleaned, and transformed before use.
- Datasets are stored and uploaded to appropriate portals, aligning with monitoring responsibilities.
- Data markers NS and ND indicate not sampled or no data for specific entries.

## Licensing and Compliance
- Compliance licences noted:
  - Establishment licence: XA11784A2
  - Project licence: P592D2677

## Relevance to Environment Monitoring and Policy
- Provides standardized, traceable measurements of faecal E. coli counts and antibiotic-associated growth on farmlets, supporting environmental health and antimicrobial resistance monitoring.
- Enables time-series comparisons and policy performance assessments through consistent data formats and clear methodological documentation.
- Aligns with aims to verify data quality, present clear outputs (tables/graphs), and enable data reuse by others for broader environmental monitoring.

## Notes and Considerations
- The dataset includes outputs both with and without antibiotic exposure, enabling assessment of resistant/effective strains.
- Some entries may be marked NS or ND, reflecting sampling gaps or missing data.