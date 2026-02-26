# readme for soil populations - IGTE_counts.csv

## Overview
- Document describing the IGTE_counts.csv readout from an evolution experiment on soil populations involving SBW25 with different plasmid/mercury treatments.
- For each treatment, six independent biological replicates are measured at two timepoints (0 and 30).
- Counts are obtained by plating on selective media to detect species and markers; CFU/ml is calculated from colony counts, dilution, and plated volume.

## Data structure and key fields
- Core fields: Treatment, Replicate, Transfer, Bacteria, Marker, Media, Volume, Dilution, Count, CFU_ml.
- Treatment (A, B, C) encodes plasmid/mercury status:
  - A: Hg compensated plasmid + mercury
  - B: wild-type plasmid, no mercury
  - C: no plasmid, no mercury
- Replicate: 1–6 (six biological replicates per treatment).
- Transfer: 0 (start) or 30 (end).
- Bacteria: species counted, determined by plating media (P. fluorescens SBW25 or P. putida KT2440).
- Marker: detected marker set:
  - All: total count for the species
  - HgR: detects plasmid-bearing strains with mercury resistance
  - KmR: detects kanamycin resistance (only for P. putida), to infer transposon transfer via pQBR57
- Media: combinations of antibiotics and mercury used to detect specific species/markers; note that concentrations are reduced over time as bacteria adapt.
  - Examples include Gm30, Gm30Hg20, Sm250, Sm250Hg20, Sm250Km50, Sm125, Sm125Hg20, Sm125Km25, Sm50, Sm50Hg20, Sm50Km10, with mercury (Hg) or kanamycin (Km) additions.
- Volume: plated volume in microliters (μL).
- Dilution: dilution factor (e.g., 10^-x).
- Count: number of colonies observed on a plate.
- CFU_ml: colony-forming units per milliliter, calculated from count, dilution, and volume; formula provided as CFU_ml = (count × dilution) / (volume × 10^-3), where volume is in μL (volume in mL is volume × 10^-3).

## Data interpretation notes
- Marker and media combinations determine which bacteria/traits are being quantified (e.g., HgR indicates plasmid-bearing, KmR indicates kanamycin resistance in P. putida).
- Media concentrations adapt over time to maintain detectable growth under evolving soil conditions.
- Volume, dilution, and count combine to yield CFU/ml, enabling cross-sample comparisons after normalization.

## Data quality and governance considerations
- Ensure consistent mappings for Treatment, Bacteria, Marker, and Media across datasets and catalogs.
- Verify that media codes and their antibiotic/mercury compositions are documented and kept in sync with the readme.
- Maintain provenance: link readme metadata to the IGTE_counts.csv rows for traceability of treatment conditions and replicates.
- Track any updates to media formulations or plating protocols that could affect comparability over time.

## Practical implications for reuse
- Useful for analyses of plasmid/mercury treatment effects on bacterial abundance and viability, under different selective pressures.
- Enables examination of replication consistency (six replicates per treatment) and temporal dynamics (start vs end).
- Provides a structured framework for extracting CFU/ml from plate counts in a standardized way, given volume and dilution data. 

## Potential challenges for Data Stewards
- Incomplete alignment between user needs and metadata granularity (e.g., detailed media/marker interpretation).
- Timely submission of complete metadata and consistent field coding across experiments.
- Handling multiple systems or formats if expanding beyond this dataset (e.g., integrating with other OTU or marker datasets).
- Managing older, non-interoperable legacy formats and ensuring backward compatibility in catalogs.