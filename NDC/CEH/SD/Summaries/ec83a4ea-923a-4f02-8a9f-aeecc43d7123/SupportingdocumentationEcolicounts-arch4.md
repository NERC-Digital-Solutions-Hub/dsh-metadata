# Supporting documentation

## Overview
- Dataset consists of a single CSV file named Ecolidatafaeces.csv.
- Contains 38 columns describing fecal sample data, animal identifiers, farmlets, cohorts, medicated records, and Escherichia coli counts with and without antibiotics.
- Data intended for analysis of E. coli counts in pig feces, including antibiotic resistance testing across multiple dilutions and weight-based CFU calculations.

## Dataset Details
- File: Ecolidatafaeces.csv
- Columns (left to right) include:
  - Sample number; Sample type; Collection method (freshly voided or from floor; grab from rectum); Sampling date.
  - Animal 1–4 identifiers (ear tag numbers); Grouping of animals (Animals 1 to 4; pools 30 animals into nine libraries: groups of 3, 3, and 4 per farmlet).
  - Farmlet (blue, green, or red) and Cohort 1 or 2 (cohort changes at slaughter).
  - Date Medicated; Medication (drug name); Reason for drug administration.
  - E. coli counts at dilutions 10-1, 10-2, 10-3, 10-4; Mean E. coli CFU/g wet weight (CFU/g wet wt) and Mean Log10 E. coli CFU/g wet weight.
  - Mean E. coli CFU/g dry weight; Mean Log10 E. coli CFU/dry wt g-1.
  - Antibiotic-assisted counts: E. coli with Tet (tetracycline), Ceph (cephalexin), Marb (marbofloxacin), Merop (meropenem) at dilutions 10-1 to 10-3; Mean Tet E. coli CFU/g wet weight; Mean Log Tet E. coli CFU/g wet wt; Mean Tet E. coli CFU/g dry wt; Mean Log10 Tet E. coli CFU/dry wt g-1; similarly for Ceph and Merob/Merop across wet and dry weights.
  - % DM (gravimetric dry matter of fecal matter); TMC (too many colonies to count); NS (not sampled); ND (no data).

## Sampling and Laboratory Methods
- Sampling protocol:
  - One gram of fecal material transferred to 9 ml sterile Ringers solution; prepared through 10-fold serial dilutions.
  - Aliquot (0.1 ml) plated in duplicate on Membrane Lactose Glucuronide Agar (MLGA) and spread evenly.
  - Antibiotics added to MLGA at specific concentrations after autoclaving and before pouring plates (16 mg/L tetracycline; 16 mg/L cephalexin; 1.0 mg/L marbofloxacin; 8 mg/L meropenem).
  - Plates dried, inverted, and incubated at 44.5°C (±0.2°C) for 18–24 hours.
- Moisture/dry matter:
  - Approximately 50 g of fecal material weighed and dried at 105°C to constant weight.
  - % dry matter calculated as: 100 - (((fresh wt. - dry wt.) / fresh wt.) * 100).

## Study Context and Provenance
- Animals tracked by unique ear tags; farmlets identified as blue, green, or red on the North Wyke farm platform.
- Samples pooled at initial sampling to prepare libraries; nine libraries derived from 30 animals (grouped 3, 3, and 4 per farmlet).
- Cohorts changed at slaughter; medicated dates and drug reasons recorded.
- Data explicitly documents both total E. coli counts and counts under antibiotic pressure, enabling resistance analysis.

## Licensing and Compliance
- Establishment licence: XA11784A2.
- Project licence: P592D2677.