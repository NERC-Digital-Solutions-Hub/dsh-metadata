# readme for soil populations - IGTE_counts.csv

## Overview
- Describes a dataset of colony counts from an evolution experiment involving SBW25 and P. putida across different plasmid/mercury conditions.
- Captures metadata and measurement details for counts obtained via selective plating, across multiple treatments, replicates, and timepoints.

## Data schema (key fields)

- Treatment
  - Describes plasmid status at start (pQBR57), whether the plasmid is wild-type or compensated (KO of pQBR57_0059), and whether mercury was added to soil (at 16 μg/g).
  - Categories: compensated plasmid with no mercury (A), compensated plasmid with mercury (Hg) (A.Hg), wild-type plasmid with no mercury (B), wild-type plasmid with mercury (B.Hg), and no plasmid with no mercury (C).

- Replicate
  - Biological replicate identifier; each treatment has 6 independent replicates (1–6).

- Transfer
  - Evolution timepoint: 0 (start) or 30 (end).

- Bacteria
  - Species counted, determined by plating media: P. fluorescens SBW25 or P. putida KT2440.

- Marker
  - Detection target for counts:
    - All: total count for the species.
    - HgR: detects plasmid bearers (or chromosomal mercury resistance; later confirmed by PCR).
    - KmR: detects kanamycin resistance (used for P. putida to track transposon Tn6291 transfer via pQBR57).

- Media
  - Plating media variants used to detect specific species/markers; antibiotic and mercury contents are listed and reduced over time as bacteria adapt.
  - Examples include combinations like gentamicin, streptomycin with/without mercury, and kanamycin.

- Volume
  - Volume plated (in μl).

- Dilution
  - Dilution factor used for plating (e.g., 10^-x).

- Count
  - Number of colonies visible on the agar plate.

- CFU_ml
  - Colony forming units per ml, calculated from count, dilution, and plated volume.

## Measurement and data generation notes

- Species and markers are identified through selective media formulations; the media composition and antibiotic/mercury concentrations evolve over time due to adaptation.
- HgR and KmR markers help distinguish plasmid-associated resistance from chromosomal or transposon-mediated resistance; HgR status may be confirmed later by PCR.
- The dataset records both the biological context (treatment, timepoint, replicate) and the assay specifics (media, marker) to support re-use and comparability.

## Data quality, interpretation, and governance

- Data quality considerations
  - Multiple media types and markers increase interpretive complexity; clear metadata is essential to map counts to specific bacterial populations and resistance traits.
  - Media formulations and selective pressures change over time; documentation of these changes is crucial for longitudinal analyses.
  - Some detections (HgR vs KmR) require follow-up confirmation (e.g., PCR) to verify the exact resistance mechanism.

- Reproducibility and provenance
  - 6 biological replicates per treatment; timepoints are 0 and 30, enabling assessment of population dynamics across conditions.
  - Clear linkage between Treatment, Replicate, Transfer, Bacteria, and Marker ensures traceability of counts to experimental conditions.

- Data usage implications for data strategy
  - The dataset is a rich example of a multi-factor experiment combining plasmid status, mercury exposure, and microbial species, requiring robust metadata, standardized units, and consistent naming.
  - To maximize discoverability and usability, maintain a comprehensive data dictionary, document measurement methods, and preserve linkage between counts and the specific media/marker conditions used.

## Implications and next steps for data leaders

- Ensure consistent data standards across the dataset (e.g., units for volume, dilution notation, and media naming).
- Maintain clear metadata describing what each Marker and Media combination detects, and when confirmatory assays (e.g., PCR) were used.
- Preserve lineage information to support reproducibility of analyses exploring plasmid dynamics, mercury effects, and resistance transfer.
- Consider creating cross-references to the experimental protocol or code used to compute CFU_ml from Count, Dilution, and Volume for full reproducibility.