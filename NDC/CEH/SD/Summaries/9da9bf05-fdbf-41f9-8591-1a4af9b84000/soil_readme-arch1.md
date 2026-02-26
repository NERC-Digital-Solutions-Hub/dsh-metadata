# readme for soil populations - IGTE_counts.csv

## Overview
- Documents the IGTE_counts.csv data from a soil evolution experiment tracking plasmid carriage (pQBR57), mercury resistance, and antibiotic markers.
- Two species involved: Pseudomonas fluorescens SBW25 and Pseudomonas putida KT2440, with counts determined by selective plating.
- Six independent biological replicates per treatment.
- Treatments vary plasmid presence, plasmid compensation status, and mercury exposure.
- Timepoints: 0 (start) and 30 (end) of the evolution experiment.
- Markers detected: All (total count), HgR (mercury resistance), and KmR (kanamycin resistance, used for detecting transfer of a transposon into P. putida).

## Columns and meanings
- Treatment: describes the initial plasmid status and mercury exposure.
  - A.Hg compensated plasmid + mercury
  - B wild-type plasmid, no compensation, with mercury
  - C no plasmid, no mercury
- Replicate: biological replicate number (1–6).
- Transfer: timepoint in the evolution experiment (0 or 30).
- Bacteria: species counted, determined by plating media.
  - P. fluorescens (SBW25)
  - P. putida (KT2440)
- Marker: which counts are detected
  - All: total count for the species
  - HgR: detects plasmid bearers (or chromosomal mercury resistance; confirmed later by PCR)
  - KmR: detects kanamycin resistance (only for P. putida; used to infer transfer of transposon Tn6291 via pQBR57)
- Media: selective additives used to identify species/markers; includes combinations of antibiotics and mercury. Examples include:
  - Gm30, Gm30Hg20, Gm6, Gm6Hg20 (gentamicin, with optional mercury)
  - Sm250, Sm250Hg20, Sm125, Sm125Hg20, Sm50, Sm50Hg20 (streptomycin with optional mercury)
  - Sm250Km50, Sm125Km25, Sm50Km10 (combinations including kanamycin)
  - Concentrations decrease over time as bacteria adapt to soil.
- Volume: volume plated in microliters (µL).
- Dilution: dilution factor plated (e.g., 10^-x).
- Count: number of colonies visible on the plate.
- CFU_ml: colony-forming units per milliliter, calculated from count, dilution, and volume.

## Experimental design notes
- Each treatment comprises six independent biological replicates.
- The media and markers are designed to detect:
  - presence/absence of the pQBR57 plasmid
  - mercury resistance (HgR)
  - transfer of the transposon Tn6291 into P. putida via pQBR57 (KmR)
- Timepoints capture changes from the start (0) to the end (30) of evolution under the defined treatments.

## Calculations and data handling
- CFU_ml is calculated using the standard plating formula:
  - CFU_ml = (count × 10^dilution × 1000) / volume
  - where volume is in microliters and 10^dilution is the dilution factor corresponding to the "Dilution" column.

## Notes and caveats
- Media concentrations (antibiotics and mercury) are reduced over time to reflect adaptation to soil environments.
- HgR detection indicates plasmid bearers or chromosomal mercury resistance, with PCR used later to confirm the mechanism.
- Data are organized to allow tracing of species, marker, treatment, replicate, and timepoint for downstream analyses of plasmid dynamics and horizontal gene transfer.