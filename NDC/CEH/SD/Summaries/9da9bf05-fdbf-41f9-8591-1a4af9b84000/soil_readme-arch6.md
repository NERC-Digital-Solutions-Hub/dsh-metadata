# readme for soil populations - IGTE_counts.csv

## Purpose
- Documentation for a dataset counting soil bacterial populations (SBW25 and P. putida KT2440) across plasmid status and mercury exposure.
- Tracks evolution experiment conditions, replication, and timepoints to enable analysis of plasmid carriage, mercury resistance, and population dynamics.

## Data fields (schema)

- **Treatment**: Describes initial plasmid status (pQBR57) and mercury exposure. Codes include:
  - A compensated plasmid, no mercury
  - A.Hg compensated plasmid + mercury
  - B wild-type plasmid, no mercury
  - B.Hg wild-type plasmid + mercury
  - C no plasmid, no mercury

- **Replicate**: Biological replicate identifier (1–6) for each treatment.

- **Transfer**: Evolution timepoint (0 = start, 30 = end).

- **Bacteria**: Species/count context determined by plating media:
  - P. fluorescens (SBW25)
  - P. putida (KT2440)

- **Marker**: Which count is detected:
  - All = total count for the species
  - HgR = detects plasmid bearers (or chromosomal mercury resistance via PCR)
  - KmR = detects kanamycin resistance (for transfer of Tn6291 into P. putida via pQBR57)

- **Media**: Selection/detection conditions used, reflecting species/marker. Includes antibiotics and mercury; concentrations decline over time as bacteria adapt. Examples:
  - Gm30 (gentamicin 30 μg/ml)
  - Gm30Hg20 (gentamicin 30 μg/ml + mercury 20 μM)
  - Sm250 (streptomycin 250 μg/ml)
  - Sm250Hg20 (streptomycin 250 μg/ml + mercury 20 μM)
  - Sm250Km50 (streptomycin 250 μg/ml + kanamycin 50 μg/ml)
  - Gm6, Gm6Hg20, Sm125, Sm125Hg20, Sm125Km25, Sm50, Sm50Hg20, Sm50Km10 (lower concentrations over time, with/without mercury/kanamycin as indicated)

- **Volume**: Volume plated, in μl.

- **Dilution**: Dilution factor plated (e.g., 10^-x).

- **Count**: Number of colonies visible on the agar plate.

- **CFU_ml**: Colony forming units per mL, calculated from Count, Dilution, and Volume.

## Calculation formula

- CFU_ml is derived from the observed count and plating parameters:
  - CFU_ml = (Count × 10^(Dilution)) / (Volume × 10^(-3))
  - Note: Volume is in μl; Dilution represents the exponent in the 10^-x dilution; this formula converts the plating result to CFU per mL.

## Experimental design context

- Treatments explore five initial plasmid/mercury conditions (A, A.Hg, B, B.Hg, C).
- Each treatment has six biological replicates.
- Measurements occur at two timepoints (0 and 30) across two species, using Marker to distinguish total counts from plasmid-bearing or resistance-marked subpopulations.

## Data use considerations

- Media concentrations decrease over time to reflect bacterial adaptation; this affects detectability and comparability across timepoints.
- Marker choices (All, HgR, KmR) enable parsing total counts from specific subpopulations (plasmid-bearing or kanamycin-resistant).
- When aggregating across replicates or timepoints, account for differences in media and marker to avoid misinterpreting population shifts.