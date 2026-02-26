# Details of data structure to ' HF_NW_herbage_quality.csv '

## Overview
- Supplement to the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf'.
- Describes the data structure for HF_NW_herbage_quality.csv.
- Dataset characteristics: 13 columns and 96 rows; grassland fertiliser trial data from 2016 at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research).
- Provenance: Henfaes samples are pre-dried and sent to Sciantec Analytical (Stockbridge Technology Centre, UK); North Wyke samples are fresh and sent to Trouw Nutrition GB.

## Measurements and data handling
- Analyses include dry matter, acid detergent fibre (ADF), ash, crude protein, metabolizable energy (ME), and neutral detergent fibre (NDF) using near-infrared spectrometry.
- Digestibility metric defined as D = ME/0.16.
- Units are on a dry matter basis:
  - Dry matter, ADF, Ash, Crude Protein: g kg-1
  - ME: MJ kg-1
  - NDF: MJ kg-1
  - D: % (digestibility)

## Dataset structure
- 13 columns (fields) and 96 rows.

## Columns (dataset fields)
- Date — Date of grass cut. Unit: none
- Site — HF|NW location of the trial (HF = Henfaes, NW = North Wyke). Unit: none
- N_app — Fertiliser application code: 1|2|3 (1st & 2nd application 90 kg ha-1, 3rd application 60 kg ha-1). Unit: none
- Block — Blocking factor of randomized block design: 1|2|3|4. Unit: none
- Plot — Plot harvested: 1–16 (plot size 2 × 6 m). Unit: none
- Treatment — Fertiliser type: AN (ammonium nitrate), U (urea), IU (inhibited urea), C (0N control). Unit: none
- Dry_matter — Dry matter content. Unit: g kg-1
- ADF — Acid detergent fibre (lignin, cellulose, and lignified N). Unit: g kg-1
- Ash — Total mineral content. Unit: g kg-1
- Crude_Protein — Crude protein content. Unit: g kg-1
- ME — Metabolizable energy. Unit: MJ kg-1
- NDF — Neutral detergent fibre. Unit: MJ kg-1
- D — Digestibility metric. Unit: %

## Context and usage
- The dataset links spatially to two trial sites, enabling GIS-based analysis by site, block, plot, and treatment over time (date).
- Suitable for map-based visualizations of herbage quality metrics and treatment effects across grassland plots.