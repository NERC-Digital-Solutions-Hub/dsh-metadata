# Supporting documentation

## Overview
- Dataset comprises two CSV files: ARGtype.csv and ARGSubtype.csv.
- Contains antibiotic resistance gene (ARG) data from pooled cattle fecal samples:
  - ARGtype.csv: ARGs per copy of 16S rRNA gene.
  - ARGSubtype.csv: ARGs per copy of ARGs per cell.
- 30 cattle across three farmlets (Red, Blue, Green); samples collected November 2016.
- Data linked to a previously deposited dataset (EIDC_SA_ec83a4ea-923a-4f02-8a9f-aeecc43d7123).

## Data composition and structure
- ARGtype.csv
  - Rows 2–25: data values.
  - Rows 26–49: data for Copy of ARGs per cell (empty cells = not detected).
  - 10 columns total: column 1 = Type.level.results; columns 2–10 = samples LZ1, LZ2, LZ3, LZ4, LZ5, LZ6, LZ7, LZ8, LZ9.
- ARGSubtype.csv
  - Rows 2–1209: data for Copy of ARGs per copy of 16S rRNA gene.
  - Rows 1210–2417: data for Copy of ARGs per cell (empty cells = not detected).
  - 10 columns total: column 1 = Type.level.results; columns 2–10 = samples LZ1, LZ2, LZ3, LZ4, LZ5, LZ6, LZ7, LZ8, LZ9.
- Sample mapping: LZ1–LZ3 Red farmlet; LZ4–LZ6 Blue farmlet; LZ7–LZ9 Green farmlet.
- Empty cells indicate the specific ARG was not detected in that sample.

## Sampling and methods (data provenance)
- Location: North Wyke Farm Platform, Rothamsted Research, North Wyke, Devon, UK.
- Time: Faecal samples collected November 2016.
- Cohort: 30 cattle (10 from each of Red, Blue, Green farmlets) selected from 90 animals.
- Pooling: Faecal samples pooled by farmlet into 3 samples per farmlet (3, 3, 4), yielding 9 total faecal samples for DNA extraction.
- DNA extraction: MO BIO PowerSoil DNA Isolation kit with an added pre-heating step (65 °C for 10 minutes).
- DNA QC: NanoDrop assessment.
- Sequencing: Performed by the sequencing unit at the University of Exeter under a commercial contract.
- Analysis: Metagenomic data analyzed at the Environmental Biotechnology Laboratory, University of Hong Kong under a commercial contract.
- Reference framework: Yin et al. ARGs-OAP v2.0 with expanded SARG database and HMMs (Bioinformatics 2018).
- Licences and approval: Establishment XA11784A2; Project P592D2677.
- Data linkage: This dataset is linked to a previously deposited dataset (EIDC_SA_ec83a4ea-923a-4f02-8a9f-aeecc43d7123).

## Data governance and usability
- Structure supports cross-referencing ARGtype and ARGSubtype with the same 9 sample columns, enabling integrated analyses.
- Metadata highlights sample origin (farmlet), and sample IDs (LZ1–LZ9); clear mapping essential for reuse.
- Documentation of processing steps (extraction method, QC, sequencing/analysis pipeline) supports reproducibility.
- Licensing information provided (establishment and project licences) to guide reuse and redistribution.
- Linkages to related datasets improve provenance and potential longitudinal analyses.

## Data quality and processing notes
- Data reflect detected vs. not detected (empty cells indicate non-detection).
- Methodological notes include pre-heating of samples and standard QC protocol.
- Analysis performed by external institutions under contract, with a published methodological reference.

## Data linkage and traceability
- Clear sample naming scheme and farmlet origin enable traceability from raw samples to processed data.
- Cross-dataset linkage to a previous ARGs dataset improves longitudinal traceability.

## Data stewardship actions
- Ensure metadata completeness for future releases (e.g., versioning of ARG-OAP/SARG references, exact sequencing chemistry, and run details).
- Maintain and publish data provenance, including licenses and project identifiers.
- Facilitate data discovery by indexing farmlet, sample IDs, and measurement type (per copy vs. per cell).
- Monitor for updates or corrections to sample mappings or methodology; annotate any changes to preserve reproducibility.