# Supporting documentation

- This dataset comprises two CSV files: ARGtype.csv and ARGSubtype.csv.
- Content overview:
  - ARGtype.csv:
    - Rows 1 contains column headings.
    - Rows 2–25: data for Copy of Antibiotic Resistant Genes (ARGs) per copy of the 16S rRNA gene.
    - Rows 26–49: data for Copy of ARGs per cell (empty cells indicate the ARG was not detected).
    - 10 columns total; column 1 is Type.level.results; columns 2–10 correspond to 9 samples (LZ1–LZ9).
  - ARGSubtype.csv:
    - Rows 1 contains column headings.
    - Rows 2–1209: data for Copy of ARGs per copy of 16S rRNA gene.
    - Rows 1210–2417: data for Copy of ARGs per cell (empty cells indicate non-detection).
    - 10 columns total; column 1 is Type.level.results; columns 2–10 correspond to 9 samples (LZ1–LZ9).

- Sampling design:
  - Source: North Wyke Farm Platform, Rothamsted Research, North Wyke, Devon, UK.
  - Time: November 2016.
  - Cohort: 30 cattle selected from 90 (10 per farmlet: Red, Blue, Green).
  - Sampling approach: faecal samples collected as cattle entered housing for winter (weaning).
  - Pooling: within each farmlet, samples were pooled to create 3 samples per farmlet, resulting in 9 faecal samples for DNA extraction.

- Laboratory and sequencing details:
  - DNA extraction: MO BIO PowerSoil DNA Isolation kit with a pre-processing step heating samples to 65°C for 10 minutes before vortexing.
  - DNA quality check: NanoDrop measurement.
  - Sequencing: conducted by the University of Exeter sequencing unit under a commercial contract.
  - Analysis: metagenomic data analyzed at the Environmental Biotechnology Laboratory, University of Hong Kong under a commercial contract.
  - Method reference: Yin, Xiaole, et al. ARGs-OAP v2.0 and SARG database with Hidden Markov Models (Bioinformatics 2018).

- Provenance and licensing:
  - Establishment licence: XA11784A2; project licence: P592D2677.
  - Data linked to a previously deposited dataset: EIDC_SA_ec83a4ea-923a-4f02-8a9f-aeecc43d7123.

- Purpose and usage notes:
  - Aims to quantify antibiotic resistance genes (ARGs) per copy of the 16S rRNA gene and per cell across nine pooled faecal samples from 30 cattle.
  - Samples labeled by farmlet and replicate: LZ1, LZ2, LZ3 (Red); LZ4, LZ5, LZ6 (Blue); LZ7, LZ8, LZ9 (Green).
  - Data interpretation:
    - Empty cells indicate that a given ARG was not detected in that sample.
    - Data are organized to support cross-sample and cross-farmlet comparisons of ARG abundance.

- Key references:
  - Yin, Xiaole, et al. ARGs-OAP v2.0 with an expanded SARG database; Bioinformatics 2018.