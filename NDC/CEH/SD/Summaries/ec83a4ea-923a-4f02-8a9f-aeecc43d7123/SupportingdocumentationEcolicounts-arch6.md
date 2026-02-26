# Supporting documentation

- This document describes a dataset contained in a single CSV file named Ecolidatafaeces.csv.
- It documents 38 columns that include sample metadata, animal identifiers, farmlet and cohort information, medicated status, and detailed microbiological measurements.
- The dataset records E. coli counts at multiple dilutions, both with and without antibiotics, and provides corresponding biomass-weighted metrics (wet and dry weight) and dry matter content.

## Dataset content and structure

- File: Ecolidatafaeces.csv
- Columns cover:
  - Sample information: Sample number, Sample type (freshly voided vs grab from rectum), Sampling date, Date Medicated.
  - Animal and grouping data: Animal 1–4 (identified by ear tag), Farmlet (blue, green or red), Cohort 1 or 2 (cohort changed at slaughter).
  - Medication details: Medication (drug name), Reason why drug administered.
  - E. coli counts without antibiotics: E. coli counts at dilutions 10^-1 to 10^-4, Mean E. coli CFU/g wet weight, Mean Log E. coli CFU/g wet weight, Mean E. coli CFU/g dry weight, Mean Log10 E. coli CFU/g dry weight.
  - E. coli counts with antibiotics: counts and means for Tet (tetracycline), Ceph (cephalexin), Marb (marbofloxacin), Merop (meropenem) across dilutions; corresponding Mean CFU/g wet weight, Mean Log CFU/g wet weight, Mean CFU/g dry weight, Mean Log10 CFU/g dry weight.
  - Dry matter and related metrics: % DM (gravimetric dry matter of faecal matter).
  - Quality/Notes: TMC (too many colonies to count), NS (not sampled), ND (no data).

## Pooling and sampling details

- Sampling approach: 1 g of faecal material collected and processed through serial dilutions; some samples pooled at the initial sampling.
- Pooling structure: nine libraries prepared from 30 animals, grouped 3, 3, and 4 per farmlet.
- Farmlets and platform: animals originate from North Wyke farm platform; farmlets identified as blue, green, or red.

## Laboratory methods

- Sample preparation: 1 g faecal material transferred to 9 ml sterile Ringers solution; serial 10-fold dilutions prepared.
- Plating: 0.1 ml of each dilution plated in duplicate on Membrane Lactose Glucuronide Agar (MLGA).
- Antibiotics: added to MLGA after autoclaving and before plating at specified concentrations:
  - Tetracycline: 16 mg/L
  - Cephalexin: 16 mg/L
  - Marbofloxacin: 1.0 mg/L
  - Meropenem: 8 mg/L
- Incubation: plates incubated inverted at 44.5 C (±0.2 C) for 18–24 hours.
- Moisture content: gravimetric determination by drying approximately 50 g of faecal matter at 105 C until constant weight.
- Dry matter calculation: % DM = 100 - (((fresh wt - dry wt) / fresh wt) × 100).

## Data interpretation and outputs

- E. coli measurements are reported as colony-forming units (CFU) per gram of faeces, in both wet weight and dry weight contexts.
- Data include means and log10-transformed values for easier comparison and statistical analysis.
- Some fields indicate data quality or availability via codes:
  - TMC: too many colonies to count
  - NS: not sampled
  - ND: no data

## Licensing and compliance

- Establishment licence: XA11784A2
- Project licence: P592D2677