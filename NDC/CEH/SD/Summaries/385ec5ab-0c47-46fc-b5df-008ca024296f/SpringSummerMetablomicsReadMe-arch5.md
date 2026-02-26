# SpringSummerMetabolomics.csv

## Overview
- Metabolomics dataset describing urine from sheep collected in spring and summer 2016 (n=5 sheep per season; total 10 samples).
- Data represent untargeted primary metabolism analysis; peak intensity values for identified compounds.
- Data collected via syringe filtration (<0.2 μm), flash freezing, stored at -80°C, shipped on dry ice to UC Davis for analysis.

## Data collection and processing

- Project and grant: Project: Uplands-N2O; Grant NE/M015351/1.
- Authors: Karina A Marsden; Lucy Lush; Jon A Holmberg; Mick J Whelan; Andrew J King; Rory P Wilson; Alice F Charteris; Laura M Cardenas; Davey L Jones; Dave R Chadwick.
- Analytical method: ALEX-CIS GC-TOF-MS (Gerstel Inc.).
- Data type: Peak intensity values for all identified compounds from untargeted primary metabolism analysis.
- Sample metadata:
  - Sample: Encodes season and sheep ID.
  - Season: Spring or Summer 2016.
  - Other headers: Identified compounds; corresponding peak intensity values.
- Quality control: Procedural blanks of ultra-pure water were syringe filtered and blank-corrected.

## Data provenance and metadata

- Data provenance: Raw data resulting from metabolomics analysis; processed to produce a table of peak intensities.
- Documentation cues: Note on reuse—"If data are reused please ensure it is fully cited."
- Storage/transfer: Samples stored at -80°C; shipped on dry ice to UC Davis for analysis.

## Data structure and accessibility

- File: SpringSummerMetabolomics.csv.
- Structure: Rows per sample; columns for Sample, Season, and peak intensities for each identified compound.
- Usability: CSV format suitable for discovery and reuse, with explicit season and sample identifiers to facilitate data discovery and cross-study comparisons.

## Data governance and stewardship considerations

- Data standards: Metadata includes project, grant, authors, sample metadata (season, sheep ID), and instrument/processing details. Consider attaching a formal metadata schema (e.g., instrument, processing steps, blank correction method) for interoperability.
- Citation and attribution: Clear instruction to cite the dataset if reused; include full citation details (as provided) in downstream records.
- Data quality: Blank correction applied; ensure future updates preserve this provenance (document any reprocessing or re-normalization).
- Versioning and updates: Establish a versioned asset with changelog if the dataset is updated (e.g., updated compound identifications, reprocessing).
- Access and sharing: No explicit access restrictions noted; ensure repository hosting supports discoverability and long-term preservation.

## Practical notes for Data Stewards

- Verify completeness of metadata (season encoding, sheep ID, compound identifiers, and units for peak intensities).
- Confirm that all authors and grant information are correctly captured in metadata records.
- Preserve raw and processed data lineage (including original raw outputs and blank-corrected results).
- Provide guidance on interpretation (e.g., what constitutes identified compounds, any transformation applied to peak intensities).
- Acknowledge potential limitations: small sample size (n=5 per season) and single study context; document these in dataset metadata for users.

## Authors and contact

- Authors: Karina A Marsden; Lucy Lush; Jon A Holmberg; Mick J Whelan; Andrew J King; Rory P Wilson; Alice F Charteris; Laura M Cardenas; Davey L Jones; Dave R Chadwick.