# Supporting documentation

- Dataset overview: Two CSV files, ARGtype.csv and ARGSubtype.csv, capturing antibiotic resistance genes (ARGs) per copy of 16S rRNA gene and per cell across 30 cattle samples.

- Data structure:
  - ARGtype.csv: 10 columns; column 1 is Type.level.results; columns 2–10 correspond to samples LZ1–LZ9. Rows 2–25 contain ARG type data; rows 26–49 contain ARGs per cell data (empty cells = not detected).
  - ARGSubtype.csv: 10 columns; column 1 is Type.level.results; columns 2–10 correspond to samples LZ1–LZ9. Rows 2–1209 contain Copy of ARGs per copy of 16S rRNA gene data; rows 1210–2417 contain Copy of ARGs per cell data (empty cells = not detected).

- Samples and design:
  - Pooled faecal samples from 30 cattle (10 per farmlet: Red, Blue, Green).
  - For each farmlet, 3 samples were pooled (Red: LZ1–LZ3; Blue: LZ4–LZ6; Green: LZ7–LZ9).

- Methods and workflow:
  - Sample collection: November 2016 at North Wyke Farm Platform, Rothamsted Research, North Wyke, Devon, UK.
  - DNA extraction: MO BIO PowerSoil DNA Isolation kit with a 65°C heating step prior to vortexing.
  - DNA quality check: NanoDrop measurement.
  - Sequencing: Performed by University of Exeter sequencing unit under a commercial contract.
  - Analysis: Metagenomic data analyzed at the Environmental Biotechnology Laboratory, University of Hong Kong, under a commercial contract.
  - Reference framework: ARGs-OAP v2.0 (expanded database with Hidden Markov Models).
  - Licence information: Establishment licence XA11784A2; project licence P592D2677.
  - Provenance: Data linked to a previously deposited dataset EIDC_SA_ec83a4ea-923a-4f02-8a9f-aeecc43d7123.

- Interpretation notes:
  - Empty cells indicate that a particular ARG was not detected in that sample.
  - The data enable analysis of ARG abundance per copy of 16S rRNA gene and per bacterial cell across farmlet-based samples.

- Data use considerations for analysts:
  - Validate mapping between sample IDs (LZ1–LZ9) and farmlets.
  - Consider combining ARGtype and ARGSubtype data for comprehensive ARG profiling.
  - Address missing data cautiously where cells are empty.
  - Acknowledge licensing and provenance when integrating with other datasets.