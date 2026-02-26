# readme for soil populations - IGTE_counts.csv

## Overview
- Documents how counts of soil-associated bacteria (Pseudomonas fluorescens SBW25 and P. putida KT2440) are collected across an evolution experiment.
- Tracks plasmid status (compensated or wild-type) and presence/absence of mercury, with corresponding markers and detection methods.
- Provides structure for counting colonies, translating counts into CFU per mL, and linking counts to treatments, replicates, timepoints, and media conditions.

## Data structure and fields
- Treatment: describes plasmid status and mercury exposure at the start of the experiment
  - A.Hg compensated plasmid + mercury
  - B wild-type plasmid, no mercury
  - B.Hg wild-type plasmid + mercury
  - C no plasmid, no mercury
- Replicate: 6 independent biological replicates per treatment (1–6)
- Transfer: timepoint in the evolution experiment
  - 0 (start point)
  - 30 (end point)
- Bacteria: species analyzed (determined by plating media)
  - P. fluorescens (SBW25)
  - P. putida (KT2440)
- Marker: detected version of the organism
  - All: total count for the species
  - HgR: detects plasmid bearers (or chromosomal mercury resistance later confirmed by PCR)
  - KmR: detects kanamycin resistance (only for P. putida) to flag transfer of transposon Tn6291 via pQBR57
- Media: plating conditions to identify species/markers; media compositions and antibiotic/mercury concentrations change over time as adaptation occurs
  - Examples: Gm30, Gm30Hg20, Sm250, Sm250Hg20, Sm250Km50, Gm6, Gm6Hg20, Sm125, Sm125Hg20, Sm125Km25, Sm50, Sm50Hg20, Sm50Km10
- Volume: volume plated (µL)
- Dilution: dilution factor plated (e.g., 10^-x)
- Count: number of colonies observed on the plate
- CFU_ml: colony forming units per mL, calculated from Count, Dilution, and Volume

## Experimental design
- Species and context: bacteria from soil; SBW25 and KT2440 are evaluated for plasmid carriage and mercury resistance
- Plasmid and mercury treatments: four described treatments focusing on plasmid presence/absence and mercury exposure
  - Compensated plasmid + mercury
  - Wild-type plasmid, no mercury
  - Wild-type plasmid + mercury
  - No plasmid, no mercury
- Timepoints: start (0) and end (30) of the evolution experiment
- Replication: six biological replicates per treatment
- Plating strategy: multiple media conditions to detect total counts and specific resistance markers; species/marker determination depends on media

## Measurements, calculations, and interpretation
- Data captured as counts of colonies under defined media conditions, per replicate, treatment, timepoint, and marker
- Markers allow separation of total species counts from plasmid-bearing or resistance-carrying subsets
- CFU_ml calculation: derived from count, dilution, and plated volume
  - Formula context: CFU_ml = (Count × Dilution) / (Volume × 1e-3) [note: exact multiplicative factors may reflect the dataset’s specific units; ensure consistent unit handling]
- Purpose for monitoring frameworks: illustrates multi-factor experimental monitoring with explicit metadata, enabling tracking of population dynamics, horizontal gene transfer indicators, and resistance under varying environmental pressures

## Metadata, data governance, and accessibility
- Metadata describe experimental conditions, markers, and plating schemes necessary to interpret counts
- Public sharing of underlying data may be a barrier if additional metadata or provenance is required
- Data quality considerations include: changing media concentrations over time, potential adaptation effects, and clear documentation of the detection markers and their confirmation (e.g., PCR for HgR)
- For monitoring applications, the dataset demonstrates the importance of:
  - Clear linkage between treatments, replicates, timepoints, and measurements
  - Comprehensive metadata to support reproducibility and data reuse
  - Data governance around sharing, provenance, and transparency of calculations (e.g., CFU/ml)