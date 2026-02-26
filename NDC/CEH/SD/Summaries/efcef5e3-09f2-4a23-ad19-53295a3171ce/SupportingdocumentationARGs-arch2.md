# Supporting documentation

## Overview
- A dataset description for two CSV files: ARGtype.csv and ARGSubtype.csv.
- Focus: Antibiotic Resistant Genes (ARGs) in cattle fecal samples, quantified as copies per 16S rRNA gene and per cell.
- Samples derived from pooled faecal material of 30 cattle across three farmlets (Red, Blue, Green) at North Wyke Farm Platform, collected November 2016.
- Data intended to support monitoring of environmental antibiotic resistance gene (ARG) abundance using standardized methods.

## Dataset contents
- ARGtype.csv
  - Structure: 10 columns; 1st column is Type.level.results; next 9 columns correspond to sample numbers.
  - Sections:
    - Rows 2–25: Copy of ARGs per copy of 16S rRNA gene.
    - Rows 26–49: Copy of ARGs per cell (empty cells indicate non-detection).
  - Samples mapped to farmlets: LZ1–LZ3 (Red), LZ4–LZ6 (Blue), LZ7–LZ9 (Green).
- ARGSubtype.csv
  - Structure: 10 columns; 1st column is Type.level.results; next 9 columns correspond to sample numbers.
  - Sections:
    - Rows 2–1209: Copy of ARGs per copy of 16S rRNA gene.
    - Rows 1210–2417: Copy of ARGs per cell (empty cells indicate non-detection).

## Samples and farmlets
- Pooling design: For each farmlet (Red, Blue, Green), 10 cattle selected from 90; pooled into 3 samples per farmlet (3, 3, 4), yielding 9 faecal samples total.
- Sample identifiers: LZ1–LZ9, with Red farmlet = LZ1–LZ3; Blue farmlet = LZ4–LZ6; Green farmlet = LZ7–LZ9.

## Measurements and interpretation
- Data represent counts of ARGs in two units:
  - Copy of ARGs per copy of 16S rRNA gene.
  - Copy of ARGs per cell.
- Empty cells indicate that a particular ARG was not detected in that sample.
- Each file organizes results by Type.level.results and the nine samples.

## Methods and workflow
- Sample collection: November 2016, cattle at North Wyke Farm Platform, Rothamsted Research, Devon, UK.
- Cohort: 30 cattle (10 per farmlet: Red, Blue, Green).
- Laboratory processing:
  - Faecal samples pooled by farmlet (3 samples for most, 4 for one).
  - DNA extraction using MO BIO PowerSoil DNA Isolation kit with a 65°C pre-heating step for 10 minutes.
  - DNA quality assessment via NanoDrop.
- Sequencing and analysis:
  - DNA sequencing conducted by the University of Exeter sequencing unit.
  - Metagenomic analysis performed at the Environmental Biotechnology Laboratory, University of Hong Kong.
  - Analytical method: ARGs-OAP v2.0 with expanded SARG database and Hidden Markov Models (reference: Yin et al. 2018).
- Licences:
  - Establishment licence XA11784A2.
  - Project licence P592D2677.
- Data provenance: Linked to the previously deposited dataset EIDC_SA_ec83a4ea-923a-4f02-8a9f-aeecc43d7123.

## Data provenance and licensing
- Data produced under specific UK licences; traceable to institutional facilities and prior deposits.
- Full methodology and references provided to enable replication and cross-study comparisons.

## Related datasets and references
- Linked prior dataset: EIDC_SA_ec83a4ea-923a-4f02-8a9f-aeecc43d7123.
- Methodological reference: Yin, Xiaole, et al. ARGs-OAP v2.0 with an Expanded SARG Database and Hidden Markov Models (Bioinformatics, 2018).