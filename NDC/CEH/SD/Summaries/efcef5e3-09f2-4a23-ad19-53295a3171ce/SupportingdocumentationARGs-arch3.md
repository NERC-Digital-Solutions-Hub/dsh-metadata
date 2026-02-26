# Supporting documentation

- The dataset comprises two CSV files: ARGtype.csv and ARGSubtype.csv.
- Purpose: count antibiotic resistance genes (ARGs) per copy of 16S rRNA gene and per cell in cattle faecal samples.
- Structure of ARGtype.csv and ARGSubtype.csv:
  - 10 columns total; first column is Type.level.results; the next nine columns correspond to sample numbers.
  - Samples are pooled faecal samples from 30 cattle across three farmlets (Red, Blue, Green): LZ1–LZ3 Red; LZ4–LZ6 Blue; LZ7–LZ9 Green.
  - Rows:
    - ARGtype.csv: rows 2–25 contain data for Copy of ARGs per copy of 16S rRNA gene; rows 26–49 contain data for Copy of ARGs per cell.
    - ARGSubtype.csv: rows 2–1209 contain per-copy data; rows 1210–2417 contain per-cell data.
  - Empty cells indicate the particular ARG was not detected in that sample.

- Data content details:
  - Measurements cover antibiotic resistance genes (ARGs) detected in pooled cattle faecal samples.

- Sampling and study design:
  - Location: North Wyke Farm Platform, Rothamsted Research, North Wyke, Devon, UK.
  - Date: November 2016.
  - Cohort: 30 cattle selected from 90 total (10 cattle per farmlet).
  - Pooling: 9 faecal samples total (3 from each farmlet; 3, 3, and 4 samples per farmlet).
  - DNA extraction: MO BIO PowerSoil DNA Isolation Kit with a 65°C pre-heating step.
  - DNA quality assessment: NanoDrop.
  - Sequencing: performed by the sequencing unit at the University of Exeter under a commercial contract.
  - Analysis: metagenomic data analyzed at the Environmental Biotechnology Laboratory, University of Hong Kong under a commercial contract.
  - Method reference: Yin, Xiaole, et al. ARGs-OAP v2.0 with an expanded SARG database and HMMs (Bioinformatics 2018).

- Licensing, provenance, and data linkage:
  - Establishment licence: XA11784A2.
  - Project licence: P592D2677.
  - Data linked to a previously deposited dataset: EIDC_SA_ec83a4ea-923a-4f02-8a9f-aeecc43d7123.
  - Underpinning methods and data are described in the supporting documentation linked to this dataset.