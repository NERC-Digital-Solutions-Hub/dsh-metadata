# Supporting documentation

## Dataset overview
- Dataset consists of a single CSV file named Ecolidatafaeces.csv.
- Contains 38 columns recorded left to right, detailing sample metadata, animal identifiers, farmlet, cohort, medicated information, and Escherichia coli counts and related metrics.
- Columns cover both standard E. coli counts in unamplified media and counts on media containing antibiotics (tetracycline, cephalexin, marbofloxacin, meropenem).

## Data structure and variables
- Sample-level information:
  - Sample number, Sample type (freshly voided, floor void, grab from rectum), Collection method, Sampling date.
  - Animal 1–4 identifiers (ear tag numbers); animals pooled into groups (nine libraries from 30 animals; grouped 3, 3 & 4 per farmlet).
  - Farmlet identifier (blue, green, red) and Cohort (1 or 2; cohort changes at slaughter).
  - Date Medicated, Medication (drug name), Reason for administration.
- E. coli counts and derived metrics:
  - E. coli counts at dilutions 10^-1, 10^-2, 10^-3, 10^-4 (per sample) and the corresponding Mean E. coli CFU/g wet weight.
  - Mean Log10 E. coli CFU/g wet weight (log-transformed value).
  - Mean E. coli CFU/g dry weight and Mean Log10 E. coli CFU/g dry weight (derived by applying % dry matter).
- Antibiotic-supplemented media:
  - For Tet (tetracycline), Ceph (cephalexin), Marb (marbofloxacin), Merop (meropenem): counts at 10^-1, 10^-2, 10^-3 and respective Means for wet weight CFU/g and wet weight log10 CFU/g; and CFU/g dry weight with log10 CFU/g-1.
- Additional columns:
  - Mean Tet E. coli CFU/g wet weight; Mean Log Tet E. coli CFU/g wet weight; Mean Tet CFU/g dry weight; Mean Log10 Tet E. coli CFU/g dry weight.
  - Mean Ceph E. coli CFU/g wet weight; Mean Log Ceph E. coli CFU/g wet weight; Mean Ceph CFU/g dry weight; Mean Log10 Ceph E. coli CFU/g dry weight.
  - Mean Marb/Mean Merop CFU values similar to above, for respective antibiotics.
  - % DM (gravimetric dry matter of faecal matter); TMC (too many colonies to count); NS (not sampled); ND (no data).
  
## Methods and laboratory procedures
- Sample processing:
  - 1 gram of faecal material transferred aseptically to 9 ml sterile Ringers solution; serial 10-fold dilutions prepared.
  - 0.1 ml aliquots plated in duplicate on Membrane Lactose Glucuronide Agar (MLGA); bacteria spread across agar.
- Antibiotic testing:
  - Antibiotics added to MLGA after autoclaving and prior to plating at specified rates: 16 mg/L tetracycline and cephalexin; 1.0 mg/L marbofloxacin; 8 mg/L meropenem.
  - Plates dried and incubated at 44.5°C ± 0.2°C for 18–24 hours.
- Moisture content and dry matter:
  - Approximately 50 g of faecal material dried at 105°C to constant weight to determine dry matter.
  - % dry matter calculated as 100 - (((fresh wt - dry wt) / fresh wt) * 100).
- Compliance and provenance:
  - Establishment licence XA11784A2; project licence P592D2677 governing the experiment.

## Data quality, governance and usage
- Provides explicit column-level descriptions and measurement methods to support data discovery, interpretation, and reuse.
- Includes coded entries (NS, ND) for not-sampled or no data, which should be handled consistently in analyses.
- Reflects pooling design and cohort changes; users should account for pooling and grouping when analyzing counts and means.
- Data governance considerations include metadata richness, provenance, and explicit licensing/licensing numbers for traceability and compliance.

## Licences and provenance
- Establishment licence: XA11784A2.
- Project licence: P592D2677.
- Source and methodology are documented to enable auditing, reproducibility, and appropriate data sharing.