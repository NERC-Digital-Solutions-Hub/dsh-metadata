# Details of data structure to ' HF_NW_herbage_quality.csv '

## Overview
- This document supplements the supporting documentation for data series in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf'.
- Describes the data structure for HF_NW_herbage_quality.csv, a dataset with 13 columns and 96 rows containing herbage quality data.
- Data originate from the 2016 grassland fertiliser trial conducted at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research).
- Henfaes samples were pre-dried before analysis; North Wyke samples were analysed from fresh material.
- Measurements performed using near-infra-red spectrometry for:
  - Dry matter (DM)
  - Acid detergent fibre (ADF)
  - Ash
  - Crude protein
  - Metabolisable energy (ME)
  - Neutral detergent fibre (NDF)
- Digestibility (D) is calculated as D = ME / 0.16.
- Units are expressed as g kg-1 for DM, ADF, Ash, Crude Protein; ME in MJ kg-1; D in %; NDF units are listed as MJ kg-1 in this dataset.

## Dataset structure
- Column header: explanation and unit

- Date: Date of grass cut

- Site: HF|NW (HF = Henfaes, NW = North Wyke)

- N_app: 1|2|3 denotes fertiliser application
  - 1st & 2nd applications 90 kg ha-1
  - 3rd application 60 kg ha-1

- Block: 1|2|3|4 (blocking factor of randomized block design)

- Plot: 1–16 (plot harvested; plot size 2 × 6 m)

- Treatment: AN|U|IU|C
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (agrotain)
  - C = 0N control

- Dry_matter: g kg-1

- ADF: Acid detergent fibre (g kg-1)

- Ash: Total mineral content (g kg-1)

- Crude_Protein: g kg-1

- ME: Metabolisable energy (MJ kg-1)

- NDF: Neutral detergent fibre (cellulose, lignin and hemi-cellulose). MJ kg-1

- D: Digestibility value (D value) as %